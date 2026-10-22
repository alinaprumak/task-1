# task-1
#include <iostream>
#include <string>

int main() {
    std::string word;
    std::cin >> word; 
    
    for (size_t i = 0; i < word.size(); ++i) {
        char letter = word[i];
        int code = int(letter);
        std::cout << letter << " " << code << " ";
        for (int bit = 7; bit >= 0; --bit) {
            std::cout << ((code >> bit) & 1);
        }
        std::cout << "\n";
    }
    
    return 0;
}
