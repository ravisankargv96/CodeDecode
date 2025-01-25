### Constructor

1. It is a spcl method, the name should be same as class name.
2. Constructor should not have a return type
3. Constructor cannot be abstract, static, synchronize & final

```
class ClassName{
    
    public ClassName(){

    }
}
```

**Note:** 
1. if you don't provide a constructor a default constructor will be initialized.
2. If you provide one then that constructor will be considered.

#### Default constructor
1. If no constructor is mentioned then default constructor will be called.
```
package code_decode;

public class Dog {

    String color;
    String name;
    String breed;

    public void wagTail() {
        System.out.println("Dog wag their tails");
    }

    public void barking() {
        System.out.println("Dog barks");
    }

    public void eating() {
        System.out.println("Dog eats");
    }

    public void printColor() {
        System.out.println(this.color);
    }
}
```

#### Parameterized constructor
2. If constructor with params are mentioned, then we has to write a default constructor (if we need to initiate with out params)
i.e. ClassName cn = new ClassName()

```
package code_decode;

public class Dog {

    String color;
    String name;
    String breed;

    // it should be written
    public Dog(){

    }

    public Dog (String clr){
        this.color = clr
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

    public void printColor() {
        System.out.println(this.color);
    }
}
```


