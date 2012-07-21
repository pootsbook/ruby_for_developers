---
layout: default
title: Explore the Box
subtitle: Get to know your surroundings
---

Having completed the steps on the [Environment Setup][i] you should now be running a virtual machine within VirtualBox via Vagrant. To login via ssh from your *host* machine’s command line type:

{% highlight sh %}
$ vagrant ssh
{% endhighlight %}

This command logs you into a *guest* machine running Ubuntu 12.04 LTS (Precise Pangolin). This machine has been provisioned using Chef-Solo and comes with the following installed:

* **Ruby 1.9.3**  
    *the latest stable version of Ruby*
* **Rails 3.2.6** *the latest stable version of Rails*
* **Sqlite3** *default SQL RDBMS for development*
* **Git** *the world’s most popular DVCS*
* **Vim** *the programmer’s text editor*
* **Node.js** *server-side JS environment*
* **Redis** *advanced key-value store*
* **MongoDB** *NoSQL DB*

Your username is `vagrant` and the root password is identical in case you need to invoke any commands with root permissions via `sudo`.


[i]: /environment.html "Environment Setup"
