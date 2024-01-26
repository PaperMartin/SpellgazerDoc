Physics Attractor
=====

| Le **Physics Attractor** est un component qui permet d'attirer ou repousser des acteurs vers un point.

.. list-table:: Paramêtres
   :widths: 25 75
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Attraction Force
     - Détermine la force avec laquelle les acteurs sont attirés. Repousse les acteurs si négatif.

.. list-table:: Events
   :widths: 25 50 25
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - AddActorEvent
     - Ajoute un acteur à la liste des acteurs attirés.
     - Acteur
   * - RemoveActorEvent
     - Retire un acteur à la liste des acteurs attirés.
     - Acteur
   * - EnableAttractionEvent
     - Active l'attraction
     - Aucun
   * - DisableAttractionEvent
     - Désactive l'attraction.
     - Aucun
