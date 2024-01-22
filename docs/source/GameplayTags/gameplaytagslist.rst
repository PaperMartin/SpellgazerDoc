Gameplay Tags
=====

| Cette page contient un index des principaux Gameplay Tags utilisés dans le projet.
| Sauf indication contraire, vous pouvez ajouter ou retirer ces tags à un acteur sans risque.

| il est possible d'ajouter des nouveaux tags relativement facilement mais consultez un des programmeurs qui touchent au système de module pour déterminer quel tags ajouter.
| Si un tag n'est pas présent dans cette liste, ne l'utilisez pas sans en avoir parlé avec un programmeur.

..
  TODO : remplacer par fichier csv

.. tabularcolumns:: |p{1/3}|p{1/3}|p{1/3}|

.. list-table:: Tags Physique
   :header-rows: 1

   * - Gameplay Tag
     - Description
     - Notes
   * - States.Physics.Gravity.GravityRemover
     - Désactive la gravité sur un acteur si au moins 1 est présent 
     - 
   * - States.Physics.Mass. etc
     - Représentent la masse actuelle d'un objet. Si le tag static est présent l'objet ne peut pas être déplacé
     - Tags Interne, Ne doivent jamais être ajouté manuellement.
   * - States.Physics.MassModifier.Increase/ReduceMass
     - Augmente ou réduit la masse d'un objet quand appliqué, peuvent être stacké (la masse est augmenté de 1 tier par stack)
     - 
   * - States.Physics.MassOverride
     - Remplace la masse d'un objet par celle spécifiée. Si plusieurs tags d'override sont présent, celui avec la masse la plus grande est choisi. 
     -
   * - States.Physics.Size.Default etc
     - Représentent la taille actuelle d'un objet.
     - Tags Interne, Ne doivent jamais être ajouté manuellement.
   * - States.Physics.SizeOverride.ForceExpand/Shrink
     - Force l'objet à devenir plus grand ou plus petit. Clear les modifications de taille faites via event (spell expand/shrink, etc) et empêche ces modifications quand appliqué.
     -

.. list-table:: Tags sans catégorie
   :header-rows: 1

   * - Gameplay Tag
     - Description
     - Notes
   * - States.Ambered
     - Représente si l'objet est ambré. Peut être ajouté a un objet à sa création où dynamiquement pendant que le jeu est actif.
     - 
