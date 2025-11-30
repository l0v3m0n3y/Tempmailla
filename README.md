# Tempmailla
api for tempmail.la Secure, Free, and Online Temporary Email Service An instant, registration-free temporary email service that helps protect your privacy and prevent spam.
# main
```cpp
#include "Tempmailla.h"
#include <iostream>

int main() {
   Tempmailla api;
    auto email = api.generate_email().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    email.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
