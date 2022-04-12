# 2021-2022_Dabadie_Labrousse

Projet **capteur de déformation low-tech à base de graphite** dans le cadre de l'UF "du capteur au banc de test" en 4ème année Génie Physique à l'INSA Toulouse. Le capteur est basé sur la variation de résistance engendrée par la déformation du capteur. En effet, le capteur repose sur le principe physique de déplacement par effet tunnel des électrons entre les nanoparticules de graphite. Lorsqu'une contrainte mécanique est appliquée sur le capteur, la distance entre les nanoparticules varie, entraînant une modification de la conductivité du capteur, et donc une variation de sa résistance qui est mesurable.

Ce fichier décrit toutes les étapes nécessaires à la réalisation du capteur: 
1. le schéma électrique sur le logiciel *LTSpice* afin de simuler la réponse idéale du capteur
2. la réalisation du shield avec le logiciel *KICAD* 
3. le code Arduino
4. l'application pour téléphone communiquant avec le capteur via Bluetooth
5. le protocole du banc de test

# Introduction: Description du projet et Cahier des Charges

Le projet est réalisé par binôme et comprend plusieurs livrables:
- un shield PCB 
- un code Arduino permettant l'acquisition de la mesure de résistance ainsi que le contrôle des fonctionnalités du shield (affichage sur l'écran OLED, commmunication Bluetooth, encodeur rotatif, potentiomètre digital)
- une application Android APK
- une datasheet du capteur

