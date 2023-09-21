### Description
Classes are very similar to [[Structures]] but with the difference that data and methods are private by default and an access specifier needs to be used to make data/methods public.

### Examples
```run-cpp
#include <iostream>

class Person {
public:
	Person(std::string name, int age) : name(name), age(age) {}
	
	void introduceSelf() {
		std::cout << "Hi, my name is " << name << std::endl;
	}
	
private:
	std::string name;
	int age;
};

int main() {
	Person p1 {"Joe Zlonicky", 22};
	p1.introduceSelf();
	
	return 0;
}
```

### More Details
Classes are usually separated into [[Headers and CPP Files]].

Classes require a semicolon at the end of the definition because the full syntax is `class MyClass {} ...instances...;`. If there was no semicolon the compiler wouldn't know if anything following was an instance or an unrelated statement.

### See Also
* [[Rule of Zero, Three, Five]]
