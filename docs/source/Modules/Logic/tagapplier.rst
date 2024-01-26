Tag Applier
=====

| Le **Tag Applier** est un component qui ajoute ou retire un ou plusieurs tags à un acteur fournis via event quand déclenché.

.. list-table:: Paramêtres
   :widths: 25 75
   :header-rows: 1

   * - Paramêtres
     - Description
   * - Tags
     - Tags à ajouter ou retirer de l'acteur.
   * - StackTags
     - Détermine si les tags devraient être ajouté plusieurs fois si AddTagsEvent est déclenché plusieurs fois d'affilé sans que RemoveTagsEvent soit déclenché.
   
.. list-table:: Events
   :widths: 25 50 25
   :header-rows: 1

   * - Event
     - Description
     - Arguments
   * - AddTagsToActorEvent
     - Ajoute les tags à l'acteur fournis dans l'event. Ignoré si StackTags n'est pas coché et que les tags ont déjà été ajouté par ce module à cet acteur.
     - Acteur
   * - RemoveTagsFromActorEvent
     - Retire les tags à l'acteur fournis dans l'event. Ignoré si aucun tag n'est ajouté actuellement par ce component à cet acteur.
     - Acteur