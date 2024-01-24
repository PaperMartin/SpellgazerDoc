Self Tag Applier
=====

| Le **Self Tag Applier** est un component qui ajoute ou retire un ou plusieurs tags à son acteur quand déclenché.

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
   * - AddTagsEvent
     - Ajoute les tags à l'acteur. Ignoré si StackTags n'est pas coché et que les tags ont déjà été ajouté par ce module.
     - Aucun
   * - OnQueryFalseCallback
     - Activé quand la query devient invalide (pas quand il y a des changements de tag sur l'acteur mais qu'elles sont déjà invalide).
     - Aucun