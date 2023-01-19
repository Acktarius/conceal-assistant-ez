# conceal-assistant-ez #

to install Conceal Assistant on CCX-BOX in just few clicks

download both files .deb and .deb.sig in the same folder
verify signature :
```
gpg --verify <file.deb.sig>
```
if you're happy with the signature
then you can right click on the conceal-assistant deb file,
choose open with other application, select Software Install.

OR 

from the terminal :

`sudo dpkg -i <file.deb>`

## What does it do ? ##
It includes 4 Bash script :

#### 2 for installation:

Preinst : Pre-install checks if you have node, npm, nodemon already installed, if not they will be installed

  Then it will place conceal-assistant folder to its destination folder : opt

Postinst : Post-installation installs the dependancies, and move + enable + start the ccx-assistant.service

#### 2 for uninstall:

Prerm : Pre-remove stops and disable ccx-assistant.service

Postrm : Post-remove deletes the service and conceal-assistant folder

