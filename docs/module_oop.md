# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?
The fail fast principle stands for stopping the current operation as soon as any unexpected error occurs. Adhering to this principle generally results in a more stable solution.
## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?
#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?
#### What is a linked list? How to find if a linked list has a loop?
#### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?
#### How does HashMap work?
HashMap in Java works on hashing principle. It is a data structure which allows us to store object and retrieve it in constant time O(1) provided we know the key.
#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)
If jey are immutable, the object's hashcode wont change and it allows caching the hashcode of different keys which makes the overall retrieval process very fast.
### Other

#### What is a garbage collector, in a nutshell?
Java applications obtain objects in memory as needed. It is the task of garbage collection (GC) in the Java virtual machine (JVM) to automatically determine what memory is no longer being used by a Java application and to recycle this memory for other uses.
## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?
Up-casting is casting to a supertype, while downcasting is casting to a subtype. Upcasting and downcasting gives us advantages, like Polymorphism or grouping of different objects. We can treat an object of a child class type to be as an object of its parent class type. This is called upcasting.
#### Which order should we catch the exceptions? Why?
Any order the compiler will accept is correct.

### Object-oriented

#### What is a class?
A class is a blueprint to create an object.
#### What is an object?
An object is an instance of a class, each object has its own set of properties.
#### What is a constructor?
Constructors are special methods in Java that have the same name as the class. Everytime we create an object a default constructor is created.
#### Do we require parameter for constructors?
We can create constructors with or without parameters. The default constructor doesn't have any parameters, so no is not required to use parameters for constructors.
#### What is an interface?
An interface is a just a class, the difference is that it has only method signatures, so no code written in the method body. The purpose of an interface is to be implemented by classes. When a class implements a interface, it needs to implement all methods in the interface.
#### What are access modifiers?
Access modifiers are a feature in Java that limit the visibility of a class to another class members. In Java there are 4 access modifiers: public, private, protected and default.
#### What is data hiding?
Data hiding is related to access modifiers. Using modifiers to hide data uses an OOP feature called Encapsulation.
#### Can a static method use non-static members?
Yes it can use non-static members, but it needs to create an object to access those members.
#### What is the difference between hiding a static method and overriding an instance method?
Hiding a static method or any method uses the OOPs principle of Encapsulation compared to overriding a instance method that uses OOPs principle of Polymorphism.
#### Define the following terms: Instantiation, Attribute, Method
Instantiation = the process of creating a new object
Attribute = is another word for field. An object can have multiple attributes of different types, suchs as int, float, boolean, String and so on.
Method = is a block of code that runs when is called. In a method is where logic and algorithms are executed.
#### Could we access a static variable (or method) from a non-static method? Why?
If we are in the same class, yes. Mainly because that variable/method belongs to the class. IF we are in a different class, only the class can access the static members.
#### Could we access a non-static variable (or method) from a static method? Why?
No because that variable belongs to an instance. We need to create an object to use those fields and methods.
#### How many instances you have of a static variable of a given class?
Only one.
#### Why is it not a good practice to write a lot of static methods?
Static methods don't fully support OOP design.
#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?
#### What is the ‘this’ reference?
Using 'this' keyword you refference the object of the current class.
#### What are base class, subclass and superclass?
When we use Inheritance a subclass extends superclass. This means the subclass has all properties of a superclass, such as methods, fields, inner classes or block of codes.
A base class is a class the will be extended, and is only used as a base for all classes to receive those properties.
#### Draw an object oriented family (as entities, with relations) on the whiteboard.

#### Difference between overloading and overriding?
Overriding = when a methods in subclass are the same in superclass we call that overriding. The method in subclass overrides the method logic by providing different code.
Overloading - We can achieve overloading only when a method has the same name and different paramaters. There are several ways to overload a method:
- multiple parameters
- different parameters type
- different paramters order
#### What are the Object Oriented Principles? Explain the concepts with realistic examples!
Inheritance - 
Polymorphism -
Encapsulation - 
Abstraction - 

#### What is method overloading?
When a method has different parameters but same method signature is called method overloading.
#### What is method overriding?
When you have same method signature in subclass and superclass is called method overriding. You can override the initial implmenetation in subclass.
#### Explain how object oriented languages attempt to simplify memory management for Programmers.

#### Explain the “Single Responsibility” principle!
The single-responsibility principle (SRP) is a computer-programming principle that states that every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class, module or function.
#### What is an object oriented program? Explain, show.
An object oriented program is a programming paradigm that is based on the concept of objects. Each object has its own set of properties.
#### How do you make a class immutable? What do you need to watch out for?
You can make a class immutable in few ways:
1. Declare class final
2. Declare class members final
3. Create getter methods and no set method.

