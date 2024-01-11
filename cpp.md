## Strings
```
#include <string.h>
```

length() or size(): Returns the number of characters in the string.
```
std::string str = "Hello, World!";
std::cout << "Length: " << str.length() << std::endl;
```

empty(): Returns true if the string is empty, false otherwise.
```
std::string str = "Hello";
if (str.empty()) {
    // String is empty
}
```

append(const std::string& str) or operator+=: Appends another string to the end of the current string.
```
std::string str = "Hello";
str += ", World!";
```

insert(size_type pos, const std::string& str): Inserts another string at the specified position.
```
std::string str = "Hello";
str.insert(5, ", World!");
```

erase(size_type pos, size_type count): Erases a portion of the string, starting from the specified position.
```
std::string str = "Hello, World!";
str.erase(7, 6); // Erase ", World"
```

replace(size_type pos, size_type count, const std::string& str): Replaces a portion of the string with another string.
```
std::string str = "Hello, World!";
str.replace(7, 5, "Universe");
```

substr(size_type pos, size_type count): Returns a substring of the current string, starting from the specified position.
```
std::string str = "Hello, World!";
std::string substring = str.substr(7, 5); // "World"
```

find(const std::string& str, size_type pos) or find_first_of, find_last_of: Finds the first occurrence of another string within the current string.
```
std::string str = "Hello, World!";
size_t found = str.find("World");
if (found != std::string::npos) {
    // "World" found in the string
}
```

compare(const std::string& str): Compares the string with another string.
```
std::string str1 = "Hello";
std::string str2 = "Hello";
if (str1.compare(str2) == 0) {
    // Strings are equal
}
```

c_str(): Returns a pointer to the null-terminated character array representing the string.
```
std::string str = "Hello";
const char* cString = str.c_str();
```

std::getline(std::istream& is, std::string& str): Reads a line from an input stream into a string.
```
std::string line;
std::getline(std::cin, line);
```






## Vectors

push_back(const T& value): Adds an element to the end of the vector.
```
std::vector<int> vec;
vec.push_back(10);
pop_back(): Removes the last element from the vector.
```

pop_back(): Removes an element from the end of the vector
```
std::vector<int> vec = {1, 2, 3};
vec.pop_back();
size(): Returns the number of elements in the vector.
```

size(): get the size of the vector
```
std::vector<int> vec = {1, 2, 3};
std::cout << "Size: " << vec.size() << std::endl;
empty(): Returns true if the vector is empty, false otherwise.
```

empty(): checks if the vector is empty and returns booleans
```
std::vector<int> vec;
if (vec.empty()) {
    // Vector is empty
}
```

at(size_type pos): Returns a reference to the element at the specified position with bounds checking.
```
std::vector<int> vec = {1, 2, 3};
int value = vec.at(1);
operator[]: Accesses the element at the specified position without bounds checking.
```

front(): Returns a reference to the first element in the vector.
```
std::vector<int> vec = {1, 2, 3};
int value = vec[1];
```

back(): Returns a reference to the last element in the vector.
```
std::vector<int> vec = {1, 2, 3};
int firstElement = vec.front();
```

begin() and end(): Return iterators pointing to the beginning and past-the-end positions of the vector, respectively.
```
std::vector<int> vec = {1, 2, 3};
for (auto it = vec.begin(); it != vec.end(); ++it) {
    // Access elements using iterators
}
```

insert(iterator pos, const T& value): Inserts an element before the specified position.
```
std::vector<int> vec = {1, 2, 3};
auto it = vec.begin() + 1;
vec.insert(it, 10);
```

erase(iterator pos): Removes the element at the specified position.
```
std::vector<int> vec = {1, 2, 3};
auto it = vec.begin() + 1;
vec.erase(it);
```

clear(): Removes all elements from the vector.
```
std::vector<int> vec = {1, 2, 3};
vec.clear();
```
