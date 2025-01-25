Complete Notes on Polymorphism
Topics:
1. Polymorphism (Theory)
2. Static Polymorphism (example)
3. type Promotion in Java (Imp Interview question)
4. overriding in java
5. upcasting in java
6. dynamic polymorphism (example)
7. can we implement dynamic polymorphism with instance variables?
8. covariant return types in java (imp interview question)

### Polymorphism
1. Ability of an object to take many forms
2. Eg. Frog
    - is an Animal
    - is a TerrestrialAnimal
    - is an AquaticAnimal
3. Any object in java that passes Is-A test is polymorphic.

**Note:** Since all objects extends oject class, hence all object are polymorphic.
    Eg.
    obj.to_string() , behaves differently from Integer, Array etc. 

#### Types of Polymorphism
1. Static Polymorphism (Method Overloading)
2. Dynamic Polymorphism (Method Overriding)

##### Static Polymorphism (Method Overloading)
1. By changing # of args
2. By changing DataTypes

**Note:** overloading isn't possible by changing the return type only. It gives compile time error due to ambiguity (in fn call)


###### Overriding
```
class Dog{
    public void spclCapabilities(){

    }
}

class Pug extends Dog{
    @override
    public void spclCapabilities(){

    }
}

class Labrador extends Dog{
    @override
    public void spclCapabilities(){

    }
}
```

##### Dynamic Polymorphism
1. a process in which a call to overridden method is resolved at runtime rather than compile time.


###### Upcasting
1. reference variable of parent Class/Interface refers to the object of child class

```
Parent pRef = new ChildObj();      //upcasting
pRef.someMethod();
```


###### Overriding vs Runtime Polymorphism

```
// Overriding
Pug pug = new Pug();
pug.spclCapabilities();

Labrador lab = new Labrador();
lab.spclCapabilities();

// Runtime polymorphism
Dog dog = new Pug();
dog.spclCapabilities();

Dog dog = new Labrador();
dog.spclCapabilities();
```














### Type Promotion
1. Smaller data type is promoted to bigger one if no matching data type is found.
eg.
    Add(int a, Long b)
    in Add(4,5) then 5 is promoted to long data type.


##### Matches Formal arguments
add(int a, int b) <-> add(4, 5)
a = 4, b = 5

##### Doesn't Match Formal arguments, But can be Promoted
add(int a, Long b) <-> add(4, 5)
a = 4, b = 5L
4 matched to a but 5 is Promoted to Long

##### Matches more than once/Ambiguity
add(int a, Long b)
add(Long a, int b)  <-> add(4, 5)

Marks ambiguity for who to promo long
