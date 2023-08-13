---
layout: page
title: Base Robot Holonome
panel: true
date: 2022-01-01 00:00:00 +0800
---

<model-viewer src="robot-base.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster.webp" shadow-intensity="1" auto-rotate environment-image="legacy" shadow-softness="0.67" exposure="2">
    <div class="progress-bar hide" slot="progress-bar">
        <div class="update-bar"></div>
    </div>
    <button slot="ar-button" id="ar-button">
        View in your space
    </button>
    <div id="ar-prompt">
        <img src="https://modelviewer.dev/shared-assets/icons/hand.png">
    </div>
</model-viewer>

## Robot Holonome

### Introduction

Un robot holonome est un type de robot mobile capable de se déplacer instantanément dans n'importe quelle direction avec une rotation complète sur lui-même. Cette capacité est rendue possible grâce à l'utilisation de roues holonomes.

### Roues Holonomes

Les roues holonomes, également appelées roues omni-directionnelles, sont conçues pour permettre un mouvement dans toutes les directions sans avoir à tourner la roue elle-même. Elles sont généralement constituées d'une série de rouleaux montés à angle par rapport à l'axe principal de la roue. Ces rouleaux permettent au robot de se déplacer latéralement tout en roulant normalement.

### Avantages des robots holonomes

1. **Maniabilité** : Les robots holonomes peuvent se déplacer dans n'importe quelle direction sans avoir à tourner. Cela les rend extrêmement maniables, en particulier dans des espaces restreints.

2. **Précision** : Grâce à leur capacité de mouvement omni-directionnel, les robots holonomes peuvent effectuer des mouvements très précis, ce qui est essentiel pour certaines applications comme la manipulation d'objets ou la navigation dans des environnements complexes.

3. **Simplicité de contrôle** : Bien que la mécanique des roues holonomes puisse sembler complexe, le contrôle d'un robot holonome est souvent plus simple que celui d'un robot non-holonome. Les mouvements peuvent être directement traduits en commandes moteur sans avoir à prendre en compte la direction dans laquelle le robot est tourné.

D'accord, je vais intégrer ces informations pour fournir une documentation technique sur la conception des robots basée sur un assemblage de trois colonnes moteur holonome.


## Conception de Robots : Assemblage de Trois Colonnes Moteur Holonome

### Introduction

La conception des robots, en particulier ceux destinés à des mouvements omni-directionnels, nécessite une approche innovante pour garantir à la fois la maniabilité et la simplicité. Dans cette optique, la conception basée sur un assemblage de trois colonnes moteur holonome est une solution efficace.

### Structure des Colonnes Moteur Holonome

Chaque colonne moteur holonome est une unité indépendante composée d'une roue holonome propulsée par un moteur. Ces colonnes sont disposées de manière à permettre au robot de se déplacer librement dans toutes les directions.

1. **Disposition Triangulaire** : Les trois colonnes de motorisation sont disposées en triangle équilatéral. Cette configuration assure une distribution uniforme du poids et une stabilité optimale. Elle simplifie également nos calculs.

2. **Mouvement Omni-directionnel** : Grâce à cette configuration en trois colonnes, le robot peut se déplacer latéralement, avancer, reculer et tourner simultanément. Chaque colonne moteur contribue à une partie spécifique du mouvement global.

3. **Simplicité de Conception** : En utilisant trois colonnes de motorisation similaires, la conception du robot est grandement simplifiée. Nous avons conçu et validé une seule colonne qui a ensuite été multipliée et assemblée afin de créer notre robot.

### Avantages de l'Assemblage de Trois Colonnes Moteur Holonome

- **Flexibilité** : Cette conception permet une grande flexibilité de mouvement, rendant le robot capable de naviguer dans des espaces restreints ou encombrés.

- **Stabilité** : La disposition triangulaire des colonnes moteur assure une stabilité accrue, même lors de mouvements rapides ou de changements de direction soudains.

- **Maintenance Simplifiée** : En cas de défaillance d'une des colonnes moteur, elle peut être remplacée ou réparée indépendamment des autres, ce qui facilite la maintenance.

C'est donc une solution élégante et efficace pour obtenir des mouvements omni-directionnels. Cette approche simplifie non seulement la conception initiale, mais facilite également la maintenance et garantit une bonne maniabilité et modularité.


## Structure du Robot : Système MakerBeam et Compléments de Construction

### Introduction

MakerBeam est un système de profilés en aluminium de petite taille, conçu pour la construction modulaire. Ces profilés offrent une base solide pour la construction de robots avancés.

### Caractéristiques du système MakerBeam

