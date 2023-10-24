# Installing-Updating-and-Removing-Software-in-Linux

<h2>Objectives</h2>

- Update VLC Media Player to the newest version
- Install Firefox on the machine
- Uninstall GIMP

<h4>Heads up</h4>

- Many commands you'll use start with "sudo". It is used across Linux to tell the system that you're the "superuser". This grants permission to perform sensitive operations, like installing or uninstalling software.

<br>

<h2>Verifying Installed Software on Linux</h2>

Use the command "dpkg -s" followed by the unique package name for a program to quickly check if it's already installed on Linux. The "-s" in dpkg stands for "search," which allows you to search for a program on your machine and see if it's installed. For example, Firefox isn't installed, but GIMP is.

    dpkg -s firefox-esr
![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/2d43e927-ad55-423c-8359-dae9babdee31)

    dpkg -s gimp
![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/3aa98e2d-7912-4d3a-a976-4ec14a36f039)

<br>

<h2>Updating VLC Media Player</h2>

The command below shows that vlc is installed, but out of date.

    dpkg -s vlc

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/10724673-a1d1-42cf-99ee-09e973113eb7)

We will update VLC by forcing an update of the package manager using the command:

    sudo apt-get install -f

This starts the update process. Lots of text will show on your terminal, and it will ask you if you'd like to continue.

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/60e86ffb-6625-43a2-b797-e359f3ab3bc2)

After it updates search vlc again to verify it got updated by looking at the version.

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/1ccc710c-528a-4c87-a66a-83b119cb38b3)

<br>

<h2>Installing Mozilla Firefox</h2>

Now let's install Firefox. Parts of this process will be unique to this installation, but most steps you take will be identical, regardless of the software you are trying to install onto your Linux machine. A lot of common programs are set up in repositories that most Linux distributions are aware of, by default. This makes installing these programs very easy. You won't have to manually download and install the program. To make sure the repositories are up to date run this command:

    sudo apt-get update
    
![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/c4e8b1d4-89a6-4e70-ad70-6a94bf1c036e)

Now you're ready to install Firefox. Run the command below in the terminal:

    sudo apt-get install firefox-esr

You'll be prompted to confirm that you'd like to continue the installation.

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/5df03198-b2b2-4d8d-8dc3-9c206a0c3131)

Firefox will now be installed. To verify that it's installed use the search command we learned earlier to search for Firefox on your machine.

    dpkg -s firefox-esr

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/381d0821-c532-4b76-862d-0910da547f3f)

<br>

<h2>Uninstalling GIMP</h2>  

GIMP, like Firefox, can be installed and uninstalled using the "apt-get" commands we used to install Firefox. To uninstall GIMP, or any other program you want to uninstall from your Linux machine, you would use "remove".

    sudo apt-get remove gimp

This will start the process of uninstalling GIMP from your machine. Confirm using "Y". 

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/9b3a0543-95aa-4af1-b755-68658c66d200)

After uninstallation, you can confirm the removal of GIMP by once again searching for the program.

    dpkg -s gimp

![image](https://github.com/n8som/Installing-Updating-and-Removing-Software-in-Linux/assets/110139109/b3debcc9-d1c3-445b-8b66-2ec84b8bfa45)

<br>

<h4>Congrats! You've now learned how to Install, Update, and Remove Software in Linux!</h4>
