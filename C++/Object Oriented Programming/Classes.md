Classes are very similar to [[Structures]] but with the difference that data and methods are private by default and an access specifier needs to be used to make data/methods public.
```c++
class Person {
public:
	Person(std::string name, int age) : name(name), age(age) {}
	
	void introduceSelf() {
		std::cout << "Hi, my name is " << name << std::endl;
	}
	
private:
	std::string name;
	int age;
}

int main() {
	Person p1 {"Joe Zlonicky", 22};
	return 0;
}
```

Classes are usually separated into [[Headers and CPP Files]].