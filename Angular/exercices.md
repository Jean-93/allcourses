# Angular 9 : Découverte de Angular - Exercices
> - [Retourner à la liste des cours](../readme.md)
> - Cours : [cliquez-ici](01.md)
> - Corrections : [cliquez-ici](corrections.md)

- [Angular 9 : Découverte de Angular - Exercices](#angular-9--d%c3%a9couverte-de-angular---exercices)
    - [Exercice 1](#exercice-1)
    - [Exercice 2](#exercice-2)
  - [!](#)
    - [Exercice 3](#exercice-3)
  - [- Lancez le serveur Angular](#ul-lilancez-le-serveur-angularli-ul)
    - [Exercice 4](#exercice-4)
  - [- Ajoutez un type `string` aux attributs : `title` et `subTitle`.](#ul-liajoutez-un-type-string-aux-attributs--title-et-subtitleli-ul)
    - [Exercice 5](#exercice-5)
  - [- Une fois résolus, saisissez `npm update` pour valider l'installation de Bootstrap](#ul-liune-fois-r%c3%a9solus-saisissez-npm-update-pour-valider-linstallation-de-bootstrapli-ul)
    - [Exercice 6](#exercice-6)
  - [!](#-1)
    - [Exercice 7](#exercice-7)
    - [Exercice 8](#exercice-8)
    - [Exercice 9](#exercice-9)
    - [Exercice 10](#exercice-10)
    - [Exercice 11](#exercice-11)
    - [Exercice 12](#exercice-12)
    - [Exercice 13](#exercice-13)
    - [Exercice 14](#exercice-14)
  - [- Rattacher ce second bouton à une action qui fera l'inverse de ce que fait le premier bouton ! (le premier "embauche", le second "vire")](#ul-lirattacher-ce-second-bouton-%c3%a0-une-action-qui-fera-linverse-de-ce-que-fait-le-premier-bouton--le-premier-%22embauche%22-le-second-%22vire%22li-ul)
    - [Exercice 15](#exercice-15)
    - [Exercice 16](#exercice-16)
      - [Dans l'enfant](#dans-lenfant)
      - [Dans le parent](#dans-le-parent)
      - [Appeler l'enfant depuis le parent en passant la variable](#appeler-lenfant-depuis-le-parent-en-passant-la-variable)
      - [Changer l'état du bouton](#changer-l%c3%a9tat-du-bouton)
    - [Exercice 17](#exercice-17)
    - [Exercice *](#exercice)

---
### Exercice 1
> [Lien vers la correction](corrections.md#correction-1)
- Modifiez ce nouveau composant (et non pas le fichier `app.component.html`) pour afficher à la place une liste de tâches :

![Tasks](img/tasksulli.png)

--- 

---
### Exercice 2
> [Lien vers la correction](corrections.md#correction-2)
- Créez un composant `task`, qui ne contiendra qu'une seule tâche, et ajoutez le plusieurs fois dans votre composant `tasks-list` afin d'avoir plusieurs tâches issues du component `task` :

![](img/new-taskslist.png)
---

---
### Exercice 3
> [Lien vers la correction](corrections.md#correction-3)
- Ouvrez un terminal dans le dossier de vos projets
- Créez un nouveau projet nommé `angular-tour-of-heroes`, sans options. Acceptez le routing Angular lorsque demandé et choisissez SCSS lorsque demandé
- Ouvrez le projet dans VSCode
- Lancez le serveur Angular
---

---
### Exercice 4
> [Lien vers la correction](corrections.md#correction-4)

- Trouvez où se situe le titre du component `app.component` et modifiez-le en `Tour of Heroes`.
- Ajoutez un type `string` aux attributs : `title` et `subTitle`.
---

---
### Exercice 5
> [Lien vers la correction](corrections.md#correction-5)

- Ajoutez Bootstrap au projet Tour of Heroes.
- Lisez les warning `WARN` affichés lors de l'installation et essayez de les résoudre : 
![](img/c0206.png)
- Une fois résolus, saisissez `npm update` pour valider l'installation de Bootstrap
---


---
### Exercice 6
> [Lien vers la correction](corrections.md#correction-6)

- Créez un component `heroes`.
- Importez ce component dans `app.component.html`.
- Dans votre component `heroes`, ajoutez un attribut `hero` de type `string` avec pour valeur le nom de héros de votre choix.
- Affichez ce nom de héros dans la partie HTML du component.

![](img/0*0*.png)
---

---
### Exercice 7
> [Lien vers la correction](corrections.md#correction-7)

- Créez un fichier `src/app/Hero.ts` et créez une interface qui contiendra les attributs `id` (de type `number`) et `name` (de type `string`).

- Importez  l'interface dans le component `app-hero`

- Remplacez le `hero` existant par un objet de type `Hero` (avec id=1)

---


---
### Exercice 8
> [Lien vers la correction](corrections.md#correction-8)

- Affichez les données du héros créé dans le component :

![](img/c0217.png)

---


---
### Exercice 9
> [Lien vers la correction](corrections.md#correction-9)

- Créez un bouton "mettre en congé" qui, une fois cliqué, active le bouton "embaucher les héros !" :

![](img/c0224.gif)

Les étapes à suivre sont :
1. Créer un bouton "Mettre en congé"
2. Ajouter un Event Binding qui écoute le clic sur le bouton
3. Quand on clique sur le bouton, activer une méthode
4. Dans la méthode, modifier la valeur de `isActivated` sur son inverse (soit true, soit false)

> Comment accéder à `isActivated` ? Quand on est dans une classe, on accède ou modifie ses propres attributs et méthodes avec `this.attribut` ou `this.method()`. Par exemple :

```js
class Hello() {
    name: string = "Thomas";

    sayHello() {
        console.log( "Hello" + this.name ) !
    }
}
```

---


---
### Exercice 10
> [Lien vers la correction](corrections.md#correction-10)

- Affichez le nom du héros dans un champ de formulaire.

![](img/c0229.png)

---

---
### Exercice 11
> [Lien vers la correction](corrections.md#correction-11)

Trouvez un moyen d'afficher le nom du héros systématiquement en majuscules grâce aux Pipes de Angular ([voir la documentation](https://angular.io/guide/pipes)).

![](img/c0235.gif)

---

---
### Exercice 12
> [Lien vers la correction](corrections.md#correction-12)

Si le nom du héros est vide, affichez sa ligne en rouge une fois que l'on clique ailleurs (classe : `list-group-item-danger` sur le `li`) :

![](img/c0318.gif)

Étapes à suivre:
- Trouvez à quel endroit ajouter la classe
- Trouvez la condition à laquelle ajouter la classe

---

---
### Exercice 13
> [Lien vers la correction](corrections.md#correction-13)

Si on clique sur "Embaucher les héros !", passer tous les héros en vert (classe: `list-group-item-success`).

![](img/c0320.gif)

Étapes à suivre:
- Écouter l'évènement `click` sur le bouton
- Le rattacher à une méthode
- Créer un nouvel attribut dans le component faux par défaut
- Faire en sorte que la méthode passe cet attribut sur vrai lorsqu'elle est appelée
- Si cet attribut est sur vrai, alors mettre la classe correspondante dans les `li`

---

---
### Exercice 14
> [Lien vers la correction](corrections.md#correction-14)

- Si on clique sur "Embaucher les héros !", changer le bouton en "Virer les héros !"
- Si on clique sur "Virer les héros !" faire en  sorte qu'ils ne soient plus verts.

![](img/c0323.gif)

Étapes à suivre:
- Ajouter une directive afin d'afficher le bouton dans un cas seulement
- Créer un autre bouton qui s'affichera dans le cas inverse
- Rattacher ce second bouton à une action qui fera l'inverse de ce que fait le premier bouton ! (le premier "embauche", le second "vire")
---


---
### Exercice 15
> [Lien vers la correction](corrections.md#correction-15)

- Créez les composants suivants :
```
hero
hero-detail 
heroes-actions
```

- Intégrez les composants entre eux aux bons endroits pour respecter cette arborescence :

```
app-root : racine de notre projet
    heroes : liste des héros
        hero: un seul héros
        hero-detail : détail d'un héros
    heroes-actions: boutons d'actions
```

> Par exemple, nous avions déjà ajouté `app-heroes` (le `heroes.component` à `app-root` (le `app.component`) de la façon suivante :

![](img/c0401.png)


---


---
### Exercice 16
> [Lien vers la correction](corrections.md#correction-16)

Dans le `app-root`, vous allez créer un bouton qui vous permette d'afficher ou de cacher la liste de héros (le `<ul class="list-group">`) dans `app-heroes`.

![](img/c0426.gif)

Étapes :
#### Dans l'enfant

> L'enfant écoute une information venant du parent, il attendun attribut testant si le `<ul class="list-group">` doit s'afficher ou pas.
1. Ajouter dans `heroes.component.ts` une variable booléenne `@Input()` qui teste si la liste est affichée ou non. Par exemple `isHeroesListShow`.

2. Modifier `heroes.component.html` pour que le `<ul class="list-group">` ne s'affiche que si `isHeroesListShow` est vrai (grâce à `*ngIf`)

#### Dans le parent
> Le parent va contenir le bouton d'action et un attribut booléen qui sera envoyé à l'enfant, qui aura la donnée "est-ce que le bouton est cliqué"  et qui changera quand on clique dessus sur vrai ou faux.
1. Créer un bouton "Afficher les héros" dans `app.component.html`
2. Créer un attribut booléen `isButtonHeroesShowToggled` dans `app.component.ts`
3. Ajouter une action de clic `(click)` sur le bouton dans `app.component.html` qui actionnera une méthode `toggleHeroesShow()` dans `app.component.ts`. Cette méthode va inverser la  valeur  de `isButtonHeroesShowToggled` de la classe.
4. Ajouter une action de clic `(click)` sur le bouton dans `app.component.html` qui actionnera une méthode `toggleHeroesShow()` dans `app.component.ts`. Cette méthode va inverser la valeur  de `isButtonHeroesShowToggled` de l'attribut.

#### Appeler l'enfant depuis le parent en passant la variable
5. Dans le `app.component.html`, appelez le composant enfant `app-heroes` en lui passant la variable  qu'il attend (`[inputAttenduParLenfant]="attributDuParentàEnvoyer"`)

#### Changer l'état du bouton
Quand le bouton fonctionne, faites en sorte qu'il affiche selon s'il est cliqué ou non :
- "afficher les héros" en bouton vert
- "cacher les héros" en bouton gris

---

---
### Exercice 17
> [Lien vers la correction](corrections.md#correction-17)

- Maintenant que vous avez envoyé le changement "Embaucher les héros" / "Virer les héros" depuis l'enfant `app-heroes-actions` vers le parent `app-root`, utilisez cette donnée pour l'envoyer à l'autre enfant `app-heroes`, de sorte à ce que `app-heroes` change les couleurs des héros quand ils sont embauchés comme avant !


---

---
### Exercice *
> [Lien vers la correction](corrections.md#correction-*)

![](img/img.png)

---