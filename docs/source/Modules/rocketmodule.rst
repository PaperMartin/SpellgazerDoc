Rocket Module
=====

| Le **rocket module** est un module qui attache un Physics Thruster à un objet, qui à son tour applique une **force constante** dans la direction de son axe X. Si vous voulez que l'acteur soit poussé vers le haut, ils faut donc rotate le module pour que l'axe X pointe vers le bas.

.. list-table:: Paramêtres
   :widths: 20 20
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Thrust Strength
     - La force appliquée par le thruster, en cm par seconde.

.. list-table:: Events
   :widths: 20 20
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - RocketTriggerEvent
     - Active le Rocket Module quand l'event est déclenché
     - Aucun
   * - RocketDisableEvent
     - Désactive le Rocket Module quand l'event est déclenché
     - Aucun
    
