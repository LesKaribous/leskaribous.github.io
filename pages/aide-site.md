---
layout: page
title: Aide gestion site
date: 2022-08-21 14:10:00 +0800
icon: fas fa-robot
order: 2
refactor: true
pannel_includes:
  - toc
img_path: ../assets/img/
---

# Pinion

Ressource pour générer des vues PCB et de la documentation interactive. 

## Liens importants

- [Pinion](https://yaqwsx.github.io/Pinion)
- [Repo GitHub Pinion](https://github.com/yaqwsx/Pinion)
- [Issue génération](https://github.com/yaqwsx/Pinion/pull/36)
- [Documentaiton Poivron Robotique](http://poivron-robotique.fr/Pinion-La-documentation-de-cartes-electroniques.html)
- 

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