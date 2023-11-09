# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 2: Mathematisches Pendel

### $\chi^{2}$-Test

Ungeachtet des Umstandes, dass i.a. ein Satz von Parametern $\{\theta_{j}\}$ existiert, für den $z$ minimal wird, kann die Beschreibung der Daten durch $\Omega(\{\theta_{j}\})$ immer noch unzureichend sein. 

Ein Maß dafür, wie gut $\Omega$ die $\{r_{i}\}$, bei optimaler Wahl der $\{\theta_{j}\}$, beschreibt ist der Wert von $z$ im Minimum
$$
\begin{equation*}
\hat{z}=\min_{\{\theta_{j}\}}\left(z(\{r_{i}\}, \{\theta_{j}\})\right).
\end{equation*}
$$
Dabei gilt: 
$$
\begin{equation*}
\begin{array}{ll}
\hat{z}/n_{\mathrm{dof}}\lesssim 1 & \text{das Modell ist mit den Daten verträglich;} \\
\hat{z}/n_{\mathrm{dof}}\gg 1 & \text{das Modell ist mit den Daten nicht verträglich,} \\
\end{array}
\end{equation*}
$$
Den Wert $\hat{z}$ bezeichnet man als **$\boldsymbol{\chi^{2}}$-Wert**. Die Aussagen zu $\hat{z}/n_{\mathrm{dof}}$ gelten mit mathematischer Strenge, d.h., führt eine (statistisch korrekt implementierte) Anpassung auf einen Wert von $\hat{z}/n_{\mathrm{dof}}\gg 1$, dann ist das zugrundeliegende Modell im Rahmen der angegebenen Unsicherheiten $\{\Delta r_{i}\}$ mit den $\{r_{i}\}$ **nicht kompatibel**. 

Dies lässt sich wie folgt verstehen: Der $\chi^{2}$-Wert ist ein Maß für die mittlere Entfernung zwischen $\Omega$ und den $\{r_{i}\}$. Große Werte weisen auf eine schlechte, kleine Werte auf eine gute Übereinstimmung zwischen $\Omega$ und den $\{r_{i}\}$, innerhalb der Streuung ([Varianz](https://de.wikipedia.org/wiki/Varianz_(Stochastik))) der $\{r_{i}\}$, hin. 

Gehen wir davon aus, dass die $\{r_{i}\}$ im Fall wiederholter Messungen *normalverteilt* sind und ihre [Erwartungswerte](https://de.wikipedia.org/wiki/Erwartungswert) wirklich durch $\Omega$ beschrieben werden können, dann folgt $\hat{z}$ der $\chi^{2}(z, n_{\mathrm{dof}})$-Verteilung, deren Erwartungswert $E[\hspace{0.05cm}z\hspace{0.05cm}]=n_{\mathrm{dof}}$ ist. Ein Wert von $\hat{z}/n_{\mathrm{ndof}}\lesssim1$ deutet darauf hin, dass der Verlauf der Modellvorhersage im Mittel innerhalb der Varianzen der $\{r_{i}\}$ liegt. Um diesen Umstand anschaulicher zu machen, wird der $\chi^{2}$-Wert oft zusätzlich in einen ***p*-Wert** übersetzt. 

Der *p*-Wert ist das Integral 
$$
\begin{equation*}
p = \int\limits_{\hat{z}}^{\infty}\chi^{2}(z, n_{\mathrm{ndof}})\,\mathrm{dz}.
\end{equation*}
$$
Unter der Annahme, dass die Erwartungswerte der $\{r_{i}\}$ tatsächlich $\Omega$ folgen, entspricht er der Wahrscheinlichkeit einen Wert von $z\geq\hat{z}$ und damit eine schlechtere Übereinstimmung des Modells mit den $\{r_{i}\}$ zu erhalten, als durch $\hat{z}$ beobachtet. Der *p*-Wert ist selbst wieder eine Zufallsvariable, die, wenn die zu ihrer Berechnung gemachten Annahmen erfüllt sind, in ihrem Wertebereich (zwischen 0 und 1) gleichverteilt ist. 

**Wir geben ein Beispiel:** Sie nehmen die Anpassung eines Modells $\Omega$ mit $k=5$ Parametern an $n=15$ Messpunkte $\{r_{i}\}$ vor, d.h. $n_{\mathrm{dof}}=10$. Nach Anpassung erhalten Sie einen $\chi^{2}$-Wert von 20, d.h. $\hat{z}/n_{\mathrm{dof}}=2$. Unter der Annahme, das die $\{r_{i}\}$ normalverteilt sind und ihre Erwartungswerte wirklich $\Omega$ folgen ist ein Ausgang des Experiments mit einem $\chi^{2}$-Wert $\geq20$ mit einer Wahrscheinlichkeit von 3% zu erwarten. Es bleibt Ihnen überlassen, basierend auf dieser Abschätzung die Aussage, dass die Erwartungswerte der $\{r_{i}\}$ tatsächlich $\Omega$ folgen zu verwerfen oder nicht. 

Um für die Beziehung zwischen $\chi^{2}$-Wert und *p*-Wert ein Gefühl zu bekommen können Sie dieses und ein paar weitere Beispiele mit dieser [Web-Anwendung der University of Illinois](http://courses.atlas.illinois.edu/spring2016/STAT/STAT200/pchisq.html) überprüfen. 

Falls ein Modell wirklich Probleme bei der Beschreibung von Messpunkten hat kann der *p*-Wert rasch Werte $\mathcal{O}(10^{-3}-10^{-10})$ annehmen. Obwohl man sich manchmal aus pragmatischen Gründen dazu entscheidet, ist es grundsätzlich zweifelhaft die Ergebnisse der Anpassung mit sehr niedrigen *p*-Werten (unkommentiert) anzugeben oder weiter zu verarbeiten. 

### Die Programmpakete kafe2 und PhyPraKit

Bei der Verwendung der Programmpakte *kafe2* und *PhyPraKit* wird zu jeder Parameteranpassung der $\chi^{2}$-Wert mit ausgegeben, was Ihnen eine Aussage über die Güte der Anpassung ([*goodness-of-fit*](https://en.wikipedia.org/wiki/Goodness_of_fit)) erlaubt. Sie sollten diesen Wert bei jeder Parameteranpassung mit beachten und diskutieren. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-c.md)

