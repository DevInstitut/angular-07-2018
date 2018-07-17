# Conversion implicite

Attention au typage faible.

Conversion implicite de types différents lors des opérations.

Les tests suivants sont tous vrais :
* `true == 1`, `true == '1'`
* `false == 0`, `false == '0'`
* `12 == '12'`

On utilisera une comparaison par type ET par valeur pour une égalité stricte.
* `a === b`, égalité en type et en valeur.
* `a !== b`, différence de type ou de valeur.