- **Dimensions du profilé** : Les profilés MakerBeam ont une section carrée de 10x10mm, ce qui les rend adaptés pour des constructions compactes et robustes.
  
- **Anodisation** : Les profilés sont disponibles en deux finitions : anodisés transparents ou noirs. Cette anodisation non seulement donne un aspect professionnel aux profilés, mais offre également une protection supplémentaire contre la corrosion.
  
- **Fixations** : Le système MakerBeam utilise des vis et des écrous de taille M3 pour les assemblages. Ces fixations sont conçues pour offrir une connexion solide et durable entre les profilés.
  
- **Supports** : Une variété de supports est disponible pour le système MakerBeam, permettant des connexions à angles droits ou d'autres configurations complexes.
  
- **Rails et chariots linéaires** : Pour les applications nécessitant un mouvement linéaire, MakerBeam propose des rails et des chariots linéaires. Par exemple, un rail de 600mm avec un chariot est disponible pour des applications nécessitant un déplacement plus long.

### Compléments de construction : PMMA et Impression 3D

- **Plaques en PMMA (Acrylique)** : Les robots intègrent des plaques en PMMA, également connu sous le nom d'acrylique. Ces plaques sont découpées au laser, ce qui permet d'obtenir des pièces de précision adaptées aux besoins spécifiques du robot. Le PMMA est un matériau transparent, résistant aux chocs, et offre une excellente transmission de la lumière.

- **Impression 3D** : De nombreuses pièces du robot sont réalisées grâce à l'impression 3D, le plus souvent en PLA (Acide Polylactique). Le PLA est un polymère biodégradable couramment utilisé en impression 3D pour sa facilité d'utilisation et sa capacité à reproduire des détails fins. Ces pièces imprimées en 3D peuvent être des engrenages, des supports, des boîtiers ou tout autre composant personnalisé nécessaire à la fonctionnalité du robot.

### Utilisation dans la construction de robots

La modularité et la robustesse du système MakerBeam, combinées aux plaques en PMMA et aux pièces imprimées en 3D, offrent une flexibilité et une personnalisation accrues. Ces matériaux permettent de créer des structures complexes, tout en conservant une esthétique soignée et une grande robustesse.

### Conclusion

La combinaison du système MakerBeam, des plaques en PMMA et de l'impression 3D offre une solution complète pour la construction de nos robots. Que ce soit pour la robustesse, la flexibilité ou l'esthétique, cette combinaison de matériaux et de techniques garantit également une réalisation rapide de nos robots. En effet, nosu disposons chez nous d'une petites laser K40 ainsi que d'imprimantes 3D. Nous sommes donc autonomes en ce qui concerne la réalisation de nos robots.

## Motorisation du Robot : Moteurs NEMA 23 et Drivers MKS Servo 57B

### Introduction

La motorisation est un élément clé de tout robot mobile. Pour garantir des mouvements précis et fiables, il est essentiel de choisir des composants de qualité. Dans cette optique, l'utilisation des moteurs NEMA 23 et des drivers MKS Servo 57B est un choix judicieux.

### Moteurs NEMA 23

- **Type de Moteur** : Les NEMA 23 sont des moteurs pas à pas. Ils transforment une impulsion électrique en un mouvement mécanique précis, permettant un contrôle précis de la position et de la vitesse.

- **Taille et Forme** : Le terme "NEMA 23" fait référence à la taille standard du moteur, avec une face avant de 2,3 pouces x 2,3 pouces.

- **Applications** : Grâce à leur précision et leur fiabilité, les moteurs NEMA 23 sont couramment utilisés dans des applications nécessitant un contrôle précis, comme les robots, les machines CNC ou les imprimantes 3D.

### Drivers MKS Servo 57B

- **Boucle Fermée** : Les drivers MKS Servo 57B fonctionnent en boucle fermée. Cela signifie qu'ils reçoivent un retour d'information constant sur la position du moteur, leur permettant d'ajuster le mouvement en temps réel.

- **Limitation des Pertes de Pas** : Grâce à cette boucle fermée, les drivers MKS Servo 57B limitent considérablement les risques de perte de pas. Si le moteur est perturbé ou s'il rencontre une résistance, le driver ajuste instantanément le courant pour maintenir le mouvement souhaité.

- **Fiabilité et Performance** : Ces drivers offrent une performance élevée et une grande fiabilité, garantissant que le moteur fonctionne de manière optimale même dans des conditions difficiles.

### Conclusion

L'association des moteurs NEMA 23 avec les drivers MKS Servo 57B offre une solution de motorisation robuste et précise. Cette combinaison garantit des mouvements fluides et fiables, réduisant les risques de défaillances ou d'erreurs lors des déplacements du robot.
  