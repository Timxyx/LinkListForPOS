## **Catch2 Cheat Sheet**

Catch2 is a unit testing framework for C++ that's known for its simplicity and header-only distribution.

### **1. Basic Setup:**

Include the Catch2 header:
\```cpp
#define CATCH_CONFIG_MAIN  // This tells Catch to provide a main() - only do this in one cpp file
#include "catch.hpp"
\```

### **2. Writing Test Cases:**

Basic test case:
\```cpp
TEST_CASE("Description of the test case") {
    REQUIRE( expression_to_test );
}
\```

Sections (subdivisions of a test case):
\```cpp
TEST_CASE("Description") {
    SECTION("Sub-description 1") {
        REQUIRE( expression_to_test );
    }
    SECTION("Sub-description 2") {
        REQUIRE( another_expression_to_test );
    }
}
\```

### **3. Assertions:**

- **Basic checks**:
  - `REQUIRE( expression );` - Fails and stops current test
  - `CHECK( expression );` - Fails but continues current test

- **Comparisons**:
  - `REQUIRE_FALSE( expression );`
  - `CHECK_FALSE( expression );`
  - `REQUIRE_THROWS( expression );`
  - `CHECK_THROWS( expression );`
  - `REQUIRE_THROWS_AS( expression, exception_type );`
  - `CHECK_THROWS_AS( expression, exception_type );`
  - `REQUIRE_NOTHROW( expression );`
  - `CHECK_NOTHROW( expression );`

- **String comparisons**:
  - `REQUIRE_THAT( string_expression, Catch::Matchers::String::equals("expected_string") );`
  - `CHECK_THAT( string_expression, Catch::Matchers::String::contains("substring") );`

### **4. Running Tests:**

- **Run all tests**: `./test_executable`
- **Run specific test**: `./test_executable "test name"`
- **List all tests**: `./test_executable --list-tests`
- **Run tests with a tag**: `./test_executable [tag_name]`

### **5. Tags and Test Case Organization:**

Tagging a test:
\```cpp
TEST_CASE("Description", "[tag1][tag2]") {
    // ...
}
\```

### **6. Floating Point Comparisons:**

For comparing floating point numbers with some tolerance:
\```cpp
REQUIRE( a == Approx(b) );
\```

---

This cheat sheet provides a basic overview of Catch2's main features. Always refer to the official Catch2 documentation for a more comprehensive understanding and additional details.
