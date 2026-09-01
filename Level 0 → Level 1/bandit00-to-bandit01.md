# Level 0 → Level 1

### **🎯 Objective:** 
> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

The approach is simple: connect remotely through **ssh** as user `bandit0`, authenticate with the default password `bandit0`, inspect the directory contents, and print the target file.

### **⌨️ Commands used:**

First to connect remotely through **ssh** and authenticate using the default password `bandit0`:

```bash 
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

<p align="center">
    <img src= "../assets/Level 0 -> Level 1/step1.png" />
</p>

Secondly, list **all** the contents of the current directory:

```bash
ls -a 
```

<p align ="center">
    <img src= "../assets/Level 0 -> Level 1/step2.png" />
</p>

Lastly, print the content of the **readme** file: 

```bash
cat readme
```

<p align ="center">
    <img src= "../assets/Level 0 -> Level 1/step3.png" />
</p>

Finally we get the password for user `bandit1` which is `6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR`.

### **💡 Key takeaways:**

**⌨️ Commands:**

* SSH Syntax: The structure ssh <user>@<host> -p <port> allows remote shell access over a non-standard port (2220).
* File Inspection: ls (list) checks current directory contents, while cat (concatenate) outputs file content directly to standard output (stdout).

**🚩 Flag:**

* Port selection flag (-p):
    * SSH connects to port 22 by default.
    * Passing `-p 2220` instructs the SSH client to override the default and establish an encrypted session through port 2220.
* Listing flags (-l, -a, -al): 
    * -l (long listing) outputs essential metadata, including file owner, group, read/write/execute permissions, and exact byte size.
    * -a (all) reveals hidden dotfiles (e.g., .bashrc, .profile), preventing critical files from being overlooked.
    * -al (or -la) combines both of the aforementioned flags.
