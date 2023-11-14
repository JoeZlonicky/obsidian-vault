### Description
Structures are used to store data together under one variable. Data and methods are public access by default.

### Examples
```c++
struct Person {
	std::string name;
	int age;
	float heightMeters;

	void introduceSelf() {
		std::cout << "My name is " << name << std::endl;
	}
}

int main() {
	Person p1 = {"Joe Zlonicky", 22, 1.75};
	return 0;
}
```