# Ubuntu Virtual Machine #

This is a very flexible virtual machine that allows you to create a simple Ubuntu Server 22.04 LTS (Jammy Jellyfish) for LAMP stack developers which also includes many related modern development tools.

Please read all the document before start using the project.

## Overview ##

A lot of PHP websites and applications don’t require much server configuration or overhead at first. This virtual machine should have all your needs for doing basic development so you don’t have to worry about configuring the virtual environment and you can simply focus on your code.

The virtual machine was provisioned with the following software:

- Ubuntu Linux.
- Apache Web Server.
- MySQL Database.
- PHP Scripting Language.

Other software included:

- Git.
- PHPMyAdmin.
- Zip.

## Setup ##

The project has the following pre-requisites:

- Git http://git-scm.com/
- Vagrant http://www.vagrantup.com/
- VirtualBox http://www.virtualbox.org/

Now execute the following command:

```
$ vagrant up
```

Once ready, you can test it by opening following URL on your browser:

```
http://192.168.80.80/
https://192.168.80.80/ (secure)
```

If you want to manage the MySQL database:

```
http://192.168.80.80/phpmyadmin/
https://192.168.80.80/phpmyadmin/ (secure)

Database Name : development
User : root
Password : pass
```

That's all, as you can see, very simple.

If you need more information related to Vagrant, go to the official [Vagrant documentation](https://www.vagrantup.com/docs).

## Why Vagrant and not Docker ##

Vagrant is a tool focused on providing a consistent development environment workflow across multiple operation systems. Docker is a container management that can consistently run software as long as a containerization system exists.

Containers are generally more lightweight than virtual machines, so starting and stopping containers is extremely fast. Most common development machines don't have a containerization system built-in, and Docker uses a virtual machine with Linux installed to provide that.

Currently, Docker lacks support for certain operating systems (such as BSD). If your target deployment is one of these operating systems, Docker will not provide the same production parity as a tool like Vagrant. Vagrant will allow you to run a Windows development environment on Mac or Linux, as well.

For microservice heavy environments, Docker can be attractive because you can easily start a single Docker VM and start many containers above that very quickly. This is a good use case for Docker. Vagrant can do this as well with the Docker provider. A primary benefit for Vagrant is a consistent workflow but there are many cases where a pure-Docker workflow does make sense.

Both Vagrant and Docker have a vast library of community-contributed "images" or "boxes" to choose from.

## MIT License ##

### Copyright (c) 2022 Esteban Spina ###

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
