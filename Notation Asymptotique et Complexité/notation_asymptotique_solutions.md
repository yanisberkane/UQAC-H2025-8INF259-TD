
# Solutions : Notation Asymptotique et Complexité

## Solution Exercice 1 : Identifier la complexité temporelle

### 1. Fonction `example1`
```cpp
void example1(int n) {
    for (int i = 0; i < n; i++) {
        std::cout << i << std::endl;
    }
}
```
**Complexité temporelle** : O(n)  
Une seule boucle exécutée `n` fois.

### 2. Fonction `example2`
```cpp
void example2(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            std::cout << i * j << std::endl;
        }
    }
}
```
**Complexité temporelle** : O(n²)  
Deux boucles imbriquées, chacune exécutée `n` fois.

### 3. Fonction `example3`
```cpp
void example3(int n) {
    int i = 1;
    while (i < n) {
        std::cout << i << std::endl;
        i *= 2;
    }
}
```
**Complexité temporelle** : O(log n)  
La valeur de `i` double à chaque itération, donc le nombre d'itérations est proportionnel à `log₂(n)`.

### 4. Fonction `example4`
```cpp
void example4(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = i; j < n; j++) {
            std::cout << i + j << std::endl;
        }
    }
}
```
**Complexité temporelle** : O(n²)  
Les boucles imbriquées exécutent des itérations dépendantes de `i`, mais la complexité globale reste quadratique.

---

## Solution Exercice 2 : Comparer des fonctions
Classement des fonctions en complexité croissante :  
1. O(1)  
2. O(log n)  
3. O(n)  
4. O(n log n)  
5. O(n²)  

---

## Solution Exercice 3 : Analyse de complexité spatiale

### 1. Fonction `example1`
```cpp
void example1(int n) {
    int arr[n];
    for (int i = 0; i < n; i++) {
        arr[i] = i;
    }
}
```
**Complexité spatiale** : O(n)  
Un tableau de taille `n` est créé en mémoire.

### 2. Fonction `example2`
```cpp
void example2(int n) {
    int x = 0;
    for (int i = 0; i < n; i++) {
        x += i;
    }
}
```
**Complexité spatiale** : O(1)  
Seules des variables simples sont utilisées, sans tableau ou structure supplémentaire.

### 3. Fonction `example3`
```cpp
void example3(int n) {
    std::vector<int> vec;
    for (int i = 0; i < n; i++) {
        vec.push_back(i);
    }
}
```
**Complexité spatiale** : O(n)  
Un vecteur dynamique contenant `n` éléments est alloué.

---

## Solution Exercice 4 : Trouver une fonction équivalente

### 1. Fonction O(n)
```cpp
void printElements(int n) {
    for (int i = 0; i < n; i++) {
        std::cout << i << std::endl;
    }
}
```

### 2. Fonction O(log n)
```cpp
void binaryTraversal(int n) {
    int i = 1;
    while (i < n) {
        std::cout << i << std::endl;
        i *= 2;
    }
}
```

### 3. Fonction O(n²)
```cpp
void printPairs(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            std::cout << "(" << i << ", " << j << ")" << std::endl;
        }
    }
}
```

---

## Solution Exercice 5 : Implémentation et vérification pratique

### 1. Recherche linéaire
```cpp
int linearSearch(int arr[], int size, int key) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == key) {
            return i;
        }
    }
    return -1; // Élément non trouvé
}
```
**Complexité temporelle** : O(n)  
Chaque élément est parcouru une fois au maximum.

### 2. Recherche binaire
```cpp
int binarySearch(int arr[], int size, int key) {
    int left = 0, right = size - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == key) {
            return mid;
        } else if (arr[mid] < key) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    return -1; // Élément non trouvé
}
```
**Complexité temporelle** : O(log n)  
À chaque itération, la taille de la recherche est divisée par deux.

**Question bonus** : La recherche binaire a une complexité de **O(log n)** dans le pire des cas.
