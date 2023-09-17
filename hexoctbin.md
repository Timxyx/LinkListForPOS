## C++ Conversion Functions: Hex, Octal, Decimal, and Binary

```cpp
#include <iostream>
#include <bitset>
#include <string>
#include <sstream>

// Convert Decimal to Hex, Octal, and Binary
void decimalToOthers(int decimal) {
    std::cout << "Hex: " << std::hex << decimal << std::endl;
    std::cout << "Octal: " << std::oct << decimal << std::endl;
    std::cout << "Binary: " << std::bitset<32>(decimal) << std::endl;
}

// Convert Hex to Decimal, Octal, and Binary
void hexToOthers(const std::string& hex) {
    int decimal = std::stoi(hex, nullptr, 16);
    decimalToOthers(decimal);
}

// Convert Octal to Decimal, Hex, and Binary
void octalToOthers(const std::string& octal) {
    int decimal = std::stoi(octal, nullptr, 8);
    decimalToOthers(decimal);
}

// Convert Binary to Decimal, Hex, and Octal
void binaryToOthers(const std::string& binary) {
    int decimal = std::stoi(binary, nullptr, 2);
    decimalToOthers(decimal);
}

int main() {
    // Test
    std::cout << "Decimal 255 to others:" << std::endl;
    decimalToOthers(255);
    std::cout << "\nHex FF to others:" << std::endl;
    hexToOthers("FF");
    std::cout << "\nOctal 377 to others:" << std::endl;
    octalToOthers("377");
    std::cout << "\nBinary 11111111 to others:" << std::endl;
    binaryToOthers("11111111");
    
    return 0;
}
```