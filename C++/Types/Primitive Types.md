
### Primitive Types

| Data Type | Typical Size | Typical Range | Notes |
| - | - | - | - |
| bool | 1 byte | true or false | It can't be just a bit because otherwise you couldn't address it in memory. |
| char | 1 byte | -127 to 127 or 0 to 255 | Signed or unsigned is implementation defined. |
| wchar_t | 2 or 4 bytes | 0 to ... | For 32 bit characters (UTF-32) on Linux and 16 bit characters (UTF-16) on Windows. Was supposed to large enough to support any printable character. It's better to use char16_t or char32_t. |
| char16_t | 2 bytes | 0 to 65,535 | For UTF-16 characters. Use std::u16string for strings.|
| char32_t | 4 bytes | 0 to 4,294,967,295 | For UTF-32 characters. Use std::u32string for strings. |
| int | 4 bytes | -2,147,483,648 to 2,147,483,647 | |
| float | 4 bytes | ±1.18x10^-38 to ±3.4x10^38 | 1 bit for sign, 8 bits for the exponent, and 23 bits for the mantissa. Can represent 0.0 with just all 0's. Should add 'f' suffix for a number to be treated as a float and not a double. |
| double | 8 bytes | 0 | Should be the default choice for floating-point numbers unless you are dealing with so many numbers that the smaller size of floats matters and the loss of precision doesn't. |
| void | | | Is an incomplete type. Can be used for void pointers or void return type. |

### Integer Modifiers

| Modifier | Usage |
| - | - |
| signed | Forces signed (+/-) representation of integer types. |
| unsigned | Forces unsigned (+) representation of integer types. |
| short | Promises a width of at least 16 bits |
| long | Promises a width of at least 32 bits|
| long long | Promises a width of at least 64 bits |

signed/unsigned and width specifiers can be used together.
### Storing consecutive data
For storing consecutive data of the same type, see [[Arrays]].
