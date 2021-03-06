---
title: Linux Crash Course
description: A workshop for students intended to get them started with Linux. Hosted by the UWB ACM.
---

Welcome to the Linux Crash Course!
Please open this website on your phone for later reference!

![Tux Penguin](Tux.png)

## https://uwb-acm.github.io/Linux-Crash-Course

## Sign-In Link

[Please sign-in by submitting your name and UW e-mail address here: https://goo.gl/forms/oSl9sYt2PzJfE4GV2](https://goo.gl/forms/oSl9sYt2PzJfE4GV2)

## Before We Begin...

1. Please pick up **one** flash drive from an ACM officer. This drive has already been formatted
  with the latest **Ubuntu 18.04 LTS** installation image for you.
  
2. Open this website on your phone, for later reference! https://uwb-acm.github.io/Linux-Crash-Course

3. (Optional) If you have a newer computer running Windows 10, you may have to disable Secure Boot.
  [Please follow the instructions listed here.](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/disabling-secure-boot)
  
4. Turn off your laptop, as we will start booting in Linux shortly. (Not sleep mode or hibernation!)

## Resources

[Slides and presentation material by Aidan Hahn](https://gitlab.com/whom/linux-workshop-fall-2018)

[Commands Reference Cheat Sheet](/LinuxLab_CheatSheet.pdf)

### Command Examples

These are most of the commands that will be demonstrated during the workshop.
Lines that begin with `$` indicate user input, other lines will show expected output.

#### Hello World

```console
$ echo "Hello World!"
Hello World!
$ pwd
/home/ubuntu
$ ls
Desktop
Documents
...
$ ls -l 
drwxr-xr-x  4 ubuntu ubuntu  4096 XXX XX XX:XX Desktop
drwxr-xr-x  7 ubuntu ubuntu  4096 XXX XX XX:XX Documents
...
$ mkdir tmp
$ ls
Desktop
Documents
...
tmp
$ cd tmp
$ pwd
/home/ubuntu/tmp
```

#### Manipulating Files

```console
$ touch index.html
$ nano index.html
(nano opens, press CTRL+O, CTRL+X to save and exit)
<html><body><h1>Hello World!</h1></body></html>
$ cat index.html
<html><body><h1>Hello World!</h1></body></html>
```

#### Installing Software (git)

```console
$ sudo apt update
...
$ sudo apt install git
(press y)
$ git clone https://gitlab.com/whom/linux-workshop-fall-2018.git
```

#### Hello World with Java

Open the built-in Text Editor application.

```java
public class Hello
{
    public static void main(String args[])
    {
        System.out.println("Hello World!");
    }
}
```

Install the Java Development Kit
```console
$ sudo apt install default-jdk
```

Save the file as `Hello.java` (case sensitive).
Compile it with 

```console
$ javac Hello.java
$ java Hello
```

#### Hello World with C++

Navigate to the directory that you cloned in _Installing Software (git)_.

```console
$ nano hello.cpp
$ g++ hello.cpp
$ ./a.out
Hello World!
```

#### SSH & SCP

```console
$ ssh netid@uw1-320-lab
$ scp Hello.java netid@uw1-320-lab
```

## Learn about UWB ACM at [uwbacm.com](https://uwbacm.com)
