---
layout: page
title: Base des robots Holonomes
panel: true
toc: true
refactor: true
date: 2022-01-01 00:00:00 +0800
img_path: ../../../assets/img/2023/
---
# Présentation

La conception de nos robots est à la fois simple et modulable, nous permettant chaque année d'ajuster nos systèmes et de faire évoluer nos robots. Depuis 2017, nous employons une base de profilés MakerBeam, combinée à la découpe laser et à l'impression 3D, pour concevoir nos robots. Et depuis 2021, nous développons des robots holonomes.
La version que nous présentons ici est une évolution de notre base holonome introduite en 2022, tout en conservant les principes de conception adoptés par l'équipe depuis 2017.

<model-viewer src="robot-base.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster-base.webp" shadow-intensity="1" auto-rotate environment-image="legacy" shadow-softness="0.67" exposure="2">
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

# Robot Holonome

Un robot holonome est un type de robot mobile capable de se déplacer instantanément dans n'importe quelle direction avec une rotation complète sur lui-même. Cette capacité est rendue possible grâce à l'utilisation de roues holonomes.

## Roues Holonomes

Les roues holonomes, également appelées roues omni-directionnelles, sont conçues pour permettre un mouvement dans toutes les directions sans avoir à tourner la roue elle-même. Elles sont généralement constituées d'une série de rouleaux montés à angle par rapport à l'axe principal de la roue. Ces rouleaux permettent au robot de se déplacer latéralement tout en roulant normalement.

<model-viewer src="omniwheel.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster-omniwheel.webp" shadow-intensity="1" auto-rotate environment-image="legacy" shadow-softness="0.67" exposure="2">
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

## Avantages des robots holonomes

1. **Maniabilité** : Les robots holonomes peuvent se déplacer dans n'importe quelle direction sans avoir à tourner. Cela les rend extrêmement maniables, en particulier dans des espaces restreints.

2. **Précision** : Grâce à leur capacité de mouvement omni-directionnel, les robots holonomes peuvent effectuer des mouvements très précis, ce qui est essentiel pour certaines applications comme la manipulation d'objets ou la navigation dans des environnements complexes.

3. **Simplicité de contrôle** : Bien que la mécanique des roues holonomes puisse sembler complexe, le contrôle d'un robot holonome est souvent plus simple que celui d'un robot non-holonome. Les mouvements peuvent être directement traduits en commandes moteur sans avoir à prendre en compte la direction dans laquelle le robot est tourné.

D'accord, je vais intégrer ces informations pour fournir une documentation technique sur la conception des robots basée sur un assemblage de trois colonnes moteur holonome.

# Les colonnes Moteur

La conception des robots, en particulier ceux destinés à des mouvements omni-directionnels, nécessite une approche innovante pour garantir à la fois la maniabilité et la simplicité. Dans cette optique, la conception basée sur un assemblage de trois colonnes moteur holonome est une solution efficace.

<model-viewer src="robot-column.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster-column.webp" shadow-intensity="1" auto-rotate environment-image="legacy" shadow-softness="0.67" exposure="2">
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

## Structure des colonnes Moteur

Chaque colonne moteur est une unité indépendante composée d'une roue holonome propulsée par un moteur. Ces colonnes sont disposées de manière à permettre au robot de se déplacer librement dans toutes les directions.

1. **Disposition Triangulaire** : Les trois colonnes de motorisation sont disposées en triangle équilatéral. Cette configuration assure une distribution uniforme du poids et une stabilité optimale. Elle simplifie également nos calculs.

2. **Mouvement Omni-directionnel** : Grâce à cette configuration en trois colonnes, le robot peut se déplacer latéralement, avancer, reculer et tourner simultanément. Chaque colonne moteur contribue à une partie spécifique du mouvement global.

3. **Simplicité de Conception** : En utilisant trois colonnes de motorisation similaires, la conception du robot est grandement simplifiée. Nous avons conçu et validé une seule colonne qui a ensuite été multipliée et assemblée afin de créer notre robot.

4. **Maintenance Simplifiée** : En cas de défaillance d'une des colonnes moteur, elle peut être remplacée ou réparée indépendamment des autres, ce qui facilite la maintenance.

C'est donc une solution élégante et efficace pour obtenir des mouvements omni-directionnels. Cette approche simplifie non seulement la conception initiale, mais facilite également la maintenance et garantit une bonne maniabilité et modularité.

# Motorisation du Robot

La motorisation est un élément clé de tout robot mobile. Pour garantir des mouvements précis et fiables, il est essentiel de choisir des composants de qualité. Dans cette optique, l'utilisation des moteurs NEMA 23 et des drivers MKS Servo 57B est un choix judicieux.

## Moteurs NEMA 23

![Alt text](Nema-23.jpg)

Nous utilisons des moteurs NEMA 23, qui sont des moteurs pas à pas capables de transformer une impulsion électrique en un mouvement mécanique précis. Cette caractéristique offre un contrôle rigoureux de la position et de la vitesse. La dénomination "NEMA 23" décrit la dimension standard de ces moteurs, ayant une face avant mesurant 2,3 pouces x 2,3 pouces. En raison de leur précision et fiabilité, ces moteurs sont fréquemment employés dans des dispositifs comme les robots, les machines CNC et les imprimantes 3D.

