# arduino_robobox1_sensor
Code de l'arduino pour la robobox premier mois 

Description :

Pour éviter le son et lumière permanent, le code ne tient compte que des changements d'état du détecteur de mouvements, et ne buzz que lors d'une activation.

Montage identique à celui de la notice, pour un mode silencieux le buzzer peut être remplacé par une led et une résistance il faut modifier le code en conséquence (commentez la ligne "joueSonEtLumiere" et dé-commentez la ligne suivante)7

D'après la documentation du capteur utilisé il fonctionne avec 2 modes: single ou serial
-en mode single le capteur reste actif pendant .delay. secondes (le temps du potentiomètre delay) et repasse à l'état low ensuite
-en mode serial le capeutr ajoute .delay. secondes à son temps d'activation pour chaque mouvement détecté pendant l'activation,
il ne repasse donc à l'état low que .delay. secondes après le dernier mouvement

Pour ce projet il est préférable d'utiliser le mode single (bridger les deux pattes sur trois les plus proche du capteur blanc)
