# Fundamental Design Principles in Object-oriented Programming

- Abstraction
- Encapsulation
- Decomposition
- Generalization

## Design Principles

### Abstraction
- Example of how a car object could be abstracted in different contexts
    <img src="assets/abstraction.jpg" alt="right" align="middle" width="60%" height="60%">

- Food objects in a grocery store and health context are represented differently.

    <img src="assets/abstraction_uml.png" alt="right" align="middle" width="60%" height="60%">

    - In the above figure, we use UML class diagrams to represent the differences between how food objects are abstracted in 2 specific cases.
    
    - A UML class diagram consists of 3 parts:
        - The top part defines the name of the class
        - The middle part defines the attributes of the class
        - The bottom part defines the behaviors of the class 

### Encapsulation

- Main ideas of encapsulation:

    <img src="assets/encapsulation.png" alt="right" align="middle" width="60%" height="60%">
    
    - Bundle attributes and behaviors that manipulate the attributes together into a self-contained object.
    - Expose certain attributes and behaviors to outside accesses.
    - Restrict access to certain attributes and behaviors to only within that object.

- Abstraction helps to define what attributes and behaviors are relevant in some context. Encapsulation ensures that these characteristics are bundled together in the same class.
- Benefits of encapsulation
    - Data integrity:
        - You prevent outside access to all the attributes, except through specific methods. For example, the 4-scale gpa attribute of *Student* class could not be directly changed to a value of 10.0
        - Implement *getter* and *setter* methods to provide access and update of the attributes.
    - Black box thinking: The class interface remains the same, while the internal implementation of the class could be changed.
- Encapsulation applies to a *Student* class
    <img src="assets/encapsulation_uml.png" alt="right" align="middle" width="60%" height="60%">

    - In this UML class diagram, we prevent direct *get* and *set* to the Student attributes via assignments. This is represented by ```-``` in front of class attributes.
    - 



### Decomposition


### Generalization


## References
- 