Le moteur que nous avons choisi pour nos robots est le même que celui que nous utilisions pour nos robots différentiels : le [23HS16-0884S](https://www.omc-stepperonline.com/fr/nema-23-bipolaire-1-8deg-0-6nm-85oz-in-0-88a-6-6v-57x57x41mm-4-fils-23hs16-0884s) de chez OMC-stepperonline.

**Spécification électrique**

- Angle de pas: 1.8deg
- Couple de maintien: 0.6Nm(84.97oz.in)
- Courant/phase: 0.88A
- Résistance/phase: 7.5ohms
- Inductance: 21.7mH±20%(1KHz)

**Spécification physique**

- Dimensions: 57 x 57mm
- Longueur du moteur: 42mm
- Diamètre d'arbre: Φ6.35mm
- Longueur de l'arbre: 20.6mm
- Poids: 500g

Nous l'avons choisis pour son encombrement réduit en longueur ainsi que pour son couple.

## Drivers MKS Servo 57B

Pour piloter nos moteurs, nous avons choisi d'utiliser des drivers déjà conçus, simplifiant ainsi le développement de cette section. L'expansion de l'impression 3D et l'usage accru des moteurs pas-à-pas ont conduit à l'introduction de nouveaux produits sur le marché ces dernières années. Depuis 2021, nous bénéficions de ces progrès en employant des drivers MKS Servo 57B en boucle fermée.

![Alt text](IMG_20210414_204120.jpg)

Ces drivers, fonctionnant en boucle fermée, reçoivent en continu des retours d'information sur la position du moteur, leur permettant d'ajuster le mouvement en temps réel. Cette caractéristique réduit significativement les risques de perte de pas. Si le moteur est perturbé ou rencontre une résistance, le driver modifie instantanément le courant pour conserver le mouvement désiré. Ces drivers garantissent une performance élevée et une fiabilité exceptionnelle, assurant le fonctionnement optimal du moteur même dans des conditions exigeantes.

L'association des moteurs NEMA 23 avec les drivers MKS Servo 57B offre une solution de motorisation robuste et précise. Cette combinaison garantit des mouvements fluides et fiables, réduisant les risques de défaillances ou d'erreurs lors des déplacements du robot.

# Structure du Robot

## Le système MakerBeam

[MakerBeam](https://www.makerbeam.com) est un système de profilés en aluminium de petite taille, conçu pour la construction modulaire. Ces profilés offrent une base solide pour la construction de robots avancés. C'est aussi un partenaire historique des Karibous ! Un grand merci à eux pour leur soutient !

![Alt text](IMG_20211017_203217.jpg)

Nous utilisons ces profilés MakerBeam, caractérisés par une section carrée de 10x10mm, idéale pour des structures à la fois compactes et solides. Ces profilés sont proposés en deux finitions : anodisés transparents ou noirs. L'anodisation, au-delà de conférer un aspect professionnel, protège également les profilés contre la corrosion. Pour assembler ces profilés, le système MakerBeam emploie des vis et des écrous de taille M3, garantissant une liaison robuste et durable. 

Il existe également une gamme variée de supports pour ce système, facilitant des connexions à angles droits ou d'autres agencements plus élaborés. Pour les besoins impliquant un mouvement linéaire, MakerBeam fournit des rails et des chariots linéaires, comme un rail de 600mm accompagné d'un chariot, adapté aux applications nécessitant une plus grande amplitude de déplacement.

## Compléments de construction

- **Plaques en PMMA (Acrylique)** : Les robots intègrent des plaques en PMMA, également connu sous le nom d'acrylique. Ces plaques sont découpées au laser, ce qui permet d'obtenir des pièces de précision adaptées aux besoins spécifiques du robot. Le PMMA est un matériau transparent, résistant aux chocs, et offre une excellente transmission de la lumière.

- **Impression 3D** : De nombreuses pièces du robot sont réalisées grâce à l'impression 3D, le plus souvent en PLA (Acide Polylactique). Le PLA est un polymère biodégradable couramment utilisé en impression 3D pour sa facilité d'utilisation et sa capacité à reproduire des détails fins. Ces pièces imprimées en 3D peuvent être des engrenages, des supports, des boîtiers ou tout autre composant personnalisé nécessaire à la fonctionnalité du robot.

## Utilisation dans la construction de robots

La modularité et la robustesse du système MakerBeam, combinées aux plaques en PMMA et aux pièces imprimées en 3D, offrent une flexibilité et une personnalisation accrues. Ces matériaux permettent de créer des structures complexes, tout en conservant une esthétique soignée et une grande robustesse.

## Conclusion

La combinaison du système MakerBeam, des plaques en PMMA et de l'impression 3D offre une solution complète pour la construction de nos robots. Que ce soit pour la robustesse, la flexibilité ou l'esthétique, cette combinaison de matériaux et de techniques garantit également une réalisation rapide de nos robots. En effet, nosu disposons chez nous d'une petites laser K40 ainsi que d'imprimantes 3D. Nous sommes donc autonomes en ce qui concerne la réalisation de nos robots.