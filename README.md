# 2021-2022_Dabadie_Labrousse

Projet **capteur de déformation low-tech à base de graphite** dans le cadre de l'UF "du capteur au banc de test" en 4ème année Génie Physique à l'INSA Toulouse. Le capteur est basé sur la variation de résistance engendrée par la déformation du capteur. En effet, le capteur repose sur le principe physique de déplacement par effet tunnel des électrons entre les nanoparticules de graphite. Lorsqu'une contrainte mécanique est appliquée sur le capteur, la distance entre les nanoparticules varie, entraînant une modification de la conductivité du capteur, et donc une variation de sa résistance qui est mesurable.

Ce fichier décrit toutes les étapes nécessaires à la réalisation du capteur: 
1. le schéma électrique sur le logiciel *LTSpice* afin de simuler la réponse idéale du capteur
2. la réalisation du shield avec le logiciel *KICAD* 
3. le code Arduino
4. l'application APK pour téléphone permettant l'envoi et la réception de données avec le capteur via un module Bluetooth
5. le protocole du banc de test

# Introduction: Description du projet et Cahier des Charges

Le projet est réalisé par binôme et comprend plusieurs livrables:
- un shield PCB 
- un code Arduino permettant l'acquisition de la mesure de résistance ainsi que le contrôle des fonctionnalités du shield (affichage sur l'écran OLED, commmunication Bluetooth, encodeur rotatif, potentiomètre digital)
- une application Android APK
- une datasheet du capteur

Pour mener à bien ce projet, nous avons simulé le capteur sur *LTSpice*, puis rédigé le code Arduino fonctionnel permettant la mesure de la résistance du capteur et le contrôle des autres éléments du shield (écran OLED, module Bluetooth, encodeur rotatif, potentiomètre digital). Nous avons par la suite branché tous les éléments sur une breadboard reliée à une carte Arduino Uno afin de tester la fonctionnalité du code. Nous avons par la suite designé en parallèle le PCB avec le logiciel *KICAD* et l'application téléphone APK grâce au logiciel *MIT APP Inventor*. Après avoir designé le PCB, nous l'avons fabriqué et avons assemblé les composants dessus en les soudant. Enfin, nous avons caractérisé et testé le capteur en déposant du graphite issu de crayon à papier dessus. Nous avons par la suite 

Liste du matériel nécessaire au projet:
