Bien sûr ! Voici la fiche de révision mise à jour, incluant une section sur la détermination de la complexité à la main.

---

## **Fiche de Révision : Complexité d'un Algorithme**

### 1. **Définition de la Complexité d'un Algorithme**
   - La **complexité d'un algorithme** mesure les ressources nécessaires pour exécuter cet algorithme en fonction de la taille de l'entrée (généralement notée `n`).
   - Deux types principaux :
     - **Complexité temporelle** : mesure le temps d'exécution.
     - **Complexité spatiale** : mesure la quantité de mémoire nécessaire.

### 2. **Notations de la Complexité**
   - **O (Notation de Landau)** : décrit la limite supérieure de la croissance de la complexité pour le pire des cas.
     - **Ω (Omega)** : limite inférieure (meilleur des cas).
     - **Θ (Theta)** : encadrement des bornes supérieure et inférieure (cas moyen).

### 3. **Principaux Ordres de Complexité Temporelle**
   | Notation | Nom                  | Description |
   |----------|-----------------------|-------------|
   | **O(1)** | Constante             | Temps constant, ne dépend pas de la taille de l'entrée. |
   | **O(log n)** | Logarithmique     | Croît lentement avec `n` (ex. recherche binaire). |
   | **O(n)** | Linéaire              | Proportionnelle à la taille de l'entrée. |
   | **O(n log n)** | Quasi-linéaire  | Exemple : tri efficace (ex. Merge Sort). |
   | **O(n^2)** | Quadratique         | Double boucle imbriquée (ex. tri par sélection). |
   | **O(2^n)** | Exponentielle       | Croissance rapide (ex. backtracking). |
   | **O(n!)** | Factorielle          | Croissance extrêmement rapide (ex. permutation complète). |

### 4. **Étapes pour Analyser la Complexité**
   - **Identifier les boucles** :
     - Une boucle simple `for` est souvent de complexité linéaire **O(n)**.
     - Des boucles imbriquées donnent souvent des complexités quadratiques **O(n²)** ou plus.
   - **Récurrence dans les appels récursifs** :
     - Par exemple, un appel récursif divisé en deux parties, comme dans la recherche binaire, est **O(log n)**.
   - **Analyser les instructions dans les boucles et appels récursifs** :
     - Étudiez les flux de contrôle (conditions, branchements) pour en évaluer l’impact.
   - **Éliminer les termes non-dominants et les constantes** :
     - Ne conservez que le terme de plus haut ordre (ex. O(n²) + O(n) ≈ O(n²)).

### 5. **Exemples de Complexité**
   - **Recherche linéaire** : O(n)
   - **Recherche binaire** : O(log n)
   - **Tri par sélection ou insertion** : O(n²)
   - **Tri fusion (Merge Sort)** : O(n log n)
   - **Problèmes de permutation** (ex. solution exhaustive) : O(n!)

### 6. **Déterminer la Complexité d'un Algorithme à la Main**
   - **1. Analyser les Boucles**
     - Une boucle qui parcourt `n` éléments a généralement une complexité **O(n)**.
     - **Boucles Imbriquées** : multiplient la complexité (ex. boucle imbriquée double : **O(n²)**).
     - **Boucles logarithmiques** : Si une boucle divise la taille de l'itération (ex. `i *= 2`), cela donne **O(log n)**.
   
   - **2. Évaluer les Conditions**
     - Les branches conditionnelles n’affectent pas toujours la complexité globale, sauf si elles contiennent des boucles ou appels récursifs.
     - Analysez chaque branche et gardez la complexité de la branche la plus coûteuse pour le pire des cas.

   - **3. Analyser les Appels Récursifs**
     - Utilisez une **relation de récurrence** pour modéliser la complexité (ex. **O(2^n)** pour une fonction qui appelle deux fois elle-même avec `n-1`).
     - Pour les algorithmes **"diviser pour régner"** (ex. recherche binaire), la complexité est souvent **O(log n)**.

   - **4. Additionner les Complexités**
     - Pour les sections d’un algorithme exécutées **séquentiellement**, additionnez leurs complexités. 
     - Retenez uniquement le terme de plus haute complexité, car il domine asymptotiquement (ex. **O(n) + O(n²) ≈ O(n²)**).

### 7. **Optimisation et Bonnes Pratiques**
   - **Choix des structures de données** : Optimiser la complexité en sélectionnant des structures adaptées (ex. table de hachage pour une recherche rapide).
   - **Réduire les redondances** : Utiliser des techniques de mémorisation en récursivité.
   - **Éviter les boucles inutiles** : Minimiser les boucles imbriquées.
   - **Utiliser des algorithmes efficaces** : Choisir des algorithmes plus performants pour de grandes entrées.

### 8. **Notions Avancées : Complexité Amortie et Moyenne**
   - **Complexité amortie** : Évaluation moyenne des opérations pour des algorithmes avec des coûts variables.
   - **Complexité moyenne** : Performances moyennes pour un ensemble typique d’entrées.

---

Cette fiche de révision vous aidera à comprendre les bases de la complexité des algorithmes et à analyser la complexité à la main pour optimiser votre code.