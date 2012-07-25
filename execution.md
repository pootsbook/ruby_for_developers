---
layout: default
title: Execution
---


{% highlight sh %}
$ irb --simple-prompt
{% endhighlight %}

{% highlight irb %}
>> puts "Hello World!"
"Hello World!"
=> nil
>>
{% endhighlight %}


{% highlight ruby %}
class Person < ActiveRecord::Base
  def name
    [first_name, last_name].join(' ')
  end

  private

  def activate!
    update_attribute(:activated, true)
  end
end
{% endhighlight %}
