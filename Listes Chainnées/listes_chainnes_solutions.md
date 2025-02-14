# Exercices sur les listes chaînées et doublement chaînées

## Listes chaînées

### Exercice 1 : Créer une classe Noeud

```CPP
class Noeud {
public:
    int valeur;
    Noeud* suivant;

    Noeud(int val) : valeur(val), suivant(nullptr) {}
};
```

### Exercice 3 : Créer une classe Liste

```CPP
class Liste {
private:
    Noeud* tete;
    Noeud* queue;

public:
    Liste() : tete(nullptr), queue(nullptr) {}

    ~Liste() {
        Noeud* courant = tete;
        while (courant) {
            Noeud* temp = courant;
            courant = courant->suivant;
            delete temp;
        }
    }
};
```

### Exercice 6 : Insertion d'un noeud au début

```CPP
void insererDebut(int val) {
    Noeud* nouveau = new Noeud(val);
    if (!tete) {
        tete = queue = nouveau;
    } else {
        nouveau->suivant = tete;
        tete = nouveau;
    }
}
```

### Exercice 7 : Insertion d'un noeud à la fin

```CPP
void insererFin(int val) {
    Noeud* nouveau = new Noeud(val);
    if (!queue) {
        tete = queue = nouveau;
    } else {
        queue->suivant = nouveau;
        queue = nouveau;
    }
}
```

### Exercice 8 : Affichage des éléments

```CPP
void afficher() {
    Noeud* courant = tete;
    while (courant) {
        std::cout << courant->valeur << " ";
        courant = courant->suivant;
    }
    std::cout << std::endl;
}
```

---

## Listes doublement chaînées

### Exercice 1 : Créer une classe NoeudDouble

```CPP
class NoeudDouble {
public:
    int valeur;
    NoeudDouble* precedent;
    NoeudDouble* suivant;

    NoeudDouble(int val) : valeur(val), precedent(nullptr), suivant(nullptr) {}
};
```

### Exercice 3 : Créer une classe ListeDouble

```CPP
class ListeDouble {
private:
    NoeudDouble* tete;
    NoeudDouble* queue;

public:
    ListeDouble() : tete(nullptr), queue(nullptr) {}

    ~ListeDouble() {
        NoeudDouble* courant = tete;
        while (courant) {
            NoeudDouble* temp = courant;
            courant = courant->suivant;
            delete temp;
        }
    }
};
```

### Exercice 6 : Insertion d'un noeud au début

```CPP
void insererDebut(int val) {
    NoeudDouble* nouveau = new NoeudDouble(val);
    if (!tete) {
        tete = queue = nouveau;
    } else {
        nouveau->suivant = tete;
        tete->precedent = nouveau;
        tete = nouveau;
    }
}
```

### Exercice 7 : Insertion d'un noeud à la fin

```CPP
void insererFin(int val) {
    NoeudDouble* nouveau = new NoeudDouble(val);
    if (!queue) {
        tete = queue = nouveau;
    } else {
        queue->suivant = nouveau;
        nouveau->precedent = queue;
        queue = nouveau;
    }
}
```

### Exercice 8 : Affichage des éléments

```CPP
void afficher() {
    NoeudDouble* courant = tete;
    while (courant) {
        std::cout << courant->valeur << " ";
        courant = courant->suivant;
    }
    std::cout << std::endl;
}
```