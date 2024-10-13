# cooker-rpi-vb

Cooker Menu for Yocto RPI tutorial (from Youtube channel: EmbeddedVB)

# Prerequists

You first need to install **Yocto** requirements : 

`sudo apt install gawk wget git diffstat unzip texinfo gcc build-essential chrpath socat cpio python3 python3-pip python3-pexpect xz-utils debianutils iputils-ping python3-git python3-jinja2 python3-subunit zstd liblz4-tool file locales libacl1`

`sudo locale-gen en_US.UTF-8`

Then you have to install a tool name **cooker** easily manage your Yocto build : 

`sudo python3 -m pip install --upgrade git+https://github.com/cpb-/yocto-cooker.git`

# Commands 

To install the project, you have to run the following command: 

`cooker cook embedded_vb_json.json`

After the download and compilation (which will take few hours), you should have the following structure : 

* layer: a folder containing all sources of the project
* builds: a folder containing all builds (based on cooker configuration for MACHINE and DISTRO). The sub-folder *build-embedded-vb* is the directory where the actual build process takes place.
* sstate-cache: stores build artifacts that can be reused in future builds, speeding up the process
* downloads:  folder where Yocto stores all the downloaded source code and files for the recipes during the build process. 

# Issues 

If you face issues, you may need to use bitbake commands. To configure your environment to interact with the build you should use the following: 

`cooker cook embedded-vb`

Otherwise, feel free to contact me at: valentin.boudevin@gmail.com with a short description of your issue. 

# Usefull links

Yocto official documentation: https://docs.yoctoproject.org/brief-yoctoprojectqs/index.html
Cooker official documentation: https://www.google.com/search?client=ubuntu-sn&channel=fs&q=cooker+yocto