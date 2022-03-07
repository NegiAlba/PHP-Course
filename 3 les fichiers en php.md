# Les fichiers en PHP

## Comment sont gérés les fichiers ?

De manière générale PHP étant un langage serveur possède un lien privilégié avec l'ensemble des fichiers du serveur.
Cela signifie aussi qu'il doit en prioriser certains, privatiser d'autres et rendre certains dossiers/fichiers facilement accessibles.

En PHP toutefois, il n'y a pas de structure de dossiers prédéfinie il faudra donc en définir une soi-même.
Beaucoup de structures ont été démocratisées et popularisées (notamment grâce à certains frameworks) mais il révèlent tous une utilisation extensive de structures privilégint l'abstrait plutôt que le cas par cas.
Les meilleurs méthodes qui permettent de jongler avec ce genre de structures sont : les variables d'environnement et les fonctions de dossiers (entre autres il existe aussi l'autoloading).

### Les variables d'environnement c'est quoi ?

Les variables d'environnement sont des variables qui répondent à une suite logique.

1. D'abord on déclare des constantes qui vont contenir nos variables servant à des fonctions importantes, ces constantes servent à rendre abstrait l'utilisation de ces fonctionnalités.
2. Créer des fonctions pures et abstraites qui permettent de rendre l'usage des constantes valides.

Ces constantes d'environnement sont généralement liés au fonctionnement interne de notre application, il s'agit par exemple de l'adresse du serveur hôte (host) ou encore du nom du dossier racine (root).
Enfin il peut s'agit d'infos strictement confidentielles qu'il ne faut pas partager, par exemple une clé d'API (API key).

Généralement le fichier qui déclare des variables d'environnement n'est pas suivi/connu par Git (_donc il ne sont pas envoyé sur un repository distant, ils ne sont d'ailleurs même pas stockés sur un repository local_) et possède une copie qui contient un mockup des variables d'environnement afin de comprendre comment structurer un fichier de variables d'environnements. Il contiennent souvent le nom **.env**

### Fonctions de dossier

Les fonctions de dossier, permettent d'accéder aux fichiers sans passer par des chemins littéraux. L'objectif reste toujours de rendre le plus abstrait que possible le projet afin de limiter les erreurs liées aux changements de plateforme.
Parmi les fonctions de dossier les plus utiles on retrouve `___DIR___` et `dirname()` qui serviront à réaliser des constantes de dossiers.
Globalement on créera une structure qui ressemblera à :

```php
$root = dirname(__DIR__).DIRECTORY_SEPARATOR;
define('APP_PATH', $root.''.DIRECTORY_SEPARATOR);
define('ASSETS_PATH', $root.''.DIRECTORY_SEPARATOR);
define('FILES_PATH', $root.''.DIRECTORY_SEPARATOR);
define('VIEWS_PATH', $root.''.DIRECTORY_SEPARATOR);
```

Les constantes englobent la plupart des dossiers importants (à conditions de préciser le nom du dossier entre les guillemets) et permettront de naviguer dans les dossiers sans créer de chemin littéraux.

### Gérer des fichiers

La gestion de fichiers en PHP est possible (PHP est d'ailleurs plutôt efficace pour cela) grâce à plusieurs fonctions PHP existantes. Gérer les PDF est plus compliqué puisque cela nécessite une extension supplémentaire.
Les fonctions PHP pour les fichiers textes sont `fopen, fread, fwrite` et les images sont `imagecreate, imagepolygon, imagepng` et permettent de lire, créer ou modifier des fichiers ou des images.
