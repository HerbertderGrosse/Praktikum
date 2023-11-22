# Hinweise für den Versuch Pendel


## Aufgabe 2: Reversionspendel

### Spezialfall: Langer dünner Stab

Für einen dünnen Stab der Länge $\ell$, der um einen seiner Endpunkte schwingt gilt für $\Theta$ und $s$:
$$
\begin{equation*}
\Theta = \frac{1}{3}m\,\ell^{2}; \qquad s = \frac{1}{2}\ell.
\end{equation*}
$$
 Daraus ergeben sich $\ell_{r}$ und $T_{0}$ zu 
$$
\begin{equation}
\begin{split}
&\ell_{r} = \frac{\frac{1}{3}m\,\ell^{2}}{\frac{1}{2}\ell\,m} = \frac{2}{3}\ell; \\
&\\
&T_{0} =2\pi\sqrt{\frac{\ell_{r}}{g}}=2\pi\sqrt{\frac{2\,\ell}{3\,g}}. 
\end{split}
\end{equation}
$$
Positioniert man $K'$ im Abstand $d=\ell_{r}$ zu $A$ besitzt das Reversionspendel zwei bemerkenswerte, nicht-triviale Eigenschaften: 

- **Eine zusätzliche Masse $\boldsymbol{m'}$ in der Position $\boldsymbol{d=\ell_{r}}$ ändert $\boldsymbol{T_{0}}$ nicht**. In diesem Fall ändern sich $\Theta$ und $s$ wie folgt:

  ```math
  \begin{equation*}
  \begin{split}
  &\Theta\to\Theta' = \frac{1}{3}m\,\ell^{2} + m'\left(\frac{2}{3}\ell\right)^{2};\\
  &\\
  &\\
  &s\,\,\to s'\, = \frac{\frac{1}{2}\ell\,m+\frac{2}{3}\ell\,m'}{m+m'}\\
  &\\
  &\\
  &T_{0} = 2\pi\sqrt{\frac{\Theta'}{(m+m')\,g\,s'}} = 2\pi\sqrt{\frac{(\frac{1}{2}m\ell+\frac{2}{3}m'\ell)\frac{2}{3}\ell}{(\frac{1}{2}\ell\,m+\frac{2}{3}\ell\,m')g}} = 2\pi\sqrt{\frac{2\,\ell}{3\,g}}.\\
  \end{split}
  \end{equation*}
  ```

  Der Vergleich mit Gleichung **(1)** zeigt, dass $T_{0}$ tatsächlich unverändert bleibt. 

- **Dreht man das Pendel um $\boldsymbol{180^{\circ}}$ um, schwingt es mit der gleichen Periode $\boldsymbol{T_{0}}$**. Beachten Sie hierzu **Skizze 1**, rechts. In gedrehtem Zustand befindet sich 1/3 des Stabs oberhalb der Aufhängung. Für das Direktionsmoment gilt daher:

  ```math
  \begin{equation*}
  D' = \frac{1}{6}\ell\,m\,g.
  \end{equation*}
  ```

  Für das Trägheitsmoment gilt nach dem [Satz von Steiner](https://de.wikipedia.org/wiki/Steinerscher_Satz):

  ```math
  \begin{equation*}
  \Theta' = \frac{1}{12}m\ell^{2}+m\left(\frac{1}{6}\ell\right)^{2} = \frac{1}{9}m\,\ell^{2}.
  \end{equation*}
  ```

  Daraus ergibt sich für $T_{0}$:

  ```math
  \begin{equation*}
  T_{0} = 2\pi\sqrt{\frac{\Theta'}{D'}}=2\pi\sqrt{\frac{\frac{1}{9}m\,\ell^{2}}{\frac{1}{6}\ell\,m\,g}} = 2\pi\sqrt{\frac{2\,\ell}{3\,g}}.
  \end{equation*}
  ```

  Der Vergleich mit Gleichung **(1)** zeigt, dass $T_{0}$ tatsächlich unverändert bleibt. 

Beide Eigenschaften sind hier für einen Spezielfall gezeigt, der auf den Versuch anwendbar ist. Sie gelten aber (ohne Beweis) allgemein! Ausführliche Betrachtungen zum Reversionspendel gehen auf [Friedrich Wilhelm Bessel](https://de.wikipedia.org/wiki/Friedrich_Wilhelm_Bessel) zurück. Unabhängig von der exakten Form des Pendels, lässt sich die Position $d=\ell_{r}$ zwischen $K$ und $K'$ also z.B. dadurch auffinden, dass $T_{0}$ in der Aufhängung in den Punkten $A$ und $A'$ den gleichen Betrag hat. Hat man $d=\ell_{r}$ sicher aufgefunden lässt sich $g$, ohne Kenntnis von $\Theta$ oder $s$,  aus der Gleichung
$$
\begin{equation*}
g = \frac{4\pi^{2}}{T_{0}^{2}}\ell_{r} = \frac{4\pi^{2}}{T_{0}^{2}}d
\end{equation*}
$$
bestimmen.

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel/doc/Hinweise-Aufgabe-2.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel/doc/Hinweise-Aufgabe-2-b.md)

