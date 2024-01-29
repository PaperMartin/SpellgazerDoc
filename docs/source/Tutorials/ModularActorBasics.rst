Créer un modular actor basique
===============================

| Sur cette page on va créer un modular actor basique.

| Ce modular actor aura un rocketmodule, et va alterner toutes les 2 secondes entre s'envoler et retomber
| On a accomplir ça via un TimerModule qui s'activera en boucle toutes les 2 secondes, qui à son tour activera un EventSequence qui alternera entre 2 autres events, qui activeront et désactiveront le RocketModule.

| Créez un nouveau blueprint de type ModularPuzzleActorBase
| Allez à la catégorie Parameters (ne changez pas de propriétés pas hors de cette catégorie) et configurez les options de base de l'acteur : 
    1. Mettez la mesh à la StaticMesh de votre choix (elle doit avoir des simple collisions)
    2. Choisissez un Material (par exemple WorldGridMaterial)
    3. Mettez DA_GlobalPhysicsData dans GlobalPhysicsData
    4. Mettez StartingMass a States.Physics.Mass.Heavy
    5. Mettez StartingFragility a States.Destruction.Fragility.Resistant (cette propriété ne fais actuellement rien mais doit quand même être configuré)
    6. Laissez Should Mesh Have Collision coché

| Ajoutez un component TimerModule et configurez ses paramêtres :
    1. Laissez Trigger Timer Event & Cancel Timer Event vide
    2. Mettez OnTimerEndCallback à Events.ModuleSystem.Generic.Event1
    3. Laissez Reset On Retrigger décoché
    4. Cochez Trigger On Spawn pour que le timer démarre quand l'acteur spawn
    5. Cochez Loop Until Cancel pour qu'il se répète en boucle
    6. Mettez Time à 2

| Ajoutez un component EventSequence et configurez ses paramêtres :
    1. Ajoutez 2 entrées à la Liste Event Sequence. Mettez la première à Events.ModuleSystem.Generic.Event2 et la deuxième à Events.ModuleSystem.Generic.Event3
    2. Mettez Trigger And Cycle Event à Events.ModuleSystem.Generic.Event1

| Ajoutez un component Rocket Module et configurez ses paramêtres : 
    1. Mettez Rocket Trigger Event à Events.ModuleSystem.Generic.Event2
    2. Mettez Rocket Disable Event à Events.ModuleSystem.Generic.Event3
    3. Mettez Thrust Strength à 100000

| Rotatez le RocketModule pour que son axe X soit pointé vers le bas
| Mettez le blueprint dans un Level et Lancez le jeu. Normalement l'acteur devrait alterne entre lentement accélerer vers le haut et retomber toutes les 2 secondes.