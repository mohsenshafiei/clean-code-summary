### Clean Code Summary

#### Naming

- use intention revealing names: `raduis` instead of `r`

- don't use abbreviations

- `name` is better than `nameString` (unnecessary informations)

- clear distinctions: avoid `getAcount`, `getAccounts`, `getAccountInfo` in the same class or e.g avoid `get`, `fetch`, `retrieve`

- use pronouncable and meaningful names

- searchable names ( can be found easily by search tools as per their meaning)

- avoid encodings (coded names)

- minimize the usage of prefixes like `addr_name`

- classes and objects should have noun or noun phrase names like `Customer`, `Account`

- methods should have verb or verb phrase name like `postPayment`, `deletePage`

- don't use cute or humorous or witty names

- accessors, mutators, and predicates should be named for their value and prefixed with `get`, `set`, and `is`.

- use names related to the solution applied like the pattern used e.g. factory , builder.

- if not possible relate it to the problem being solved, like relate variables to address e.g. `addressName`, `addressNumber` etc.

- add meaningful context, like creating a class which will hold the variables that are being used in the same context, this will make the variables belong to that class and thus have contextual meaning.


#### Function & Methods

- functions should be small: one line, two,three or four maximum

- This means that `if` statements, `for` loops and `while` loops, should be one line long, obviously this line should be calling another function.

- for `switch` statements, every case should have one line, usually a call to another function.

- indentation level in functions should not be bigger than one or two levels.

- functions should do only one thing

- functions shouldn't have side effects

- function names should be descriptive, don't be afraid to make them very long as long as they are descriptive.

- be consistent in naming the functions, meaning, don't make `includeName()`, `addAdress()`, instead: `includeName()`, `includeAdress()`, Or, `addName()`, `addAdress()`.

- code should be like telling a story, can be read as a top down narrative, every function leading to the next one smoothly .

- every function should have one level of abstraction, the other level should be in another function that follows the first one

- we should never use output arguments in functions, i.e. functions that takes a variable as its argument, then change its state, it is very confusing.

- it is better that functions shouldn't have arguments at all!, or at least one argument, three arguments maximum.

- don't return a boolean as a validation for the successful operation of a function.

- A try and catch block should exist alone in one function i.e. error handling is one thing to do, as we have said previously, functions should do only one thing.


#### Comments

- comments are a necessary evil, we should be writing functions in a descriptive way, so that we can avoid writing comments at all, so the ideal case is that there should be no comments at all!.

- comments should be used only as an explanation , never add obsolete code as a comment, instead remove it and depend on version control systems to preserve the history of the code.

- `TODO` comments are ok because the IDE can find them easily before ending the project.

- don't write redundant comments, if the code is self explanatory no need to add comments.

- instead of using comments as function headers, replace them with a descriptive name for the function if possible.

- instead of writing a comment to explain a long line of code, divide this line into more simpler lines by using local variables so as to make the code more descriptive and readable.

- attribute comments like: `/* added by john smith on 1/10..*/` are ok but not to be a MISLEADING info or to be excessive.

- don’t put interesting historical discussions or irrelevant descriptions of details into your comments

- don't put comments that have poor or no connection to the code it explains.


#### Formating

- *Vertical Formatting*: The file length in lines should be around the size of : 200-500 lines, this is not mandatory off course , but to be followed whenever possible.

- *Vertical Opennes*: Methods should be separated by blank lines, also lines of code that differ in functionality should be separated by blank lines.

- on the other hand: Vertical density (no blank lines) implies close link or association.

- *Vertical distance*: Concepts that are closely related should be kept vertically close to each other , e.g. methods of similar functions or of related function should be grouped and ordered together We want to avoid forcing our readers to hop around through our source files and classes.

- variable declarations inside methods should be as close as possible to their usages.

- instance variable declarations should be in one location and most preferably on the top of the class, or at least in the bottom.

- *Dependent Functions*: If one function calls another, they should be vertically close, and the caller should be above the callee, if at all possible.

- *Conceptual Affinity*: Certain bits of code want to be near other bits, The stronger that affinity, the less vertical distance there should be between them. Affinity might be caused because a group of functions perform a similar operation

- *Horizontal Formatting*: lines should be of the sizes 100-120-max 200 characters.

- indentation should be used to show different levels of hierarchy in the file.

- don't break the indentation rule even in the case of short If statements or short methods.


#### Objects and Data Structures

- in that context, the `data structure class`, exposes its data (variables) and have no meaningful (significant) methods or functions.

- while a `normal class` (Called Object here by the author after Object oriented), like `MainActivity`, `ListAdapter`, `Calculator`, `Iterator`, hides their data, and exposes their methods that work on those data.


#### Error Handling

- there must be a good amount of separation between your business logic code and your error handling code.

- too much error handling is not good, don't use `If` statements instead of `try and catch` blocks.

- try to provide context with exceptions, i.e. Create informative error messages and pass them along with your exceptions. Mention the operation that failed and the type of failure.

- if you are using logging in your application, pass along enough information to be able to log the error in your catch.

- if we have a method that in some cases will return a value/object that might cause an error, usually we will surround the output from this method with try and catch, but, as a better practice, we should refactor this method to always return an error-free value/object.

- don't return `null`, don't pass `null` to methods
