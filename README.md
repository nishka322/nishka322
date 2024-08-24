## C++ Code Example

```cpp
#include <iostream>
#include <vector>
#include <string>

class GitHubProfile {
public:
    GitHubProfile(std::string uname, std::string name, std::string lang, std::vector<std::string> stack, std::string location, std::string status)
            : username(uname), name(name), language(lang), stack(stack), location(location), status(status) {}

    void about() const {
        std::cout << "Привет, меня зовут " << name << ", или " << username << " на GitHub." << std::endl;
        std::cout << "Я более 10 лет занимаюсь написанием технической документации и люблю делиться знаниями." << std::endl;
        std::cout << "В свободное время я практикуюсь в различных языках программирования, хотя мой основной стек для написания документации включает: ";
        for (size_t i = 0; i < stack.size(); ++i) {
            std::cout << stack[i];
            if (i < stack.size() - 1) {
                std::cout << ", ";
            }
        }
        std::cout << "." << std::endl;
        std::cout << "Если вы хотите увидеть мои достижения в программировании, вы можете ознакомиться с моими публичными репозиториями на GitHub." << std::endl;
        std::cout << "Я также рассматриваю предложения на проекты в области DaC (Data as Code), так что не стесняйтесь связаться со мной!" << std::endl;
    }

private:
    std::string username;
    std::string name;
    std::string language;
    std::vector<std::string> stack;
    std::string location;
    std::string status;
};

int main() {
    system("chcp 65001"); // Set code page to UTF-8
    std::vector<std::string> stack = {"Markdown", "XML", "HTML", "CSS"};
    GitHubProfile me("Nishka", "Макс", "Русский", stack, "РФ", "Рассматриваю предложения на проекты DaC");
    me.about();
    return 0;
}

### Watch the snake eat my contributions:

![snake gif](https://github.com/nishka322/nishka322/blob/output/snake.svg)

