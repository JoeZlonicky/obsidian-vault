Name mangling is a technique used by compilers to encode additional information about the scope, type, linkage, and other identifying information within a single name. The primary purpose of this is to support [[Function Overloading]], which allows multiple functions to have the same name but different parameter lists.

For example, given the function
```c++
int add(int a, int b)
{
	return a + b;
}
```
A compiler might generate the mangled name `_Z3addii` to encode the function name as well its two int parameters.

The exact rule for name mangling are implementation and platform dependent.

A tool such as `c++filt` can be used to demangle a mangled name back to its original identifier, which can be useful when debugging.
```bash
$ echo "_Z3addii" | c++filt
add(int, int)
```
