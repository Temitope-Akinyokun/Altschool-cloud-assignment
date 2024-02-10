# cloud-assignment-1

Creating a new user "Alt School" with home directory "/home/altschool".
Creating sub-directories code, tests, personal, misc in the home directory. 
(using vagrant user).

```bash 
    #creating a new user "altschool" with home directory /home/altschool.(using vagrant user).
    sudo useradd -m altschool

    #switch to altschool user
    sudo su - altschool

    #creating sub-directories in altschool user home directory.
    mkdir code tests personal misc
```

### TASK 1

```bash 
    #change directory to tests directory using absolute pathname
    cd ~/tests
```

### TASK 2

```bash 
    #change directory to tests directory using relative pathname
    cd ./tests
```

###
