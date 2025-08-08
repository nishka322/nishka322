## About

```cpp
#include <iostream>
#include <vector>
#include <string>

class GitHubProfile {
public:
    GitHubProfile(std::string uname, std::string name, std::string lang, std::vector<std::string> stack, std::string focus)
        : username(uname), name(name), language(lang), stack(stack), focus(focus) {}

    void about() const {
        std::cout << "Привет! Меня зовут " << name << ", на GitHub я известен как " << username << "." << std::endl;
        std::cout << "Я более 10 лет занимаюсь технической документацией и обожаю делиться знаниями." << std::endl;
        std::cout << "Здесь демо-проекты, тестовые решения и идеи, которые я реализовал на практике." << std::endl;
        std::cout << "Мой основной стек для решения прикладных задач документирования: ";
        for (size_t i = 0; i < stack.size(); ++i) {
            std::cout << stack[i];
            if (i < stack.size() - 1) std::cout << ", ";
        }
        std::cout << "." << std::endl;
        std::cout << "Основная работа это обеспечение " << focus << " проектов." << std::endl;
        std::cout << "Заглядывайте в репозитории — может, найдёте что-то полезное или вдохновляющее." << std::endl;
    }

private:
    std::string username;
    std::string name;
    std::string language;
    std::vector<std::string> stack;
    std::string focus;
};

int main() {
    system("chcp 65001");
    std::vector<std::string> stack = {"Java", "JS", "TS", "Phyton", "CSS"};
    GitHubProfile profile("Nishka", "Макс", "Русский", stack, "DocOps");
    profile.about();
    return 0;
}
