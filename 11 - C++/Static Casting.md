### Definition
`static_cast` is a casting method that allows you to convert between different data types or pointer types. A compile-time check is done to ensure the cast is safe.

### Examples
```cpp
int main() {
    int a = 10;
    float b = static_cast<float>(a);

    int* p = &a;
    float* p2 = static_cast<float*>(p);

    enum Color = {RED, GREEN, BLUE}
    int value = 1;
    Color myColor = static_cast<Color>(value);  // GREEN
    return 0;
}
```

### More Details
`static_cast` can be used to cast to derived classes but should only be used if you know the cast will succeed. Otherwise you would be better off sacrificing runtime performance to perform [[Dynamic Casting]] and checking the result.