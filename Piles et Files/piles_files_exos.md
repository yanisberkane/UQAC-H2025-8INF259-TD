# Exercices : Piles et Files en C++
## Exercice 1 : Implémentation d'une pile (Stack)
Implémentez une classe générique `Stack` en C++ à l'aide d'un tableau dynamique `std::vector`.
Ajoutez les fonctions suivantes :
- `void push(T value)` : Ajouter un élément au sommet de la pile.
- `T pop()` : Retirer et retourner l'élément au sommet de la pile.
- `T peek()` : Retourner l'élément au sommet sans le retirer.
- `bool isEmpty()` : Vérifier si la pile est vide.
- `size_t size()` : Retourner le nombre d'éléments dans la pile.
- `void clear()` : Vider la pile.

Indice : Utilisez un template pour que la pile puisse contenir n'importe quel type d'élément.

Exemple attendu :

```cpp
Stack<int> stack;
stack.push(10);
stack.push(20);
std::cout << stack.peek(); // Affiche 20
stack.pop();
std::cout << stack.isEmpty(); // Affiche 0 (false)
```

## Exercice 2 : Utilisation de `std::stack`
Créez une pile d'entiers en utilisant `std::stack`.
Ajoutez les valeurs de 1 à 5 dans la pile.
Affichez et retirez les éléments de la pile jusqu'à ce qu'elle soit vide.

Exemple attendu :

```cpp
5
4
3
2
1
```

## Exercice 3 : Implémentation d'une file (Queue)
Implémentez une classe générique `Queue` en C++ à l'aide d'un tableau dynamique `std::vector`.
Ajoutez les fonctions suivantes :
- `void enqueue(T value)` : Ajouter un élément à la fin de la file.
- `T dequeue()` : Retirer et retourner l'élément au début de la file.
- `T front()` : Retourner l'élément au début sans le retirer.
- `bool isEmpty()` : Vérifier si la file est vide.
- `size_t size()` : Retourner le nombre d'éléments dans la file.
- `void clear()` : Vider la file.

Indice : Utilisez un template pour que la file puisse contenir n'importe quel type d'élément.

Exemple attendu :

```cpp
Queue<int> queue;
queue.enqueue(10);
queue.enqueue(20);
std::cout << queue.front(); // Affiche 10
queue.dequeue();
std::cout << queue.isEmpty(); // Affiche 0 (false)
```

## Exercice 4 : Utilisation de `std::queue`
Créez une file d'entiers en utilisant `std::queue`.
Ajoutez les valeurs de 1 à 5 dans la file.
Affichez et retirez les éléments de la file jusqu'à ce qu'elle soit vide.

Exemple attendu :

```cpp
1
2
3
4
5
```

## Exercice 5 : Problème pratique - Inverser une chaîne de caractères avec une pile
Écrivez un programme qui lit une chaîne de caractères.
Utilisez une pile (`std::stack`) pour inverser la chaîne.
Affichez la chaîne inversée.

Exemple attendu :

```text
Entrée : "hello"
Sortie : "olleh"
```

## Exercice 6 : Gestion des priorités avec une file de priorité
Utilisez `std::priority_queue` pour gérer des tâches avec des priorités.
Ajoutez des paires `(priorité, tâche)` dans la file.
Affichez et retirez les tâches par ordre décroissant de priorité.

Exemple attendu :

```cpp
Tâches :
3 - Faire la vaisselle
1 - Étudier
5 - Aller au sport

Sortie :
Aller au sport
Faire la vaisselle
Étudier
```
