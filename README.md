Run the using electron prebuilt using "npm start" command from root directory (or "electron ." in the electron_build directory if installed globally)

To replicate the issue,
1. Set the build.asar to false in the development package.json
2. run "npm run packageMAC" in the root directory
3. open dist/mac/Electron_with_notifications.app manually or type "cd dist/mac && open -a Electron_with_notifications"
4. Press the button to show the notifications working as expected
5. set the build.asar to true (or remove the option) in the development package.json
6. repeat steps 2-3
7. Press the button and no notification will appear.