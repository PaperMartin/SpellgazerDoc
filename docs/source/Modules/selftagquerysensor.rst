Self Tag Query Sensor
=====

| Le **Self Tag Query Sensor** est un component qui déclenche un event quand une Tag Query devient valide ou invalide sur son propre acteur. Il est donc utilisé pour réagir à des changements d'état sur l'acteur, que ce soit des changements de size/masse, ou des changements de tag causé par d'autres modules.
| Les **Tag Query** sont des ensembles de conditions de présence ou absence de tags sur un acteur donné qui doivent être remplies pour que la Tag Query soit valide.

.. list-table:: Paramêtres
   :widths: 20 20
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Tag Query
     - Tag Query qui contient toutes les conditions de présence/absence de tag à remplir.
   
.. list-table:: Callbacks
   :widths: 20 20 20
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - OnQueryTrueCallback
     - Activé quand la query devient valide (pas quand il y a des changements de tag sur l'acteur mais qu'elles sont déjà valide).
     - Aucun
   * - OnQueryFalseCallback
     - Activé quand la query devient invalide (pas quand il y a des changements de tag sur l'acteur mais qu'elles sont déjà invalide).
     - Aucun