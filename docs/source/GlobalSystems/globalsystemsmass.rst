.. _global_systems_mass:

Masse
=====

**Masse**

| La masse physique d'un acteur est calculé par le component MassHandler.
| Son comportement est influencé par plusieurs éléments :
| *Les paramêtres du ModularActor* : Il est possible d'y configurer la masse par défaut de l'acteur.
| *La section Mass de DA_GlobalPhysicsData* : Il est possible de configurer dans GlobalPhysicsArchetypePerMass la masse physique correspondante à chaque tier de masse.
| *Les tags MassModifiers* : Quand des tags MassModifiers (IncreaseMass et ReduceMass) sont appliqué, la masse est recalculé selon le nombre de chaque tags présent sur l'objet.
| *Les tags MassOverride* : Quand un tag MassOverride est appliqué, sa masse correspondante remplace entièrement la masse calculé tant qu'il est présent.