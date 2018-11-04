## 1. List the features of Java Programming language.

There are the following features in Java Programming Language.

* **Simple**: Java is easy to learn. The syntax of Java is based on C++ which makes easier to write the program in it.

* **Object-Oriented**: Java follows the object-oriented paradigm which allows us to maintain our code as the combination of different type of objects that incorporates both data and behavior.

* **Portable**: Java supports read-once-write-anywhere approach. We can execute the Java program on every machine. Java program (.java) is converted to bytecode (.class) which can be easily run on every machine.

* **Platform Independent**: Java is a platform independent programming language. It is different from other programming languages like C and C++ which needs a platform to be executed. Java comes with its platform on which its code is executed. Java doesn't depend upon the operating system to be executed.

* **Secured**: Java is secured because it doesn't use explicit pointers. Java also provides the concept of ByteCode and Exception handling which makes it more secured.

* **Robust**: Java is a strong programming language as it uses strong memory management. The concepts like Automatic garbage collection, Exception handling, etc. make it more robust.

* **Architecture Neutral**: Java is architectural neutral as it is not dependent on the architecture. In C, the size of data types may vary according to the architecture (32 bit or 64 bit) which doesn't exist in Java.

* **Interpreted**: Java uses the Just-in-time (JIT) interpreter along with the compiler for the program execution.

* **High Performance**: Java is faster than other traditional interpreted programming languages because Java bytecode is "close" to native code. It is still a little bit slower than a compiled language (e.g., C++).

* **Multithreaded**: We can write Java programs that deal with many tasks at once by defining multiple threads. The main advantage of multi-threading is that it doesn't occupy memory for each thread. It shares a common memory area. Threads are important for multi-media, Web applications, etc.

* **Distributed**: Java is distributed because it facilitates users to create distributed applications in Java. RMI and EJB are used for creating distributed applications. This feature of Java makes us able to access files by calling the methods from any machine on the internet.

* **Dynamic**: Java is a dynamic language. It supports dynamic loading of classes. It means classes are loaded on demand. It also supports functions from its native languages, i.e., C and C++.

## 2. What do you understand by Java virtual machine?

Java Virtual Machine is a virtual machine that enables the computer to run the Java program. JVM acts like a run-time engine which calls the main method present in the Java code. JVM is the specification which must be implemented in the computer system. The Java code is compiled by JVM to be a Bytecode which is machine independent and close to the native code.

## 3. What is the difference between JDK, JRE, and JVM?

#### JVM
JVM is an acronym for Java Virtual Machine; it is an abstract machine which provides the runtime environment in which Java bytecode can be executed. It is a specification which specifies the working of Java Virtual Machine. Its implementation has been provided by Oracle and other companies. Its implementation is known as JRE.

JVMs are available for many hardware and software platforms (so JVM is platform dependent). It is a runtime instance which is created when we run the Java class. There are three notions of the JVM: specification, implementation, and instance.

#### JRE
JRE stands for Java Runtime Environment. It is the implementation of JVM. The Java Runtime Environment is a set of software tools which are used for developing Java applications. It is used to provide the runtime environment. It is the implementation of JVM. It physically exists. It contains a set of libraries + other files that JVM uses at runtime.

#### JDK
JDK is an acronym for Java Development Kit. It is a software development environment which is used to develop Java applications and applets. It physically exists. It contains JRE + development tools. JDK is an implementation of any one of the below given Java Platforms released by Oracle Corporation:

    Standard Edition Java Platform
    Enterprise Edition Java Platform
    Micro Edition Java Platform

## 4. What types of memory areas are allocated by JVM?

* **Class(Method) Area**: Class Area stores per-class structures such as the runtime constant pool, field, method data, and the code for methods.
* **Heap**: It is the runtime data area in which the memory is allocated to the objects
* **Stack**: Java Stack stores frames. It holds local variables and partial results, and plays a part in method invocation and return. Each thread has a private JVM stack, created at the same time as the thread. A new frame is created each time a method is invoked. A frame is destroyed when its method invocation completes.
* **Program Counter Register**: PC (program counter) register contains the address of the Java virtual machine instruction currently being executed.
* **Native Method Stack**: It contains all the native methods used in the application.

## 5. What gives Java its 'write once and run anywhere' nature? 

The bytecode. Java compiler converts the Java programs into the class file (Byte Code) which is the intermediate language between source code and machine code. This bytecode is not platform specific and can be executed on any computer.

## 6. What is classloader?

Classloader is a subsystem of JVM which is used to load class files. Whenever we run the java program, it is loaded first by the classloader. There are three built-in classloaders in Java.

