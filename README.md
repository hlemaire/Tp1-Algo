### Échelle de difficulté

1. x - trivial (0.4 point).
2. x x - facile (0.8 point).
3. x x x - moyen (1.2 point).
4. x x x x - difficile (1.6 point).
5. x x x x x - challenge (2 points).

---

### Récapitulatif

* Max 8 exercices
* Actuel 8 exo = 9.6p
* 1 de x x - facile (0.8 point).
* 6 de x x x - moyen (1.2 point).
* 1 de x x x x - difficile (1.6 point).

---

## Exercice 1 (x x x Échanger le contenu de deux variables). = 1.2p

1.  Dérouler l’algorithme 2.6.1

    ```
      0 |  a  |  b  |
      1 |  1  |  2  |
      2 |  2  |  |  |
      3 |  |  |  2  |
    ```

    Résultat a = 2 et b = 2 donc la valeur de a n'existe plus.

2.  Expliquer ce qui semble bloquant et pourquoi la solution proposée par Bob pourrait fonctionner

    Le problème dans cette algorithme est que la valeur de b viens écrasé la valeur de a donc les deux variables finissent avec la valeur de b.

3.  Écrire l’algorithme qui implémente la solution proposée par Bob.

    ```
    1 données : "←"
       entrée : a : nombre
       entrée : b : nombre
       sortie : c : nombre
    2 début
       c ← a
       a ← b
       b ← c
       affiche("Vos nombres sont :", a, " et ", b)
    3 fin
    ```

---

## Exercice 2 (x x Moyenne de 4 nombres). = 0.8p

1.  Écrire un algorithme qui calcule en sortie la moyenne de 4 nombres en entrée.

    ```
    1 données : "←"
        1 | entrée : a : nombre
        2 | entrée : b : nombre
        3 | entrée : c : nombre
        4 | entrée : d : nombre
        5 | entrée : x : nombre
        6 | sortie : x : nombre
    2 début
        1 | x ← a + b + c + d
        2 | x ← x / 4
    3 fin
    ```

---

## Exercice 4 (x x x Division euclidienne sans modulo). = 1.2p

1.  Bob a vu dans certains pseudo-codes l’utilisation d’opérateurs `div` et `mod`... Proposer à Bob des instructions qui calculent le quotient et le reste d’une division euclidienne.

    ```
    1 données : "←"
        1 | entrée : a : entier
        2 | entrée : b : entier
        3 | sortie : q : entier
        4 | sortie : r : entier
    2 début :
        q ← ⌊ a ÷ b ⌋
        r ← a - (b × q)
        affiche("le quotient est", q,"et le reste est", r)
    3 fin
    ```

---

## Exercice 5 (x x x Déroulement d’un pseudo-code). = 1.2p

1.  Alice aimerait que vous dérouliez l’algorithme pour les entrées 11 et 5...

    ```
      0  |  a  |  b  |  c  |
      1  | 11  |  5  |  |  |
      2  |  |  |  |  | 11  |
      3  | 27  |  |  |  |  |
      4  |  |  | 11  |  |  |
    ```

---

## Exercice 6 (x x x Écriture depuis énoncé en français). = 1.2p

1.  Charlie vend des pièces imprimées en 3D... Bob aimerait que vous lui proposiez un programme qui calcule le prix de chaque article après cette augmentation.

    ```
    1 données : "←"
    	1 | entrée : prix : nombre
    2 début :
    	1 | prix ← prix * 1.15
        2 | affiche(prix"€ après augmentation")
    3 fin
    ```

---

## Exercice 9 (x x x x Calculer l’amende d’un excès de vitesse). = 1.6p

1.  Un étudiant révise le code de la route... Proposer un pseudo-code qui demande vitesse et limitation à un utilisateur puis calcule si l’utilisateur risque une amende et un retrait de points.

    ```
    1 données : "←"
       1 |entrée : vitesse : nombre
       2 |entrée : limitation : nombre
       3 |sortie : amende : nombre
       4 |sortie : points : nombre
    2 variables :
       1 | exces : nombre
    3 début
       1 | exces ← vitesse - limitation
       2 | si exces < 0 alors
       3 |   affiche("Pas d'excès de vitesse")
       4 | sinon si exces < 5 alors
       5 |   amende ← 0
       6 |   points ← 0
       7 |   affiche("Amende possible mais aucun retrait de points")
       8 | sinon si exces >= 5 /\ exces < 20 alors
       9 |   si limitation > 50 alors
      10 |     amende ← 68
      11 |     points ← 1
      12 |   sinon
      13 |     amende ← 135
      14 |     points ← 1
      15 |   affiche("Amende de", amende," et perte de", points,"points")
      16 | sinon si exces >= 20 /\ exces < 30 alors
      17 |   amende ← 135
      18 |   points ← 2
      19 |   affiche("Amende de", amende," et perte de", points,"points")
      20 | sinon si exces >= 30 /\ exces < 40 alors
      21 |   amende ← 135
      22 |   points ← 3
      23 |   affiche("Amende de", amende," et perte de", points,"points")
      24 | sinon si exces >= 40 /\ exces < 50 alors
      25 |   amende ← 135
      26 |   points ← 4
      27 |   affiche("Amende de", amende," et perte de", points,"points")
      28 | sinon si exces >= 50 alors
      29 |   amende ← 1500
      30 |   points ← 6
      31 |   affiche("Amende de", amende," et perte de", points,"points")
    4 fin
    ```

---

## Exercice 10 (x x x Déterminer une catégorie d’âge). = 1.2p

1. Écrire un pseudo-code qui demande son âge à l’utilisateur puis lui affiche la catégorie des groupes établis selon le cycle de vie correspondante :
   *  Enfant : moins de 14 ans.
   *  Adolescent : de 15 à 24 ans.
   *  Adulte : de 25 à 64 ans.
   *  Aîné : plus de 65 ans.

    ```
    1 données:
        1 | entrée : age : entier
        2 | entrée : categorie : char1
    2 début:
        1 | si age < 0 \/ age > 150 alors
        2 |     affiche("Vous n'avez pas saisi un âge correct.")
        3 | sinon si age < 14 alors
        4 |     categorie ← "Enfant"
        5 | sinon si age <= 24 alors
        6 |     categorie ← "Adolescent"
        7 | sinon si age <= 64 alors
        8 |     categorie ← "Adulte"
        9 | sinon
       10 |     categorie ← "Aîné"
       11 | affiche("vous êtes :",categorie)
    3 fin
    ```
---

## Exercice 12 (x x x Mot de passe). = 1.2p

1.  Écrire un pseudo-code qui prend deux entiers en entrée et renvoie en sortie s’ils correspondent à l’une des combinaisons (premier, second) suivantes :
    * (1234, 42)
    * (1337, 1235)

    ```
    1 données : "←"
    	1 | entrée : premier : entier
    	2 | entrée : seconde : entier
    2 début :
    	1 | si premier = 1234 /\ seconde = 42 \/ premier = 1337 /\ seconde = 1235 alors
    	2 | 	affiche("gg!")
    	3 | sinon
    	4 | 	affiche("faux")
    3 fin
    ```

*Pour ce pseudo code j'ai affiché directement mais sinon j'aurais fait une sortie et au lieu de affiche("gg!") j'aurais fait resultat ← 1 si c'est vrai et resultat ← 0 si faux.*




