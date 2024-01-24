Overlap Sensor Module
=====

| L'**Overlap Sensor Module** est un module qui représente une zone de trigger sphérique et déclenche des events lorsque des acteurs entrent ou sortent de cette zone.

.. list-table:: Paramêtres
   :widths: 25 75
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Radius
     - Radius de la zone de trigger.
   * - IsScaleAbsolute
     - Détermine si le radius prend en compte la scale de l'acteur. Si coché, le radius reste le même peu importe la scale actuelle de l'acteur.

.. list-table:: Callbacks
   :widths: 25 50 25
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - OnActorEnterCallback
     - Activé quand un acteur entre dans la zone de trigger.
     - Acteur qui entre dans la zone de trigger.
   * - OnActorExitCallback
     - Activé quand un acteur sort de la zone de trigger.
     - Acteur qui sort de la zone de trigger.