* **Bootstrap ClassLoader**: This is the first classloader which is the superclass of Extension classloader. It loads the rt.jar file which contains all class files of Java Standard Edition like java.lang package classes, java.net package classes, java.util package classes, java.io package classes, java.sql package classes, etc.
* **Extension ClassLoader**: This is the child classloader of Bootstrap and parent classloader of System classloader. It loads the jar files located inside $JAVA_HOME/jre/lib/ext directory.
* **System/Application ClassLoader**: This is the child classloader of Extension classloader. It loads the class files from the classpath. By default, the classpath is set to the current directory. You can change the classpath using "-cp" or "-classpath" switch. It is also known as Application classloader.

## 7. Is Empty .java file name a valid source file name?

Yes, Java allows to save our java file by .java only, we need to compile it by javac .java and run by java classname Let's take a simple example:

```java
//save by .java only  
class A {  
    public static void main(String args[]){  
    System.out.println("Hello java");  
    }  
}  
```
compile by javac .java  
run by     java A  

## 8. Is delete, next, main, exit or null keyword in java?
No.

## 9. If I don't provide any arguments on the command line, then what will the value stored in the String array passed into the main() method, empty or NULL?

It is empty, but not null.

## 10. What if I write static public void instead of public static void?

The program compiles and runs correctly because the order of specifiers doesn't matter in Java.

## 11. What is the default value of the local variables?

The local variables are not initialized to any default value, neither primitives nor object references. 

## 12. What are the various access specifiers in Java?

In Java, access specifiers are the keywords which are used to define the access scope of the method, class, or a variable. In Java, there are four access specifiers given below.

* **Public** The classes, methods, or variables which are defined as public, can be accessed by any class or method.
* **Protected** Protected can be accessed by the class of the same package, or by the sub-class of this class, or within the same class.
* **Default** Default are accessible within the package only. By default, all the classes, methods, and variables are of default scope.
* **Private** The private class, methods, or variables defined as private can be accessed within the class only.

## 13. What is the purpose of static methods and variables?

The methods or variables defined as static are shared among all the objects of the class. The static is the part of the class and not of the object. The static variables are stored in the class area, and we do not need to create the object to access such variables. Therefore, static is used in the case, where we need to define variables or methods which are common to all the objects of the class.

For example, In the class simulating the collection of the students in a college, the name of the college is the common attribute to all the students. Therefore, the college name will be defined as static.

## 14. What are the advantages of Packages in Java?

There are various advantages of defining packages in Java.

* Packages avoid the name clashes.
* The Package provides easier access control.
* We can also have the hidden classes that are not visible outside and used by the package.
* It is easier to locate the related classes.



-------------------------

## 15.(1) Explain public static void main(String args[]).
## 16.(2) Why Java is platform independent?
## 17.(3) Why java is not 100% Object-oriented?
## 18.(4) Which class is the superclass of all classes?
## 20.(5) Java is Pass by Value or Pass by Reference?
## 21.(6) Can we have multiple public classes in a java source file?
## 22.(7) What is Java Package and which package is imported by default?
## 23.(8) What are access modifiers?
## 24.(9) Can we call a non-static method from inside a static method?
## 25.(10) What are wrapper classes?
## 26.(11) What are constructors in Java?
## 27.(12) Can a class have multiple constructors?
## 28.(13) What is Enum in Java?
## 29.(14) What is the difference between double and float variables in Java?
## 30.(15) What is the difference between continue and break statement?
## 31.(16) What is singleton class and how can we make a class singleton?
## 32.(17) Why Strings in Java are called as Immutable?
## 33.(18) What is the difference between equals() and == ?
## 34.(19) What are the differences between Heap and Stack Memory?
## 35.(20) What is Garbage Collection?
## 36.(21) What does super keyword do?
## 37.(22) What is this keyword?
## 38.(23) What is Polymorphism?
## 39.(24) What is data encapsulation and what's its significance?
## 40.(25) What is the benefit of Composition over Inheritance?
## 41.(26) What is the difference between abstract classes and interfaces?
## 42.(27) Can an interface implement or extend another interface?
## 43.(28) Can we declare a class as Abstract without having any abstract method?
## 44.(29) What is method overloading and method overriding?
## 45.(30) Can you override a private or static method in Java?
## 46.(31) What is multiple inheritance? Is it supported by Java?
## 47.(32) What is association?
## 48.(33) What do you mean by aggregation?
## 49.(34) What is composition in Java?
What is difference between Error and Exception?
How can you handle Java exceptions?
What are the differences between Checked Exception and Unchecked Exception?
What purpose does the keywords final, finally, and finalize fulfill?
What are the differences between throw and throws?
What is exception hierarchy in java?
What are the differences between processes and threads?
Why Runnable Interface is used in Java?
What are the two ways of implementing multi-threading in Java?
What is a finally block? Is there a case when finally will not execute?
What is synchronization?
Can we write multiple catch blocks under single try block?
In multi-threading how can we ensure that a resource isn't used by multiple threads simultaneously?
Describe different states of a thread.
