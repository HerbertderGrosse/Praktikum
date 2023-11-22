# Hinweise für den Versuch Pendel


## Aufgabe 1: Fadenpendel

### Modell des Fadenpendels

Unter Vernachlässigung von Reibungseffekten und bei kleinen Auslenkungen $\varphi_{0}$  wird die Schwingung des Fadenpendels durch die Differentialgleichung des [physikalischen Pendels](https://de.wikipedia.org/wiki/Physikalisches_Pendel) 
$$
\begin{equation}
\begin{split}
&\Theta\ddot{\varphi}+\underbrace{m\,s\,g}\,\varphi=0\\
&\hphantom{\Theta\ddot{\varphi}\quad}\equiv D \\
&\\
&\varphi(t) = \varphi_{0}\sin(\omega_{o}\,t+\phi)
\end{split}
\end{equation}
$$
beschrieben, wobei $\Theta$ dem Trägheitsmoment, $g$ der Erdbeschleunigung, $m$ der Masse und $s$ dem Abstand zwischen Aufhängung und Schwerpunkt des Pendels entsprechen. $D$ bezeichnet das [Direktionsmoment](https://de.wikipedia.org/wiki/Direktionsmoment). Aus Gleichung **(1)** lassen sich die Kreisfrequenz $\omega_{0}$ und Periode $T_{0}$ bestimmen:
$$
\begin{equation}
\omega_{0} = \sqrt{\frac{D}{\Theta}}=\sqrt{\frac{m\,\ell\,g}{\Theta}};\qquad T_{0}=2\pi\sqrt{\frac{\Theta}{D}}=2\pi\sqrt{\frac{\Theta}{m\,\ell\,g}}.
\end{equation}
$$
Mit Hilfe des [Satzes von Steiner](https://de.wikipedia.org/wiki/Steinerscher_Satz) lässt sich $\Theta$ aus dem Trägheitsmoment einer homogenen Kugel  abschätzen: 
$$
\begin{equation}
\Theta = m\,s^{2} + \frac{2}{5}\,m\,r^{2},
\end{equation}
$$
wobei $r$ dem Radius der Kugel entspricht. Beachten Sie, dass $s$ nicht die Länge des Fadens, sondern der Abstand zwischen Aufhängung und Schwerpunkt des Pendels ist. Wenn Sie die Masse des Fadens gegenüber der Masse der Kugel vernachlässigen, fällt der Schwerpunkt des Pendels mit dem Schwerpunkt der Kugel zusammen.

Einsetzen von Gleichung **(3)** in Gleichung **(2)** führt zu einer Bestimmungsgleichung für $g$:
$$
\begin{equation*}
\begin{split}
g = \frac{4\pi^{2}}{T^{2}}\left(s +\frac{2}{5}\frac{r^{2}}{s}\right).
\end{split}
\end{equation*}
$$

### Abweichungen von der Kleinwinkelnäherung

Verlässt man die [Kleinwinkelnäherung](https://de.wikipedia.org/wiki/Kleinwinkeln%C3%A4herung) wird Gleichung **(1)** zu einer nicht-linearen Differentialgleichung der Form 
$$
\begin{equation*}
\begin{split}
&\Theta\ddot{\varphi}+\underbrace{m\,s\,g}\,\sin\varphi=0\\
&\hphantom{\Theta\ddot{\varphi}\quad}\equiv D
\end{split}
\end{equation*}
$$
die zwar immer noch [exakt lösbar](https://de.wikipedia.org/wiki/Mathematisches_Pendel#Exakte_L%C3%B6sung), aber nicht mehr analytisch geschlossen darstellbar ist. Die Lösung erfordert die Verwendung [elliptischer Funktionen](https://de.wikipedia.org/wiki/Jacobische_elliptische_Funktionen#Die_drei_grundlegenden_Jacobischen_Funktionen). Die Periode lässt sich in diesem Fall durch eine Reihenentwicklung annähern, deren erste Korrektur wie folgt aussieht:
$$
\begin{equation}
T_{0}(\varphi_{0}) = T_{0}\left(1+\frac{1}{4}\sin^{2}\left(\varphi_{0}/2\right)\right).
\end{equation}
$$
### Hinweise zur Durchführung

- Bestimmen Sie $T_{0}$ über eine geeignete Anzahl an Perioden. Geben Sie entsprechende Unsicherheiten an.
- Messen Sie zur Überprüfung des funktionalen Zusammenhangs von $T_{0}(\varphi_{0})$, bei großen Winkelauslenkungen am besten fortlaufend, beginnend bei $\varphi_{0}\gtrsim60^{\circ}$. Aufgrund der Dämpfung des Pendels verringert sich $\varphi_{0}$ mit der Zeit von selbst. Gehen Sie dabei wie folgt vor:
  - Bestimmen Sie $T_{0}(\varphi_{0})$ aus einer geeigneten Anzahl an fortlaufenden Perioden. 
  - Warten Sie dann bis $\varphi_{0}$ um etwa $5^{\circ}$ abgenommen hat und bestimmen Sie einen neuen Wert von $T_{0}(\varphi_{0})$. Geben Sie eine geeignete Unsicherheit für Ihre Abschätzung von $\varphi_{0}$ an. 
  - So erhalten Sie eine Messreihe von mindestens 6 Punkten. Stellen Sie die Messreihe in geeigneter Weise graphisch dar und vergleichen Sie die Abhängigkeit mit der Erwartung aus Gleichung **(4)**.

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel)

