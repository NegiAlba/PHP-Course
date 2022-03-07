# PHP sous XAMPP/WAMP

## Créer un projet web

Accéder au dossier htdocs/www dans notre dossier d'installation \*AMP et on va créer un dossier au nom de notre projet.
Créer un fichier avec l'extension .php et le tour est joué.

## La syntaxe PHP

### Balises PHP

Les balises pour rédiger du code en PHP sont <?php et ?>

### Instruction d'affichage

L'instruction d'affichage de PHP est echo. Elle vous permet d'afficher du texte, des retours de fonctions de manière visible et des variables (et constantes).
Il existe aussi l'instruction print, qui est moins populaire.

### Les variables

Une variable est une donnée que je vais créer et enregistrer le temps de l'exécution de mon application. C'est une donnée que je conserver momentanément pour la réutiliser ultérieurement.

La syntaxe pour créer des variables est `$variable`

Il faut lui assigner une valeur (ce n'est pas nécessaire pour la création, mais pour l'utilisation oui) avec la syntaxe `$variable = 'valeur'`

On peut afficher les valeurs des variables avec une instruction echo.

Le nom d'une variable commence nécessairement par une lettre ou un underscore(\_), sinon le nom est invalide.

On peut assigner des variables à d'autres variables. Il y aura une assignation par valeur (on peut aussi assigner par référence).

Assignation par valeur `$variableA = $variableB`. La variableA est égale à la valeur de la variableB au moment de l'assignation.
Assignation par référence `$variableA = &$variableB` La variableA est égale à la variableB en toutes circonstances.

On peut assigner tous les types de données à des variables.

### Les opérateurs

Parmi les opérateurs utilisables, il y a tout ceux que l'on connait déja : +,-,/,\*.

L'égalité à un opérateur particulier : il s'agit de deux fois le signe = `==`

Les opérateurs restent généralement les mêmes sauf s'ils indiquent une inégalité/égalité stricte.

Il existe une syntaxe pour assigner des valeurs via un calcul. Il s'agit d'une combinaison entre l'opérateur d'assignation `=` et un opérateur de calcul.

Exemples :

```
+=
*=
/=
-=
```

Ils servent généralement à créer une réassignation de la valeur d'une variable via sa valeur initiale.

### Concaténation

Permet d'inclure une variable dans une instruction d'affichage.
L'opérateur de concaténation est un point `.`

Il existe une nouvelle méthode de concaténation qui consiste à utiliser des double guillemets. Attention cette méthode n'est pas inétressante avec des constantes.

### Commentaires

En PHP il existe 3 méthodes pour commenter.

La plus classique est `// commentaire`. Permet de faire un commentaire sur une seule ligne.
La seconde `/* commentaire */`. Permet de faire des commentaires multi-ligne en commencant pas un `/*` et en finissant par `*/`.
La dernière permet de faire des commentaires inline (Sur la même ligne que du code). `# commentaire`

### var_dump et print_r

Ce sont des instructions qui permettent d'afficher les variables (et les tableaux) en détails pour le développement.

## Types de données

Il y a 3 grands groupes de types de données.

Les types scalaires (scalar types)

- Boolean (bool) - true / false
- Integer (int) - 1,2,3,4,5,6,-85 (sans virgules)
- Float (float) - 1.5 ,2.5 ,4.99 (avec virgules)
- String (string) - 'Hello', 'World', 'Nom'

Les types composés (compound types)

- Arrays (array) - `[0,1,2,3,'a','b','c']`
- Objets (objects)
- Callables (callable)
- Iterables (iterable)

Les types spéciaux (special types)

- Resource
- Null

### Type Hinting

En travaillant avec des fonctions ou des objets, on peut renseigner le type utilisé par la fonction ou l'objet afin d'assurer une compatibilité optimale. Généralement c'est préfixer un argument ou une variable.

```php
function newFunction(int $x,int $y){
    return $x+$y;
}
```

### Type Casting et Type docs

C'est l'idée de forcer le retour d'une valeur via une type particulier pour le type casting, ou d'exiger un type pour le type doc.
Le type casting se fait en préfixant avec le type entre parenthèses `(string) $variable`

```php
function newFunction(int $x,int $y) : int
{
    return (int) $x+$y;
}
```

## Fonctions

Une fonction c'est un bout de code réutilisable qui va exécuter des opérations.

Une fonction ressemble a :

```php
function maFonction($argument)
{
    #Corps de la fonction
    #...
    return $argument; # Retour de la fonction
}

maFonction(20); # Appel de la fonction avec comme argument 20.

```
