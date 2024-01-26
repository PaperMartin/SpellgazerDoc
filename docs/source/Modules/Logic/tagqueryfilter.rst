Tag Query Filter
=====

| Le **Tag Query Filter** est un component qui déclenche un callback quand un acteur fournis commence où arrête à remplir une Tag Query.
| Les **Tag Query** sont des ensembles de conditions de présence ou absence de tags sur un acteur donné qui doivent être remplies pour que la Tag Query soit valide.

| Le filtrage ne se fait pas seulement au moment où un acteur est ajouté au filtre, mais en continu tant qu'il n'y est pas retiré.
| Un utilisage commun serait de le placer aprês un OverlapSensor pour seulement détecter les acteurs qui sont dans une zone et qui ont ou n'ont pas certains tags.

.. list-table:: Paramêtres
   :widths: 25 75
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Tag Query
     - Tag Query qui contient toutes les conditions de présence/absence de tag à remplir.
   
.. list-table:: Events
   :widths: 25 50 25
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - AddActorToCheckEvent
     - Ajoute un acteur au filtre.
     - Acteur
   * - RemoveActorToCheckEvent
     - Retire un acteur du filtre
     - Acteur

.. list-table:: Callbacks
   :widths: 25 50 25
   :header-rows: 1

   * - Callbacks
     - Description
     - Arguments
   * - OnActorMatchQueryCallback
     - Activé quand un acteur dans le filtre remplis les conditions de la query.
     - Acteur
   * - OnActorStopMatchingQueryCallback
     - Activé quand un acteur dans le filtre ne remplis plus les conditions de la query.
     - Acteur
   * - OnFirstActorMatchQueryCallback
     - Activé quand le premier acteur dans le filtre remplis les conditions de la query. (par exemple, si il y a 5 acteurs dans le filtre actuellement, que aucun ne remplissent la condition, et que le 3e acteur se met à la remplir, le callback sera activé avec le 3e acteur en argument)
     - Acteur
   * - OnLastActorStopMatchingQueryCallback
     - Activé quand le dernier acteur dans le filtre ne remplis plus les conditions de la query. (par exemple, si il y a 5 acteurs dans le filtre actuellement, que seulement le 3e remplis la condition, et qu'il se met à ne plus la remplir, le callback sera activé avec le 3e acteur en argument)
     - Acteur