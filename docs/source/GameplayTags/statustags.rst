Gameplay Tags De Status
=====
| Les **Tags de Status** sont des tags qui représentent de façon abstraite différents aspects de **l'état d'un acteur**. 
| Par défaut les tags eux même n'ont pas de fonctionnalité, à la place leur influence sur le gameplay vient de la façon dont les différents systèmes globaux ou modules/components réagissent à leur présence.
| Il faut donc voir l'application de tags de status à un acteur comme une **transmission d'information**, plutôt qu'une véritable prise de contrôle de l'aspect d'un acteur.
| Un tag donné peut être **ajouté plusieurs fois d'affilé à un acteur**, donc si 2 modules/components ou systèmes appliquent les mêmes tags il n'y a à prioris pas de risque de conflit. Certains tags sont même fait pour être stacké (par exemple MassModifier).

| Cette page contient un index des principaux tags de status utilisés dans le projet.
| Sauf indication contraire, vous pouvez ajouter ou retirer ces tags à un acteur sans risque.

.. note:: 
    il est possible d'ajouter des nouveaux tags relativement facilement mais consultez un des programmeurs qui touchent au système de module pour déterminer quel tags ajouter.
    Si un tag n'est pas présent dans cette liste, ne l'utilisez pas sans en avoir parlé avec un programmeur.

..
  TODO : remplacer par fichier csv?

.. list-table:: Tags de Status Physique
   :widths: 25 50 25
   :header-rows: 1

   * - Tag
     - Description
     - Notes
   * - States.Physics.Gravity.GravityRemover
     - Désactive la gravité sur un acteur si au moins 1 est présent 
     - 
   * - States.Physics.Mass. etc
     - Sont automatiquement ajouté/retiré de chaque ModularActor par MassHandler, représentent la masse actuelle d'un objet. Si le tag static est présent l'objet ne peut pas être déplacé
     - Tags Interne, Ne doivent jamais être ajouté manuellement.
   * - States.Physics.MassModifier.Increase/ReduceMass
     - Augmente ou réduit la masse d'un objet quand appliqué, peuvent être stacké (la masse est augmenté de 1 tier par stack)
     - 
   * - States.Physics.MassOverride
     - Remplace la masse d'un objet par celle spécifiée. Si plusieurs tags d'override sont présent, celui avec la masse la plus grande est choisi. 
     -
   * - States.Physics.Size.Default etc
     - Sont automatiquement ajouté/retiré de chaque ModularActor par SizeHandler, représentent la taille actuelle d'un objet.
     - Tags Interne, Ne doivent jamais être ajouté manuellement.
   * - States.Physics.SizeOverride.ForceExpand/Shrink
     - Force l'objet à devenir plus grand ou plus petit. Clear les modifications de taille faites via event (spell expand/shrink, etc) et empêche ces modifications quand appliqué.
     -

.. list-table:: Tags de Status sans catégorie
   :widths: 25 50 25
   :header-rows: 1

   * - Gameplay Tag
     - Description
     - Notes
   * - States.Ambered
     - Représente si l'objet est ambré. Peut être ajouté a un objet à sa création où dynamiquement pendant que le jeu est actif.
     - 
