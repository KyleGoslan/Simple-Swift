# Type Casting

Swift is a ***Type Safe*** language. That means that it is obsessed with what type of data is associated with what

When we declare a variable or constant, there are a few ways we can do it:

```swift
let someNumber = 5 

let anotherNumber: Int = 8
```

These lines essentially do the same thing (with the exception of the constant name and the actual number clearly). The extra syntax in the second example is simply declaring the type of data that ‘anotherNumber’ is going to be an Int value. One of the most useful bits of advice I got when I started learning swift is to read the colon as “is of type”. To that line would read as “The constant anotherNumber is of type Int and equals 8”.

That being said the preferred way is to leave the type declaration off and let swift infer the type itself. In this example its blatantly clear the ‘anotherNumber’ is an integer, so there is no need for the explicit type declaration.

Type safety is awesome! Why? Well it simply means that once a value is set we know what type of data it will contain. That means that A String will always be a String, never an Int or any other type of data.