### Encapsulation
1. It's also known as Data Hiding
Eg. Imagine a Chocolate wrapper
    1. It may contain nuts, Caramel etc. But everything is hidden under a wrapper
    2. It got shipped with packing.

2. Similarly, class has Data & Methods. These Data & Methods are wrapped as a single unit in class
    Eg. Arrays
    1. Index level access (getters, i.e. arr.get(i))
    2. Adding Elements (behaviour)

3. Variables & Methods are hidden in class
4. They can be accessed only through objects
5. Practically to implement it, create private variables & public methods

#### Advantages of Encapsulation
1. By providing only a setter or getter method, you can make the class read-only or write-only.

2. It provides you the control over the data. You can write logic in setter and decide what is to be saved and what NOT.

3. It is a way to achieve data hiding in Java because other class will not be able to access the data through the private data members.

4. The standard IDE's are providing the facility to generate getters & setters. So, it is easy and fast to create an encapsulated class in Java.

Eg. To encapsulate below code.
1. Make all the instance variables as private
2. Add getters & setters to it.

**Before Encapsulating**
```
    package code_decode;

    public class Dog {

        String color;
        String name;
        String breed;
        int age;

        public void wagTail() {
            System.out.println("Dog wag their tails");
        }

        public void barking() {
            System.out.println("Dog barks");
        }

        public void eating() {
            System.out.println("Dog eats");
        }
    }
```
**After Encapsulating**
1. i.e. Adding Getters & Setters
```
    package code_decode;

    public class Dog {

        private String color;
        private String name;
        private String breed;
        private int age;

        //color
        public String getColor(){

        }

        public void setColor(){

        }

        public String getName(){

        }

        public String getbreed(){

        }
        
        public void wagTail() {
            System.out.println("Dog wag their tails");
        }

        public void barking() {
            System.out.println("Dog barks");
        }

        public void eating() {
            System.out.println("Dog eats");
        }
    }
```
