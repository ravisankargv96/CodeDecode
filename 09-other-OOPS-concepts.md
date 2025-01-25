## Recap
### OOPs Concepts
1. Object
2. Class

1. Inheritance
2. Polymorphism
3. Abstraction
4. Encapsulation

There are other concepts also.

1. Coupling
2. Cohesion
3. Association
    1. Aggregation
    2. Composition


## Other Concepts
### Association
1. Weak Association (Aggregation)
    - Relation between 2 has-A objects are weak
2. Strong Association (Composition)
    - Relation between 2 has-A objects are strong

#### Weak Association
1. both objects can exists independently

```
public class Driver{
    private Car car;
}

// Driver <-> Car can exists independently.
```

```
public class Team{
    List<Player> players;
}

// Player can exist without Team
// Team can exist without Player
// So, Player <-> Team are weakly associated
```

#### Strong Association:
2. One Object can't exists without other

```
public class Car{
    private Engine engine;
}

// Without Engine there is no Car
// So Car is Strongly associated with Engine 
// i.e. Car -> Engine 
```


