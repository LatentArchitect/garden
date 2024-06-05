# Programming Theory and Core Concepts

# My Notes

!!! NOTE Types VS Classes:
    
    In type theory terms;

    - A type is an abstract interface.
    Types generally represent nouns, such as a person, place or thing, or something nominalized,

    - A class represents an implementation of the type.
    It is a concrete data structure and collection of subroutines

    Different concrete classes can produce objects of the same abstract type (depending on type system).

    *For example, one might implement the type Stack with two classes: SmallStack (fast for small stacks, but scales poorly) and ScalableStack (scales well but high overhead for small stacks).*

    Similarly, a given class may have several different constructors.

    ![Alt text](image.png)
    The banana example.
    - A **`Banana`** *type* would represent the properties and functionality of bananas in general.

    - The **`ABCBanana`** and **`XYZBanana`** classes would represent ways of producing bananas.
      (Different banana suppliers in real life, or different data structures and functions to represent and draw bananas in a video game).

        The **`ABCBanana`** class could then produce particular bananas which are instances of the **`ABCBanana`** class, they would be objects of type Banana.

    It is not rare the programmer provide a single and only implementation for a type. In this case the *class* name is often identical with the *type name*. But there is still a type (which could be extracted in an interface if required), and an implementation (which would implement the separate interface) which builds instances (objects) of the class.

    [^1]


<!-- # Footer # -->

[^1]: 