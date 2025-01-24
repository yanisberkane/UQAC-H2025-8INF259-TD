
# Exercices de TD : Notation Asymptotique et Complexité

## Exercice 1 : Identifier la complexité temporelle
Pour chaque fonction ci-dessous, déterminez la complexité temporelle en notation asymptotique **O()**.

### Fonctions :
1. ```cpp
   void example1(int n) {
       for (int i = 0; i < n; i++) {
           std::cout << i << std::endl;
       }
   }
   ```

2. ```cpp
   void example2(int n) {
       for (int i = 0; i < n; i++) {
           for (int j = 0; j < n; j++) {
               std::cout << i * j << std::endl;
           }
       }
   }
   ```

3. ```cpp
   void example3(int n) {
       int i = 1;
       while (i < n) {
           std::cout << i << std::endl;
           i *= 2;
       }
   }
   ```

4. ```cpp
   void example4(int n) {
       for (int i = 0; i < n; i++) {
           for (int j = i; j < n; j++) {
               std::cout << i + j << std::endl;
           }
       }
   }
   ```

## Exercice 2 : Comparer des fonctions
Classez les fonctions suivantes en fonction de leur complexité croissante (de la plus faible à la plus forte) :
1. O(n)
2. O(n log n)
3. O(1)
4. O(n^2)
5. O(log n)

### Exemple attendu :
Classement : O(1), O(log n), O(n), O(n log n), O(n^2)

## Exercice 3 : Analyse de complexité spatiale
Analysez la complexité spatiale des fonctions suivantes en fonction de leur utilisation mémoire.

### Fonctions :
1. ```cpp
   void example1(int n) {
       int arr[n];
       for (int i = 0; i < n; i++) {
           arr[i] = i;
       }
   }
   ```

2. ```cpp
   void example2(int n) {
       int x = 0;
       for (int i = 0; i < n; i++) {
           x += i;
       }
   }
   ```

3. ```cpp
   void example3(int n) {
       std::vector<int> vec;
       for (int i = 0; i < n; i++) {
           vec.push_back(i);
       }
   }
   ```

## Exercice 4 : Trouver une fonction équivalente
Pour chaque fonction de complexité ci-dessous, proposez une fonction avec une complexité asymptotique équivalente :
1. O(n)
2. O(log n)
3. O(n^2)

### Indice
Pensez à implémenter une boucle, une recherche binaire, ou des boucles imbriquées selon les besoins.

## Exercice 5 : Implémentation et vérification pratique
1. Implémentez une fonction de recherche linéaire dans un tableau, et analysez sa complexité temporelle.
2. Implémentez une fonction de recherche binaire dans un tableau trié, et analysez sa complexité temporelle.

### Exemple de tableau :
```cpp
int arr[] = {1, 3, 5, 7, 9, 11};
int n = sizeof(arr) / sizeof(arr[0]);
```

### Question bonus :
Quelle est la complexité de la recherche binaire dans le pire des cas ?

---

Ces exercices vous aideront à comprendre les bases de la notation asymptotique et à analyser les algorithmes en termes de complexité temporelle et spatiale. Si vous avez besoin d'autres exemples ou d'une aide supplémentaire, n'hésitez pas !
