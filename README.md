# Braille
Le braille est un système d'écriture utilisé pour lire au toucher plutôt qu'à la vue. 
Chaque caractère est composé de 6 points dans une grille 2x3, où chaque point peut soit être une bosse, soit être plat (pas de bosse). 
Je prévois de traduire les signes sur les produits manufacturés en braille afin que les gens puissent sentir les bosses sur les produits et «lire» le texte avec leur toucher. 
L'imprimante spéciale qui peut imprimer les bosses sur les panneaux attend les points dans l'ordre suivant :

```
1 4
2 5
3 6
```
Ainsi, étant donné le mot ```code``` en texte brut, vous obtenez les points Braille :
```
11 10 11 10
00 01 01 01
00 10 00 00
```
Où 1 représente une bosse et 0 représente aucune bosse. Ensemble, le code devient la chaîne de sortie ```100100101010100110100010```.

Ainsi, la fonction (plaintext) prend un paramètre de chaîne et renvoie une chaîne de 1 et de 0 représentant les bosses et l'absence de bosses dans la chaîne d'entrée. 
La fonction est capable d'encoder les 26 lettres minuscules, de gérer les lettres majuscules en ajoutant une marque de capitalisation Braille avant ce caractère et d'utiliser un caractère blanc ```(000000)``` pour les espaces. 
En supposant que les produits à imprimer comportent moins de cinquante caractères et n'utilisent que des lettres et des espaces.

---

## Cas de test
### Input:
``` (string) plaintext = "code" ```
### Output
``` (string) "100100101010100110100010" ```
### Input:
``` (string) plaintext = "Braille" ```
### Output
``` (string) "000001110000111010100000010100111000111000100010" ```
---
## Cas d'utilisation
- Fabrication d'articles d'épicerie accessibles
- Blocs Braille réutilisables et réimprimables
