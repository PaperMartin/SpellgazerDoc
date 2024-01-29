Créer un modular actor basique
===============================

| Sur cette page on va créer un modular actor basique.

| Ce modular actor aura un rocketmodule, et va alterner toutes les 2 secondes entre s'envoler et retomber
| On a accomplir ça via un TimerModule qui s'activera en boucle toutes les 2 secondes, qui à son tour activera un EventSequence qui alternera entre 2 autres events, qui activeront et désactiveront le RocketModule.

| Créez un nouveau blueprint de type ModularPuzzleActorBase
| Allez à la catégorie Parameters (ne changez pas de propriétés pas hors de cette catégorie) et configurez les options de base de l'acteur : 

    #. Mettez la mesh à la StaticMesh de votre choix (elle doit avoir des simple collisions)
    #. Choisissez un Material (par exemple WorldGridMaterial)
    #. Mettez DA_GlobalPhysicsData dans GlobalPhysicsData
    #. Mettez StartingMass a States.Physics.Mass.Heavy
    #. Mettez StartingFragility a States.Destruction.Fragility.Resistant (cette propriété ne fais actuellement rien mais doit quand même être configuré)
    #. Laissez Should Mesh Have Collision coché

| Ajoutez un component TimerModule et configurez ses paramêtres :

    #. Laissez Trigger Timer Event & Cancel Timer Event vide
    #. Mettez OnTimerEndCallback à Events.ModuleSystem.Generic.Event1
    #. Laissez Reset On Retrigger décoché
    #. Cochez Trigger On Spawn pour que le timer démarre quand l'acteur spawn
    #. Cochez Loop Until Cancel pour qu'il se répète en boucle
    #. Mettez Time à 2

| Ajoutez un component EventSequence et configurez ses paramêtres :

    #. Ajoutez 2 entrées à la Liste Event Sequence. Mettez la première à Events.ModuleSystem.Generic.Event2 et la deuxième à Events.ModuleSystem.Generic.Event3
    #. Mettez Trigger And Cycle Event à Events.ModuleSystem.Generic.Event1

| Ajoutez un component Rocket Module et configurez ses paramêtres : 

    #. Mettez Rocket Trigger Event à Events.ModuleSystem.Generic.Event2
    #. Mettez Rocket Disable Event à Events.ModuleSystem.Generic.Event3
    #. Mettez Thrust Strength à 100000

| Rotatez le RocketModule pour que son axe X soit pointé vers le bas
| Mettez le blueprint dans un Level et Lancez le jeu. Normalement l'acteur devrait alterne entre lentement accélerer vers le haut et retomber toutes les 2 secondes.