#### How many instances can be created for an abstract class?
You can't create a an instance from an asbtract class.
## Programming languages

### Java

#### What is autoboxing and unboxing?
Autoboxing and Unboxing. Autoboxing is the automatic conversion that the Java compiler makes between the primitive types and their corresponding object wrapper classes
#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?
Use a unsigned integer.
#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?
A variable is available only in the scope it was defined (curly brackets). 
#### What is the purpose of the ‘equals()’ method?
.equals() evaluates to the comparison of values in the objects.
#### What is the difference between '==' and 'equals()'?
== checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects.
#### What does the ‘static’ keyword mean?
Method or field defined static is only available at class level.
#### Why is the main() method declared as static? Explain.
Java main() method is always static, so that compiler can call it without the creation of an object or before the creation of an object of the class
#### What is the default access modifier in a class?
In java the default access modifier is the one with no access modifier.
#### What is the JVM?
A Java virtual machine (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode. 
#### What is the difference between the JRE and the JDK?
JDK is a software development kit whereas JRE is a software bundle that allows Java program to run
#### What is the difference between long and Long?
long is an primitive type and Long is a class.
#### Can a long store bigger numbers than a Long?
No.
#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.
java.util.ArrayList;
java.util.Collections;
java.util.List;
#### What are the access modifiers in Java? Which one could we use for class?
public, private, protected and default. For class we can use public and default.
#### Can an “enum” contain methods in Java? Explain.
Enum can contain constructors, methods, fields.
#### When would you use a private/protected/public attribute? What is the difference?
Private is used when you want to limit access only insde the class, protected inside the class but can be accessed if that class is inherited.
Using public you can access the class from anywhere.
#### How do you prevent developers from subclassing a class?
Create a private constructor, make the class final.
#### How do you prevent developers from overriding a method in a subclass?
Use the final keyword.
#### How do you prevent developers from changing the value of a variable?
Make the variable static final.
#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!
Use Currency class.
#### What happens if you try to call something, that you have no access to, because of data hiding?
You get an error that Java compiler can't find that member.
#### What happens if you try to delete/drop an item from an array, while you are iterating over it?
You will get IndexOutofbounds exception.
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?
you will get ConcurrentModificationException exception.
#### What happens if you try to add an item to the end of an array, while you are iterating over it?
ArrayIndexOutOfBoundsException
#### If you need to access the iterator variable after a for loop, how would you do it?
#### Which interfaces extend the Collection interface in Java. Which classes?
List, Queue, Set
#### What is the connection between equals() and hashCode()? How are they used in HashMap?
1) If two objects are equal, then they must have the same hash code. 
2) If two objects have the same hash code, they may or may not be equal. 
#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?
Checked exception are the exceptions that happen whe you compile a program and uncheked at runtime.
Checked exception - ClassNotFoundException
Unchked exception - ArithmeticException
#### What is Error in Java and how does it relate to Exception?
Both Exception and Error classes are inherited from Throwable class.
#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?
You can use finnaly to run code in both situation ( exception or no exception).
For example in a connection to a database you want to close the exception if the querry was executed or there is an exception.
#### What is the largest number you can work with in Java?
#### When you use method overriding, can you change the access level of the method, from protected to public? Why?When you use method overriding, can you change the access level of the method, from public to protected? Why?
On overriding no because it needs to be the same access level to the one in superclass.
#### Can the main method be overridden? Explain your answer!
In short, main method can be overloaded but cannot be overridden in Java simply because its a static method.
#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?
#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?
#### What does "final" mean in case of a variable, method or a class?
In variable using final, you create a constant
For methods, prevent method overriding.
For classes, prevent inheritance.
#### What is the super keyword?
super is used to call superclass constructor and members if they are the same in subclass.
#### What are “generics”? When to use? Show examples.
ava Generic methods and generic classes enable programmers to specify, with a single method declaration, a set of related methods, or with a single class declaration, a set of related types.
#### What is the benefit of having “generic” containers?
Generics add stability to your code by making more of your bugs detectable at compile time.
#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?
#### What is an annotation? What can be annotated and how? Show examples.
Annotations help to associate metadata (information) to the program elements i.e. instance variables, constructors, methods, classes, etc.
### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?

### Database

#### How can you connect your application to a database server? What are the possible ways?
You can use JDBC whichs is a standard to connect to a database and execute querry or JPA which is a more advanced way to connect to database and use ORM. 
#### What do you know about database normalization?
Normalization is the process of organizing data in a database.
