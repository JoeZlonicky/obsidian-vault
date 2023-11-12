The `auto` keyword automatically deduces the type of a variable, or the return type of a function, at compile time.

### Examples
```cpp
auto myFunction() {
    return 2 + 2;  // int deduced
}

int main() {
    auto myValue = 0.2f;  // float deduced
    return 0;
}
```