# **Plan du Contenu :**

- ## **[Types de Données](#1-types-de-données)**
    - **[Types de Base](#types-de-base)**
    - **[Modificateurs de Type](#modificateurs-de-type)**
    - **[Classes de Stockage](#classes-de-stockage)**
    - **[Qualificateurs ](#qualificateurs)**

- ## **[Déclaration de Variables](#2-déclaration-de-variables)**

- ## **[Lecture et Écriture des données](#3-lecture-et-écriture-des-données)**
    - **[Affichage formaté avec `printf`](#affichage-formaté-avec-printf)**
    - **[Lecture formatée avec `scanf`](#lecture-formatée-avec-scanf)**

- ## **[Caractères d'Échappement](#4-caractères-déchappement)**

- ## **[Opérateurs](#5-opérateurs)**
    - **[Opérateurs Arithmétiques](#opérateurs-arithmétiques)**
    - **[Opérateurs de Comparaison](#opérateurs-de-comparaison-relationnels)**
    - **[Opérateurs Logiques](#opérateurs-logiques)**
    - **[Opérateurs d'Affectation](#opérateurs-daffectation)**
    - **[Opérateurs Bit à Bit](#opérateurs-bit-à-bit)**

- ## **[Structures Conditionnelles](#6-structures-conditionnelles)**
    - **[Condition Simple](#condition-simple)**
    - **[Alternative](#alternative)**
    - **[Imbriquée](#imbriquée)**
    - **[Choix Multiple](#choix-multiple)**

- ## **[Structures Répétitives](#7-structures-répétitives)**
    - **[Boucle `for`](#boucle-for)**
    - **[Boucle `while`](#boucle-while)**
    - **[Boucle `do`...`while`](#boucle-dowhile)**

- ## **[Contrôle des Boucles](#8-contrôle-des-boucles)**

- ## **[Tableaux](#9-tableaux)**
    - **[Déclaration d'une Tableau](#déclaration)**
    - **[Taille d'un Tableau](#taille-dun-tableau)**

- ## **[Chaînes de Caractères](#10-chaînes-de-caractères)**
    - **[Fonctions de Base](#1-types-de-données)**
    - **[Fonctions de Conversion](#1-types-de-données)**
    - **[Fonctions de Manipulation de Caractères](#1-types-de-données)**
    - **[Fonctions d'Entrée/Sortie](#1-types-de-données)**

- ## **[Fonctions](#11-fonctions)**
    - **[Déclaration](#déclaration-1)**

- ## **[Pointeurs](#12-pointeurs)**
    - **[Déclaration](#déclaration-2)**
    - **[Initialisation](#initialisation)**
    - **[Accès à la valeur pointée](#pointeur-et-tableaux)**
    - **[Pointeur et tableaux](#pointeur-et-tableaux)**
    - **[Pointeur de pointeur](#pointeur-de-pointeur)**
    - **[Pointeur et fonctions](#pointeur-et-fonctions)**
    - **[Pointeurs constants](#pointeurs-constants)**


- ### **[Allocation Dynamique de la Mémoire](#13-allocation-dynamique-de-la-mémoire)**
    - **[`malloc()` Allocation de mémoire brute](#malloc-allocation-de-mémoire-brute)**
    - **[`calloc()` Allocation avec initialisation à zéro](#calloc-allocation-avec-initialisation-à-zéro)**
    - **[`realloc()` Modification de la taille d'une allocation](#realloc-modification-de-la-taille-dune-allocation)**
    - **[`free()` Libération de la mémoire](#free-libération-de-la-mémoire)**

- ## **[Structures](#14-structures)**
    - **[Déclaration](#déclaration-3)**
    - **[Accès aux champs](#accès-aux-champs)**

- ## **[Unions](#15-unions)**
    - **[Déclaration](#déclaration-4)**
    - **[Tableau Comparatif](#tableau-comparatif-entre-les-unions-et-les-structures-en-c)**

- ## **[Énumérations](#16-énumérations)**
    - **[Déclaration Avec valeurs par défaut](#déclaration-avec-valeurs-par-défaut)**
    - **[Déclaration Avec valeurs personnalisées](#déclaration-avec-valeurs-personnalisées)**

- ## **[Types Synonymes](#17-types-synonymes)**

- ## **[Champs de Bits](#18-champs-de-bits)**

- ## **[Taille d'une Structure](#19-taille-dune-structure)**

- ## **[Gestion des Fichiers](#20-gestion-des-fichiers)**
    - **[Ouverture d’un fichier](#ouverture-dun-fichier)**
    - **[Modes d’ouverture](#modes-douverture)**
    - **[Vérification d’ouverture](#vérification-douverture)**
    - **[Fermeture d’un fichier](#fermeture-dun-fichier)**
    - **[Écriture](#écriture)**
    - **[Lecture](#lecture)**
    - **[Autres fonctions utiles](#autres-fonctions-utiles)**

- ## **[Programmation Modulaire](#21-programmation-modulaire)**
    - **[Fichier d'En-Tête (`*.h`)](#fichier-den-tête-h)**
    - **[Fichier Source (`*.c`)](#fichier-source-c)**
    - **[Fichier Principal (`main.c`)](#fichier-principal-mainc)**
    - **[Compilation avec plusieurs modules](#compilation-avec-plusieurs-modules)**
    - **[Compilation Directe](#compilation-directe)**
    - **[Directives Clés](#directives-clés)**

- ## **[Bibliothèques](#22-bibliothèques)**

---

<h3 align="center"><a href="https://github.com/t4lhawi/Programmation-Cpp" target="_blank">Lien de Programmation en Language C++</a></h3>

---

<h3 align="center"><a href="https://github.com/t4lhawi/Embedded-C" target="_blank">Programmation en C – Systèmes Embarqué</a></h3>


---

## **1. Types de Données**

- ### **Types de Base**
    | **Type**      | **Taille (en octets)** | **Description**                                                                  |
    | ------------- | ---------------------- | -------------------------------------------------------------------------------- |
    | `char`        | 1                      | Caractère (valeur ASCII), ou petit entier (-128 à 127 ou 0 à 255).               |
    | `bool`        | 1                      | Type booléen (`true` ou `false`), défini dans `<stdbool.h>`.                     |
    | `int`         | 4                      | Entier standard signé (-2³¹ à 2³¹−1 sur 32 bits).                                |
    | `float`       | 4                      | Nombre réel en précision simple (≈ 7 chiffres significatifs).                    |
    | `double`      | 8                      | Nombre réel en double précision (≈ 15 chiffres significatifs).                   |
    | `long double` | 8, 10 ou 16            | Nombre réel en précision étendue (dépend de l’implémentation).                   |
    | `void`        | —                      | Indique l’absence de type ou de valeur (utilisé pour les fonctions sans retour). |


- ### **Modificateurs de Type**
    Les **modificateurs** changent la taille ou le signe des types entiers et réels.
    
    | **Combinaison possible** | **Taille (octets)** | **Description**                         |
    | ------------------------ | ------------------- | --------------------------------------- |
    | `short int` / `short`    | 2                   | Entier court (–32 768 à 32 767).        |
    | `unsigned short int`     | 2                   | Entier court non signé (0 à 65 535).    |
    | `unsigned int`           | 4                   | Entier non signé (0 à 4 294 967 295).   |
    | `long int` / `long`      | 4 ou 8              | Entier long (dépend de l’architecture). |
    | `unsigned long int`      | 4 ou 8              | Entier long non signé.                  |
    | `long long int`          | 8                   | Entier très long (au moins ±9×10¹⁸).    |
    | `unsigned long long int` | 8                   | Entier très long non signé.             |
    | `signed char`            | 1                   | Caractère signé (–128 à 127).           |
    | `unsigned char`          | 1                   | Caractère non signé (0 à 255).          |

    > 💡 **Remarque**
    > Les tailles peuvent varier selon la machine et le compilateur (utiliser `sizeof(type)` pour vérifier).


- ### **Classes de Stockage**
    Les **classes de stockage** définissent la durée de vie et la portée (visibilité) des variables.
    
    | **Spécificateur** | **Description**                                                                        |
    | ----------------- | -------------------------------------------------------------------------------------- |
    | `auto`            | Valeur automatique (par défaut pour les variables locales).                            |
    | `static`          | Conserve la valeur de la variable entre plusieurs appels de fonction.                  |
    | `extern`          | Indique que la variable est définie dans un autre fichier.                             |
    | `register`        | Suggestion pour stocker la variable dans un registre (accès rapide, mais non garanti). |



- ### **Qualificateurs**
    Les **qualificateurs** modifient le comportement du compilateur vis-à-vis de la variable.
    
    | **Qualificateur** | **Description**                                                                              |
    | ----------------- | -------------------------------------------------------------------------------------------- |
    | `const`           | Variable non modifiable (lecture seule).                                                     |
    | `volatile`        | Empêche les optimisations sur la variable (utile pour registres matériels ou interruptions). |
    | `restrict`        | (C99) Indique que le pointeur est la seule référence à la donnée qu’il pointe.               |


- **Déterminer l'Intervalle des Types de Données**
    - **Pour les types signés**
       - L'intervalle est de $`-2^{n-1}`$ à $`2^{n-1} - 1`$, où $`n`$ est le nombre de bits utilisés pour le type.
    
    - **Pour les types non signés**
       - L'intervalle est de $`0`$ à $`2^n - 1`$, où $`n`$ est le nombre de bits utilisés pour le type.

---

## **2. Déclaration de Variables**
```c
Type Nom_var = valeur;
const Type Nom_const = valeur;
```
---

## **3. Lecture et Écriture des données**

- ### **Affichage formaté avec `printf`**

    ```c
    %[flags][largeur][.précision][modificateur]spécificateur
    ```

    - **`flags`** (optionnel) Contrôle l'alignement, le remplissage, etc.
      - `-` Alignement à gauche.
      - `0` Remplissage avec des zéros.
      - `+` Affiche le signe (+ ou -) pour les nombres.
      - ` ` (espace) Ajoute un espace pour les nombres positifs.
      - `#` Format alternatif (ex: `0x` pour les hexadécimaux).
    
    - **`largeur`** (optionnel) Nombre minimal de caractères à afficher.
      - Exemple `%5d` → Affiche un entier avec une largeur minimale de 5.
    
    - **`.précision`** (optionnel) Nombre de chiffres après la virgule pour les flottants, ou nombre maximal de caractères pour les chaînes.
      - Exemple `%.2f` → Affiche un flottant avec 2 chiffres après la virgule.
      - Exemple `%.5s` → Affiche uniquement les 5 premiers caractères d'une chaîne.
    
    - **`modificateur`** (optionnel) Modifie la taille du type de donnée.
      - `h` `short` (ex: `%hd` pour un `short int`).
      - `l` `long` (ex: `%ld` pour un `long int`).
      - `ll` `long long` (ex: `%lld` pour un `long long int`).
      - `L` `long double` (ex: `%Lf` pour un `long double`).
    
    - **`spécificateur`** Détermine le type de donnée.
      - `d` ou `i` Entier signé.
      - `u` Entier non signé.
      - `f` Flottant.
      - `c` Caractère.
      - `s` Chaîne de caractères.
      - `p` Pointeur.
      - `%` Affiche le caractère `%`.
      
    
        | **Caractère** | **Type de donnée**               | **Exemple**                              |
        |---------------|----------------------------------|------------------------------------------|
        | **%d**        | Entier signé (int)               | `printf("%d", 42);` → `42`               |
        | **%f**        | Nombre à virgule flottante       | `printf("%.2f", 3.14);` → `3.14`         |
        | **%c**        | Caractère (char)                 | `printf("%c", 'A');` → `A`               |
        | **%s**        | Chaîne de caractères (char *)    | `printf("%s", "Hello");` → `Hello`       |
        | **%p**        | Adresse mémoire (pointeur)       | `printf("%p", &x);` → `0x7ffdfb2c`       |
        | **%%**        | Affiche le caractère `%`         | `printf("%%");` → `%`                    |


- ### **Lecture formatée avec `scanf`**

    ```c
    %[*][largeur][modificateur]spécificateur
    ```

    - **`*`** (optionnel) Ignore la donnée lue (ne la stocke pas).
    - **`largeur`** (optionnel) Nombre maximal de caractères à lire.
    - **`modificateur`** (optionnel) Modifie la taille du type de donnée (comme pour `printf`).
    - **`spécificateur`** Détermine le type de donnée (comme pour `printf`).

        | **Caractère** | **Type de donnée**               | **Exemple**                              |
        |---------------|----------------------------------|------------------------------------------|
        | **%d**        | Entier signé (int)               | `scanf("%d", &x);` (lit un entier)       |
        | **%f**        | Nombre à virgule flottante       | `scanf("%f", &y);` (lit un float)        |
        | **%c**        | Caractère (char)                 | `scanf("%c", &c);` (lit un caractère)    |
        | **%s**        | Chaîne de caractères (char *)    | `scanf("%s", str);` (lit une chaîne)     |
        | **%p**        | Adresse mémoire (pointeur)       | `scanf("%p", &ptr);` (lit un pointeur)   |


---

## **4. Caractères d'Échappement**

| **Séquence** | **Description**                                   | **Valeur ASCII** |
|--------------|---------------------------------------------------|------------------|
| `\0`         | Caractère nul (fin de chaîne)                     | 0                |
| `\a`         | Alarme (bip sonore)                               | 7                |
| `\b`         | Backspace (retour arrière)                        | 8                |
| `\t`         | Tabulation horizontale                            | 9                |
| `\n`         | Nouvelle ligne (line feed)                        | 10               |
| `\v`         | Tabulation verticale                              | 11               |
| `\f`         | Saut de page (form feed)                          | 12               |
| `\r`         | Retour chariot (carriage return)                  | 13               |
| `\"`         | Guillemet double                                  | 34               |
| `\'`         | Apostrophe                                        | 39               |
| `\\`         | Barre oblique inversée                            | 92               |
| `\?`         | Point d'interrogation (utilisé dans les trigraphes)| 63               |
| `\xhh`       | Caractère représenté par sa valeur hexadécimale   | Dépend de `hh`   |
| `\ooo`       | Caractère représenté par sa valeur octale         | Dépend de `ooo`  |

---

## **5. Opérateurs**

- ### **Opérateurs Arithmétiques**

    | **Opérateur** | **Description**                     | **Exemple**         |
    |---------------|-------------------------------------|---------------------|
    | `+`           | Addition                            | `a + b`             |
    | `-`           | Soustraction                        | `a - b`             |
    | `*`           | Multiplication                      | `a * b`             |
    | `/`           | Division                            | `a / b`             |
    | `%`           | Modulo (reste de la division)       | `a % b`             |
    | `++`          | Incrémentation (ajoute 1)           | `a++` ou `++a`      |
    | `--`          | Décrémentation (soustrait 1)        | `a--` ou `--a`      |


- ### **Opérateurs de Comparaison (Relationnels)**
    
    | **Opérateur** | **Description**                     | **Exemple**         |
    |---------------|-------------------------------------|---------------------|
    | `==`          | Égal à                              | `a == b`            |
    | `!=`          | Différent de                        | `a != b`            |
    | `>`           | Supérieur à                         | `a > b`             |
    | `<`           | Inférieur à                         | `a < b`             |
    | `>=`          | Supérieur ou égal à                 | `a >= b`            |
    | `<=`          | Inférieur ou égal à                 | `a <= b`            |


- ### **Opérateurs Logiques**

    | **Opérateur** | **Description**                     | **Exemple**         |
    |---------------|-------------------------------------|---------------------|
    | `&&`          | ET logique                          | `a && b`            |
    | `\|\|`        | OU logique                          | `a \|\| b`          |
    | `!`           | NON logique (inverse)               | `!a`                |


- ### **Opérateurs d'Affectation**

    | **Opérateur** | **Description**                     | **Exemple**         |
    |---------------|-------------------------------------|---------------------|
    | `=`           | Affectation simple                  | `a = b`             |
    | `+=`          | Ajoute et affecte                   | `a += b` (équivaut à `a = a + b`) |
    | `-=`          | Soustrait et affecte                | `a -= b` (équivaut à `a = a - b`) |
    | `*=`          | Multiplie et affecte                | `a *= b` (équivaut à `a = a * b`) |
    | `/=`          | Divise et affecte                   | `a /= b` (équivaut à `a = a / b`) |
    | `%=`          | Modulo et affecte                   | `a %= b` (équivaut à `a = a % b`) |
    | `&=`          | ET binaire et affecte               | `a &= b` (équivaut à `a = a & b`) |
    | `^=`          | OU exclusif binaire et affecte      | `a ^= b` (équivaut à `a = a ^ b`) |
    | `>>=`         | Décalage à droite et affecte        | `a >>= b` (équivaut à `a = a >> b`)| 
    | `<<=`         | Décalage à gauche et affecte        | `a <<= b` (équivaut à `a = a << b`) |


- ### **Opérateurs Bit à Bit**

    | **Opérateur** | **Description**                          | **Exemple** |
    | ------------- | ---------------------------------------- | ----------- |
    | `&`           | ET binaire                               | `a & b`     |
    | `^`           | OU exclusif (XOR) binaire                | `a ^ b`     |
    | `~`           | NON binaire (inversion de tous les bits) | `~a`        |
    | `<<`          | Décalage des bits à gauche               | `a << 2`    |
    | `>>`          | Décalage des bits à droite               | `a >> 2`    |


---

## **6. Structures Conditionnelles**

- ### Condition Simple 
    ```c
    if (condition) {
        instructions;
    }
    ```

- ### Alternative
    ```c
    if (condition) {
        instructions;
    } else {
        instructions;
    }
    ```

- ### Imbriquée
    ```c
    if (condition1) {
        instructions;
    } else if (condition2) {
        instructions;
    } else {
        instructions;
    }
    ```

- ### Choix Multiple
    ```c
    switch(expression) {
        case valeur1:
            instructions;
            break;
        case valeur2:
            instructions;
            break;
        default:
            instructions;
            break;
    }
    ```

---

## **7. Structures Répétitives**
- ### Boucle for
    ```c
    for (initialisation; condition; incrément) {
        instructions;
    }
    ```

- ### Boucle while
    ```c
    while (condition) {
        instructions;
    }
    ```

- ### Boucle do...while
    ```c
    do {
        instructions;
    } while (condition);
    ```
---

## **8. Contrôle des Boucles**
```c
// break interrompt immédiatement la boucle
break;

// continue passe à l'itération suivante
continue;

// goto transfère l'exécution vers une étiquette définie dans le programme
goto;
```

---

## **9. Tableaux**
- ### **Déclaration**
    ```c
    // Tableau à une dimension
    Type Nom_Tab[taille];
    
    // Tableau à deux dimensions
    Type Nom_Tab[nbr_lignes][nbr_colonnes];
    ```
- ### **Taille d'un Tableau**
    ```c
    // Tableau à une dimension
    int taille = sizeof(Nom_Tab) / sizeof(Nom_Tab[0]);
    
    // Tableau à deux dimensions
    int nbr_lignes = sizeof(Nom_Tab) / sizeof(Nom_Tab[0]);
    int nbr_colonnes = sizeof(Nom_Tab[0]) / sizeof(Nom_Tab[0][0]); 
    ```

---


## **10. Chaînes de Caractères**

- ### **Fonctions de Base (`<string.h>`)**

    | **Fonction** | **Syntaxe**              | **Description**                          |
    |--------------|--------------------------|------------------------------------------|
    | **`strlen`** | `strlen(str);`           | Longueur de `str` (sans `\0`).           |
    | **`strcpy`** | `strcpy(dest, src);`     | Copie `src` dans `dest`.                 |
    | **`strncpy`**| `strncpy(dest, src, n);` | Copie `n` caractères de `src` dans `dest`.|
    | **`strcat`** | `strcat(dest, src);`     | Ajoute `src` à la fin de `dest`.         |
    | **`strncat`**| `strncat(dest, src, n);` | Ajoute `n` caractères de `src` à `dest`. |
    | **`strcmp`** | `strcmp(str1, str2);`    | Compare `str1` et `str2` (0 si égales).  |
    | **`strncmp`**| `strncmp(str1, str2, n);`| Compare `n` caractères de `str1` et `str2`. |



- ### **Fonctions de Conversion (`<stdlib.h>`)**

    | **Fonction** | **Syntaxe**              | **Description**                          |
    |--------------|--------------------------|------------------------------------------|
    | **`atoi`**   | `atoi(str);`             | Convertit `str` en entier (`int`).       |
    | **`atol`**   | `atol(str);`             | Convertit `str` en entier long (`long`). |
    | **`atof`**   | `atof(str);`             | Convertit `str` en flottant (`double`).  |



- ### **Fonctions de Manipulation de Caractères (`<ctype.h>`)**

    | **Fonction** | **Syntaxe**              | **Description**                          |
    |--------------|--------------------------|------------------------------------------|
    | **`isalpha`**| `isalpha(c);`            | Vérifie si `c` est une lettre (A-Z, a-z).|
    | **`isdigit`**| `isdigit(c);`            | Vérifie si `c` est un chiffre (0-9).     |
    | **`isalnum`**| `isalnum(c);`            | Vérifie si `c` est une lettre ou un chiffre. |
    | **`islower`**| `islower(c);`            | Vérifie si `c` est une minuscule.        |
    | **`isupper`**| `isupper(c);`            | Vérifie si `c` est une majuscule.        |
    | **`tolower`**| `tolower(c);`            | Convertit `c` en minuscule.              |
    | **`toupper`**| `toupper(c);`            | Convertit `c` en majuscule.              |



- ### **Fonctions d'Entrée/Sortie (`<stdio.h>`)**

    | **Fonction** | **Syntaxe**              | **Description**                          |
    |--------------|--------------------------|------------------------------------------|
    | **`fgets`**  | `fgets(str, n, stream);` | Lit une ligne de `stream` dans `str` (max `n` caractères). |
    | **`fputs`**  | `fputs(str, stream);`    | Écrit `str` dans `stream`.               |

---

## **11. Fonctions**
- ### **Déclaration**
```c
Type_retour nom_fonction(Type param1, Type param2) {
    // Code
    return valeur;
}
```
---

## **12. Pointeurs**

- ### **Déclaration**
    ```c
    type *ptr;
    ```

- ### **Initialisation**
    ```c
    ptr = &variable;
    ```


- ### **Accès à la valeur pointée**
    ```c
    *ptr;
    ```

- ### **Pointeur et tableaux**
    ```c
    ptr = tableau;
    ptr[i];   // ou *(ptr + i)
    ```

- ### **Pointeur de pointeur**
    ```c
    type **ptr;
    ```

- ### **Pointeur et fonctions**
    ```c
    void fonction(type *parametre) {
        // modification via *parametre
    }
    // Appel
    fonction(&variable);
    ```


- ### **Pointeurs constants**

    - `const type *ptr`
    
        - **Valeur pointée constante** (lecture seule)
        - L’adresse peut changer    
        - ```c
            *ptr = val;   // ❌ interdit
            ptr = autre;  // ✅ autorisé
            ```
    
    - `type *const ptr`
    
        - **Adresse constante**
        - La valeur pointée est modifiable
        - ```c
            *ptr = val;   // ✅ autorisé
            ptr = autre;  // ❌ interdit
            ```
    
    - `const type *const ptr`
        
        - **Adresse et valeur pointée constantes**
        - ```c
            *ptr = val;   // ❌ interdit
            ptr = autre;  // ❌ interdit
            ```

    > **Astuce** lire **de droite à gauche** pour savoir ce qui est constant.

---

## **13. Allocation Dynamique de la Mémoire**
- ### `malloc()` Allocation de mémoire brute
    ```c
    // Alloue de la mémoire non initialisée
    Type *pointeur = malloc(taille * sizeof(Type));
    ```

- ### `calloc()` Allocation avec initialisation à zéro
    ```c
    // Alloue et initialise la mémoire à 0
    Type *pointeur = calloc(nbr_elements, sizeof(Type));
    ```

- ### `realloc()` Modification de la taille d'une allocation
    ```c
    // Redimensionne une zone mémoire allouée
    pointeur = realloc(pointeur, nouvelle_taille * sizeof(Type));
    ```

- ### `free()` Libération de la mémoire
    ```c
    // Libère la mémoire allouée
    free(pointeur);
    ```
---

## **14. Structures**
- ### Déclaration
   ```c
   struct nom_structure {
       type1 champ1;
       type2 champ2;
   } variables;
   ```

- ### Accès aux champs
     ```c
     variable.champ;  // Accès direct
     pointeur->champ; // Accès via pointeur
     ```
---

## **15. Unions**
- ### Déclaration
   ```c
   union nom_union {
       type1 champ1;
       type2 champ2;
   } variables;
   ```

- ### **Tableau Comparatif** entre les **unions** et les **structures** en C

    | **Caractéristique**         | **Structure (`struct`)**                          | **Union (`union`)**                        |
    |-----------------------------|--------------------------------------------------|--------------------------------------------|
    | **Déclaration**             | `struct nom { type1 champ1; type2 champ2; ... };`| `union nom { type1 champ1; type2 champ2; ... };` |
    | **Taille en mémoire**       | Somme des tailles de tous les champs.            | Taille du plus grand champ.                |
    | **Utilisation de la mémoire**| Chaque champ a son propre espace mémoire.        | Tous les champs partagent le même espace mémoire. |
    | **Accès aux champs**        | Tous les champs sont accessibles simultanément.  | Un seul champ peut être utilisé à la fois. |
    | **Initialisation**          | Tous les champs peuvent être initialisés.        | Seul le premier champ peut être initialisé.|
    | **Utilisation typique**     | Représenter un objet avec plusieurs attributs.    | Représenter un type pouvant stocker un seul type de données à la fois. |


---

## **16. Énumérations**
- ### Déclaration Avec valeurs par défaut
   ```c
   enum nom_enum {
       CONST1,
       CONST2,
       ...
   } variables;
   ```

- ### Déclaration Avec valeurs personnalisées
     ```c
     enum nom_enum {
         CONST1 = valeur1,
         CONST2 = valeur2,
         ...
     } variables;
     ```
---

## **17. Types Synonymes**
   ```c
   typedef type_existant nouveau_nom;
   ```

  - **Exemples**
    ```c
    typedef int Entier;       // Entier est un synonyme de int
    typedef float Reel;       // Reel est un synonyme de float
    typedef char Caractere;   // Caractere est un synonyme de char
    ```

---

## **18. Champs de Bits**
   ```c
   struct {
       unsigned int champ1 nombre_de_bits;
       unsigned int champ2 nombre_de_bits;
   } variables;
   ```

---

## **19. Taille d'une Structure**
   ```c
   struct nom_structure {
        type1 champ1;
        type2 champ2;
    } variables;

    printf("Taille de la structure %zu octets\n", sizeof(variable));
   ```
---

## **20. Gestion des Fichiers**
La gestion des fichiers permet de lire, écrire, créer ou modifier des fichiers sur le disque en utilisant les fonctions de la bibliothèque standard `<stdio.h>`.

- ### **Ouverture d’un fichier**
    ```c
    FILE* fichier = fopen("nom_fichier.txt", "mode");
    ```

- ### **Modes d’ouverture**
    | Mode  | Description                        |
    |-------|------------------------------------|
    | `"r"` | Lecture (fichier existant)         |
    | `"w"` | Écriture (crée ou écrase)          |
    | `"a"` | Ajout (écriture en fin de fichier) |
    | `"r+"`| Lecture + écriture                 |
    | `"w+"`| Lecture + écriture (efface)        |
    | `"a+"`| Lecture + ajout                    |


- ### **Vérification d’ouverture**
    ```c
    if (fichier == NULL) {
        printf("Erreur lors de l’ouverture du fichier.\n");
    }
    ```
    > Toujours vérifier si le fichier a été ouvert correctement

- ### **Fermeture d’un fichier**
    ```c
    fclose(fichier);
    ```

- ### **Écriture**
    ```c
    fprintf(fichier, "Texte %d\n", valeur);
    fputc('A', fichier);
    fputs("Chaîne", fichier);
    ```

- ### **Lecture**
    ```c
    fscanf(fichier, "%d", &valeur);
    fgetc(fichier);
    fgets(chaine, taille, fichier);
    ```


- ### **Autres fonctions utiles**

    | Fonction        | Utilité                                |
    |----------------|-----------------------------------------|
    | `feof(f)`       | Teste la fin de fichier                 |
    | `ferror(f)`     | Vérifie les erreurs                     |
    | `rewind(f)`     | Remet le curseur au début               |
    | `fflush(f)`     | Vide le tampon du fichier               |
    | `remove("nom")` | Supprime un fichier                     |
    | `rename(old,new)`| Renomme un fichier                     |

---

## **21. Programmation Modulaire**  

- ### **Fichier d'En-Tête (`*.h`)**
    ```c
    #ifndef MODULE1_H  // Garde contre les inclusions multiples
    #define MODULE1_H
    
    // Déclarations (fonctions, constantes, types) pour module1
    
    #endif
    ```

    ```c
    #ifndef MODULE2_H
    #define MODULE2_H
    
    // Déclarations (fonctions, constantes, types) pour module2
    
    #endif
    ```

  > - Un fichier `.h` par module `module1.h`, `module2.h`
  > - Chaque fichier utilise ses propres gardes (`#ifndef MODULE1_H`, etc.)

- ### **Fichier Source (`*.c`)**
    ```c
    #include "module1.h"  // Inclusion du fichier d'en-tête correspondant
    
    // Implémentations des fonctions du module1
    ```

    ```c
    #include "module2.h"  // Inclusion du fichier d'en-tête correspondant
    
    // Implémentations des fonctions du module2
    ```

  > - Un fichier `.c` pour chaque module `module1.c`, `module2.c`
  > - Ne jamais inclure un fichier `.c` dans un autre fichier `.c`

- ### **Fichier Principal (`main.c`)**
    ```c
    #include "module1.h"
    #include "module2.h"
    
    int main() {
      // Appels aux fonctions de module1 et module2
    }
    ```

- ### **Compilation avec plusieurs modules**
    ```bash
    gcc -c module1.c -o module1.o
    gcc -c module2.c -o module2.o
    gcc -c main.c -o main.o
    gcc main.o module1.o module2.o -o programme
    ```

  > - Compilation séparée des modules (`.c → .o`)
  > - Édition de lien finale avec tous les objets (`.o`)

- ### **Compilation Directe**
    ```bash
    gcc main.c module1.c module2.c -o programme
    ```
    
    > - Compile les trois fichiers `.c` directement sans générer de `.o` intermédiaires,


- ### **Directives Clés**
  - `#include "fichier.h"` Inclusion locale (dans le projet)
  - `#include <fichier.h>` Inclusion système (ex. `<stdio.h>`)
  - `#ifndef` / `#define` / `#endif` Protection contre les inclusions multiples

---

## **22. Bibliothèques**
Les bibliothèques standard du C fournissent des fonctions pour de nombreuses tâches courantes.

- **`<stdio.h>`** Entrée/sortie standard.
  - Fonctions `printf`, `scanf`, `fopen`, `fclose`, etc.

- **`<stdlib.h>`** Gestion de la mémoire, nombres aléatoires et conversions.
  - Fonctions `malloc`, `free`, `rand`, `exit`, etc.

- **`<string.h>`** Manipulation des chaînes de caractères.
  - Fonctions `strlen`, `strcpy`, `strcat`, `strcmp`, etc.

- **`<math.h>`** Opérations mathématiques avancées.
  - Fonctions `pow`, `sqrt`, `sin`, `cos`, `log`, etc.

- **`<ctype.h>`** Classification et manipulation des caractères.
  - Fonctions `isalpha`, `isdigit`, `toupper`, `tolower`, etc.

- **`<time.h>`** Gestion du temps et des dates.
  - Fonctions `time`, `clock`, `difftime`, `strftime`, etc.

- **`<stdbool.h>`** Type booléen (`true`, `false`).

- **`<limits.h>`** et **`<float.h>`** Définit les limites des types numériques.

---

<h3 align="center"> 🧑🏻‍💻 | Made By <a href="https://github.com/t4lhawi" target="_blank">Mohamed Talhaoui</a></h3>
