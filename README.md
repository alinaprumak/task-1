# task-1
#include <iostream>
#include <string>

int main() {
    std::string word;
    // Зчитуємо одне слово з консолі
    std::cin >> word; 
    // Проходимо циклом по кожній літері
    for (size_t i = 0; i < word.size(); ++i) {
        char letter = word[i];
        int code = int(letter); // Отримуємо ASCII-код символу
        // Виводимо літеру та її ASCII-код через пробіл
        std::cout << letter << " " << code << " ";
        // Збираємо двійковий запис рівно у 8 розрядів
        for (int bit = 7; bit >= 0; --bit) {
            std::cout << ((code >> bit) & 1);
        }
        std::cout << "\n"; // Перехід на новий рядок
    }
    
    return 0;
}
