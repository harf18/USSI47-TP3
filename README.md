# TP3 : Classes et Objets

### Objectifs
Manipuler les classes :

- Création de classe & instanciation d'objet
- Constucteurs
- Méthodes
- Attributs

### Prérequis
- Cloner le projet sur votre poste dans le repertoire de votre choix
- Ouvrir le projet :
  - Sur l'écran d'accueil d'IntelliJ, cliquer sur **Open**
  - Sélectionner le dossier **tp3-xxx** qui a été copié depuis github puis cliqué sur **OK**.
  - Le projet s'ouvre
  - Allez vérifier que le SDK est bien sélectionné dans **File > Project Structure** onglet **Project**

### Utilisation de GIT

- Créer une nouvelle branche **prenomNom**
- Faire **1 commit** par exercice
- Ouvrir **une seule** *pull request* sur github et **ne pas** la fermer/merger !!

----

### Modalité du TP

- Utiliser la méthode *main()* de la classe **Exec** pour tester vos développements : Création d'objets, appel de méthodes, etc... au rythme ou vous le desirez, ce n'est pas précisé dans chaque exercice.
- Toutes les classes des exercices doivent être ajoutées au package **net.lecnam.ussi2a.tp3**

> Si vous ne l'avez pas encore fait, pensez a créer une nouvelle branche **prenomNom**

### Exercice 1

- Créer une classe **Point**. Ajouter les 2 propriétés d'un point avec le bon type. Ces propriétés représent les coordonnées du point.
- Ajouter un **constructeur** pour initialiser ces 2 propriétés.
- Écrire une méthode **translate(double x, double y)** qui déplace le point (ajoute les valeurs passées en paramètre aux coordonnées du point)
- Redéfinir la méthode **equals(Point p)** pour tester l'égalité de deux Points (l'ordonnée et l'abscisse sont égales)
- Redefinir la méthode **toString()** pour qu'elle retourne un String qui décrits les attributs x et y du Point. (peut être que votre IDE peut vous aider...)
- Ecrire une méthode **retourneDistance(Point p)** qui retourne la distance entre le point et un autre Point. *aide : pensez au théorème de pytagore et reflechissez 2 minutes, ça ira plus vite que de trouver des réponses juste sur google  et c'est plus gratifiant !!*

> Pensez à tester dans Exec en créant 2 point et en affichant la distance
>
> Pensez a faire votre 1er commit !!  

### Exercice 2
Créer une classe **Rectangle**. Un rectangle possède 2 longeurs (double) et un Point d'origine (pour le situer dans le plan)

> Pensez a faire un commit !!

### Exercice 3
Dans la classe Rectangle, créer 2 constructeurs prenant respectivement en paramètre : 

- 1 Point (le point d'origine du rectangle) et 2 double (les 2 longueurs). 

- 4 double : les 2 premiers doubles sont les coordonnées du point d'origine et les 2 suivant correspondent aux 2 longueurs.

Chaque constructeur doit initaliser les attributs du rectangle.  
On considère les longeurs et coordonnées comme forcément positives, **ne pas gérer le cas d'erreur**.

> Pensez a faire un commit !!

### Exercice 4
Dans la classe **Rectangle**
- Écrire une méthode **retourneSurface()** qui calcule et retourne la surface du rectangle. 
- Écrire une méthode **translate(double, double)** qui déplace un rectangle (revient a faire un translate du Point d'origine du rectangle)

> Pensez a faire un commit !!

### Exercice 5
Dans la classe **Rectangle**
- Écrire une méthode **contient(Point)** qui teste si un point donné en paramètre est à l'intérieur du rectangle (retourne un booléen). 

> Pensez a faire un commit !!

### Exercice 6
Dans la classe **Rectangle**
- Redéfinir la méthode **equals(Rectangle)** pour tester l'égalité de deux rectangles (2 rectangles sont égaux s'ils ont le même point d'origine et leurs mêmes longeurs identiques).
- Redefinir la méthode **toString()** pour qu'elle retoune une chaine qui retourne les attributs du Rectangle ainsi que sa surface.

> Pensez a faire un commit !!

### Exercice 7
Créer une classe **Dessin**. Cette classe contient un tableau (merci de bien utiliser un tableau même si vous connaissez les List) de 10 Rectangles et une propriété qui indique le nombre de rectangles instanciés dans le dessins.

> Pensez a faire un commit !!

### Exercice 8
Dans la classe **Dessin**, écrire une méthode **ajout(Rectangle)** qui permet d'ajouter un rectangle dans le tableau. Aidez vous de la propriété qui indique le nombre de rectangle pour ajouter le rectangle dans le 1er indice libre du tableau

> Pensez a faire un commit !!

### Exercice 9
Dans la classe **Dessin**
- Écrire une méthode **retourneSurface()** qui calcul et retourne la surface total de tous les rectangles (même s'ils se superposent)
- Écrire une méthode **translate(double x, double y)** qui déplace tous les rectangles. 

> Pensez a faire un commit !!

### Exercice 10
Créer une méthode **retournePlusGrandRectangle()** qui retourne le plus grand rectangle parmi les rectangles du Dessin

> Pensez a faire un commit !!

### Exercice 11
Effacer vos tests de la méthode **main()** de la classe **Exec** et :
  - Instancier un objet Dessin
  - Ajouter plusieurs rectangles
  - Afficher la surface totale des rectangles
  - Afficher les informations du plus grand rectangle
  - Déplacer les rectangles
  - Afficher les informations du plus grand rectangle

> Pensez a faire votre commit !!  
> Pensez à faire un push (```git push origin *prenomNom*```)  
> Si elle n'est pas déjà ouverte, ouvrez une pull request (branche **prenomNom** vers **master**) NE PAS LA FERMER/MERGER !

### Exercice 12 (bonus)

Sans utiliser l'héritage (pour ceux qui connaissent), créer une classe Carre avec ses propriétés et les mêmes méthodes adaptées au carré que celles de la classe rectangle.

> Pensez a faire un commit !!

### Exercice 13 (bonus)

Ajouter la prise en charge des carrés dans la classe Dessin. Pensez à utiliser instanceOf pour savoir si l'objet est un carré ou un rectanble. retourneSurface() doit retourner les surfaces total et ajouter une méthode retournePlusGrandCarre()

> Pensez a faire un commit !!

### Exercice 14 (bonus)

Dans la classe rectangle, écrire une méthode **contient(Carre)** qui teste si un carré donné en paramètre est à l'intérieur d'un rectangle (retourne un booléen). 

> Pensez a faire un commit !!

### Exercice 15 (bonus)

Dans la classe Carre, écrire une méthode **contient(Rectangle)** qui teste si un rectangle donné en paramètre est à l'intérieur d'un triangle (retourne un booléen). 

> Pensez a faire un commit !!



