# Game_taches_chronologique

La variable mydata contient un tableau d'objets correspondant aux tâches.

le 1° objet est bidon pour commencer le comptage à 1 et pas à 0

name contient l'intitulé de la tâches

cond contient la ou les conditions de la tâches

si cond contient plusieurs tâches, elle sont séparée par des virgules

Exemple :
~~~~
var mydata=[
        {name:"base"},
        {name:"action 1", cond:"0"},
        {name:"action 2", cond:"1"},
        {name:"action 3", cond:"1"},
        {name:"action 4", cond:"2,3"}
    ];
 ~~~~
 
correspond à action1 --> action 2 --> action 3 --> action 4

ou  action1 --> action 3 --> action 2 --> action 4

parce que :

* action 2 et 3 sont conditionnées par action 1
* action 4 est conditionné par action 2 et 3

Pour mélanger les tâches, il est possible de se faire un fichier excel 
Exemple :
~~~~
+---+---+-------+--------+---------+----+---+
|new|old|av     | name   | milieux |cond|ap |
+---+---+-------+--------+---------+----+---+
|   | 1 |{name:"|action 1|", cond:"|0   |"},|
|   | 2 |{name:"|action 2|", cond:"|1   |"},|
|   | 3 |{name:"|action 3|", cond:"|2   |"},|
+---+---+-------+--------+---------+----+---+
~~~~

et de jouer avec les filtres et tris pour mélanger puis réajuster les conditions en fonction des nouvelles positions.
