# Variables & Constants

## Variables

To create a variable in swift, you start with the keyword 'var', followed by your name (camel cased, because you're a good developer) and then a value:

```swift
var someWords = "Hello World"
```

Variables, as the name implies, ***can change*** over time. For example at a later point you could reassign the 'someWords' value:

```swift
someWords = "Something else"
```

## Constants

Constants are declared very similarly to variables, except instead of 'var', you use 'let':

```swift
let name = "Kyle"
```

Again, as the name suggests, constants ***cannot change***. Once they are set, they keep the value until they are deallocated.

### Notes

So why would you ever use a constant, they’re like variables, but with restrictions, right? Yes, but there are two main reasons. Most importantly, it makes your intent very clear. By making something a constant, you are explicitly stating that this value will not change, ever. By using a variable, you are stating that, yes, this may well change when I use it again at a later point in time. Secondly, the compiler can make some slight optimisations for constantly.

Xcode will actually inform you if you have declared a variable and never changes it, and suggest you change it to a constant, and if you try to change a constant it force you to change it’s declaration to a variable.

### Tip

Basically, just declare everything with ‘let’. When you try and change it Xcode will force you to change the declaration.