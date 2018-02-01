# Swift

## ★ History
Swift is an open-source compiled language created by Apple in 2014. It is referred to as a "protocol-oriented programming" language, supports multiple-paradigms, and is built with the open-source LLVM compiler.

## ★ External resources
https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AboutTheLanguageReference.html



## ★ Types

### Value-types
* Structures: Strings, Characters, Booleans, Integers, Floating-point numbers, Arrays, Dictionaries
* Enumerations: Optionals

### Reference-types
* Functions
* Classes
* Closures


#### Basic Operators
* Arithmetic ( `+` `-` `/` `*` `%` )
* Comparisons ( `==` `!=` `>` `<` `>=` `<=` )
* Ternary ( `x < y ? ifTrue : ifFalse` )
* Logical operators ( `!` `&&` `||` )
* Closed (inclusive) Range ( `1...5` )
* Half-Open (non-inclusive) Range ( `1..<5` )

#### String interpolation
```swift
var firstName = "Helior"
var fullName = "\(firstName) Colorado"
var profile = "(fullName) —— \n He is a person."
// Helior Colorado
// He was a person.

```

### Collections

* Arrays are zero-indexed and ordered
* Dictionaries are unordered
* Accessing Dictionary values in subscript-notation yields an optional
* Sets are unordered, and each element contains a unique value
* Tuples store mixed values, zero-indexed

##### Creating Empty arrays:
```swift
var emptyArray:Array<String> = [] //explicitly-typed
var emptyArray4:[Int] = []        //short-hand of above

var emptyArray2 = Array<String>() //type initializer
var emptyArray3 = [Double]()      //short-hand of above
```

##### Initiating an array:
```swift
// Single-dimensional
var arrayWithInitialValues = ["one", "two", "three"]  //type is implicit

// multi-dimensional
var treeOfSkills: [[String]] = [
    ["Attack", "Barrage", "Heavy Hitter"],
    ["Guard", "Evasion", "Run Like Hell"]
]
```

##### Empty dictionaries:
```swift
var emptyDictionary1:Dictionary<Int, Int> = [:]   //explicitly-typed
var emptyDictionary2:[String:String] = [:]        //short-hand of above

var emptyDictionary3 = Dictionary<Int, String>()  //type initializer
var emptyDictionary4 = [String:String]()          //short-hand of above
```

##### Initiating a dictionary:
```swift
// Single-dimensional
var dictionaryWithInitialValues = ["name": "Helior", "dob": "1984-11-02"]

// Multi-dimensional
var multiDimentionalDictionary = [
    "set1": ["one", "two", "three"],
    "set2": ["four", "five", "six"]
]

```

##### Empty sets:
```swift
var emptySet2: Set<Int> = []    // explicitly-typed
var emptySet = Set<Int>()       // type initializer

```

##### Initilizing tuples:
```swift
var myTuple:(String, Int, Bool) = ("stuff", 44, true)
```



## ★ Control-flow statements

#### Optional binding
`if let`, `if let...else`, `guard let...else` are the recommended way of unwrapping options, as opposed to force or implicit unwrapping. Remember that `if let` assigned variables only exists within this inner scope, while `guard let` assignments are available to the scope they're defined.

### if let...
From my observations, the `if let` pattern is for executing a block of code only when the expression of `if let x = y` yields a non-nil value, in conjunction with assigning the value to `x`.

### guard let.. else
Particularly useful for multiple validation checks while keeping code read-able ★

### do...catch
Arbitrary block of code, in which you can catch a thrown error within a specific scope [?]

### defer
Defer will execute in FILO (first, in last out) order at the end of the block they are defined in, regardless how the code block exits (return, break, error, etc.)



## ★ Class properties

### Computed properties

### didSet



## ★ Protocols
### Defining a protocol
```swift
public protocol MyProtocolDelegate: parentProtocolClass {
  func requiredDelegateMethod() // optional parameter list
  optional func optionalDelegateMethod()
}
```

### Invoking a delegate's method
Remember that a class' delegates are not always guarenteed to exist, so treat them as *optionals*. Likewise, with optional delegate methods.
```swift
// Invoke required delegate method
self.delegate?.requiredDelegateMethod()

// Invoke optional delegate method
self.delegate?.optionalDelegateMethod?()
```

### Working with Objective-C
Requires using the `@objc` syntax, for the protocol, and also the method if it's optional.

```swift
@objc public protocol MyProtocolDelegate: parentProtocolClass {
  func requiredDelegateMethod() // optional parameter list
  @objc optional func optionalDelegateMethod()
}
```

### Conforming to a delegate
A class definition must indicate which protocols it conforms to:
```swift
public class myClass: MyProtocolDelegate {
  func requiredDelegateMethod() {/*...*/}
}
```



## ★ Operational stuff
#### Files to ignore in SCM
Refer to [Github's Swift.gitignore](https://github.com/github/gitignore/blob/master/Swift.gitignore) for an exhaustive list.
* `xcuserdata/`

#### Dependency Management

Libraries
* https://cocoapods.org/
* https://github.com/Carthage/Carthage
* https://swift.org/package-manager/

Discussion links:
* https://guides.cocoapods.org/using/using-cocoapods.html#should-i-check-the-pods-directory-into-source-control


## ★ Initializing a project
* Create an Xcode single-page app project
* Define your dependency manager
