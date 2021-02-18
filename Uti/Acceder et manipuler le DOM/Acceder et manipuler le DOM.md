# Acceder et manipuler les elements du DOM
==========================================

## document.getElementById()

Cette méthode va rechercher un élément dans le document HTML en se basant sur son ID.

Exemple: 
--------

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