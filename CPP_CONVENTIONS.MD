# Conventions
## Spacing
There should be no line wasted, curly braces should share the line of the statement or declaration, like so:
```cpp
if(whatever) {
    // Code
} else {
    // Other code
}
```
Statements that have 1 line of code should still use curly braces for readability, like so:
```cpp
if(whatever) {
    // Code
}
```
## Comments
Single line comments should have spacing after the slashes, like so:
```cpp
// This is a comment
/* This is another comment */
```
Multiline comments should only be used for documentation, and should follow single lines spacing rules, like so:
```cpp
/*
* This is a documentation comment
*/
```
Commented code is not allowed:
```cpp
/*printf("Hello");
printf("World");*/
```
## Variables
Class variables and local variables should follow camel case, like so:
```cpp
int helloWorld = 23;
```
Global variables are **NOT ALLOWED!**, Instead of globals, use singletons and static variables, like so:
```cpp
class System {
    static int Whatever = 23;
}
```
Static variables should follow the pascal naming convention.
## Classes
Classes should start with 'li', and be in pascal case afterwards, like so:
```cpp
class liQuad {
public:
    Quad();
    ~Quad();
private:
    int ID;
};
```
The public section should be above the private and protected section.
## Typedefs
Typedefs should be in camel case, with '_t' at the end, like so:
```cpp
typedef unsigned char myTypedef_t;
```
## Structs
Structs follow similar rules to typedefs, and be lightweight, with no functions, like so:
```cpp
struct testStruct_t {
    int x;
    int y;
};
```
## Enums
Enums follow the same rules as typedefs and enums. Type specification and value specification with enums is optional. Enum values should be in screaming snake case, and should be unique to the program to avoid errors, like so:
```cpp
enum testEnum_t : int {
    VALUE = 0,
    VALUE2
};
``` 
## Functions/Methods
Public and private functions should be in pascal case, with a '_' being in the front of the private functions name, like so:
```cpp
void PublicFunction() {
    // Code
}

void _PrivateFunction() {
    // Other code
}
```
## Defintions
Definitions should be in screaming snake case, like so:
```cpp
#define TEST_DEF 0x17
```
## Consts
Consts variables aren't discouraged, but they aren't encouraged either, they should only be used if the value can not and should not be modified. Const functions are encouraged, to keep code clean, if you write a function that does modify a variable, you should create a seperate function for it or mark the variable as 'mutable'.
## Namespaces
Namespaces should be in pascal case, like so:
```cpp
namespace TestNamespace {
    // Declarations
}
```
## Misc
- Autos are **FORBIDDEN**.
