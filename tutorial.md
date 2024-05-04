
## Create Shortcut to Hide Desktop Icons

1. **Open Shortcuts on Mac:**
   - Launch the Shortcuts app.
   ![Shortcuts App Mainpage](/hide_desktop_icons/shortcuts_mainpage.png)


2. **Add a New Shortcut:**
   - Click the `+` button to start creating a new shortcut.
   ![Create New Shortcut](/hide_desktop_icons/create_new_shortcut.png)

3. **Set Up Run Shell Script:**
   - Type `Terminal` in the search bar.
   - Double-click on "Run Shell Script". You might be prompted to give permissions to Shortcuts for actions. A new action panel will appear with a default script that says `echo "Hello World"`.
   ![Add Run Shell Script](/hide_desktop_icons/add_shortcut.png)

4. **Edit the Script:**
   - Click on the script line, delete it, and type:
     ```
     defaults write com.apple.finder CreateDesktop -bool false
     ```
   - Ensure settings such as Shell, Input, and Run as Administrator remain unchanged.

     ![First Command](/hide_desktop_icons/hide_shortcut_firstcommand.png)

5. **Add Another Script to Refresh Finder:**
   - Repeat the steps to add a "Run Shell Script".
   - Type:
     ```
     killall Finder
     ```

6. **Run the Shortcut:**
   - Press the play button to execute. This will hide all desktop icons. Icons can still be accessed via Finder, and this does not affect file contents.

### Add the Shortcut to the Menu Bar

1. **Name Your Shortcut:**
   - Right-click on the Shortcut in the Shortcuts app and name it "Hide Desktop Icons".
   ![Hide Shortcut Final](/hide_desktop_icons/hide_shortcut_final.png)

2. **Move to Menu Bar:**
   - Drag the Shortcut to the Menu Bar listed on the left.
   - A Shortcuts icon will appear on your Menu Bar on the upper left side of your Mac.

3. **Use the Shortcut:**
   - Click the Shortcut icon in the Menu Bar to hide your desktop icons with one click.

## Create Shortcut to Unhide Desktop Icons

1. **Follow the Same Initial Steps:**
   - Open Shortcuts, add a new Shortcut, and setup "Run Shell Script" as described above.

2. **Set Up the Unhide Script:**
   - Instead of two actions, just add one with the following code:
     ```
     defaults write com.apple.finder CreateDesktop -bool true; killall Finder
     ```

3. **Name and Add to Menu Bar:**
   - Name the Shortcut "Unhide Desktop Icons".
   - Follow the same steps to add this Shortcut to the Menu Bar.

By following these steps, you can easily toggle the visibility of your desktop icons directly from the Menu Bar.

Enjoy a tidier desktop with just the click of a button!
