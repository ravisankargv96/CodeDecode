#### Inheritance / Is-a Relation:
child Is-a Parent (i.e. Dog Is-a Animal)

Animal:
    int eyes
    int legs

Cat: Animal
    String sound = "Meows"

Dog: Animal
    String sound = "Barks"

#### Types of inheritance in java
1. Single
2. Multi-level
3. hierarchical
4. multiple
5. hybrid

#### Single:
Child: Parent

1. refers to a child & parent class relationship where a class extends another class.
2. Involves 2 class (Parent & child)
3. Child is also known as **SubClass**
e.g. Dog: Animal

#### Multilevel Inheritance:
Child1: Parent
Child3: Child2
ChildN: ...

1. Refers to a child & parent relationship where a super child class extends the child class.
2. i.e. 
```
Class Child1 extends Parent
```
&
```
Class Child2 extends Child1
```

3. Eg.
```
Class Dog extends Animal
```
& 
```
Class Labrador extends Dog
```

#### Hierarchical Inheritance:
Child1 : Parent
Child2 : Parent
Child3 : Parent

1. Refers to a child and parent class relationship where more than one classes extends the same class.

#### Hybrid Inheritance:
Child1 : Parent
Child3 : Child1

Child2 : Parent

1. Combination of more than one types of inheritance in a single program (e.g. Single & hierarchial Combination)

#### Multiple Inheritance:
Child1 : Parent1
Child1 : Parent2

1. Extending more than one classes, which means a child class has 2 Parent classes.
2. It's not implemented in java.

Why?

Eg. 
```
    TerrestrialAnimals:
        breath()
            //through Lungs

    AquaticAnimals:
        breath()
            //through Grills

    AmphibianAnimals: TerrestrialAnimals, AquaticAnimals
        breath()
            // ?
```
It'll raise ambiguity, if parent have 2 different outcomes of same behavior. 

For not arising the above kind of issue, java isn't supporting Multiple Inheritance
