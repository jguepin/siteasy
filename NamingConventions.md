# Introduction #
Pour avoir un code cohérent et lisible, il faudrait respecter des conventions de nommage en PHP et Javascript. J'ai choisi les conventions imposées par Zend, le framework PHP le plus utilisé, parce que apparemment c'est ce qui se fait le plus couramment (vu qu'aucune convention de codage n'a l'air conseillée officiellement pour PHP). On peut bien sûr tout changer et refaire nos propres conventions, mais autant profiter de ce qui est déjà utilisé.

**Ici il s'agit bien du nommage des variables/classes/méthodes, non pas du style du code à adopter.**

# Classes #

Les noms de classes ne peuvent contenir que des caractères alphanumériques. Les chiffres sont autoriés mais découragés dans certains cas. Les underscores sont permis seulement pour représenter un séparateur de chemin : le fichier "Zend/Db/Table.php" peut correspondre à la classe "Zend\_Db\_Table".

Si un nom de classe comprend plusieurs mots, la première lettre de chaque mot doit être une majuscule. Plusieurs lettres majuscules à la suite ne sont pas autoriées : la classe "Zend\_PDF" n'est pas autorisée, tandis que "Zend\_Pdf" l'est.

# Classes abstraites #

En général, les classes abstraites doivent suivre les même conventions que les **classes**, avec un règle supplémentaire : les noms de classes abstraites doivent se terminer avec le terme "Abstract", qui ne doit pas être précédé d'un underscore. Par exemple, Zend\_Controller\_Plugin\_Abstract est un nom invalide, tandis que Zend\_Controller\_PluginAbstract l'est.

# Interfaces #

En général, les interfaces doivent suivre les même conventions que les **classes**, avec un règle supplémentaire : les noms d'interfaces doivent se terminer avec le terme "Interface", qui ne doit pas être précédé d'un underscore. Par exemple, Zend\_Controller\_Plugin\_Interface est un nom invalide, tandis que Zend\_Controller\_PluginInterface l'est.

# Noms de fichiers #

Pour tous les autres noms de fichiers, seulement les caractères alaphanumériques, les undersocres, et le tiret ("-") sont autorisés. Les espaces sont formellement interdits.

Les noms de fichiers doivent coïncider avec les noms de classes, comme indiqué plus haut.

# Fonctions et méthodes #

Les noms de fonctions doivent contenir uniquement des caractères alphanumériques. Les underscores ne sont pas permis. Les nombres sont permis mais découragés dans la plupart des cas.

Les noms de fonctions doivent toujours commencer par une lettre minuscule. Lorsqu'un nom de fonction est composé de plus d'un mot, la première lettre de chaque nouveau mot doit être **majuscule**. Cela s'appelle le formatage "camelCase".

La _verbosité_ est encouragée. Les noms de fonctions doivent être assez verbeux pour décrire complètement le but et le comportement de la fonction. Voici une liste de noms de fonctions acceptables :

```
filterInput()
 
getElementById()
 
widgetFactory()
```

Pour la programmation orientée objet, les méthodes d'accès aux variables statiques ou d'instance doivent toujours être préfixées avec "get" ou "set". En cas d'implémentation d'un design pattern, comme les patterns Singleton ou Factory, le nom de la méthode doit contenir le nom du pattern.

Pour les méthodes déclarées comme "private" ou "protected", le premier caractère du nom de la méthode doit être **un underscore**. Ceci est le seul cas dans lequel il faut mettre un underscore dans le nom d'une méthode (les méthodes publiques ne doivent jamais en contenir).

Les fonctions dans le contexte global, "flottantes", sont permises mais découragées. Il est mieux d'imbriquer ces fonctions dans une classe statique.

# Variables #

Les noms de variables peuvent uniquement contenir des caractères alphanumériques. Les underscores ne sont pas permis. Les nombres sont permis dans les noms de variables mais découragés.

Pour les variables d'instances déclarées avec un accès "private" ou "protected", le premier caractère du nom de la variable doit être **un underscore**. Les variables publiques ne doivent jamais commencer par un underscore.

De la même manière que pour les noms de fonctions, les noms de variables doivent toujours commencer par une lettre minuscule et suivre la convention de majuscules "camelCaps".

La verbosité est encouragée. Les variables doivent être assez verbeuses pour décrire les données que le développeur souhaite y stocker. Les noms tels que "$i" ou "$n" sont découragés sauf dans un contexte de petite boucle. Si la boucle contient plus de 20 lignes de code, la variable d'index doit avoir un nom plus descriptif.

# Constantes #

Les constantes peuvent contenir des caractères alphanumériques et des underscores. Les nombres sont permis dans les noms de constantes.

Toutes les lettres utilisées dans les noms de constantes sont en majuscules, et les mots sont séparés par des underscores. Par exemple, **EMBED\_SUPPRESS\_EMBED\_EXCEPTION** est permis mais **EMBED\_SUPPRESSEMBEDEXCEPTION** ne l'est pas.

Les constantes doivent être définies comme attributs de classes avec le mot-clé "const". La définition d'une constante dans le contexte global avec la fonction "define" est permis mais fortement découragé.

# Page contenant les conventions complètes #

http://framework.zend.com/manual/en/coding-standard.naming-conventions.html