# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 2: Mathematisches Pendel

### Parameterschätzung mit der $\chi^{2}$-Methode

Bei der [Parameterschätzung](https://de.wikipedia.org/wiki/Sch%C3%A4tzfunktion) legen Sie einer Menge von $n$ Datenpunkten $\{r_{i}=(x_{i}, y_{i}):\hspace{0.05cm} i=1\ldots n\}$ ein Modell $\Omega(\{\theta_{j}\})$ zugrunde das von $k$ Parametern $\{\theta_{j}\}$ abhängen kann. Im Rahmen einer [Optimierungsaufgabe](https://de.wikipedia.org/wiki/Optimierungsproblem) sind die Werte der $\{\theta_{j}\}$ zu bestimmen, mit denen $\Omega(\{\theta_{j}\})$ die $\{r_{i}\}$ am besten beschreibt. Für physikalische Messungen wird die Möglichkeit des Modells die Daten zu beschreiben auf Grundlage der Unsicherheiten $\{\Delta r_{i}=(\Delta x_{i}, \Delta y_{i})\}$ eingeschätzt, mit denen die $\{r_{i}\}$ bestimmt wurden. 

Die Übersetzung dieser Aufgabenstellung in ein mathematisches [Modell](https://de.wikipedia.org/wiki/Statistisches_Modell) erfolgt mit Hilfe einer **Kostenfunktion**, die bei der im Praktikum vorwiegend verwendeten Methode zur Parameterschätzung der [Zustandssumme](https://de.wikipedia.org/wiki/Zustandssumme) der Abstände zwischen $\Omega(\{\theta_{j}\})$ und den $\{r_{i}\}$
$$
\begin{equation}
z = \sum\limits_{i=1}^{n}\frac{||\Omega(\{\theta_{j}\}-r_{i}||_{2}^{2}}{\Delta r_{i}}
\end{equation}
$$
entspricht. Die Optimierungsaufgabe besteht darin, den kleinsten Wert von $z$ im Raum der Parameter $\{\theta_{j}\}$ zu finden. Diese Methode wird als "Methode der kleinsten Quadrate" oder $\chi^{2}$-Methode bezeichnet. Der Name leitet sich aus der folgenden Tatsache ab: 

Interpretieren wir die $\{r_{i}\}$ als [Zufallsvariablen](https://de.wikipedia.org/wiki/Zufallsvariable), die nach einer allgemeinen [Wahrscheinlichkeitsdichte](https://de.wikipedia.org/wiki/Wahrscheinlichkeitsdichtefunktion) verteilt sind, dann ist $z$, das eine Funktion von Zufallsvariablen ist, ebenfalls eine Zufallsvariable. Man bezeichnet $z$ allgemein als [Schätzfunktion](https://de.wikipedia.org/wiki/Sch%C3%A4tzfunktion). Diese ist wiederum selbst nach einer Wahrscheinlichkeitsdichte, der [Stichprobenverteilung](https://de.wikipedia.org/wiki/Sch%C3%A4tzfunktion#Stichprobenverteilung), verteilt. Im allgemeinen ist es nicht möglich für die Stichprobenverteilung eine mathematisch geschlossene Form anzugeben. Sind die $\{r_{i}\}$ aber *normalverteilt*, dann folgt die Zufallsvariable $z$ der [$\chi^{2}(z, n_{\mathrm{dof}})$-Verteilung](https://de.wikipedia.org/wiki/Chi-Quadrat-Verteilung)  für $n_{\mathrm{dof}}$ Freiheitsgrade, mit $n_{\mathrm{dof}}\equiv n-k$. Der Begriff [Freiheitsgrad](https://de.wikipedia.org/wiki/Anzahl_der_Freiheitsgrade_(Statistik)) leitet sich aus der folgenden beispielhaften Vorstellung ab: 

In der $xy$-Ebene wird eine Gerade durch zwei Datenpunkte $(x_{1}, y_{1})$ und $(x_{2}, y_{2})$ bestimmt. Das mathematische Modell zur Beschreibung einer Geraden, $\Omega(a_{0}, a_{1}, x): a_{1}\hspace{0.05cm}x+a_{0}=0$, besitzt zwei Parameter $a_{0}$ und $a_{1}$. Durch die Punkte $(x_{1}, y_{1})$ und $(x_{2}, y_{2})$ sind $a_{0}$ und $a_{1}$ eindeutig bestimmt und es besteht keine Freiheit die Parameter zu variieren. Ein Modell, das genauso viele Parameter besitzt, wie Messpunkte zur Anpassung zur Verfügung stehen, bezeichnet man als *saturiert*. Sobald ein weiterer Punkt $(x_{3}, y_{3})$ hinzukommt ist nicht mehr garantiert, dass $\Omega$ durch geeignete Wahl der Parameter $a_{0}$ und $a_{1}$ jeden Punkt exakt berührt und das Minimum von $z$ wird nicht mehr trivial gefunden. Das Modell hat einen Freiheitsgrad, aus dem ein nicht-triviales Minimum abgeleitet werden kann.  

Zur Vereinfachung der Diskussion macht man in Textbüchern oft die folgenden Annahmen, **die i.a. jedoch eher selten gegeben sind**:  

- Die Werte $\{x_{i}\}$ sind [Ausprägungen](https://de.wikipedia.org/wiki/Statistische_Variable) einer [Zufallsgröße](https://de.wikipedia.org/wiki/Zufallsvariable) $x$, die *keine* Unsicherheiten haben;
- Das Modell $\Omega(\{\theta_{j}\},x)$ ist dann eine Funktion von $x$ und der Parameter $\{\theta_{j}\}$.

In diesem Fall nimmt Gleichung **(1)** die geläufigere Form 
$$
\begin{equation}
z = \sum\limits_{i=1}^{n}\frac{\left(\Omega(\{\theta_{j}\},x_{i})-y_{i}\right)^{2}}{\Delta y_{i}}
\end{equation}
$$
an. 

Die Optimierungsaufgabe für Gleichung **(2)** kann grundsätzlich analytisch geschlossen gelöst werden, solange $\Omega$ nur *linear* von den Parametern $\{\theta_{j}\}$ abhängt. Heutzutage werden solche (und weitaus kompliziertere) Parameterschätzungen algorithmisch von Computern durchgeführt. Mit den Programmpakten *kafe2* und *PhyPraKit* stehen Ihnen geeignete Werkzeuge hierzu zur Verfügung. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-b.md)

