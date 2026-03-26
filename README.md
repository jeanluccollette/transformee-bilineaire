# Propriétés de la transformée bilinéaire

## Objectif de la transformation

On se propose de convertir une fonction de transfert $H(p)$ d'un système à temps continu en une fonction de transfert
$R(z)$ d'un système à temps discret, via le changement de variable dont l'expression est donnée ci-dessous.

$$p = \\frac{2 \\left(1 - z^{-1}\\right)}{T_{e} \\left(1 + z^{-1}\\right)}$$

Dans cette expression, $T_e$ est la période d'échantillonnage qui détermine le fonctionnement des conversions analogique-numérique et numérique-analogique.
Les réponses harmoniques associées sont respectivement $H(i\omega)$ avec $0 \leq \omega \lt +\infty$ et $R(e^{i\Omega T_e})$ avec $0 \leq \Omega \lt \dfrac{\pi}{T_e}$.

L'idée est de faire en sorte que $H(i\omega) \approx R(e^{i\Omega T_e})$ pour $\omega=\Omega \ll \dfrac{\pi}{T_e}$.

## Conservation de la stabilité

En posant $z = r e^{i \\Omega T_{e}}$, la transformation devient :

$$p = \\frac{2 \\left(1 - \\frac{e^{- i \\Omega T_{e}}}{r}\\right)}{T_{e} \\left(1 + \\frac{e^{- i \\Omega T_{e}}}{r}\\right)}$$

En posant $p = \sigma + i \omega$, on obtient :

$$\\sigma = \\Re(p) = \\frac{2 \\left(r^{2} - 1\\right)}{T_{e} \\left(r^{2} + 2 r \\cos{\\left(\\Omega T_{e} \\right)} + 1\\right)}$$

$$\\omega = \\Im(p) = \\frac{4 r \\sin{\\left(\\Omega T_{e} \\right)}}{T_{e} \\left(r^{2} + 2 r \\cos{\\left(\\Omega T_{e} \\right)} + 1\\right)}$$

Le terme $\\left(r^{2} + 2 r \\cos{\\left(\\Omega T_{e} \\right)} + 1\\right)$ au dénominateur de ces expressions vaut $\\sin{\\left(\\Omega T_{e} \\right)}^2$ lorsque la dérivée s'annule. Dès lors, le disque unité ($r \\lt 1$) dans le plan complexe des $z$ est transformé en le demi-plan gauche ($\\sigma \\lt 0$) dans le plan complexe des $p$. La stabilité est donc préservée lors du changement de variable.

## Relation sur les réponses harmoniques

Avec les relations préalablement établies, il apparaît que $\\sigma = 0$ pour $r = 1$. Le cercle unité est donc transformé en l'axe imaginaire.

Par ailleurs, pour $r = 1$ :

$$\\Omega = \\frac{2 \\arctan{\\left(\\frac{T_{e} \\omega}{2} \\right)}}{T_{e}}$$

$$\\omega = \\frac{2 \\tan{\\left(\\frac{\\Omega T_{e}}{2} \\right)}}{T_{e}}$$

Ainsi, $H(i\omega) = R(e^{i\Omega T_e})$, mais avec la relation ci-dessus liant $\\omega$ et $\Omega$. Il faut cependant remarquer que $\\omega \\approx \\Omega$ pour $\Omega \ll \dfrac{\pi}{T_e}$

## Conclusion

Ce changement de variable sur $H(p)$, utilisant la transformation bilinéaire,  donne accès à une fonction $R(z)$ telle que $H(i\omega) \approx R(e^{i\Omega T_e})$ pour $\omega=\Omega \ll \dfrac{\pi}{T_e}$
