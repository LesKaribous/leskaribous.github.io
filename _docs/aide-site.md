---
layout: doc
title: Aide gestion site
panel: true
toc: true
---

# Pinion

Ressource pour générer des vues PCB et de la documentation interactive. 

## Liens importants

- [Pinion](https://yaqwsx.github.io/Pinion)
- [Repo GitHub Pinion](https://github.com/yaqwsx/Pinion)
- [Issue génération](https://github.com/yaqwsx/Pinion/pull/36)
- [Documentation Poivron Robotique](http://poivron-robotique.fr/Pinion-La-documentation-de-cartes-electroniques.html)

## Comment générer une vue d'un PCB

- Créer un repertoire avec le fichier PCB.kicad.pcb
- Ajouter un repertoire *"web"* poru la génération des fichiers pinion
- Ouvrir *"KiCad 7.0 Command Prompt"*
- Lancer la commande de génération du template du fichier de spécification YAML :
**Exemple :**

```bash
pinion template 
--board C:\Users\adrie\Documents\GitHub\leskaribous.github.io\pages\2023\main-board\MainBoard-2023.kicad_pcb 
--output C:\Users\adrie\Documents\GitHub\leskaribous.github.io\pages\2023\main-board\mainBoard.yml
```

- Générer les fichiers *"web"* :
**Exemple :**

```bash
pinion generate plotted 
--board C:\Users\adrie\Documents\GitHub\leskaribous.github.io\pages\2023\main-board\MainBoard-2023.kicad_pcb 
--specification C:\Users\adrie\Documents\GitHub\leskaribous.github.io\pages\2023\main-board\mainBoard.yml web\ 
--libs cli
```

**Note -** Voir [issue #36](https://github.com/yaqwsx/Pinion/pull/36) : ajouter `--libs cli` pour éviter `erreur TypeError: 'NoneType' object is not iterable`

Pour vérifier le bon fonctionnement de la page : `pinion serve -b --directory web/`

## Intégration dans une page du site (jekyll)

- Créer un fichier markdown avec le nom du PCB dans le repertoire `Pages\(année)`
- Adapter le code suivant en fonction des besoins :

```html
<div id="pinionDemo"></div>

<script src="web/pinion.js"></script>
<link rel="stylesheet" href="web/pinion.css">

<script>
    pinion.setup(document.getElementById("pinionDemo"), {
        source: "web"
    });
</script>
```

# Affichage d'une vidéo

Le fichier d'inclusion `embedded_video.html` vous permet d'intégrer facilement des vidéos YouTube dans vos pages Markdown. Voici comment l'utiliser :

## Syntaxe de base

La syntaxe de base pour utiliser `embedded_video.html` est la suivante :

`{``% include embedded_video.html video_id="VIDEO_ID" %}`

Remplacez `VIDEO_ID` par l'identifiant de la vidéo YouTube que vous souhaitez intégrer. Par exemple, pour une vidéo dont l'URL est `https://www.youtube.com/watch?v=CscO3rPIJTU`, l'identifiant de la vidéo serait `CscO3rPIJTU`.

## Spécifier le moment de démarrage

Si vous souhaitez que la vidéo commence à un moment spécifique, vous pouvez utiliser le paramètre `start`. Ce paramètre prend un nombre qui représente le nombre de secondes à partir du début de la vidéo. Par exemple, pour faire démarrer la vidéo à 30 minutes et 3 secondes (soit 1803 secondes), vous pouvez utiliser :

`{``% include embedded_video.html video_id="CscO3rPIJTU" start="1803" %}`

## Spécifier la largeur et la hauteur

Vous pouvez également spécifier la largeur et la hauteur de la vidéo en utilisant les paramètres `width` et `height`. Ces paramètres prennent des chaînes de caractères qui représentent la largeur et la hauteur en pixels ou en pourcentage. Par exemple, pour définir une largeur de `500px` et une hauteur de `350px`, vous pouvez utiliser :


`{``% include embedded_video.html video_id="CscO3rPIJTU" width="500px" height="350px" %}`


## Valeurs par défaut

Si vous n'indiquez pas de valeur pour `start`, `width`, ou `height`, des valeurs par défaut seront utilisées :

- `start` : Par défaut, la vidéo commencera dès le début (`0`).
- `width` : Par défaut, la largeur de la vidéo sera de `100%`.
- `height` : Par défaut, la hauteur de la vidéo sera de `250`.

---

# Utilisation du composant Match Display

Le composant Match Display est un include Jekyll qui permet d'afficher une représentation attrayante d'un match. Il comprend un titre, les détails des adversaires avec leurs scores respectifs, une vidéo intégrée de YouTube, et une description.

Pour utiliser ce composant, il suffit d'ajouter le code suivant à votre fichier Markdown :

`{``% include match_display.html title="Votre titre ici" opponent1="Nom de l'équipe 1 ici" score1="Score de l'équipe 1 ici" opponent2="Nom de l'équipe 2 ici" score2="Score de l'équipe 2 ici" video_id="ID de la vidéo YouTube ici" start="Timestamp de départ de la vidéo ici" description="Description du match ici" %}`

Voici une description détaillée de chaque paramètre :

- `title` : Le titre du match. Ce sera le titre affiché au-dessus des détails du match.

- `opponent1` et `opponent2` : Les noms des deux équipes qui ont participé au match.

- `score1` et `score2` : Les scores respectifs des deux équipes.

- `video_id` : L'identifiant de la vidéo YouTube à intégrer. Vous pouvez obtenir cet identifiant à partir de l'URL de la vidéo sur YouTube. Par exemple, pour l'URL "https://www.youtube.com/watch?v=dQw4w9WgXcQ", l'ID de la vidéo serait "dQw4w9WgXcQ".

- `start` : Le timestamp à partir duquel la vidéo doit commencer à jouer, en secondes.

- `description` : Une description détaillée du match. Cette description peut être écrite en Markdown pour permettre une mise en forme riche.

Lorsque ces paramètres sont remplis, l'inclusion générera une belle représentation de votre match qui peut être utilisée sur n'importe quelle page de votre site Jekyll.