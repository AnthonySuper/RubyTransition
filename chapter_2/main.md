Hashes
------

A hash is a pretty important concept in Ruby, so I figured I'd cover it here.

Just like a ```NSDictionary``` in Objective-C, a Hash is a way to group keys and values together.
In Ruby, however, the keys don't have to be strings.
They can be anything you like.

First, let's start with an example, using Ruby's dedicated hash syntax.
```
2.1.1 :001 > h = {"name" => "Bob", :age => 10, 15 => 1}
 => {"name"=>"Bob", :age=>10, 15=>1}
2.1.1 :002 > h["name"]
 => "Bob"
2.1.1 :003 > h[:age]
 => 10
2.1.1 :004 > h[15]
 => 1
```

### Symbols

Most of the time, in Ruby, you want to use a symbol as the key for a hash.
The reasons for that are slightly advanced, but ask me and I'll explain them if you wish.

You make a new symbol by putting a ```:``` before a word. So:
```ruby
:name
:age
:date
# You can also use underscores:
:date_time
# Capital letters are technically allowed, but it's bad practice:
:Name
```

Symbols work well as a key for a hash because they are very clean and concise.
They only require a single character, unlike strings (```:name``` vs ```"name"```).
They are also significently faster.

### Arrays

Like in Objective-C, an array is a way to put a large list of values together.
They are easier to create, however:

```
2.1.1 :001 > ary = [:bob, :joe, :larry]
 => [:bob,:joe,:larry]
```

You can access a member of the array with a 0-based index.

```
2.1.1 :002 > ary[0]
 => :bob
2.1.1 :003 > ary[2]
 => :larry
```

### Task:

Make a hash containing information about yourself. It should contain your first name, last name, age, and favorite color.

When you are done, see [Chapter 3](../chapter_3/main.md)

