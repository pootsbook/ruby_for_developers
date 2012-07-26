---
layout: default
title: Putting Ruby into Practice
---

This is an extended example, broken up into different sections. By the end you should have worked through a number of the concepts you have met so far.

## ISBN nightmares

John, your boss, has handed you a file of what look like ISBN numbers. You have to make sense of them, and then go and fetch book details from the Amazon API.

Create a file with the following data:

```
978-05965-161-78  
978 14302 23634  
978-032 158 4106  
978-0321743121  
978-1934-356-470  
978-03214904-52  
```

The first step will be to reading the file using Ruby and make a list of ISBNs that you can then ‘clean up’ and validate. It would be really useful for John if you could check their validity using the check digit, and also convert them to ISBN 10 for his legacy librarian application.

## A Valid ISBN.

Details about ISBNs can be found on [Wikipedia](http://en.wikipedia.org/wiki/Isbn).

- An ISBN has either 10 or 13 digits.
- An ISBN can contain dashes, but these should be removed for manipulation.
- There is a way to use the last digit (Checksum) to validate it, details are on Wikipedia.

The second step will be to get and manipulate the book details that come back from Amazon.
