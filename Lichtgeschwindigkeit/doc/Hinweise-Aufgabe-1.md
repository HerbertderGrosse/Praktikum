# Hinweise für den Versuch Lichtgeschwindigkeit

## Aufgabe 1: Drehspiegelmethode

### Prinzip der Messung

Diese Methode zur Messung von $c$ basiert auf der Vorstellung eines Wellenpakets, das sich mit endlicher *Gruppengeschwindigkeit* zwischen Dreh- und Endspiegel ausbreitet. Um die Strecke zwischen Dreh- und Endspiegel ($a+b$ in der [Skizze](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/Musterprotokoll/Lichtgeschwindigkeit/figures/Drehspiegelmethode.png)) zurückzulegen benötigt das Wellenpaket die endliche Zeit: 

$$
\begin{equation}
\Delta t = \frac{2(a+b)}{c}
\end{equation}
$$
In dieser Zeit hat sich der Drehspiegel, der sich mit der Frequenz $\nu$ dreht um den Winkel 

$$
\begin{equation}
\alpha=2\pi\,\nu\Delta t
\end{equation}
$$
weiter gedreht. Da für die Reflexion am Drehspiegel Einfallswinkel gleich Ausfallswinkel gilt wird der Strahl unter dem Winkel $2\alpha$ vom Drehspiegel zurück reflektiert. Ohne Drehung des Spiegels würde der Strahl in sich selbst zurück reflektiert werden. Durch die Drehung des Spiegels um den Winkel $\alpha$ erscheint der Strahl auf einem Schirm um die Strecke $s$ zu seinem Ursprung versetzt. Der Versatz $s$ ergibt sich (unter Annahme der Kleinwinkelnäherung) aus $\alpha$ nach

$$
\begin{equation}
\frac{s}{\ell} = \tan(2\alpha)\approx2\alpha
\end{equation}
$$
Daraus ergibt sich die Gleichung zur Berechnung von $c$:

$$
\begin{equation}
c = 8\pi\frac{\ell\,\nu\left(a+b\right)}{s}
\end{equation}
$$
Im Aufbau durchläuft der Lichtstrahl einen Strahlteiler, so dass ein Teil des Strahls senkrecht zur Lichtquelle auf einen Schirm projiziert wird. Der Winkel des Strahlteilers muss genau justiert sein, was eine potentielle Quelle systematischer Fehlmessungen darstellt.

### Die Sammellinse im Strahlengang

Die Sammellinse im Strahlengang hat die Funktion den Strahl auf einen Punkt zu fokussieren. Sie wird so aufgestellt, dass ihr Brennpunkt im Drehspiegel liegt. Lichtstrahlen aus dem Brennpunkt werden hinter der Linse auf parallele Bahnen gebeugt. Auf dem Rückweg vom Endspiegel wird der Strahlengang wieder in den Brennpunkt auf dem Drehspiegel zurück fokussiert. **Dies geschieht nur entlang der optischen Achse der Linse**. Durch diese Konstruktion findet eine Auswahl der Lichtpakete statt, die zu einem festen Zeitpunkt $t_{0}$ genau entlang der optischen Achse der Linse reflektiert werden. Der Drehspiegel hat also zu Beginn der "Laufzeitmessung" immer die gleiche Winkelposition, für die ein Gegenstand ($G$) in ein Bild ($B$) abgebildet wird. Für die ($b'$) Bild- und ($g'$) Gegenstandsweite gilt, mit den Angaben aus der [Skizze](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/Musterprotokoll/Lichtgeschwindigkeit/figures/Drehspiegelmethode.png):

$$
\begin{equation}
\begin{split}
&g' = \ell+f \\
&b' = a+b-f
\end{split}
\end{equation}
$$
Unter Verwendung der [Linsengleichung](https://de.wikipedia.org/wiki/Linsengleichung) lässt sich so der Abstand $\ell$ zwischen Laser und Drehspiegel bestimmen, bei dem der Laserstrahl ($G$) als $B$ im Endspiegel abgebildet wird:

$$
\begin{equation}
\begin{split}
&\frac{1}{f} = \frac{1}{g'} + \frac{1}{b'} = \frac{1}{\ell+f} + \frac{1}{a+b-f}; \\
&\\
&\frac{1}{\ell+f} = \frac{1}{a+b-f} - \frac{1}{f} = \frac{a+b-2f}{(a+b-f)\,f}; \\
&\\
&\ell = \frac{(a+b-f)\,f}{a+b-2f} -f = \frac{(a+b-f)\,f - (a+b-2f)\,f}{a+b-2f};\\
&\\
&\ell= \frac{f^{2}}{a+b-2f}.
\end{split}
\end{equation}
$$
Mit den vorgegebenen Werten von $a$, $b$, $f$ und der Position des Drehspiegels ergibt sich die optimale Position $\ell$ des Lasers. Da die Position des Lasers fest vorgegeben ist sollten Sie an dieser Stelle nur verfizieren, ob und dass die vorgenommene Justierung sinnvoll ist.

### Hinweise zur Durchführung

- Tragen Sie Messpunkte für 10–12 Wertepaare aus $\nu$ und $s$ graphisch auf und nehmen Sie eine geeignete Anpassung vor. Begründen Sie das der Anpassung zu Grunde gelegte Modell.
- Geben Sie ein Maß für die Güte der Anpassung (*goodness of fit*) als $\chi^{2}/\mathrm{ndof}$ und als $p$-Wert an und bewerten Sie die Anpassung. 
- Überlegen Sie welche äußeren Parameter Sie für die Bestimmung von $c$ noch kontrollieren müssen und wie gut dies der Fall ist.
- Geben Sie Ihr Ergebnis aus der Anpassung mit statistischen und systematischen Unsicherheiten an. 

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit)
