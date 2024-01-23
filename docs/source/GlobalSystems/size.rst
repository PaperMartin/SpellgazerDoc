Size
=====

| Le système de size détermine la taille d'un acteur à n'importe quel moment donné selon plusieurs facteurs : 

| - **La scale par défaut** : La scale du transform de l'acteur, définis dans le level ou blueprint
| - **Le Size Index** : Valeur interne qui représente le "tier" de taille actuel de l'objet.
| - **Le Size Multiplier**: Un multiplicateur qui existe pour chaque tier de taille.

| La  Taille actuelle d'un objet correspond donc à sa scale par défaut multiplié par le Size Multiplier correspondant à son Size Index actuel.

| Le SizeIndex actuel est lui même déterminé par les facteurs suivants :

| - **La présence du tag Ambered** : Si le tag n'est pas présent, l'acteur restera au tier de taille par défaut (1, qui correspond à Default)
| - **Les GameplayEvent TryIncrease/DecreaseSize**: Quand activé sur un acteur, essaye de réduire ou augmenter de 1 l'index. Ineffectif si l'acteur n'a pas le tag Ambered.
| - **La présence de tags SizeOverride** : Actuellement seulement ForceExpand/Shrink, quand appliqué ils forcent l'index de l'acteur au tier correspondant à l'override (sauf si l'acteur est déjà à un tier plus grand/petit que le tier correspondant à l'override)

| Il y a plusieurs paramêtres globaux customizable pour le système de Size dans DA_GlobalPhysicsData :

| - **GlobalSizeArchetypes** : Les différents tiers de taille. Un SizeArchetype contient un tag identifiant la size, un tag SizeOverride indiquant le tag à appliquer pour forcer un objet à cette size (optionnel), et un SizeMultiplier. Les archetypes doivent être dans leur ordre de plus petit à plus grand dans la liste.
| - **SizeChangeSpeed** : Détermine la vitesse constante à laquelle les objets changent de tier de taille.