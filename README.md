# 2021-2022_Dabadie_Labrousse

Projet **capteur de déformation low-tech à base de graphite** dans le cadre de l'UF "du capteur au banc de test" en 4ème année Génie Physique à l'INSA Toulouse. Le capteur est basé sur la variation de résistance engendrée par la déformation du capteur. En effet, le capteur repose sur le principe physique de déplacement par effet tunnel des électrons entre les nanoparticules de graphite. Lorsqu'une contrainte mécanique est appliquée sur le capteur, la distance entre les nanoparticules varie, entraînant une modification de la conductivité du capteur, et donc une variation de sa résistance qui est mesurable.

Ce fichier décrit toutes les étapes nécessaires à la réalisation du capteur: 
1. le schéma électrique sur le logiciel *LTSpice* afin de simuler la réponse idéale du capteur
2. la réalisation du shield avec le logiciel *KiCad* 
3. le code Arduino
4. l'application APK pour téléphone permettant l'envoi et la réception de données avec le capteur via un module Bluetooth
5. le protocole du banc de test

# 1. Introduction: Description du projet et Cahier des Charges

Le projet est réalisé par binôme et comprend plusieurs livrables:
- un shield PCB 
- un code Arduino permettant l'acquisition de la mesure de résistance ainsi que le contrôle des fonctionnalités du shield (affichage sur l'écran OLED, commmunication Bluetooth, encodeur rotatif, potentiomètre digital)
- une application Android APK
- une datasheet du capteur

Pour mener à bien ce projet, nous avons simulé le capteur sur *LTSpice*, puis rédigé le code Arduino fonctionnel permettant la mesure de la résistance du capteur et le contrôle des autres éléments du shield (écran OLED, module Bluetooth, encodeur rotatif, potentiomètre digital). Nous avons par la suite branché tous les éléments sur une breadboard reliée à une carte Arduino Uno afin de tester la fonctionnalité du code. Nous avons par la suite designé en parallèle le PCB avec le logiciel *KiCad* et l'application téléphone APK grâce au logiciel *MIT APP Inventor*. Après avoir designé le PCB, nous l'avons fabriqué et avons assemblé les composants dessus en les soudant. Enfin, nous avons caractérisé et testé le capteur en déposant du graphite issu de crayon à papier dessus. Nous avons par la suite mesuré la variation de résistance relative du capteur en fonction de sa déformation. 

Liste du matériel nécessaire au projet:
- 1 carte Arduino Uno
- 3 condensateurs de 100nf
- 1 condensateur de 1µF
- 2 résistances de 100kΩ
- 1 résistance de 10kΩ
- 1 résistance de 1kΩ
- 1 AOP LTC1050
- 1 module Bluetooth HC-05
- 1 écran OLED I2C
- 1 encodeur rotatif KY-040
- 1 potentiomètre digital MCP-41XXX

# 2. Simulation du circuit transimpédance avec le logiciel *LTSpice*

Le capteur délivre un courant de faible intensité et la carte Arduino Uno mesure seulement des tensions entre 0 et 5V. Il est donc nécessaire d'intégrer un circuit transimpédance afin de convertir les variations de courant du capteur en variations de tension mesurable par la carte. Ce circuit doit aussi réduire les bruits liés à la mesure et amplifier le signal d'entrée pour pouvoir délivrer une tension mesurable.
Le document nommé Simulation_Capteur présente l'essentiel des informations liées à la simlation du capteur.

# 3. Code Arduino 

# 4. Création du PCB sur le logiciel *KiCad*
## 4.1 Elaboration des symboles et empreintes

Dans cette section, les symboles et empreintes des composants non initialement présents sur le logiciel *KiCad* sont présentés. 

- Amplificateur Opérationnel LTC1050
