# AR-Browser - CSC13010 - Software Design
## Install Pakages for Server
Install Homebrew
```sh
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Install Node
```sh
$ brew install node
```
Install npm packages
- webshot
```sh
$ npm install webshot
```
- flatiron
```sh
$ npm install flatiron
```
- union
```sh
$ npm install union
```
- union
```sh
$ npm install cheerio
```
## Set up Server
- Open GetImage.js -> Replace "app.start(3000,"Your-IP-address")" to your IP network Address -> Save
- Open GetImage.js -> change .listen(port,'Your-IP-address')" to your IP network Address -> Save
## Set up Brower in Unity (Unity Version 2019.4.9f1)
- Open AR Browser VPN with Unity
- Go to Assets/Scripts/BrowserController.cs
- Replace IP_ADDRESS = "Your-IP-address" to your IP network Address -> Save
## Run Project
1. Open Terminal
```sh
$ cd server
$ node GetImage.js
```
2.Open another Terminal
```sh
$ cd server
$ node GetLinks.js
```
3. Go to Unity -> Play

**NOTE**: If you have problem like:
```sh
ReferenceError: primordials is not defined
```
1. In the same directory where you have package.json create an npm-shrinkwrap.json file with the following contents:
```sh
{
  "dependencies": {
    "graceful-fs": {
        "version": "4.2.2"
     }
  }
}
```
2. Open terminal, cd to the same directory and run
```sh
$ node install
```
