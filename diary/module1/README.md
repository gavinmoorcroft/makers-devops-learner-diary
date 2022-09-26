<< [Back to Root](../../README.md)

<< [Back to Diary](../README.md)

# Module 1

Module 1 is split into three sections
 - [Phase 1 - The Command Line](#phase-1---the-command-line)
 - [Phase 2 - Git Version Control](#phase-2---git-version-control)
 - [Phase 3 - Programming](#phase-3---programming)

### Challenges

All  challenges I do for this module can be [found here](challenges.md)

## Phase 1 - The Command Line

During this phase of Module 1 we took a look at the basics of the CLI. Noting of this was taxing and is pretty basic stuff. Not anything that needs to be recorded as I use this on a daily basis on my day job.

## Phase 2 - Git Version Control

TODO

## Phase 3 - Ruby Foundations


## Array

[Doc page for Array](https://ruby-doc.org/core-3.0.0/Array.html)

## hash 
[Doc page for Hash](https://ruby-doc.org/core-3.1.2/Hash.html)

I found a hash a little more awkard to work with as the syntax to add a new item to a hash just doesn't want to flow from my fingers for some reason.

 to create a hash 
 ```ruby
 hash_name = {'labelA' => 'valueA','labelB' => 'valueB'}
 ```

to read from a hash
```ruby
hash_name['label_name']
 ```

 to add to a hash
 ```ruby
hash_name['new+label_name'] = 'name_value'
 ```

### Useful methods
values

length

empty?

has_key?

has_value?

clear

shift

## Regular expressions with Ruby
regular expresions are surrounded by /[]/

you can cycle through a regular express and check each item in a string using ```=~```, such as 
 ```ruby
required_chars = /[!@$%&]/

if password =~ required_chars
    code here
else
   code here
end
 ```
this snippet will check through the password variable looking for any of the !, @, $, % and & symbols.






## Classes

Classes are the building blocks of what makes ruby a OOP. They allow us to define the blueprint for creating objects that we can then use in our programs

classes are defined using the keyword `class` and require closing using `end`. any methods that the class will contain are placed between these words

We make use of classes by instantiating them into objects through the use of the `.new` method on the class.

Defining a class

```ruby
class name
  def hello
    return "Hello!"
  end

  def good_bye
    return "Good bye!"
  end
end
```

### Instantiating a class
you instantiate a class by ceating a new object of that class through the use of the `.new` method on that class

```ruby
greeter = Greeter.new
```
You can then use that instance of the class as follows:

```ruby
greeter.hello
```

### *Initialize*

we can use `initialize` to initialize the class so something happens immeditalty upon that classes instantiation. This is done as follows

```ruby
 class Maths
  def initialize
    puts 1+2+3
  end
end
```

in the above case when the Maths class is instantiated it will puts `6` to the terminal immediately.


### Instance Variables

We can have variables at the class level, called instance variables, and the arguments for these can be set at time of instantiation by passing them to the `.new` nethod. 

We create these Instance Variables through the use of the `@` symbol when declaring these variables, and we do in in the initialize method and pass the variables at the time of instantiation.

``` ruby
class ClassName
 def initialize (arg1, arg2, arg3)
   @arg1 = arg2
   @arg2 = arg2
   @arg3 = arg3
 end
end
```
we can then create the objecs of the class by passing the arguments to the classes `.new` method.


```ruby
object_name = Classname.new(arg 1, arg2, arg3)
```
### Attribute Reader

An `attribute` is a `instance variable` and ruby has `attribute readers` to return these attributes. This is a method that allows you to access the attribute in the class instance. 

This is similar in function to a `Getter` in Java

You define the attribute reader through a method in your class:

``` ruby
def method_name
    return @attribute
  end

```
 ## Scope
 Scope details how and where variables can be used within a program. basically, variables and thier visibility.
 
 There are four levels of scope:

* Class variable (@@a_variable): Available from the class definition and any sub-classes. Not available from anywhere outside.
* Instance variable (@a_variable): Available only within a specific object, across all methods in a class instance. Not available directly from class definitions.
* Global variable ($a_variable): Available everywhere within your Ruby script.
* Local variable (a_variable): It depends on the scope. You’ll be working with these most and thus encounter the most problems, because their scope depends on various thing

