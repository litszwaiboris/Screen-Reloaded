# 1. Create a executable script. 🙂
### Open your terminal first: Press the start button and type ```terminal``` and select the Console, Konsole, Terminal or anything but in the result of search.
### Use your desired editor to create a new file with ```.sh``` in the end of the file at any places. Just remember don't delete it.
### For vim, you type ```vi``` and path of your like.
#### Example: ```vi /home/user/abc.sh```
### For nano you type ```nano``` and path of your like.
#### Example: ```nano /home/user/abc.sh```
# 2. Getting the "modeline" thingy 😎
### Before we get to the editing part, you need something named "modeline" which represents your configuration by into numbers code.
### Exit the editor.
#### For vim, first press the esc button on your keyboard to exit INSERT mode and enter ```:qw``` to exit
#### For nano, press `Control`, ```X```  together in your keyboard and press `Y` to exit and save the script.
### We're back to the screen to proceed the next step. If you still in the editor, try again.
### If you want the resolution is 1920x1080 120hz. Then type command ```gtf 1920 1080 120```. Change them as you want.
### You will get the result like the below photo (ofc without the logo lol)
### Copy all the text after "Modeline" and the space
<img width="727" alt="Screenshot 2022-08-23 at 4 13 05 PM" src="https://user-images.githubusercontent.com/72115911/186256730-c4117385-32ef-482c-987a-2aa0647ad53e.png">

# 3. Filling the script that we create in step 1. 😝
### Before we get to filling it. We need to get the display that your using.
#### Create a new tab in your terminal and type in `xrandr -q | grep -i connected primary`
#### Use this as a reference to my next steps with `"display"`
### Repeat all the steps of step 1.
### After your editor appeared on your screen with your script created before, enter this.
```
#!/bin/bash
xrandr --newmode "the copied code"
xrandr --addmode "display" "the quoted text in the copied code"
xrandr --output "display" --mode "the quoted text in the copied code"
```
### Save the script and exit the editor as I said before.
# 4. Make the script executable. 🤨
### There's something missing in this script which cannot make it being executed which is the permission.
### Open your terminal and type the below.
```
chmod +x "your script place"
chmod 775 "your script place"
```
### You're done with this script. You can move on to the next step which is the final step of this tutorial.
# 5. Make it run automatically when you boot up 🥳
### Open your terminal.
### Create a new file at `/etc/xdg/autostart/` but now the name isn't end with `.sh` but `.desktop`.
#### Enter these texts in the file.
```
[Desktop Entry]
Name="You like"
Exec="Your script path"
Terminal=false
Type=Application
X-GNOME-Autostart-enabled=true
```
### Exit and save it as I said before.
### Reboot the computer and if it changes as you want it. You're finished and COMPLETED this tutorial.
### Congrats of you followed the tutorial and suceed. This means you're a semi-pro in Linux now.
### You can now sit back and enjoy your auto resolution script in every boot up!!!
