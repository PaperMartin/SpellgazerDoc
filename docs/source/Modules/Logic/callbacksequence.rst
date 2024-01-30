Callback Sequence
=====

| Le **Callback Sequence** est un module qui contient une liste de callback. A chaque activation de TriggerAndCycle, il active l'event sur lequel il est actuellement positionné, puis passe au suivant. Quand il arrive à la fin de la liste il retourne au début.

| Précédemment appelé Event Sequence.

.. list-table:: Events
   :widths: 25 50 25
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - TriggerAndCycleEvent
     - Active le callback actuel dans la liste puis se positionne sur le suivant.
     - Aucun
    
.. list-table:: Callbacks
   :widths: 25 50 25
   :header-rows: 1

   * - Callbacks
     - Description
     - Arguments
   * - CallbackSequence
     - Liste de callbacks activé séquentiellement par TriggerAndCycleEvent.
     - Aucun