Supposons une machine de Turing universelle $M$, capable de simuler n'importe quel algorithme $A$ en $T(M(A(d)))$ unités de temps sur des données $d$ ; et $N$ une machine universelle quelconque, pouvant être $M$. Dans ce cas, si la machine $M$ simule $N(A(d))$, elle devra nécessairement exécuter toutes les étapes de calcul de $N(A(d))$ au minimum, sans parler du surcoût mobilisé par l'interprétation des données et de l'algorithme ou par l'encapsulation. Son temps d'exécution sera donc au minimum égal (et souvent supérieur) à l'exécution directe de l'algorithme $A$ par $M$.

$$
\forall M, N, A, d \quad T(M(N(A(d)))) \geq T(M(A(d)))
$$

Dans un [[Univers calculable localement]] ou un [[Univers globalement calculable]], on sait que l'univers à un instant $t + 1$ est isomorphe à une machine de Turing universelle $U(F(S_t)$ qui simule les règles de l'univers $F$ en fonction de son état actuel $S_{t}$. On comprend donc que le temps d'exécution d'une machine $M$ simulant les règles d'évolution de l'univers est toujours supérieur au temps d'exécution des règles d'évolution de l'univers par l'univers. Autrement dit, il est impossible de prédire le futur de notre univers depuis son intérieur avant que celui-ci n'advienne.

$$
T(U(M(F(S_{t})))) \geq T(U(F(S_{t})))
$$

D'ailleurs, si $M$ est une machine contenue dans l'univers et qu'elle tente de simuler l'univers entier, y compris elle-même, elle devra simuler sa propre exécution. Ce problème, appelé paradoxe de l'auto-référence, implique que le temps de calcul va croître à l'infini au fur et à mesure des simulations récursives de $M$ par elle-même : l'exécution sera comparable à une boucle infinie.

$$
\space M \in S_{t} \implies T(M(F(S_{t}))) \to \infty
$$