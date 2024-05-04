# Hide and Unhide Desktop Icons on Mac

Welcome to the `Hide-Desktop-Icons-on-Mac` repository! This guide is designed to help you quickly make all the desktop icons on your Mac invisible with just a single click. Whether you're preparing to share your screen in a meeting, showing something on your laptop to a friend or simply prefer a cleaner workspace, this solution is for you. And yes, I know Windows has this built in..

I found myself needing a straightforward method to hide all the folders and icons cluttering my desktop during presentations, but I didn't want to spend money on an app for such a basic function. After failing to find a practical tutorial online that met my needs, I decided to create one. This repository not only serves as a guide but also as a personal documentation, in case I ever need to remember how to set this up again.

Below, you'll find step-by-step instructions on how to create Mac Shortcuts using the Terminal app that allows you to hide and unhide your desktop icons effortlessly. No third-party software required—just a couple of shortcuts right in your Menu Bar for easy access.

## Create Shortcut to Hide Desktop Icons

1. **Open Shortcuts on Mac:**
   - Launch the Shortcuts app.

2. **Add a New Shortcut:**
   - Click the `+` button to start creating a new shortcut.

3. **Set Up Run Shell Script:**
   - Type `Terminal` in the search bar.
   - Double-click on "Run Shell Script". You might be prompted to give permissions to Shortcuts for actions. A new action panel will appear with a default script that says `echo "Hello World"`.

4. **Edit the Script:**
   - Click on the script line, delete it, and type:
     ```
     defaults write com.apple.finder CreateDesktop -bool false
     ```
   - Ensure settings such as Shell, Input, and Run as Administrator remain unchanged.

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
