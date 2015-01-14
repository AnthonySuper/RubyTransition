String Interpolation and Blocks
-------------------------------

This chapter covers some topics that are pretty different.
One is familiar, one is alien.
Let us start with the familiar.

### String Interpolation

The easiest way to teach this is with a bunch of examples.

```
2.1.1 :001 > i = 10
 => 10 
2.1.1 :002 > str = "i is #{i}"
 => "i is 10" 
2.1.1 :003 > i = 20
 => 20 
2.1.1 :004 > str
 => "i is 10" 
2.1.1 :005 > name = "Anthony"
 => "Anthony" 
2.1.1 :006 > str = "Hello, #{name}!"
 => "Hello, Anthony!" 
2.1.1 :007 > "I can do expressions, too! 1 plus 1 is #{1+1}"
 => "I can do expressions, too! 1 plus 1 is 2" 
```

#### Task:
Play around with String Interpolation in a Terminal for a bit

### Blocks

Blocks in Ruby are very similar to those in Objective-C, with some key differences.
For example, their syntax isn't [awful](goshdarnblocksyntax.com).
There's also a few different ways to declare them. The first is the Proc way:
```Ruby
block = Proc.new do |x|
  "x is #{x}"
end

block.call(10) # "x is 10"
```

The second is the Lambda way. Actually, there's two of those as well:

```
# First way
lam = lambda do |x|
  "x is #{x}"
end

lam.call(10) # Same thing as the Proc method

# Second way:

lam = ->(x) do
  "x is #{x}"
end

lam.call(10) # You can guess what this does

```

The main difference has to do with how they return a value.
In a lambda, they return like calling a method normally. 
In a Proc, they just return: they don't care what you're doing, they're returning to the top level, dangit.
So if you call a Proc with a return in a method, it will instantly return from that method, regardless of where you are.

I tend to use lambdas far more often.

### Task

Make a lambda which does something interesting.

When you are ready, it's time for [Chapter 5!](../chapter_5/main.md)

