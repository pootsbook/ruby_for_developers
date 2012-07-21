---
layout: default
title: String
---

Ruby documentation: [String][rdoc-string]

## Instantiation

It seems a little ridiculous to even talk about instantiating a new String object. There is no fanfare, it is as simple as you think:

{% highlight irb %}
>> "Hello World!"
=> "Hello World!"
>> string = "Hello World!"
=> "Hello World!"
>> string.class
=> String
{% endhighlight %}

It’s also possible to use the class method `new`:

{% highlight irb %}
>> String.new("Hello World!")
=> "Hello World!"
{% endhighlight %}

## Instance Methods

It’s sometimes helpful to see methods grouped logically, rather than in a big long definition list. Where methods speak for themselves, no explanation is given.

### Interrogative

`#start_with`  
`#end_with`  
`#chr`  
`#include?`  
`#length` / `#size`  
`#empty?`  

`#count`  
`#index`  
`#rindex`  
`#slice` / `#[]` 

`#eql?`, `#==`, `#===`  
`#scan`  
`#match`, `#=~`  
`#inspect`  

### Formatting

`#center`  
`#ljust`  
`#rjust`  

### Cleaning

`#chomp`, `#chomp!`  
`#chop`, `#chop!`  
`#strip`, `#strip!`  
`#lstrip`, `#lstrip!`  
`#rstrip`, `#rstrip!`  

### Transforming

`#upcase`, `#upcase!`  
`#downcase`, `#downcase!`  
`#swapcase`, `#swapcase!`  
`#capitalize`, `#capitalize!`  
`#reverse`, `#reverse!`  

`#sub`, `#sub!`  
`#gsub`, `#gsub!`  
`#squeeze`, `#squeeze!`  
`#tr`, `#tr!`  
`#tr_s`, `#tr_s!`  
`#slice!` / `#[]=`  



[rdoc-string]: http://www.ruby-doc.org/core-1.9.3/String.html
