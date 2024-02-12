# 1st Cloud Assignment

Your login name: altschool i.e., home directory /home/altschool. The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.

#### Questions
1. Change directory to the tests directory using absolute pathname
1. Change directory to the tests directory using relative pathname
1. Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory
1. Create an empty file named fileB in the misc directory. Populate the file with a dummy content afterwards
1. Copy contents of fileA into fileC
1. Move contents of fileB into fileD
1. Create a tar archive called misc.tar for the contents of misc directory
1. Compress the tar archive to create a misc.tar.gz file
1. Create a user and force the user to change his/her password upon login
1. Lock a users password
1. Create a user with no login shell
1. Disable password based authentication for ssh
1. Disable root login for ssh

**Answers**

**Your login name: altschool i.e., home directory /home/altschool.**
**The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified**

```
sudo useradd - m -s/usr/bin/bash Altschool 
sudo passwd Altschool
sudo usermod -aG sudo Altschool
su Altschool
pwd
mkdir code tests personal miscs
ls
```
![Altschool-HomeDir](./images/usrhome.PNG)
![Altschool-sudoPriviledge](./images/sudo_priviledges.PNG)
![ConfirmationofHome](./images/confirmation_of_home.PNG)
![CreateDirectories](./images/create_directories.PNG)

**you are running commands from the home directory.**
```
echo $HOME
ls
```

- Change directory to the tests directory using absolute pathname
```
cd /home/Altschool/tests
```
![Absolute-path](./images/Absolute-path.PNG)


- Change directory to the tests directory using relative pathname
```
cd tests
```
![Relative-path](./images/relative-path.PNG)


- Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory
```
echo 'Hello A' > miscs/fileA
```
![echoFIle](./images/newFIle-with-echo.PNG)


- Create an empty file named fileB in the misc directory. Populate the file with a dummy content afterwards
```
touch miscs/fileB to create the fileB then use vi editor to put dummy content vi fileB.

press i to insert and type the dummy content (mezikko is a baller) then after press escape and put :wq and click enter.

cat fileB shows up mezikko is a baller.
```
![fileBTOuch](./images/fileBwith-TOuch.PNG)
![dummyCOntent](./images/dummy-content-fileB.PNG)


- Copy contents of fileA into fileC
```
cp fileA fileC
```
![copyCOntent](./images/copy-contents.PNG)


- Move contents of fileB into fileD
```
mv fileB fileD
```
![moveCOntent](./images/move-contents.PNG)


- Create a tar archive called misc.tar for the contents of misc directory
```
tar -cvf misc.tar 
```
![tarAFile](./images/tar_a_file.PNG)


- Compress the tar archive to create a misc.tar.gz file
```
gzip misc.tar
```
![gzip.tarAFile](./images/gzip.tar.PNG)


- Create a user and force the user to change his/her password upon login
```
sudo useradd lewinski
add pasword sudo passwd lewinski
enforce passwd change
sudo chage -d 0 lewinski
```
![forcePassChange](./images/force.passwordchange.PNG)


- Lock a users password
```
sudo passwd -l lewinski 
to unlock it, you use -u
```
![lockPassword](./images/lock.password.PNG)


- Create a user with no login shell
```
sudo useradd -s /usr/sbin/nologin chinaza
```
![nologinShell](./images/nologin.shell.PNG)


- Disable password based authentication for ssh
```
sudo vi /etc/ssh/sshd-config
```
![disable.pass.auth](./images/disable.pass.auth.ssh.PNG)


-  Disable root login for ssh
```
sudo vi /etc/ssh/sshd-config
```
![disable.rootLogin](./images/disable.rootLoginForssh.PNG)

