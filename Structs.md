# Structs

## Structure
A structure is a container, it can hold a bunch of things
* these can be of any type

Structure are used to organize related data (variables)
The structure s essentially a pre-cursor to Object Orientation
* In C++ they have evolved and look even closer to classes
* Unlike Object Orientation we do not have visibility modifiers

It's safe to treat a structure like a class/object

### Example
Each *thing* in a structure is called member
Each *member* has a name, a type and value
Names follow the rules for var names
Types can be any defined type

```cpp
{

    struct StudentRecord
    {
        char *name; //student name
        double hw[3]; //homework grades
        double test[2]; //test grades
        double ave; //final average
    };

}
```

When defining a structure we create a new data type
* similar to Object Oriented Programming
Once defined we create variables of this new type
* `StudentRecord stu;` variable on the stack

We can create pointers with it as well
* `StudentRecord* ptr;`

## Accessing Members
These are treated like variables
Use member to access operator '.'

```cpp
{

    cout << stu.name << endl;
    stu.hw[2] = 82.3;

}
```

## Assignment
Structures can be use just like variables

```cpp
{

    StudentRecord s1,s2;
    s1.name = "Mark Ash";
    ...
    s2 = s1; //copies this entire structure

}
```

## Pointers and Structs
Pointers to structures are often used
There is another member access operator used with pointers

```cpp
{

    StudentRecord *sptr;
    ...
    cout << "Name is " << sptr->name;
    cout << "Ave is " << sptr->ave;

}
```
This is the same syntax used in Object Orientation
* Used when building data structures