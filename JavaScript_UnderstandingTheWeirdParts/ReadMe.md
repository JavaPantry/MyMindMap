#JavaScript: Understanding the Weird Parts
## Section 1 Getting Started
1. Introduction and The Goal of This Course
2. Setup
3. Big Words and Javascript
4. Watching this Course in High Definition
5. Understanding, Frameworks, and The Weird Parts
## Section 2 Execution Contexts and Lexical Environments
6. Conceptual Aside: Syntax Parsers, Execution Contexts, and Lexical Environments
7. Conceptual Aside: Name/Value Pairs and Objects
8. Downloading Source Code for This Course
9. The Global Environment and The Global Object
B3-Global-Environment.zip
10. The Execution Context - Creation and Hoisting
B4-Hoisting.zip
11. Conceptual Aside: Javascript and 'undefined'
B5-Undefined.zip
12. The Execution Context - Code Execution
B6-Execution.zip
13. Conceptual Aside: Single Threaded, Synchronous Execution
14. Function Invocation and the Execution Stack
B6-Execution.zip
15. Functions, Context, and Variable Environments
B9-Variable-Environments.zip
16. The Scope Chain
B10-Scope-Chain.zip
17. Scope, ES6, and `let`
    - brief explain keyword `let` vs. `var` 
18. What About Asynchronous Callbacks?
B11-What-About-Asynchronous-Callbacks.zip
## Section 3 Types and Operators
19. Conceptual Aside: Types and Javascript
20. Primitive Types
21. Conceptual Aside: Operators
22. Operator Precedence and Associativity
Operator-Precedence-In-Javascript.pdf
23. Operator Precedence and Associativity Table
24. Conceptual Aside: Coercion
25. Comparison Operators
Equalty-Comparison-And-Sameness.pdf
26. Equality Comparisons Table
27. Existence and Booleans
C8-Booleans-Existence.zip
28. Default Values
C9-Default-Values.zip
29. Framework Aside: Default Values
## Section 4 Objects and Functions
30. Objects and the Dot
D1-Objects-And-The-Dot.zip
31. Objects and Object Literals
D2-Object-Literals.zip
32. Framework Aside: Faking Namespaces
D3-Faking-Namespaces.zip
33. JSON and Object Literals
D4-JSON.zip
34. Functions are Objects D5-Functions-Are-Objects.zip
    - Functions are 1-st class objects
    - assign properties to function
