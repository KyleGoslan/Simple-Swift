# Classes

Classes really are the bread and butter of object oriented programming (OOP). They are the building blocks of any applications which allow you to create *"objects"* to work with.

Essentially, a class couples together variables/contants and functions into one manageable package for you to work with.

Classes are abstract blueprints for the objects that your application needs to work with.

#### As a starting point:

+ Each class should be its own Swift file.
+ Classe should start with an **upper case** letter and are camel cased.
+ Classes start with the keyword `class`, the class name and then a set of curly brackets.
+ Everything goes inside these brackets.

```Swift
class Person {

}
```

The above is a class decleration for a `Person` object. It doesn't do a lot at the moment, but already we can start creating `Person` objects in our application:

```Swift
let someone = Person()
```

Lets expand the class to make it a bit more useful. Generally you can think of objects as being made up of two main components.

+ Its properties
+ Its methods (functions)

## Properties

Lets start with adding some properties. Properties are simply constants and vairables within a class, think of them as the information associated with the object. For example sticking with our `Person` class, typically a person may have an age and an name:

```Swift
class Person {

  let name: String!
  var age: Int!

}
```

Here we're saying that a `Person` has a *name* which is a `String` and an *age* which is an `Int`. We've declared a name as a constant and age as a variable, in our example a persons age can change, but once a name is set, they are not allowed to change it. At the moment, we will actully have a compile error, that's because name hasn't be given a default value. We could fix this by setting it as `nil`, but lets look at adding an *initilizer* to solve this problem:

```Swift
init(name: String, age: Int) {
  self.name = name
  self.age = age
}
```

The `init` is a decleration looks a lot like a normal function, just without the keyword `func`. All classes get a default initilizer which we dont have to write, but would like like `init()`. The one we've writen above works exactly like a normal funtion, we are saying that we want to pass a name which is of type `String` and an age which is of type `Int`. We then assign those value we passed into the init to the respective propertive of the `Person` object.

### Self?

You may be wondering what this `self` word is all about. Well, the constants that we pass into our init are called "name" and "age" which are the same names we gave our poperties. Within the init function "name" and "age" would reference the values passed into it opposed to the properties. Prefixing them with `self` make it clear were referencing the class properties.
