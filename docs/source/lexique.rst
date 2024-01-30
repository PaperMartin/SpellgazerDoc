Lexique
=======

Cette page contient un lexique des termes utilisés dans le reste de cette documentation. Les définitions données ici ne sont pas aussi complête que celles données dans les pages dédiées.

.. list-table:: Lexique
   :widths: 25 75
   :header-rows: 1

   * - Mot
     - Description
   * - Gameplay Tag
     - Identifiant utilisé par une variété de système pour communiquer. N'a pas de fonctionnalité par soit même.
   * - Event Tag
     - Gameplay Tag utilisé pour représenter une "fréquence" de communication entre systèmes de jeux.
   * - Event
     - Fréquence à laquelle un module ou component peut réagir d'une façon spécifique quand un signal est émit. (ex: sur RocketModule, quand un signal est transmis sur la fréquence correspondante au tag configuré dans RocketTriggerEvent, la rocket s'activera)
   * - Callback
     - Fréquence sur laquelle un module ou component va émettre un signal sous certaines conditions(ex: A la fin de son compte à rebourd, Timer Module Emet un signal sur la fréquence correspondante au tag configuré dans OnTimerEndCallback).
   * - Global System
     - Systèmes qui définissent les rêgles les plus basique et universelle du jeu.(ex: système de masse, système de size,etc)
   * - ModularActor
     - Type d'acteur qui peut être composé de modules/components, et qui est soumis aux rêgles établies par les Global Systems.
   * - Module/Component 
     - Briques de construction d'un ModularActor. Représente un set de fonctionnalité qui peut être assigné à un acteur.
