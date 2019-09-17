## How to install NODEJS on linux


\# Download do nodejs
--------

1. Download Link (Choose linux version):
  ```
  https://nodejs.org/en/
  ```
2. Open terminal:

3. Go to the 'Downloads' directory:
  ```
  cd Downloads
  ```

4. Unzip the file (Locate your nodejs file):
  ```
  tar -Jxf node-v10.16.3-linux-x64.tar.xz
  ```

5. Create directory:
  ```
  sudo mkdir /usr/lib/nodejs
  ```

6. Move the unzipped file to the created directory:
  ```
  sudo mv node-v10.16.3-linux-x64 /usr/lib/nodejs/node-v10.16.3
  ```

7. Edit file '~/.profile':
  ```
  sudo nano ~/.profile
  ```

8. Insert in file finish':
  ```
  # nodejs
  export NODEJS_HOME=/usr/lib/nodejs/node-v10.16.3
  export PATH=$NODEJS_HOME/bin:$PATH
  ```

9. Restart '~/.profile':
  ```
  . ~/.profile 
  ```
6. Done, Now test:
  ```
  node -v
  ```
  ```
  npm -v
  ```
