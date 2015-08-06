---
layout: post
title:  "A Bit of Binary"
date:   2015-08-05
categories: jekyll update
---
Binary numbers are based on a base-2 numeral system, wherein the digits most typically used are 0 and 1. Generally,
especially when it comes to power-related items, a 0 represents an 'off' position while a 1 represents a '1' position.
When counting, the same can be said to be true for the positions that either the 0s or 1s hold, where only the positions
containing 1 are really counted. In the next bit, I will break down how binary counting works in its most simplest form.

For this example, we will only use 16 bits, of which are 0 - 15 when we count.  
First up is a demonstration of 0:  
    
    0000 = 0  

Next up is the representation of 15:

    1111 = 15

Now you may be asking, "how in the world does this make any sense?" Well, let's start off by writing an example of how a
base-2 system works. From there it shouldn't be too hard to figure out the rest (in fact, all base systems work the same 
and the knowledge aquired here can easily be transplanted into understanding any other base numeral system!).

From the right to left, a base system starts with power 0 and to the relative base, and increments from there for every digit
place to the left.

Example:

    0001 is numerical value 2^0 which equals 1
    0010 is numerical value 2^1 which equals 2
    0100 is numerical value 2^2 which equals 4
    1000 is numerical value 2^3 which equals 8

Add up the corresponding placements of 1 within a binary statement, and you can now easily get the sum!

Example 1:
    
    What is the number produced by 1101?
    Answer: 13
    Solution: 1101 = 8 + 4 + 1 = 13

Example 2:

    What is the binary represation of the number 7?
    Answer: 0111
    Solution: 7 = 4 + 2 + 1 = 0111

As stated earlier, the same principles can be applied to any base numeral system which can come in handy, especially with
front end development and the hexadecimal system for CSS.