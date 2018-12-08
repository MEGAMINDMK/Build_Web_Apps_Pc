# How to create apps
1.create a folder at path C:\Users\urusernamegoeshere\your-app<br>
2.now create 4 files in it<br>
<a href="https://imgbb.com/"><img src="https://imgur.com/D9QpLgV.jpg" alt="bevr" border="0"></a><br>
3.in index.html type<br>
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Hello World!</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```
4.in main.js type<br>
```js
const { app, BrowserWindow } = require('electron')

// Keep a global reference of the window object, if you don't, the window will
// be closed automatically when the JavaScript object is garbage collected.
let win

function createWindow () {
  // Create the browser window.
  win = new BrowserWindow({ width: 800, height: 600, icon: __dirname + '/icon.ico'})

  // and load the index.html of the app.
  win.loadFile('index.html')

  // Open the DevTools.
  win.webContents.openDevTools()

  // Emitted when the window is closed.
  win.on('closed', () => {
    // Dereference the window object, usually you would store windows
    // in an array if your app supports multi windows, this is the time
    // when you should delete the corresponding element.
    win = null
  })
}

// This method will be called when Electron has finished
// initialization and is ready to create browser windows.
// Some APIs can only be used after this event occurs.
app.on('ready', createWindow)

// Quit when all windows are closed.
app.on('window-all-closed', () => {
  // On macOS it is common for applications and their menu bar
  // to stay active until the user quits explicitly with Cmd + Q
  if (process.platform !== 'darwin') {
    app.quit()
  }
})

app.on('activate', () => {
  // On macOS it's common to re-create a window in the app when the
  // dock icon is clicked and there are no other windows open.
  if (win === null) {
    createWindow()
  }
})

// In this file you can include the rest of your app's specific main process
// code. You can also put them in separate files and require them here.
```
5.in package.json type<br>
```json
{
  "name": "your-app",
  "version": "0.1.0",
  "description": "my first app",
  "license": "MIT",
  "repository": "https://github.com/MEGAMINDMK",
  "main": "main.js",
  "scripts": {
    "start": "electron ."
  }

```
6.now open node.js
7.type cd C:\Users\urusernamegoeshere\your-app<br>
8. type the following and wait after each command has executed successfully<br>
```
npm install --save-dev electron
npm start // use this to check how ur app looks, then closee it to perform next step
npm install -g electron-packager
electron-packager . --asar --overwrite
```
<br>
8.now u will see a new folder created in ur main folder named as your-app-win32-x64<br>
9.Copy this folder to somewhere save share it with your freinds<br>
10.share it with your freinds
