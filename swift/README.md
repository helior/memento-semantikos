## Swift

#### History
Swift is an open-source compiled language created by Apple in 2014. It is referred to as a "protocol-oriented programming" language, supports multiple-paradigms, and is built with the open-source LLVM compiler.


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

* Arrays are zero-indexed and ordered
* Dictionaries are not in order
* Accessing Dictionary values in subscript-notation yields an optional

##### Creating Empty arrays:
```
var emptyArray:Array<String> = [] //explicitly-typed
var emptyArray4:[Int] = []        //short-hand of above

var emptyArray2 = Array<String>() //type initializer
var emptyArray3 = [Double]()      //short-hand of above
```

##### Initiating an array:
```
// Single-dimensional
var arrayWithInitialValues = ["one", "two", "three"]  //type is implicit

// multi-dimensional
var treeOfSkills: [[String]] = [
    ["Attack", "Barrage", "Heavy Hitter"],
    ["Guard", "Evasion", "Run Like Hell"]
]
```

##### Empty dictionaries:
```
var emptyDictionary1:Dictionary<Int, Int> = [:]   //explicitly-typed
var emptyDictionary2:[String:String] = [:]        //short-hand of above

var emptyDictionary3 = Dictionary<Int, String>()  //type initializer
var emptyDictionary4 = [String:String]()          //short-hand of above
```

##### Initiating a dictionary:
```
// Single-dimensional
var dictionaryWithInitialValues = ["name": "Helior", "dob": "1984-11-02"]

// Multi-dimensional
var multiDimentionalDictionary = [
    "set1": ["one", "two", "three"],
    "set2": ["four", "five", "six"]
]

```
