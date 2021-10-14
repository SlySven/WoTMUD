# WoTMUD
WoTMUD triggers/aliases/scripts/timers/keys/buttons/maps

The purpose of this repository is to host a collection of files for playing the WoTMUD on Mudlet, and provide an easy method of downloading and installing these files from the Mudlet command line. Please read through the following information and instructions below carefully before proceeding, and follow the steps in order to get started with a map and communications window. 


# Connecting to the game

These files are for Mudlet (https://www.mudlet.org/), a client that can be used to connect to various MUD games. Mudlet can be downloaded at https://www.mudlet.org/download/ for Windows, Linux, and macOS.

1. Open Mudlet. WoTMUD is one of the default profiles in Mudlet, so you can either (1) click on that profile and (4) connect, or (2) and (3) create a new profile with WoTMUD's information to (4) connect.
![mudlet_login_1](https://user-images.githubusercontent.com/52049495/137241355-72d43d03-b406-49ad-8623-3eb2d646b96b.png)

At this point if you are new to WoTMUD, I would recommend checking out our forums (https://forums.wotmud.info/) or game Discord server (https://forums.wotmud.info/viewtopic.php?f=74&t=7300) for more information. There is a Newbie Guide (https://forums.wotmud.info/viewtopic.php?f=76&t=12535) that should walk you through some of the basics of the game. At the very least, you need to have a character created that you can login to in order to proceed.

I should be able to be reached by tagging @weisluke in the Discord (preferably in the "#mudclient_helpdesk" channel) if you have questions about this guide or need help.

# Downloading and installing the package handler

1. Click on the file "wotpack_installer.mpackage" above. It will take you to a new page.
![wotpack_installer_1](https://user-images.githubusercontent.com/52049495/137240395-f9a6ca92-70fe-49f9-a185-227afe748527.png)

2. Click on the "Download" button. This should download the file and save it in your computer's default "Downloads" directory.
   1. Alternatively, you can right click on the "Downloads" button and "Save link as" to save it to a specific spot on your computer, e.g. the desktop.
![wotpack_installer_2](https://user-images.githubusercontent.com/52049495/137240737-23e0e19f-5c7e-49de-a497-06e431b414aa.png)

3. Login to the MUD with Mudlet and open Packages -> Package Manager from the top toolbar of icons, and click the Install at the bottom of the window that pops up. Navigate to the location you saved the wotpack_installer.mpackage file, select it, and click open. 
![mudlet_packages_1](https://user-images.githubusercontent.com/52049495/137245638-82093947-ec96-4d65-96fb-632570e2612a.png)

4. You should see an automatic help message from the package installation on your screen. If so, you can then close the Package Manager.
   1. If not, try typing "wotpack help" into the command line and hit enter.
   2. If no help message appears, something likely went wrong. Reach out for help. 

Assuming everything worked properly, what you have just installed is a script that will handle downloading and installing other triggers/aliases/scripts/timers/keys/buttons/maps from this repository via commands sent through the Mudlet command line.

5. You will notice that your font changed after installing this package. Unless you're a male channeler who's already tainted, you will probably want to change the font to sonething other than Comic Sans. You can open Settings -> Main display, and from there change the font and font size. Additionally, I would recommend making sure that the box marked "Echo Lua errors to the main console" is checked. This will assist with possible debugging, both if you need help, or if you eventually start making your own aliases/triggers/scripts.
![mudlet_settings_1](https://user-images.githubusercontent.com/52049495/137246210-491b3c45-3d6f-452e-9896-fbad996c51fd.png)
6. Additionally, you can change the default command separator in Settings -> Input line. For users who are unfamiliar, this allows you to type, e.g., "smile;wave" and have the commands "smile" and "wave" sent to the MUD separately. The default command separator is ";;", although many people prefer a single semi-colon ";" instead.
![mudlet_settings_2](https://user-images.githubusercontent.com/52049495/137246430-b1498db2-4918-456c-8d11-73e31e1b2739.png)


# Installing map scripts and a map file

1. The first step for installing these map scripts is to remove the generic mapper by going to Packages->Package Manager, clicking on the "generic_mapper", and then clicking "Remove packages". After that, you will need to restart Mudlet and login again. DO NOT SKIP THIS STEP.
![mapper_install_1](https://user-images.githubusercontent.com/52049495/137246750-164a86ff-137a-4be5-8f59-8f9a0544736c.png)

2. Make sure that you have following settings on the MUD (by typing them into the command line):
   1. "color complete" on. The mapper scripts need the room name colors to properly work.
   2. "brief" off. The mapper will work with brief mode on, just not as well (though still pretty dang well if I do say so myself, given the limitations of picking out rooms from only name and exit combinations). In a few steps, after installing the mapper, you can instead type "map brief" to have the mapper scripts manually gag the room descriptions so they don't show up on the screen, while still using them to determine your position.
3. Type "wotpack install mapper" into the command line and hit enter.
![mapper_install_2](https://user-images.githubusercontent.com/52049495/137247375-d129dd1c-0fe4-4fa3-b58b-b0fce5faa4df.png)

4. If things are successful, you should receive some messages along the lines of "(wotpack_installer): New mapper_scripts successfully installed." A new window should appear in the top right of the screen as well, though it will say that there are no rooms in the map. This is because we need to download the map file. 
![mapper_install_3](https://user-images.githubusercontent.com/52049495/137247489-22d1b16a-27a7-40c3-9331-ebfcf809c1b1.png)

5. Type "map update". You should again receive some messages about the map file downloading and installing. This may take a moment depending on your internet speed. Once that is done, the message in the top right map window should change to say that you have a map loaded, but Mudlet doesn't know where you are.
![mapper_install_4](https://user-images.githubusercontent.com/52049495/137247712-21450f8b-c8bd-43af-aec3-742d2730d68f.png)

6. Look at your room. You should see debugging next to room names, room descriptions, and direction and look inputs. This is normal. See if the map centers on your position. If the rooms are too small, you can adjust their size at the bottom of the map window (along with the size of the room exit lines). 
![mapper_install_5](https://user-images.githubusercontent.com/52049495/137248267-59c8b130-2dfa-4973-959d-7253f640b772.png)

7. You can type "map debug" to turn off the debug messages. If there are problems with the mapper, these messages can be useful in narrowing down what the issue is. 
![mapper_install_6](https://user-images.githubusercontent.com/52049495/137248345-50ee7931-b074-4cb8-9db0-4c4f890f6f8a.png)

The appearance of the map can be further changed with some tabs in the settings window, and some aliases I've built into the map script. I won't go into detail on those here, but feel free to reach out to me with questions. 

# Installing a communications window script
1. To get a communications window that stores says/chats/nars/etc, type "wotpack install communications" into the command line and hit enter. Test it out by saying something to ensure that it is capturing things properly. If it looks like it installed correctly, you can type "comms debug" as well.
![communications_install_1](https://user-images.githubusercontent.com/52049495/137248611-a7aa3f64-80e2-41bf-bb4c-955f0d1ffb2f.png)


# Installing other files

You can type "wotpack view files" to get a list of all possible files available for download. This list is NOT displayed very neatly, hopefully I can change that in the future. You can use commands from the help message to install particular pieces, or everything. Most names should be self explanatory.

