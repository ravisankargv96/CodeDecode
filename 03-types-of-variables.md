### 3 Types of variables in Java
1. Local variables
2. Instance variables
3. Class variables

### Instance Variables

1. Object is created with the use of the **new** keyword in heap memory
2. Declared within class but outside any methods/constructor or any block.
3. They have default values
4. Access modifiers can be given for instance variables
5. It's advisiable that, they should be created when it's used by more than 1 methods or variables. Since they are in memory untill object get's destroyed.

Eg. Code for **Instance variables**

```
    package com.codeDecode.startup;

    public class Fruits {

        public static void main(String[] args) {
            
            ExoticFruits ef = new ExoticFruits();
            ef.dragonFruit = 7;
            ef.kiwi = 8;
            
            ExoticFruits efNew = new ExoticFruits();
            
        }
    }

    class ExoticFruits {
        
        //Instance variables
        int dragonFruit = 2;
        int kiwi = 5;

        public void method(){
            System.Out.println(dragonFruit)
        }

        public static void method2(){
            ExoticFruits ef = new ExoticFruits()
            // can be called only through instance
            System.Out.println(ef.dragonFruit)
        } 
    }
```

**Note:** 
1. In a static block if you need to call instance variable,
    - create an object
    - then call obj.instance
2. In nonstatic block it can be called directly by variable name (or this.variableName).


### Local variables

1. Declared within Inside methods/ Constructor Blocks (shown in eg.)
2. these are created & initialized when methods/constructors/blocks are entered (in stack memory) & destroyed when method is completed. 
3. (or) Local variables are visiable only within the declared method/constructor/block (since created in stack memory)
4. Access modifiers cannot be used for local variables.
5. No default values for local variables, so local variables should be declared & initial value should be assigned before it's used.
6. Local variable can't be defined with **static** keyword


Eg. code for **local variables**.

```
    package com.codeDecode.startup;

    public class Marks {

        public static void main(String[] args) {
            Marks m = new Marks ();
            m.getMarks();
        }
        
        public void getMarks() {
        
            // local variables
            int maths = 40;
            int physics - 80;
            int biology = 99;
            System.out.print(maths + physics + biology);
        }
    }
```

### Class Variables: (similar type to instance variables)
1. Also known as static Variables. Declared outside methods/Constructors/Block
2. There would only be one copy of each class variable per class, regardless of how many objects are created from it.
3. Default values are same as instance variables
4. static variables can be accessed by calling with
    - class name 
        ClassName.VariableName (advisable)
    - Apart from object name
        ClassName cn = new ClassName()
        cn.VariableName
    Both are valid.
5. It can't be local
6. Memory allocation for static variable happens only once when the class is loaded in the memory. it doesn't depend on **objects life**


```
public class Dog{
    
    // class variable
    static String hospitalName = "xyz";
    
    // instance variable
    String color;
    String name;
}
```

