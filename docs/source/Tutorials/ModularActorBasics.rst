Créer un modular actor basique
===============================

| Sur cette page on va créer un modular actor basique.

| Ce modular actor aura un rocketmodule, et va alterner toutes les 2 secondes entre s'envoler et retomber
| On a accomplir ça via un TimerModule qui s'activera en boucle toutes les 2 secondes, qui à son tour activera un EventSequence qui alternera entre 2 autres events, qui activeront et désactiveront le RocketModule.

1. Créez un nouveau blueprint de type ModularPuzzleActorBase

.. image:: MAB_CreateActor.png


2. Allez à la catégorie Parameters (ne changez pas de propriétés pas hors de cette catégorie) et configurez les options de base de l'acteur : 

.. image:: MAB_BaseParams.png

3. Ajoutez un component TimerModule et configurez ses paramêtres :

.. image:: MAB_TimerParams.png

4. Ajoutez un component EventSequence et configurez ses paramêtres :

.. image:: MAB_EventSequenceParams.png

5. Ajoutez un component Rocket Module et configurez ses paramêtres : 

.. image:: MAB_RocketParams.png

6. Rotatez le RocketModule pour que son axe X soit pointé vers le bas (une rotation à -90 sur l'axe Y devrait suffire)
7. Mettez le blueprint dans un Level et Lancez le jeu. Normalement l'acteur devrait alterne entre lentement accélerer vers le haut et retomber toutes les 2 secondes.