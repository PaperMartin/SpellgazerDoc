Timer Module
=====

| Le **Timer Module** est un module qui déclenche un event après un certain temps et peut être lui même déclenché ou annulé par d'autres events.

.. list-table:: Paramêtres
   :widths: 20 20
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Reset on Retrigger
     - Détermine si le timer doit repartir de 0 si il est activé alors qu'il est déjà en cours
   * - Trigger on Spawn
     - Détermine si le timer doit être activé dès le spawn de l'acteur.
   * - Loop until Cancel
     - Détermine si le timer doit se répéter jusqu'à ce qu'il soit cancel.
   * - Time
     - Détermine le temps avant que l'event soit déclenché.

.. list-table:: Events
   :widths: 20 20 20
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - TriggerTimerEvent
     - Lance le timer.
     - Aucun
   * - CancelTimerEvent
     - Annule le timer si il est en cours.
     - Aucun
    
.. list-table:: Callbacks
   :widths: 20 20 20
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - OnTimerEndCallback
     - Activé à la fin du timer.
     - Aucun