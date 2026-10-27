
#include <iostream>
using namespace std;

// Single Inheritance
class Animal {
public:
    void eat() {
        cout << "Animal is eating." << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Dog is barking." << endl;
    }
};

// Multilevel Inheritance
class Puppy : public Dog {
public:
    void weep() {
        cout << "Puppy is weeping." << endl;
    }
};

// Multiple Inheritance
class Father {
public:
    void fatherProperty() {
        cout << "Father's property." << endl;
    }
};

class Mother {
public:
    void motherProperty() {
        cout << "Mother's property." << endl;
    }
};

class Child : public Father, public Mother {
public:
    void childProperty() {
        cout << "Child's property." << endl;
    }
};

// Hierarchical Inheritance
class Shape {
public:
    void display() {
        cout << "This is a shape." << endl;
    }
};

class Circle : public Shape {
public:
    void drawCircle() {
        cout << "Drawing a circle." << endl;
    }
};

class Rectangle : public Shape {
public:
    void drawRectangle() {
        cout << "Drawing a rectangle." << endl;
    }
};

// Hybrid Inheritance
class Person {
public:
    void showPerson() {
        cout << "This is a person." << endl;
    }
};

class Student : public Person {
public:
    void showStudent() {
        cout << "This is a student." << endl;
    }
};

class Sports {
public:
    void showSports() {
        cout << "Student participates in sports." << endl;
    }
};

class Result : public Student, public Sports {
public:
    void showResult() {
        cout << "Displaying student result." << endl;
    }
};

int main() {
    cout << "SINGLE INHERITANCE" << endl;
    Dog d;
    d.eat();
    d.bark();

    cout << "\nMULTILEVEL INHERITANCE" << endl;
    Puppy p;
    p.eat();
    p.bark();
    p.weep();

    cout << "\nMULTIPLE INHERITANCE" << endl;
    Child c;
    c.fatherProperty();
    c.motherProperty();
    c.childProperty();

    cout << "\nHIERARCHICAL INHERITANCE" << endl;
    Circle cir;
    Rectangle rect;
    cir.display();
    cir.drawCircle();
    rect.display();
    rect.drawRectangle();

    cout << "\nHYBRID INHERITANCE" << endl;
    Result r;
    r.showPerson();
    r.showStudent();
    r.showSports();
    r.showResult();

    return 0;
}
