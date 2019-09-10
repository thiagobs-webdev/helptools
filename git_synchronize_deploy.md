\# Server Setup
--------

1. Your server live directory:
  ```
  /var/www/domain.com
  ```
2. Your server repository:
  ```
  /var/repo/site.git
  ```
  
\# Creating Our Repository
--------

1. Login to your VPS from command line and type the following:
```
  cd /var
  mkdir repo && cd repo
  mkdir site.git && cd site.git
  git init --bare
  ```
  > Obs: **--bare** means that our folder will have no source files, just the version control.
  
2. Hooks - **'post-receive'** is executed when a 'push' is completely finished and it's the one we are interested in.
  ```
  cd hooks
  ```
  
  2.1 Create the file 'post-receive' by typing:
  ```
  cat > post-receive
  ```
  
  2.2 A blank line indicating that everything you type will be saved to this file. So let's type, press 'control-d' to save:
  ```
  #!/bin/sh
  git --work-tree=/var/www/domain.com --git-dir=/var/repo/site.git checkout -f
  ```
  
  2.3 Done, now we leave VPS:
  ```
  exit
  ```
  
  
  \# Local Machine
  --------
  
  1. Create your repo:,
  > OBS: Skip this step if you already have your git repository created.
  ```
    cd /my/workspace
    mkdir project && cd project
    git init
  ```
  
  2. Remote path of our repository. Tell Git to add a remote called 'live':
  ```
  git remote add live ssh://user@mydomain.com/var/repo/site.git
  ```
  
  3. Done. In your next commit, just 'push' with 'live':
  ```
  git push live master
  ```
  
  
