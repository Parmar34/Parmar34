#include <iostream>

class Person {
public:
    Person(const char *name = "John Doe", int age = 0) : name(name), age(age) {}

    void display() {
        std::cout << "Name: " << name << ", Age: " << age << std::endl;
    }

private:
    const char *name;
    int age;
};

int main() {
    Person p1; // uses default values "John Doe" and 0
    Person p2("Jane Doe"); // uses default value 0
    Person p3("Bob Smith", 42);

    p1.display(); // prints "Name: John Doe, Age: 0"
    p2.display(); // prints "Name: Jane Doe, Age: 0"
    p3.display(); // prints "Name: Bob Smith, Age: 42"

    return 0;
}
