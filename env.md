---
title: Environment Setup
subtitle: Installing a Ruby and Rails Ready Vagrant Box
---

Vagrant and VirtualBox are being used to provide a consistent Ruby and Rails environment. A box has been provisioned with the necessary packages and tools. There is an added bonus of operating in a sandbox, minimizing disruption to your host machine. Set it up by following the instructions below.

* Download and install VirtualBox
* Download and install Vagrant
* Create a new directory to hold your project, e.g:

``` bash
$ mkdir ~/ruby_course
$ cd ruby_course
```

* Download and setup the Vagrant box:

``` bash
$ vagrant box add test https://s3.amazonaws.com/railstraining/rails_test.box
$ vagrant init test
$ vagrant up
```