35. Function Statements and Function Expressions
D6-Function-Expressions.zip
36. Conceptual Aside: By Value vs By Reference
D6b-By-Value-By-Reference.zip
37. Objects, Functions, and 'this' D7-Object-Functions-And-This.zip
    - this in function depends how function is called (if invoked as object's method) 
    - use of `var self = this;` to reference current scope instead global
38. Conceptual Aside: Arrays - Collections of Anything
D7b-Arrays-Collections-Of-Anything.zip
39. 'arguments' and spread D8-Arguments.zip
    - ES6 `spread`
    - ES6 default parameter concept instead `lang = lang || 'en'`
    - ES6 `...otherArguments`
40. Framework Aside: Function Overloading D9-Function-Overloading.zip
41. Conceptual Aside: Syntax Parsers
42. Dangerous Aside: Automatic Semicolon Insertion D11-Automatic-Semicolon-Insertion.zip
    - replace '\n' with semicolon
43. Framework Aside: Whitespace D12-Whitespace.zip
44. Immediately Invoked Functions Expressions (IIFEs) D14-IIF-Es.zip
    - `()` after function expression declaration 
    - wrap function expression  in parenthesis and end with `()` `(function(){console.log('Hello IIFE')}())`
45. Framework Aside: IIFEs and Safe Code D15-IIF-Es-And-Safe-Code.zip
46. Understanding Closures D16-Closures.zip
    - function greet(whattosay) {return function(name) {console.log(whattosay + ' ' + name);}}
47. Understanding Closures - Part 2 D16b-Closures-Part-2.zip
    - demonstrate use of IIFE within closures
48. Framework Aside: Function Factories D17-Function-Factories.zip
    - factory of closures
    - one use of closures is a set of specialized functions with predefined default parameters
49. Closures and Callbacks D18-Closures-And-Callbacks.zip
    - explain that callbacks exploit closures idea 
50. call(), apply(), and bind() D19-Call-Apply-Bind.zip
    - func.bind(obj)  bind `this` within _func_ with _obj_
    - func.call(obj, arg1, arg2, ...) bind `this` within _func_ with _obj_ and call func with arguments
    - func.apply(obj, [arg1, arg2, ...]) bind `this` within _func_ with _obj_ and call func with **array** of arguments
    - an example of usage - **function borrowing** `console.log(person.getFullName.apply(person2));` _person2_ object **borrows** function `getFullName` from _person_ object   
    - an example of usage - **function currying** `var multipleByTwo = multiply.bind(this, 2);console.log(multipleByTwo(4));` preset first parameter to **2**
51. Functional Programming D20-Functional-Programming.zip
    - demo an idea of _Functional Programming_ in simple example of passing **func** as argument to function which apply this **func** to every array element
    - demo how to use **bind** to pass additional parameter to **func** 
52. Functional Programming - Part 2 D20b-Functional-Programming-Part-2.zip
    - huge open source well documented functional programming library [UnderscoreJs](http://underscorejs.org)
    - [lodash](https://lodash.com) add some extra features
## Section 5 Object-Oriented Javascript and Prototypal Inheritance
53. Conceptual Aside: Classical vs Prototypal Inheritance
    - Inheritance: one object gets access to the properties and methods of another object
54. Understanding the Prototype E2-Understanding-The-Prototype.zip
    - explain _ _ *__proto__* _ _  pointer (never use it directly)
55. Everything is an Object (or a primitive)
56. Reflection and Extend E4-Reflection-And-Extend.zip
    - Reflection object caln look at itself, listing and changing its properties and methods
    - to list all properties `for(prop in obj){if(obj.hasOwnProperty(prop)) print obj[prop]}`
    - _underscoreJs_ method to extend objects let we have three object in our code  `_.extend(parent, child1, child2)` will __NOT__ make __children__ inherit from `parent` but add __children's__ properties and methods to `parent`
    - ES6 willl have `extends` keyword
## Section 6 Building Objects
57. Function Constructors, 'new', and the History of Javascript F1-Function-Constructors-New-History.zip
58. Function Constructors and '.prototype' F2-Function-Constructors-And-Prototype.zip
    - Use of  **new** keyword and add methods to **prototype** (also is a *keyword* available only to add methods to prototype) 
59. Dangerous Aside: 'new' and functions
60. Conceptual Aside: Built-In Function Constructors F4-Built-In-Function-Constructors.zip
61. Dangerous Aside: Built-In Function Constructors
    - use [MomentJs](http://momentjs.com) for dates
62. Dangerous Aside: Arrays and for..in
    - do NOT use __for in__ with arrays. Eventually you'll get tot trouble if framework add property to _**Array**_'s prototype
63. Object.create and Pure Prototypal Inheritance F7-Object-Create-And-Prototypal.zip
    - new browsers support: create object from prototype  `var person = {}; var john = Object.create(person);` useless because you need to overwrite prototype's properties
    - _**Polyfill**_ - code that adds a feature which the engine may lack
    - check if function supported `if(!Object.create){... polyfill ....}`
64. ES6 and Classes
    - classes in ES^ are just _**syntactic sugar**_
## Section 7 Odds and Ends
65. Initialization H1-Initialization.zip
66. 'typeof' , 'instanceof', and Figuring Out What Something Is. H2-Typeofinstanceof.zip
67. Strict Mode H3-Strictmode.zip
68. Strict Mode Reference gogle `MDN strict mode`
## Section 8 Examining Famous Frameworks and Libraries
69. Learning From Other's Good Code
70. Deep Dive into Source Code: jQuery - Part 1 I2-Deep-Dive-J-Query.zip
71. Deep Dive into Source Code: jQuery - Part 2
72. Deep Dive into Source Code: jQuery - Part 3
## Section 9
Let's Build a Framework / Library!
73. Requirements
74. Structuring Safe Code J2-Structuring-Safe-Code.zip
75. Our Object and Its Prototype J3-Our-Object-And-Prototype.zip
76. Properties and Chainable Methods J4-Properties-And-Chainable-Methods.zip
77. Adding jQuery Support J5-Adding-J-Query-Support.zip
78. Good Commenting J6-Good-Commenting.zip
79. Let's Use Our Framework J7-Lets-Use-Our-Framework.zip
80. A Side Note
## Section 10 BONUS Lectures
81. TypeScript, ES6, and Transpiled Languages
    - github Traceur  (even has a demo)
82. Transpiled Languages References
    - For more on Typescript head to: http://www.typescriptlang.org 
    - and try out writing Typescript code in your browser here: http://www.typescriptlang.org/Playground
    - For more on Traceur head to: https://github.com/google/traceur-compiler
    - and try out writing ES6 code in Traceur in your browser here: https://google.github.io/traceur-compiler/demo/repl.html#
## Section 11 BONUS: Getting Ready for ECMAScript 6
83. Existing and Upcoming Features
    - To read a list of features existing or coming in ES6, head here:  [ES6 features project](https://github.com/lukehoban/es6features)
84. ES6 Features Reference
## Section 12 Conclusion
85. Learning to Love the Weird Parts