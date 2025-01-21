# Solutions des Exercices : Piles et Files en C++

## **Exercice 1 : Implémentation d'une pile (Stack)**
```cpp
#include <iostream>
#include <vector>

template <typename T>
class Stack {
private:
    std::vector<T> elements;

public:
    void push(T value) {
        elements.push_back(value);
    }

    T pop() {
        if (elements.empty()) {
            throw std::out_of_range("Stack is empty");
        }
        T top = elements.back();
        elements.pop_back();
        return top;
    }

    T peek() {
        if (elements.empty()) {
            throw std::out_of_range("Stack is empty");
        }
        return elements.back();
    }

    bool isEmpty() {
        return elements.empty();
    }

    size_t size() {
        return elements.size();
    }

    void clear() {
        elements.clear();
    }
};

int main() {
    Stack<int> stack;
    stack.push(10);
    stack.push(20);
    std::cout << stack.peek() << std::endl; // Affiche 20
    stack.pop();
    std::cout << stack.isEmpty() << std::endl; // Affiche 0 (false)

    Stack<std::string> stringStack;
    stringStack.push("Hello");
    stringStack.push("World");
    std::cout << stringStack.peek() << std::endl; // Affiche World

    return 0;
}
```

## **Exercice 2 : Utilisation de `std::stack`**
```cpp
#include <iostream>
#include <stack>

int main() {
    std::stack<int> stack;

    for (int i = 1; i <= 5; ++i) {
        stack.push(i);
    }

    while (!stack.empty()) {
        std::cout << stack.top() << std::endl;
        stack.pop();
    }

    return 0;
}
```

## **Exercice 3 : Implémentation d'une file (Queue)**
```cpp
#include <iostream>
#include <vector>

template <typename T>
class Queue {
private:
    std::vector<T> elements;

public:
    void enqueue(T value) {
        elements.push_back(value);
    }

    T dequeue() {
        if (elements.empty()) {
            throw std::out_of_range("Queue is empty");
        }
        T front = elements.front();
        elements.erase(elements.begin());
        return front;
    }

    T front() {
        if (elements.empty()) {
            throw std::out_of_range("Queue is empty");
        }
        return elements.front();
    }

    bool isEmpty() {
        return elements.empty();
    }

    size_t size() {
        return elements.size();
    }

    void clear() {
        elements.clear();
    }
};

int main() {
    Queue<int> queue;
    queue.enqueue(10);
    queue.enqueue(20);
    std::cout << queue.front() << std::endl; // Affiche 10
    queue.dequeue();
    std::cout << queue.isEmpty() << std::endl; // Affiche 0 (false)

    Queue<std::string> stringQueue;
    stringQueue.enqueue("Bonjour");
    stringQueue.enqueue("Monde");
    std::cout << stringQueue.front() << std::endl; // Affiche Bonjour

    return 0;
}
```

## **Exercice 4 : Utilisation de `std::queue`**
```cpp
#include <iostream>
#include <queue>

int main() {
    std::queue<int> queue;

    for (int i = 1; i <= 5; ++i) {
        queue.push(i);
    }

    while (!queue.empty()) {
        std::cout << queue.front() << std::endl;
        queue.pop();
    }

    return 0;
}
```

## **Exercice 5 : Inverser une chaîne de caractères avec une pile**
```cpp
#include <iostream>
#include <stack>
#include <string>

int main() {
    std::string input;
    std::cout << "Entrez une chaîne : ";
    std::cin >> input;

    std::stack<char> stack;

    for (char ch : input) {
        stack.push(ch);
    }

    std::string reversed;
    while (!stack.empty()) {
        reversed += stack.top();
        stack.pop();
    }

    std::cout << "Chaîne inversée : " << reversed << std::endl;

    return 0;
}
```

## **Exercice 6 : Gestion des priorités avec une file de priorité**
```cpp
#include <iostream>
#include <queue>
#include <vector>
#include <string>

int main() {
    std::priority_queue<std::pair<int, std::string>> tasks;

    tasks.push({3, "Faire la vaisselle"});
    tasks.push({1, "Étudier"});
    tasks.push({5, "Aller au sport"});

    while (!tasks.empty()) {
        std::cout << tasks.top().second << std::endl;
        tasks.pop();
    }

    return 0;
}
```
