## How to install xammp on linux


\# Download do xammp
--------

1. Download Link (Choose linux version):
  ```
  https://www.apachefriends.org/pt_br/download.html
  ```
2. Open terminal:

3. Go to the 'Downloads' directory:
  ```
  cd Downloads
  ```

4. Instalation permission (Locate your xammp file):
  ```
  sudo chmod +x xampp-linux-x64-7.3.6-0-installer.run
  ```

5. Run instalation (Locate your xammp file):
  ```
  sudo ./xampp-linux-x64-7.3.6-0-installer.run
  ```

6. Done, Now let's set up PHP:
 

\# Creating symbolic link to PHP
--------

1. Into in directory of settings linux:
   ```
   cd /usr/local/bin
  ```

2. Create link of run PHP:
  ```
  sudo ln -s /opt/lamp/bin/php php
  ```

3. Done, Now Check PHP version to confirm previous step:
   ```
   php -v
  ```
4. The output should look like this:
    >PHP 7.3.6 (cli) (built: Jun  3 2019 09:27:32) ( NTS )
    Copyright (c) 1997-2018 The PHP Group
    Zend Engine v3.3.6, Copyright (c) 1998-2018 Zend Technologies


\# Run XAMPP
--------

1. Start XAMPP:
   ```
   sudo /opt/lampp/lampp start
   ```
 Or too
   ```
   sudo /opt/lampp/manager-linux-x64.run
   ```

\# XAMPP unistall
--------

    > /opt/lampp/uninstall



\# Extra Settings
--------

1. Set htdocs permission:
   ```
   sudo chmod 777 /opt/lampp/htdocs/
   ```

