---
layout: default
title: Execution
---

## Running Ruby

There are two main ways to run or execute Ruby code on your machine. One involves invoking the `ruby` executable from the command line and the other from within a REPL via `irb`. Both commands come by default after installing Ruby.

### Command Line Execution

#### Inline

The simplest way to run a Ruby expression is to do it inline on the command line with `ruby -e`:

{% highlight sh %}
$ ruby -e 'puts "Hello World!"'
Hello World!
{% endhighlight %}

#### Ruby File

Ruby files have a file-ending of `.rb`. Given a file `hello_world.rb` with the following contents,

{% highlight ruby %}
puts "Hello World!"
{% endhighlight %}

it can be run as follows:

**CODE** hello_world.rb  
{% highlight sh %}
$ ruby hello_world.rb
Hello World!
{% endhighlight %}

#### Executable Script

You can turn that file into an executable script by adding a line called the shebang to the very top. There’s no need for the `.rb` extension either.

**CODE** hello_world
{% highlight ruby %}
#!/usr/bin/env ruby

puts "Hello World!"
{% endhighlight %}

Make it executable then run it:

{% highlight sh %}
$ chmod +x hello_world
$ ./hello_world
Hello World!
{% endhighlight %}

### Interactive RuBy (irb)

`irb` is a Read Eval Print Loop (REPL) for Ruby that allows you to enter Ruby expressions and statements and returns the result.

{% highlight sh %}
$ irb --simple-prompt
{% endhighlight %}

{% highlight irb %}
>> puts "Hello World!"
"Hello World!"
=> nil
>>
{% endhighlight %}

In the previous example the return value or result of the expression `puts "Hello World!"` is indicated by the **Hash Rocket** (`=>`) and it is nil. Try some arithmetic:

{% highlight irb %}
>> 9 + 6
=> 15
>> 9 * 6
=> 54
{% endhighlight %}

Or some string concatenation:

{% highlight irb %}
>> "Hello ".concat "World!"
=> "Hello World"
>> "Hello " + "World!" 
=> "Hello World"
>> "Hello " << "World!"
=> "Hello World!"
{% endhighlight %}

Notice that there are three different ways of doing the same thing. This is a good example of **The Principle of Least Surprise**. Another is:

{% highlight irb %}
>> "Hello World!".length
=> 12
>> "Hello World!".size
=> 12
{% endhighlight %}
