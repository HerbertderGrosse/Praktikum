# Hinweise für den Versuch Resonanz

## Aufgabe 1: Freie Schwingung [2/2]

###  Hinweise zur Durchführung

#### Aufgabe 1.1: Schwingung ohne äußere Dämpfung

Verwenden Sie Gleichung (**(6)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/doc/Hinweise-Aufgabe-1.md)) als Modell für die Anpassung an die aufgezeichneten Daten. Der funktionale Zusammenhang in Gleichung **(6)** bleibt im Fall einer Zeitableitung, bis auf Betrag und Phase der Schwingung unverändert. Sie können das gleiche Modell also auch zur Anpassung von $\omega(t)$ verwenden.

#### Aufgabe 1.2: Bestimmung des Trägheitsmoments $\Theta$

Der Faden wirkt als [Kraftwandler](https://de.wikipedia.org/wiki/Kraftwandler) für die Kraft $\vec{F}_{j}=m_{j}\,\vec{g}$. Wenn Sie den Faden so anbringen, dass er über die Radnut bei $r=r_{a}$ führt gilt: 
$$
\begin{equation*}
\left|\vec{M}_{j}\right|=\left|\vec{r}_{a}\times\vec{F}_{j}\right| = r_{a}\,F_{j}; \qquad \vec{r}_{a}\perp\vec{F}_{j}
\end{equation*}
$$
Aus der Momentenfreiheit im statischen Fall ergibt sich $D\hspace{0.05cm}\varphi_{j}=r_{a}\hspace{0.05cm}F_{j}=r_{a}\hspace{0.05cm}g\hspace{0.05cm}m_{j}$.  Mit Hilfe der Messungen von $D$ und $\omega_{0}$ können Sie $\Theta$ aus Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/doc/Hinweise-Aufgabe-1.md)) bestimmen. **Für die Messung liegen Ihnen die Massen $m_{j}=5,10,20\hspace{0.05cm}\mathrm{g}$ vor.** Messen Sie die Auslenkung in beiden Drehrichtungen.

Zum Vergleich können Sie $\Theta$ aus der Geometrie des [Pohlschen Rads](https://de.wikipedia.org/wiki/Pohlsches_Rad) wie folgt abschätzen:
$$
\begin{equation*}
\Theta = \int\limits_{r_{i}}^{r_{a}}r^{2}\mathrm{d}m = \int\limits_{r_{i}}^{r_{a}}r^{3}\,d\,\rho\,\mathrm{d}r\,\mathrm{d}\phi = \frac{\pi}{2}\rho\,d\left(r_{a}^{4}-r_{i}^{4}\right).
\end{equation*}
$$
In diesem Fall berücksichtigen Sie lediglich den Ring des Schwungrads und nehmen an, dass dieser eine homogene Massenverteilung mit der Dichte $\rho$ besitzt. Die Dicke des Schwungrads wird mit $d$ bezeichnet, $r_{i}$ entspricht dem inneren und $r_{a}$ dem äußeren Radius des Schwungrads. Die entsprechenden Werte können Sie aus der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/Datenblatt.md) entnehmen.

#### Aufgabe 1.3: Schwingung mit äußerer Dämpfung

Sie können den Strom $I_{\mathrm{B}}$ zur Erzeugung des Magnetfelds aus dem CASSY-System steuern. Führen Sie die folgenden Aufgabenteile für mindestens vier verschiedene Werte von $I_{\mathrm{B}}$ durch. **Wir schlagen $I_{\mathrm{B}}=100,200,400,700\hspace{0.05cm}\mathrm{mA}$ vor. **

Bestimmen Sie $\lambda$ auf zwei Arten: 

- Zum einen durch Anpassung des Modells aus Gleichung (**(6)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/doc/Hinweise-Aufgabe-1.md)) an die aufgezeichneten Daten, wie für Aufgabe 1.1. 
- Zum anderen aus dem Dämpfungsverhältnis aus Gleichung (**(7)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/doc/Hinweise-Aufgabe-1.md)). 

Überprüfen Sie die Abhängigkeiten $\omega(I_{\mathrm{B}})$ und $\lambda(I_{\mathrm{B}})$. Korrigieren Sie hierzu $\lambda(I_{\mathrm{B}})$ auf die intrinsische Dämpfung des [Pohlschen Rads](https://de.wikipedia.org/wiki/Pohlsches_Rad) $\lambda_{0}$ aus Aufgabe 1.1 gemäß
$$
\begin{equation*}
\lambda(I_{\mathrm{B}}) \to \hat{\lambda}(I_{\mathrm{B}}) = \lambda(I_{\mathrm{B}})-\lambda_{0}.
\end{equation*}
$$
Bestimmen Sie $Q$ aus Gleichung (**(8)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz/doc/Hinweise-Aufgabe-1.md)).

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Resonanz/doc/Hinweise-Aufgabe-1.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Resonanz)
