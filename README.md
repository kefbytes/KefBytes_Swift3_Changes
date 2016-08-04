# Changes for Swift 3

*Number 1 goal is source compatibility*

---
### Protocol syntax 
The protocol syntax 
`<someProtocol, anotherProtocol>` 
will be replaced with 
`someProtocol & anotherProtocol`
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0095-any-as-existential.md>

---
### GCD has been given a makeover*Swift 3 eliminates a lot of boilerplate code from GCD
* This link gives a good overview of the GCD changes ######<https://medium.com/swift-and-ios-writing/a-quick-look-at-gcd-and-swift-3-732bef6e1838#.d9j7l0wgv>
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0088-libdispatch-for-swift3.md>

---
### The NS prefix has been removed on old foundation classes like Calendar and Date
* NSNotificationCenter now NotificationCenter
* NSFileManager now FileManager

	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0086-drop-foundation-ns.md>

---
### Core Graphics has been updated
* unwrap the current graphics context first and perform all drawing operations related to it afterwards
	
---
### Cocoa API names have changed
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0005-objective-c-name-translation.md>
	
---
### Function parameters
* Parameters all now have names unless specified otherwise with an underscore
* previously the first parameter name was included in the function name, now it is moved to the parameter list
	 * This makes method names themselves shorter and more consistent
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0046-first-label.md>

* Function types as parameters now have parentheses around their parameters
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0066-standardize-function-type-syntax.md>

* Labeling parameters in a function as var is going away
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0003-remove-var-parameters.md>

---
### Function/Method Naming
* Names have been changed to become more succient
* API functions have had meaningless words removed for more streamlined function names
* Methods that return or modify a value have been renamed with suffixes like"-ed" or"-ing"
* Each time Swift 3 modifies the method by adding a "d" to the end: this is a value that's being returned

---
### Enumeration
* cases now use lowerCamelCase
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0006-apply-api-guidelines-to-the-standard-library.md>
	
---
### Self
* You can now call Self to get the containing type
* Expanded Self to class members and value types
	
---
### Swift Package Manager
* will download dependencies, compile them, and link them together to create libraries and executables	
	
######<https://github.com/apple/swift-package-manager>
	
---
### Compiler
* Moved object from heap to stack (heap to Stack promotion for classes)
* Caches multiple files at once (Compiler caching as much as it can)
* Code optimization reduces size of compiled Swift code
* Whole Module Optimization on by default

---
### Xcode	
* Smarter with right click*jump to definition (right click to definition is much smarter and takes you to more meaningful code)
* Improves precision of error and warning messages
* Warning about unused return values of functions

---
### Operators
* ++ and -* operators are eliminated
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0004-remove-pre-post-inc-decrement.md>
	
---
### Control Flow
* For loop is replaced with either for-in or Strideable 
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0007-remove-c-style-for-loops.md>

* Switch cases with multiple patterns have new functionality
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0043-declare-variables-in-case-labels-with-multiple-patterns.md>
	
	
---
### Properties
* now use lowerCamelCase instead of UpperCamelCase
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0006-apply-api-guidelines-to-the-standard-library.md>
	
---
### CGContext
* functions that start with "CGContext" now get mapped to properties methods on a CGContext object

---
### Sort functions	
* sort() is renamed to sorted(), and sortInPlace() is renamed to sort().
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0006-apply-api-guidelines-to-the-standard-library.md>
	
---
### Attributes
* Attribute arguments use a colon (replace = with :)
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0040-attributecolons.md>
	
---
### Debugging
* identifiers have changed
Swift 2.2Swift 3.0
* `__FILE__`	`#file`
* `__LINE__`	`#line`
* `__COLUMN__`	`#column`
* `__FUNCTION__``#function`
* `__DSO_HANDLE__``#dsohandle`	
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0028-modernizing-debug-identifiers.md>
	
---
### Strings
* replace string selectors with the #selector() keyword
* for example when adding a target to a button
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0022-objc-selectors.md>

* Key-path strings have been replaced with the #keyPath() expression for KVC and KVO
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0062-objc-keypaths.md>

* String hashing algorithm improved
	
---
### Generics
* move where clause to end of type def
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0081-move-where-expression.md>
	
---
### Features removed	
* Currying func declaration syntax
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0002-remove-currying.md>

* implicit tuple splat in calls
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0029-remove-implicit-tuple-splat.md>
	
---
### Core language Enhancements
* Scoped access level, new fileprivate access level
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0025-scoped-access-level.md>

* case lables with multiple variable bindings
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0043-declare-variables-in-case-labels-with-multiple-patterns.md>

* generic Type Aliases
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0048-generic-typealias.md>

* Referencing Objective-C key-paths
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0062-objc-keypaths.md>

* Referencing the selector for property getters and setters
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0064-property-selectors.md>

* Typealiases in protocols and protocol extensions
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0092-typealiases-in-protocols.md>

---
### Core Language Syntactic cleanups
* inout moved to be part of the type
* Requiring leading dot prefixes for enum instance members
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0036-enum-dot.md>

* Move @noescape and @autoclosure to be type attributes
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0049-noescape-autoclosure-type-attrs.md>

* Enforcing order of defaulted parameters
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0060-defaulted-parameter-order.md>

* Converting dynamicType from a property to an operator
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0096-dynamictype.md>
	
---
### Type System
* UnsafePointer use optionals
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0055-optional-unsafe-pointers.md>

* Remove ImplicitlyUnwrappedOptionals*if the value can be used as an optional it is. 
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0054-abolish-iuo.md>
	
---
### Collection Indexing Model changed
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0065-collections-move-indices.md>

---
### Standard Library Enhancements

* Add a Lazy flatMap for sequences of optionals
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0008-lazy-flatmap-for-optionals.md>

* Conversions Unsafe[Mutable]Pointer to Int and UInt
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0016-initializers-for-converting-unsafe-pointers-to-ints.md>

* Change Unmanaged to use UnsafePointer
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0017-convert-unmanaged-to-use-unsafepointer.md>

* Add first(where:) method to sequences
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0032-sequencetype-find.md>

* Add generic result and error handing to autoreleasepool()
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0061-autoreleasepool-signature.md>

* Failable numeric conversion intializers
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0080-failable-numeric-initializers.md>

* Add a public base property to slices
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0093-slice-base.md>

* Add sequence(first:next:) and sequence9state:next:) to the stdlib
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0094-sequence-function.md>
	
---
### Line control statements use the #sourceLocation(file:line) syntax
	
######<https://github.com/apple/swift-evolution/blob/master/proposals/0034-disambiguating-line.md>
	



