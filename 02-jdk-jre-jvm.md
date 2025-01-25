### JVM JRE & JDK?
Before jumping into the internals of Java, let's understand how a Java source file is
executed.

1. We write the Java source code in simple .java file using an editor or IDE
(integrated development environment) e.g. Eclipse or IntelliJ Idea.
2. Program has to be compiled into bytecode. Java compiler (javac) compiles the sourcecode to Simple.class file.
3. This class file can be executed in any platform/OS by JVM (Java virtual
machine).
4. JVM translates bytecode into native machine code which machines can execute.

Flow:
Simple.java  -> java Compiler -> simple.class -> JVM (executes) -> machine code

Note: before executing simple.class -> machine code, JVM pulls the library code
library Code -> JVM


### What is JDK?

1. JDK is a superset of JRE. JDK contains everything that JRE has, along with development tools for developing, debugging, and monitoring Java applications.
2. You need JDK when you need to develop Java applications.
3. Same as JREs, JDKs are also platform dependent. So take care when you download the JDK package for your machine.

### What is JRE?
1. JRE (Java Runtime Environment) is a software package that provides Java class libraries, along with Java Virtual Machine (JVM), and other components to run applications written in Java programming. JRE is the superset of JVM. 

2. If you need to run Java programs, but not develop them, JRE is what you need. (best eg. EBS)

    The following steps takes place at runtime.
    1. Class loader
    2. Byte Code Verifier
    3. Just in time compiler

### Hierachy:

JVM
JVM + Library classes -> JRE 
JVM + Library classes + Development Tools -> JDK

### What is JVM ?
1. Java Virtual machine (JVM) is the virtual machine that runs the Java bytecodes (**.class**). 
2. You get this bytecode by compiling the **.java** files into .class files using (javac - java compiler). **.class** files contain the bytecodes understood by the JVM.

Note: javac -> java compiler

### Flow:
src code -> JDK (javac) -> bytecode (**.class**) -> JVM 

library methods (present in JRE) -> JVM (pulls) 

Now using JIT (Just In time compiler)
(**.class**) -> machine level

i.e. flow1 + flow2 -> JVM (JIT) -> machine code.
