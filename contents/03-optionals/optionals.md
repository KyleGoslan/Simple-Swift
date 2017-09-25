# Optionals

Swift is obsessed with everything being in a valid state. That is to say a for example String has to contain a valid string. It can’t be a number, or anything else (see Swift Type Casting) or even nil.

That is unless we mark the value as an optional. I’ll start by stating there is much more to be said about optionals than will be covered here, this is just the core concept.

Generally is you see an exclamation point (!) or question mark (?), it’s a safe assumption that you’re dealing with an optional value. **Only in the case of a variable/constant being marked as an optional can it contain a nil value.**

Optionals also have to have their type declared. Lets take a look at one:

```Swift
  var name: String?
```

This creates a new name variable which *can* contain a String (and only a String) but but *can* be nil, and in fact is currently nil. We can then set this value at a later point in time just like any other value:

```Swift
  name = "Kyle"
```

If we were to print this to our console at this point we would see “Optional(Kyle)”. That’s because we haven’t unwrapped the optional value.

Another way we could do a similar thing is:

```Swift
  var name: String!
```

## The difference between ? and !

? – Indicates that this value may or may not contain a value, it could be nil.

! – Indicates that by the time we come to use it, it **will** contain a valid value.
