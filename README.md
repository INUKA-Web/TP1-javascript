# Instructions pour le TP

## URL du cours

https://perso.liris.cnrs.fr/lionel.medini/enseignement/M1IF03/CM/4_0_JS.pdf

Pour utiliser la console du navigateur : ouvrir une page web et appuyer sur F12 et aller dans l'onglet "Console".

## Exemples de code

- Déclaration et utilisation de variables

```javascript
var a = 12;

function incremente(a) {
    return a+1;
}

a = incremente(a);

function decremente(a) {
    return a-1;
}

a = decremente(a);

// Pour afifcher une popup :
alert(a);
```

- Passage d'une fonction en argument d'une autre fonction (callback)

```javascript
function modifieVariable(a, f) {
    return f(a);
}

a = modifieVariable(a, incremente);
```

- S'abonner à un événement
```javascript
document.body.onclick = function(){
    alert(modifieVariable(a, decremente));
}
```

- Fermeture (closure)

```javascript
function soustrait(y) {
    return function (x) {
        return x - y;
    }
}

var soustrait2 = soustrait(2);

soustrait2(5);
```

- Manipulations du DOM

```javascript
// Récupération du premier paragraphe de la page :
var p = document.getElementsByTagName("p")[0]

// Récupération de la liste des sous-noeuds de ce paragraphe :
p.childNodes

// Récupération du premier noeud texte à l'intérieur de ce paragraphe :
p.childNodes[0]

// Récupération du contenu du premier noeud texte à l'intérieur de ce paragraphe :
p.childNodes[0].data

// Création d'un nouveau noeud dans le document (mais non affiché)
var texte1 = document.createTextNode("COUCOU")

// Ajout du nouveau noeud à la fin de la liste des sous-noeuds du paragraphe :
p.appendChild(texte1)
```


## /!\ Pour la prochaine fois

Télécharger et installer NodeJS : https://nodejs.org/en/
