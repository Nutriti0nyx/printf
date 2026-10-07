# PRINTF
***

## Task
Le projet consistait en la reproduction de la fonction printf() de stdio.h en C. Elle doit renvoyer une chaine de caractère ainsi qu'eventuellement une ou plusieurs variables inserees en arguments et placees dans la chaine de caractere avec %.
Il prend en charge l'affichages de valeurs :
* Entieres (%d)
* Decimales non signée (%u)
* Octodecimales (%o)
* Hexadecimales (%x)
* De chaines (%s)
* De caracteres (%c)
* D'adresse de pointer (%p)
La fonction renvoie egalement le nombre de caracteres affiches
%% renvoie %


## Description
La fonction write() a ete utilisee pour ecrire les caracteres de la chaines fournie. Des conditions (if else) prevoient les cas d'affichages de valeurs en detectant les %.
Les valeurs deja en caracteres sont affichees telles qu'elles. Les autres sont converties en chaines de caracteres sur une base demandee avec la creation d'une fonction decTo(valeur, base).
Les chaines de caractere autres s'affichent avec la fonction print(str), creee pour parcourir une chaine et ecrire avec write() chacune des valeurs. Print renvoie ensuite la longueur de la chaine.

Un compteur de caracteres affiches est tenu a jour et renvoye a la fin.

En cas de cas impossible ("%\0") la fonction s'arrête.
## Installation
La fonction n'est pas faite pour etre utilisee seule. My_printf.c doit donc etre compile avec un autre programme appelant la fonction.

Dans la version fournie, un test est ecrit avec main(). Il faut une compilation (gcc -o [nom] my_printf.c) pour le faire fonctionner.

Le programme fonctionne avec les en-tete : stdbool.h, unistd.h, string.h, stdarg.h et stdlib.h
Le test fonctionne avec l'en-tete : stdio.h


## Usage
int printf(char * restrict str,...)
str est la chaine a afficher, contenant eventuellement des %)
... est un nombre indefini de valeurs presumees valides
