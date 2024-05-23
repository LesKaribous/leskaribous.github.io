---
layout: page
title: Robot 2025 - Rèflexions
panel: false
toc: true
---

# Reflexions et idées pour le robot 2025

## Les choses à changer pour 2025 

### Les PAMIs 

Réduire la taille de la carte :

- Passer sur des ESP32 sans antenne intégrés : https://www.mouser.fr/ProductDetail/Espressif-Systems/ESP32-S3-WROOM-1U-N16R2
- Passer sur des batteries d'appareil photo ([Exemple 1](https://www.amazon.fr/ENEGON-LP-E6NH-Batteries-Rechange-Compatible/dp/B08R8FH3NJ/ref=sr_1_8?__mk_fr_FR=ÅMÅŽÕÑ&crid=VXUFGA2MASML&dib=eyJ2IjoiMSJ9.bdRtNROjCfEbG8Ip4GixMXPXzECKBdjD-O145UZNbSJi3E9qiUzNdkhh3nrkxa6vzE1OaydhoebICsUA3LpAGBzxsePq0jWkyUz257v45bIrXDjgWQF2XHNSWMLgY6OBlnLQv0alowaDaTVj39x42aPJvqqIssAWQN1qVacNpN_YqQbl_1QT0OuoTAywf7ZklNMBwMkVxuAfmGo4Nl71NiRNxynbkhswrf02y97yOpSFYnyDSWKqjNrYw3dBFsbqpIRuu7oWainc3KBwq2lTWtAwlBotwCV_8r_VEIcvVA4._RmGu8ATVesv_flToQE84E6378el4fXW_YNyEEsczbA&dib_tag=se&keywords=lp-e6nh+USB&qid=1715621745&sprefix=lp-e6nh+usb%2Caps%2C118&sr=8-8))

### Les Robots

Les moteurs actuels, [23HS16-0884S](https://www.omc-stepperonline.com/fr/nema-23-bipolaire-1-8deg-0-6nm-85oz-in-0-88a-6-6v-57x57x41mm-4-fils-23hs16-0884s), ne sont pas assez puissants en haute vitesse. Le couple chute drastiquement. 

![alt text](nema23curve.png)

D'après notre [calculateur](https://makerspace-amiens.fr/pages/calculateur-moteur-robot/), il nous faut un moteur capable d'un couple de 50N.cm à 318 tr/min (voir conditions d'entrées ci-après) 

![alt text](calculmoteur.png)

Si on souhaite rester en moteur Pas-à-pas pour le moment, la reférence semble [17HS24-2104S](https://www.omc-stepperonline.com/fr/nema-17-bipolar-1-8deg-65ncm-92oz-in-2-1a-3-36v-42x42x60mm-4-wires-17hs24-2104s) toute indiquée, et il existe [des lots de 3 moteurs](https://www.omc-stepperonline.com/fr/3-pcs-nema-17-bipolar-1-8deg-65ncm-92oz-in-2-1a-3-36v-42x42x60mm-4-wires-3-17hs24-2104s) à des prix interessants.

![alt text](17HS24-2104S.png)

- Numéro de pièce du fabricant: 17HS24-2104S
- Type de moteur: bipolaire
- Angle de pas: 1.8deg
- Couple de maintien: 65Ncm(92oz.in)
- Courant/phase: 2.1A
- Résistance/phase: 1.6ohms

![alt text](couplemoteurnema17.png)

# Liens importants

- recommandations pour cables I2C : https://docs.px4.io/main/en/assembly/cable_wiring.html#:~:text=I2C%20bus%20signal%20cross%2Dtalk,GND%20per%2030cm%20cable%20length.