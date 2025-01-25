### Classes & Objects

1. All the real world entities can be treated like class
2. Eg. Dog
    features (properties):
        color,
        name,
        breed
    behaviors (methods):
        wagging tail,
        barking
        eating

**Converting the real world entity to POJO**
```
    package code_decode;

    public class Dog {

        // features
        String color;
        String name;
        String breed;

        // behaviour
        public void wagTail() {
        
        }
        public void barking() {

        }

        public void eating() {

        }
    }
```

**Note:** default access modifier will be present if not specified.
i.e. those fields can be accessed with in package(Assume)

```
    package code_decode;

    public class MainClass {
    
        public static void main(String args[]) {
            
            Dog tommy = new Dog();
            tommy.barking();
            // color is default so, it can be accessed
            tommy.color = "black"; 
            tommy.printColor();

            Dog dog1 = new Dog();
            dog1.eating();
            dog1.color = "white";
            dog1.printColor();
        }
    }
```
