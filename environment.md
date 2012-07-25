---
title: Environment Setup
subtitle: Installing a Ruby and Rails Ready Vagrant Box
layout: default
---

Vagrant and VirtualBox are being used to provide a consistent Ruby and Rails environment. A box has been provisioned with the necessary packages and tools. There is an added bonus of operating in a sandbox, minimizing disruption to your host machine. Set it up by following the instructions below.

* [Download][vbd] and install [VirtualBox][vb] (version > 4.1)
* [Download][vd] and install [Vagrant][v] (version > 1.0)
* Create a new directory to hold your project, e.g:

{% highlight sh %}
$ mkdir ~/ruby_course
$ cd ruby_course
{% endhighlight %}

* Download and setup the Vagrant box:

{% highlight sh %}
$ vagrant box add rubyrails https://s3.amazonaws.com/railstraining/rubyrails.box
$ vagrant init test
$ vagrant up
{% endhighlight %}

Login to the box and browse to the shared directory:

{% highlight sh %}
$ vagrant ssh
$ cd /vagrant
{% endhighlight %}

Inspect your environment:

{% highlight sh %}
$ ruby -v
ruby 1.9.3p194 (2012-04-20 revision 35410) [x86_64-linux]
$ rails -v
Rails 3.2.6
{% endhighlight %}


[vbd]: https://www.virtualbox.org/wiki/Downloads "Oracle VirtualBox Download Page"
[vb]: https://www.virtualbox.org/ "Oracle VirtualBox"
[v]: http://vagrantup.com/ "Vagrant"
[vd]: http://downloads.vagrantup.com/tags/v1.0.3 "Vagrant Download Page"

