# cloud-assignment-1

Your login name: altschool i.e., home directory /home/altschool. The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.


```bash 
    #creating a new user "altschool" with home directory /home/altschool.
    #(using vagrant user).
    sudo useradd -m altschool

    #adding altschool user to sudo group to be able to complete tasks 9 - 13.
    usermod -aG sudo altschool 

    #switch to altschool user.
    sudo su - altschool

    #creating sub-directories in altschool user home directory.
    mkdir code tests personal misc
```

### TASK 1

```bash 
    #change directory to tests directory using absolute pathname.
    cd ~/tests
```

### TASK 2

```bash 
    #change directory to tests directory using relative pathname.
    cd ./tests
```

### TASK 3

```bash
    #use echo command to create a file named fileA with text content "Hello A" in the misc directory.
    echo "Hello A" > ~/misc/fileA
```

### TASK 4

```bash
    #create an empty file named fileB in the misc directory. Populate the file with a dummy content afterwards.
    touch ~/misc/fileB
    echo "A dummy text" > ~/misc/fileB
```

### TASK 5

```bash
    #copy contents of fileA into fileC.
    cp ~/misc/fileA ~/misc/fileC
```

### TASK 6

```bash
    #move contents of fileB into fileD.
    mv ~/misc/fileB ~/misc/fileD
```

### TASK 7

```bash
    #Create a tar archive called misc.tar for the contents of misc directory.
    tar cf misc.tar ~/misc
```

### TASK 8

```bash
   #compress the tar archive to create a misc.tar.gz file.
   tar czf misc.tar.gz ~/misc.tar
```

### TASK 9

```bash
   #create a user and force the user to change his/her password upon login.

   #creating user specifying password.
   sudo useradd -m -p klaroline user1

   #expiring password.
   sudo passwd -e user1
```

### TASK 10

```bash
   #lock a users password.

   #creating a user specifying password.
   sudo useradd -m -p stelena user2

   #locking password.
   sudo passwd -l user2
```

### TASK 11

```bash
    #create a user with no login shell.
    sudo useradd -m -s /sbin/nologin user3
```

### TASK 12

```bash
   #disable password based authentication for ssh.

   #open sshd_config file with vim editor.
   sudo vi /etc/ssh/sshd_config

   #edit line with "PasswordAuthentication", setting value to no.
   PasswordAuthentication no

   #to effect changes after saving and exiting the editor.
   sudo service ssh restart
```

### TASK 13

```bash
   #disable root login for ssh.

   #open sshd_config file with vim editor.
   sudo vi /etc/ssh/sshd_config

   #edit line with "PermitRootLogin", setting value to no.
   PermitRootLogin no

   #to effect changes after saving and exiting the editor.
   sudo service ssh restart
```
