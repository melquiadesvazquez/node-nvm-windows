# How to run multiple versions of NodeJS with NVM for Windows 10
I had several problems installing Node with NVM on Windows and following these instructions I fixed the issues:

1 Uninstall NodeJS compleatly from your machine.
  * Open the Windows Powershell as Admin (very important)
  * Run nvm list to make make sure what NodeJS versions are installed, if there are any, run nvm uninstall <version>
  * Control panel > Programs > Uninstall a program > NodeJS
  * Delete C:\Program Files\nodejs
  * Delete %appdata%\npm
  * Delete %appdata%\npm-cache
  * Delete the references to npm on your environment variables rundll32 sysdm.cpl,EditEnvironmentVariables
  * Reboot your machine
2 Open the Windows Powershell as Admin (very important)
  * Download NVM from https://github.com/coreybutler/nvm-windows/releases
  * Extract the file to your desktop and install it as Admin (very important)
  * Run the following
  
  ```
  Set-ExecutionPolicy Unrestricted -Scope CurrentUser -Force
  nvm install 10.11.0
  nvm use 10.11.0
  npm install --global --production npm-windows-upgrade
  npm-windows-upgrade --npm-version latest
  nvm list  
  ```
  
  
  
  
