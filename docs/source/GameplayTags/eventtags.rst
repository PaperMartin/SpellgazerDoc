Gameplay Tag D'Events
=====
| Les **Tags d'Event** servent à connecter ensemble des modules/components sans avoir a écrire de code. Il faut voir chaque tag d'Event comme une **fréquence de transmission** locale à chaque acteur.

| La plupart des modules/components ont dans leur paramêtres des paramêtres avec **"Event** ou **Callback** dans leur nom. Les paramêtres Callbacks représentent quels tags d'event auront leur event associé déclenché par différentes fonctionnalités du comportement de ce module, tandis que les paramêtres Event représentent quels tags d'event déclencheront quels fonctionnalités du module.
| Dans une situation où un module 1 a le tag A dans un paramêtre Callback1, et que un module 2 a le tag A dans un paramêtre Event1, le module 1 pourra déclencher l'event associé au tag A, ce qui à son tour déclenchera la fonctionnalité associé a l'Event1 du module 2.

| Ces events peuvent également **transmettre** différent types d'informations qu'on appelle des **arguments**. 
Certains modules/components qui réagissent à des events ne se préoccupent pas des arguments (TagApplier, RocketModule), mais d'autres s'attendent à des types d'arguments spécifique et ne fonctionneront pas correctement si ils ne sont pas présents (TagQueryFilter, PhysicsAttractor). 
Il pourrait potentiellement y avoir plus tard des Modules/Components qui réagissent à certains arguments mais peuvent quand même fonctionner sans.

| Cette page contient un index des principaux tags d'event utilisés dans le projet, ainsi que leurs arguments habituellement associé. Ils sont pensé pour être utilisé dans des conditions précises, mais comme les tags de status n'ont pas par eux même de fonctionnalité.
| Sauf indication contraire, vous pouvez utilisez ces tags sur des modules sans risque.

.. note:: 
    La plupart des tags d'event ont plusieurs duplicata avec un nombre associé. Ils existent pour permettre l'utilisation de plusieurs events similaire séparémment sur un même acteur, et donc généralement correspondent à la même description et aux mêmes arguments.
    Si un tag n'est pas présent dans cette liste, ne l'utilisez pas sans en avoir parlé avec un programmeur.

..
  TODO : remplacer par fichier csv?

.. list-table:: Tag D'Events
   :widths: 25 50 25
   :header-rows: 1

   * - Tag
     - Description
     - Argument
     - Notes
   * - Events.ModuleSystem.Sensor.OnEnter
     - Représente la détéction d'un acteur par un sensor.
     - Acteur détécté
     - 
   * - Events.ModuleSystem.Sensor.OnExit
     - Représente la fin de la détéction d'un acteur par un sensor.
     - Acteur détécté
     -
   * - Events.ModuleSystem.Filter.OnActorPassFilter
     - Représente qu'un acteur ajouté a un filtre a remplis les conditions du filtre.
     - Acteur filtré
     - 
   * - Events.ModuleSystem.Filter.OnActorStopPassingFilter
     - Représente qu'un acteur ajouté a un filtre ne remplis plus les conditions du filtre.
     - Acteur filtré
     -
   * - Events.ModuleSystem.Filter.OnFirstActorPassFilter
     - Représente le premier passage d'un acteur à travers un filtre dans lequel aucun acteur ne passe actuellement
     - Acteur filtré
     - 
   * - Events.ModuleSystem.Filter.OnLastActorStopPassingFilter
     - Représente le dernier acteur à ne plus passer à travers un filtre dans lequel au moins un acteur passe actuellement
     - Acteur filtré
     - 

