# Encapsulation & Access Modifiers

### Object encapsulation (Information Hiding)
- It is a language mechanism for restricting direct access to some of an object's components or members
- This retriction could be useful:
  Where privacy in the object’s components is a concern
  Where object’s members need to be protected from deliberate or inadvertent manipulation

### Enforcing Encapsulaction
- Encapsulation is a OO principle that is implemented at language level
- OO languages should have mechanisms for supporting or enforcing encapsulation
- Most pure OO languages use Access Modifiers to enforce/implement encapsulation

### Access Modifiers
- Access modifiers set the access levels to class components – that is, fields (variables), methods, (and constructors)
- Java defines 4 access levels:
    Private
    Friendly
    Protected
    Public

### Private
The Java keyword private is used to grant private access
Methods, variables, (and constructors) that are declared private can only be accessed within the declared class itself
That is, other classes will not be able to access these private members
Private access modifier is the most restrictive access level
Top level classes and interfaces cannot be declared private

### Friendly
This is the default level of access in Java
It is also known as package access
There is no keyword for this level of access
It is declared implicitly by the absence of the other access modifiers – except when dealing with interfaces
Package or friendly access means that any component with this level of access is visible to classes within the same package

### Protected
The Java keyword protected is used to grant protected access
Protected access cannot be applied to top level classes and interfaces
Methods and fields can be declared protected, however methods and fields in a interface cannot be declared protected
Protected access means that the components declared protected are visible to the package and all subclasses

### Public
The Java keyword public is used to grant public access
A class, data field, method, constructor, interface, etc, can be declared public
The component(s) declared public can be accessed from any other class
That is, fields, methods, etc declared inside a public class can be accessed from any class belonging to the Java Universe
However, if the public class we are trying to access is in a different package, then we will need to import the class first

### Data Field Encapsulation
Encapsulation of class members using access modifiers works quite well
However, it seems to work better for methods than it does for data fields
Two challenges encapsulating data fields with only access modifiers are:
A lack of control
A lack of flexibility
Therefore, only using access modifiers to encapsulate data fields is not sufficient

### Good OOP Practice
It is therefore good practice to NOT access data members directly, from outside the class
Data members should instead be accessed using getter and setter methods
However, data members should be accessed directly from within the class itself

### How getter/setter methods
If a class Student for example, has a data member called age, then age would be encapsulated as follows:
The data member age would be made private
private int age;

We would then create a getter method in the Student class like this:

public int getAge() {
return age;
}

We would then create a setter method in the Student class like this:

public void setAge(int age) {
this.age = age;
}






