Masse
=====

| Le système de masse détermine la masse physique en KG d'un acteur en fonction de tiers de masse configurable globalement, ainsi que plusieurs Gameplay Tags. 
| Il est possible de configurer la masse par défaut d'un acteur via un des tags de masse.

| Son comportement est influencé par plusieurs paramètres ainsi que par les tags appliqués sur l'acteur :

| **Les paramêtres du ModularActor** : Il est possible d'y configurer la masse par défaut de l'acteur, via un des tags de masse.
| **La section Mass de DA_GlobalPhysicsData** : Il est possible de configurer dans GlobalPhysicsArchetypePerMass la masse physique correspondante à chaque tier de masse.
| **Les tags MassModifiers** : Quand des tags MassModifiers (IncreaseMass et ReduceMass) sont appliqué, la masse est recalculé selon le nombre de chaque tags présent sur l'objet.
| **Les tags MassOverride** : Quand un tag MassOverride est appliqué, sa masse correspondante remplace entièrement la masse calculé tant qu'il est présent.