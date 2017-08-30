## Objective-C

#### History
Objective-C is regular C (literally) with additional symbols sprinkled on top to enhance the language. Apple Inc. backs the development of this language, but is phasing out in favor of the Swift language.

#### Object-oriented bits
###### Definitions
Each class defined requires 2 files, a **header** file (`.h`) and an **implementation** file (`.h`).
A few tips:
* don't expose instance variables, create accessors instead.

MyClass.h
```
#import <Foundation/Foundation.h>

@interface MyClass : NSObject
  -(void)myCoolPublicMethod:(NSString *)value1Name;
  // [insert more public methods here]
@end
```

MyClass.m
```
#import "MyClass.h"

@interface MyClass()
  [insert private instance properties here]
@end

@implementation MyClass
  -(void)myCoolPublicMethod:(NSString *)value1Name {...}
  [insert implementation of other methods here]
@end
```

###### Private methods
Define the method signature in the `@interface` block of the implementation file (`.m`), then provide the implementation code in the `@implementation` block of the same file. Prefix with a dash (`-`), in parenthesis the return type, the name of the method, followed by a list of parameters and with their public name, type, and local-scope name.
```
@interface MyClass()
  -(void)myRadPrivateMethod:(NSString *)value1Name
@end

@implementation
  -(void)myRadPrivateMethod:(NSString *)value1Name {...}
@end
```

###### Private properties
TODO

###### Public methods
Define method signature in `@interface` block of the header file (`.h`), then provide the implementation code in the `@implementation` block of the implementation (`.m`) file. Prefix with a dash (`-`), in parenthesis the return type, the name of the method, followed by a list of parameters and with their public name, type, and local-scope name.
```
@interface MyClass
  -(void)myCoolPublicMethod:(NSString *)value1Name
@end
```

```
@implementation
  -(void)myCoolPublicMethod:(NSString *)value1Name {...}
@end
```

###### Public properties
TODO
