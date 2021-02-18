# Acceder et manipuler les elements du DOM
==========================================

## document.getElementById()

 Cette méthode va rechercher un élément dans le document HTML en se basant sur son ID.

Exemple 
-------

> const myAnchor = document.getElementByDi('my-anchor');

 cette ligne de commande va pârecourir le document HTML et retourner l'ID de l'élément correspondant.

## getElementByClassName()

 Cette méthode prend en paramètre  la classe des éléments désités pour les renvoyer sous forme de liste.

Exemple
-------

> HTML
 <div>
  <div class="content">Contenu 1</div>
  <div class="content">Contenu 2</div>
  <div class="content">Contenu 3</div>
</div>
> JS
 const contents = document.getElementByClassName('content');
 const firstContent = contents[0];

## getElementsByTagName()

 Prend en paramètre le nom de la balise à rechercehr et retourne la liste des éléments correspontants. 

Exemple 
-------

> HTML
 <div>
  <article>Contenu 1</article>
  <article>Contenu 2</article>
  <article>Contenu 3</article>
  <article>Contenu 4</article>
 </div>
> JS
 const articles = document.getElementsByTagName('article');
 const thirdArticle = articles[2];

## document.querySelector()

 Cette méthode permet de de faire des recherches plus complexes et plus pointues. 

Exemple
-------

> HTML

 <div id="myId">
    <p>
        <span><a href="#">Lien 1</a></span>
        <a href="#">Lien 2</a>
        <span><a href="#">Lien 3</a></span>
    </p>
    <p class="article">
        <span><a href="#">Lien 4</a></span>
        <span><a href="#">Lien 5</a></span>
        <a href="#">Lien 6</a>
    </p>
    <p>
        <a href="#">Lien 7</a>
        <span><a href="#">Lien 8</a></span>
        <span><a href="#">Lien 9</a></span>
    </p>
</div>

> JS

 const elt = document.querySelector("#myId p.article > a");

 Dans cet exemple, la ligne de commande renverra uniquement le "Lien 6".

## querySelector()

 Renvoie le premier élément qui correspond à la recherche.
 Il renvera donc le premier élément trouvé ou "null" si aucun élément correspondant au paramètre n'a été trouvé.
 
Exemple
-------

> JS
 element = document.querySelector(sélecteurs);

## Recherche depuis un élément

 Chaque élément est un objet javaScript avec ses proipriétés et ses fonctions dont cetaines permettent de parcourir les enfants et les parents de chaque élément.

 ### element.children
  
  Cette proprié"té retourne la liste des enfants de l'élément. 

 ### element.parentElement
  
  Retourne le parent de l'élément.

 ### element.nextElementSibling / element.previousElementSibling
  
  Ces propriétés permettent de naviguer vers l'élement précédent ou suivant du même niuveau que notre élément.

Exemple
-------

 > HTML
  
  <div id="parent">
    <div id="previous">Précédent</div>
    <div id="main">
        <p>Paragraphe 1</p>
        <p>Paragraphe 2</p>
    </div>
    <div id="next">Suivant</div>
  </div>

> JS
 
 const elt = document.getElementById('main');

 "elt.children" retournera les "p" qui ontg des enfants dans le "#main"

 "elt.parentElement" retourne la "div" ayant l'id "parent"

 "elt.nextElementSibling" retournera l'élément qui a l'id "next"

 "elt.previousElementSibling" retourne l'élément qui a l'id previous

 

