# Methods & Functions

Methods and functions in Swift work similarly to many other languages, if you understand functions in another language, chances are it won't take you long to feel right at home in Swift.



## Method vs Function

For simplicity here regard the words "method" and "function" as interchangable, as the keyword to define them is `func` I'll use the term "function" from here on.

Functions are simple a block of code that you have wrapped up and given a name to. They can be as long or as short as you like, this largely depends on how comple the task that the function performs is. Although it's generally a good idea to try and keep your functions as short and concise as possible, this keep things clear and managable.



### Declaring a Function

A simple function might look something like this:

```Swift
func saySomething() {
  print("Hello")
}
```
As you can see, they start with the keyword `func`, are then given a name (camel cased), a set of bracket, then a set of curly brackets which contain the body of the function. In the above example this simple prints the word "Hello".



## Calling A Function

Once you have a function defined, you have to *call* it in order to execute it. Calling a function is straight forward, you just write the name of the function followed by a set of brackets. Calling the function we declared above would look like this:

```Swift
saySomething()
```

This `saySomething` function can now be called time and time again to repete a task, performing the same action every time, in this case printing the words "Hello", but what if we wanted it to change slightly each time? This is where "arguments" come in...



## Functions With Arguments

Arguments (sometimes called parameters) can be "passed" to a function to subtly (or in some cases dramatically) change how that function executes. Carrying on from our above example, the empty set of brackets after the function name signals that it currently accepts no arguments, lets change that.

Rather than printing the word "Hello" every time, let's give ourselves the ability to change the word that is printed. To do this we need to change the decleration of the function to accept a `String`:

```Swift
func saySomething(words: String) {
  print(words)
}
```

Arguments come two parts, first a name, then the `Type`. The value of that argument then exists as a constant that we can use within the body of the fucntion. So here we print out `words`, which will be whatever value is "passed" to the function when we call it, which now looks like this:

```Swift
saySomething(words: "Hello")

saySomething(words: "Something else")
```

Above, we're making two calles to the *same* function, but passing in different arguments. We can no longer call the function as before, Xcode will tell us that we are missing an argument and offer us a Fix-it.

**Note:** As always Swift if obsessed with **Type**. This is a good thing, in the above example it means we can't pass an `Int` where the function is expecting a `String`. If we tried to do so we would get an error.
