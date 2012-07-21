---
layout: default
title: Using Redis
---

Redis is installed and running on `localhost`, port `6379`. Using it is simple with the `redis` rubygem.

### irb

{% highlight sh %}
$ irb --simple-prompt
{% endhighlight %}

{% highlight irb %}
>> require 'redis'
=> true
>> redis = Redis.new
=> #<Redis client v2.1.1 connected to redis://127.0.0.1:6379/0 (Redis v2.4.2)>
>> redis.set("mykey", "Hello World!")
=> "OK"
>> redis.get("mykey")
=> "Hello World!"
{% endhighlight %}

### Rails

Add redis-rb to your `Gemfile`:

{% highlight ruby %}
gem 'redis'
{% endhighlight %}

Assign a Redis instance to a global variable in an initializer `config/initializers/redis.rb`:
{% highlight ruby %}
$redis = Redis.new
{% endhighlight %}


{% highlight sh %}
$ rails console
{% endhighlight %}

{% highlight irb %}
>> $redis
=> #<Redis client v2.1.1 connected to redis://127.0.0.1:6379/0 (Redis v2.4.2)>
>> $redis.set("mykey", "Hello World!")
=> "OK"
>> $redis.get("mykey")
=> "Hello World!"
{% endhighlight %}

### More Information

Read more about Redis at [redis.io][redis] and on using it with Ruby on the [redis gem README][redis-rb] on GitHub. Jim Neath has a good writeup on common Redis usecases with Rails on [his blog][redis-neath].

[redis]: http://redis.io "Redis"
[redis-rb]: https://github.com/redis/redis-rb
[redis-neath]: http://jimneath.org/2011/03/24/using-redis-with-ruby-on-rails.html "Using Redis with Ruby on Rails"
