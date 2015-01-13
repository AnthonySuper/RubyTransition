## The REPL

Ruby, unlike Objective-C, does not need to be compilled in order to run.
This allows us to do some interesting things.
Perhaps the nicest side effect is the ability to have a REPL.
REPL stands for Read-Eval-Print Loop.

It is comprised of four steps

1. Read user input.
2. Evaluate this user input as a line of code in the language.
3. Print out the result of that evaluation.
4. Go back to 1.

Ruby's REPL is called IRB, for "Interactive RuBy."
It has some limitations, making a program called "pry" generally better, but we can't install that on school computers due to administration issues.
So we're stuck with IRB.
Don't worry, it can do the job just fine.

With that, let's begin...

### Getting to know Ruby
First off, just type "hello" into a console.

```
2.1.1 :001 > "hello"
 => "hello"
```

So, after reading the word hello in quotes, ruby evaluates it to... the word hello in quotes.
This teaches us that Ruby evaluates strings to themselves.

Let's try it with a number:

```
2.1.1 :002 > 1
 => 1
```

Interesting. Numbers also evaluate to themselves.

Does math work the way we expect?

```
2.1.1 :003 > 2 + 2
 => 4
```

Nice.
### Variables
In Objective-C, we could assign values to a variable.
So, if we wanted the number 10 in a variable, we'd do this:

```Objective-C
int i = 10;
```

Ruby is similiar, with one key difference: Ruby is dynamically typed.
This means that the language doesn't really care about what a variable is---it can be a string, or a number, or even an object.
As a result, assigning a variable is simple:

```
2.1.1 :004 > i = 10
 => 10
```

Ruby will remember that the variable ```i``` has the value ```10```, like so:
```
2.1.1 :005 > i
 => 10
```

Of course, Ruby is dynamically typed. So we can do this:

```
2.1.1 :005 > i = "I'm not a number!"
 => "I'm not a number!"
```

When you feel comfortable with this concept, move onto [Chapter 2](../chapter_2/main.md)

