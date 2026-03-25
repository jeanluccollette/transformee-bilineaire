# Propriétés de la transformée bilinéaire

## Objectif de la transformation

On se propose de convertir une fonction de transfert $H(p)$ d'un système à temps continu en une fonction de transfert
$R(z)$ d'un système à temps discret, via le changement de variable dont l'expression est donnée ci-dessous.

$$p = \\frac{2 \\left(1 - z^{-1}\\right)}{T_{e} \\left(1 + z^{-1}\\right)}$$

Dans cette expression, $T_e$ est la période d'échantillonnage qui détermine le fonctionnement de la conversion analogique-numérique.
Les réponses harmoniques associées sont respectivement $H(j\omega)$ avec $0 \leq \omega \lt +\infty$ et $R(e^{j\Omega T_e})$ avec $0 \leq \Omega \lt \dfrac{\pi}{T_e}$.

L'idée est de faire en sorte que $H(j\omega) \approx R(e^{j\Omega T_e})$ pour $\omega=\Omega \ll \dfrac{\pi}{T_e}$.

## Conservation de la stabilité

