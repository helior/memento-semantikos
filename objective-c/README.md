## Objective-C

### History
Objective-C is regular C (literally) with additional symbols sprinkled on top to enhance the language. Apple Inc. backs the development of this language, but is phasing out in favor of the Swift language.

### Object-oriented bits
#### Defining classes
Each class defined requires 2 files, a **header** file (`.h`) and an **implementation** file (`.h`).
A few tips:
* don't expose instance variables, create accessors instead.

MyClass.h
```
#import <Foundation/Foundation.h>

@interface MyClass : NSObject
  -(void)myCoolPublicMethod:(NSString *)value1Name;
  // [define public methods here]
@end
```

MyClass.m
```
#import "MyClass.h"

@interface MyClass()
  // [define private instance properties here]
  // [define private methods here]
@end

@implementation MyClass
  -(void)myCoolPublicMethod:(NSString *)value1Name {
    // [code goes here]
  }
@end
```

#### Private methods
Define the method signature in the `@interface` block of the implementation file (`.m`), then provide the implementation code in the `@implementation` block of the same file. Prefix with a dash (`-`), in parenthesis the return type, the name of the method, followed by a list of parameters and with their public name, type, and local-scope name.
```
@interface MyClass()
  -(void)myRadPrivateMethod:(NSString *)value1Name;
@end

@implementation
  -(void)myRadPrivateMethod:(NSString *)value1Name {
    // [code goes here]
  }
@end
```

#### Private properties
`@TODO`

#### Public methods
Define method signature in `@interface` block of the header file (`.h`), then provide the implementation code in the `@implementation` block of the implementation (`.m`) file. Prefix with a dash (`-`), in parenthesis the return type, the name of the method, followed by a list of parameters and with their public name, type, and local-scope name.
```
@interface MyClass
  -(void)myCoolPublicMethod:(NSString *)value1Name;
@end
```

```
@implementation
  -(void)myCoolPublicMethod:(NSString *)value1Name {
    // [code goes here]
  }
@end
```

#### Public properties
`@TODO`
