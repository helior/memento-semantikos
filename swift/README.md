## Swift

#### History
Swift is an open-source language created by Apple. It borrows


### Types

##### Value-types
* Structures: Strings, Characters, Booleans, Integers, Floating-point numbers, Arrays, Dictionaries
* Enumerations: Optionals

##### Reference-types
* Functions
* Classes
* Closures



### Basic Operators
* Arithmetic ( `+` `-` `/` `*` `%` )
* Comparisons ( `==` `!=` `>` `<` `>=` `<=` )
* Ternary ( `x < y ? ifTrue : ifFalse` )
* Logical operators ( `!` `&&` `||` )
* Closed (inclusive) Range ( `1...5` )
* Half-Open (non-inclusive) Range ( `1..<5` )

### String interpolation
```
var firstName = "Helior"
var fullName = "\(firstName) Colorado"
var profile = "(fullName) —— \n He was a person."
// Helior Colorado
// He was a person.

```

### Collections

##### Arrays:
```
// Choose your syntax..
var emptyArray:Array<String> = []
var emptyArray2 = Array<String>()
var emptyArray3 = [Double]()
var emptyArray4:[Int] = []
```
