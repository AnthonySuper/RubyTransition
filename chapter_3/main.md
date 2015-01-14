Classes and Methods
-------------------

Ruby, like Objective-C, has Classes and methods.
They way classes are delcared and the way methods are used looks very different, but the general concepts are very similar.

To begin, we will start with the most fundamental concept in Ruby:

### Everything is an Object

Yep, everything.
Everything in Ruby is an instance of a class.
This includes fundamental types, like strings or numbers. Have a look!

```
2.1.1 :001 > 1.class
 => Fixnum
```

Yep. That simple. Quite literally everything in Ruby is some sort of object.

### Messages are Everywhere
In Objective-C, we sent messages like this:

```Objective-C
[object sendMessage];
```

Ruby's syntax is a lot cleaner:
```Ruby
object.send_message
```

When sending a message with arguments in Objective-C, we used something like this:

```Objective-C
[object sendMessageWithArgument: other andADifferentArgument: 15];
```

In Ruby, this is also simpler:

```Ruby
object.send_message(other, 15)
```

### Making our Own Classes

Er... This gets really awkward to do in a REPL.

Let's learn to edit files first, shall we?

### Editing Files

This is pretty easy.

1. First, open up a new tab in your terminal. You should be in the same folder as this repository.
2. Type ```mkdir tasks``` to make a new folder called "tasks"
3. Type ```cd tasks``` to get into this folder.
4. Type ```touch first_class.rb``` to make a new file called "first_class.rb". Ruby files end in .rb, similar to how Objective-C files ended in either .h or .m. There is no seperation of interfaces and implementations in Ruby; both go in the same file. This simplifies things a lot.
5. Navigate to that folder in Finder and double-click the file. It should open in Xcode. I'd recommend a different editor for Ruby normally (either [Sublime Text](http://www.sublimetext.com/) if you're a normal person or [Vim](http://www.vim.org/) if you are a wizard), but the school doesn't let us install software, so we'll make do with what we have.

Now you're ready to edit some Ruby.

### Our own Classes (For Real this time)

Let's start with a simple example. I'll provide the full definition first,
then break it down line-by-line.

```Ruby
class Person
  def name
    @name
  end

  def name=(n)
    @name = n
  end
end

p = Person.new
p.name = "Anthony"
puts p.name
```
Run this with "ruby first_class.rb"

#### Breakdown
To start off:

```Ruby
class Person
  # Stuff that isn't important right now
end
```
This declares a new class, called "Person".
Class names in Ruby MUST start with a capital letter.

```Ruby
  def name
    # ...
  end
```
This declares a new method for this class. Similiar to:
```Objective-C
-(NSString) name{

}
```

Since Ruby is dynamically typed, we don't care what it returns.
So we omit that part of the declaration.

```Ruby
   @name 
```

There are a few things going on here.

First, classes in Ruby have member variables, just like in Objective-C.
In Ruby, however, you declare variables differently.
Whenever you use a ```@``` before a variable name while in a class, it becomes a member variable.

Second, Ruby doesn't neccisarily need a "return" statement.
There is an implicit return at the start of the last line in a method.

```Ruby
   def name=(n)
      # ...
   end
```

Ruby methods allow you to "overload" operators, like the ```=```.

The arguments in Ruby have no type, being just a list of variable names you can use inside of a method.

Now, let's go down a bit.

```Ruby

p = Person.new

```

Similar to 

```Objective-C

Person *p = [[Person alloc] init];
```

```Ruby
p.name= "Anthony"
```

Calls the method you declared earlier, ```name=```, with the argument of "Anthony". 
This sets the local variable ```@name``` to "Anthony".

```Ruby
puts p.name
```

Calls the method ```name```.
This returns ```@name```, which, if you recall, we set to "Anthony" earlier.

The ```puts``` is a function that prints something on the screen.

It stands for "put string".

### Task

Write 2 other methods, ```age``` and ```age=```. Set the age of your person object, and print it.

When you're ready, move on to [Chapter 4](../chapter_4/main.md)

