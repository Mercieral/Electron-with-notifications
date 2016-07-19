A repository that recreates an issue where node-notifier will silently fail when using electron's ASAR archive to package applications. The method used to notify (using ipcMain/render) is not necessary in this application but is the similar method that is needed in my full application.


Run the using electron prebuilt using "npm start" command from root directory (or "electron ." in the electron_build directory if installed globally)

To replicate the issue,
1. run "npm install" in the root directory
2. Set the build.asar to false in the development package.json
3. run "npm run packageMAC" in the root directory
4. open dist/mac/Electron_with_notifications.app manually or type "cd dist/mac && open -a Electron_with_notifications"
5. Press the button to show the notifications working as expected
6. set the build.asar to true (or remove the option) in the development package.json
7. repeat steps 2-3
8. Press the button and no notification will appear.