Bienvenue sur la documentation SpellGazer
===================================

Cette documentation contient (ou contiendra) des explications sur comment les différents systèmes de SpellGazer fonctionnent, et comment les utiliser.

L'implémentation du gameplay de SpellGazer est en grande partie basé sur les **ModularActors**. Le fonctionnement de ces acteurs repose sur plusieurs éléments :

| **Les systèmes globaux** : Ce sont les systèmes qui existent sur tout objets dynamique dans le jeu, leur fonctionnement est configurable mais consistent. 
| Exemples : MassHandler gère la masse de l'objet, SizeHandler gère sa taille, etc.

| **Les modules / components** : Ce sont des éléments ajoutable à un ModularActor. Ils sont dans l'ensemble fait pour être manipulé par des designers, et sont configuré et combiné ensemble pour définir le comportement d'un ModularActor sous différentes circonstances. 
| Exemples : RocketModule qui applique une force continu à son acteur dans une direction, TimerModule qui quand activé par un event, active un autre event au bout d'un certain temps.

| **Les Gameplay Tags de Status** : Ce sont des tags qui peuvent être ajouté ou retirer sur un ModularActor, soit par l'acteur lui même, soit par des influences externes.
| Certains tags sont utilisé en interne par des systèmes globaux, d'autres purement par des modules.

| **Les Gameplay Tags d'Events** : Ce sont des évènements déclenché sur un ModularActor par des modules/components ou des facteurs externes. Ils sont eux même définis sous forme de Gameplay Tags. Les noms de variables correspondantes aux events sur les modules/components indiquent si elle correspondent à un event auxquel le module réagis (Event) ou que le module déclenche (Callback)

Le reste de cette documentation contient des explications sur les différents systèmes, modules, tags et events de SpellGazer.


..
   **Lumache** (/lu'make/) is a Python library for cooks and food lovers
   that creates recipes mixing random ingredients.
   It pulls data from the `Open Food Facts database <https://world.openfoodfacts.org/>`_
   and offers a *simple* and *intuitive* API.

   Check out the :doc:`usage` section for further information, including
   how to :ref:`installation` the project.

Contenu
--------

.. toctree::
   :maxdepth: 1
   :caption: Modules & Components
   :name: sec-modules

   Modules/index

.. toctree::
   :maxdepth: 1
   :caption: Systèmes Globaux
   :name: sec-systems
   :glob:

   GlobalSystems/*

.. toctree::
   :maxdepth: 1
   :caption: Gameplay Tags
   :name: sec-tags
   :glob:

   GameplayTags/*

.. toctree::
   :maxdepth: 1
   :caption: Tutoriels
   :name: sec-tutorials
   :glob:

   Tutorials/*
