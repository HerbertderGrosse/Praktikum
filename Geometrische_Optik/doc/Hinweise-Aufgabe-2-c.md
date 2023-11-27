# Hinweise für den Versuch Geometrische Optik

## Aufgabe 2: Vermessung eines Zweilinsensystems $L$ [4/5]

### Bestimmung von $f_{1}$ und $f_{2}$

Zur Lösung dieser Aufgabe stehen Ihnen wieder mehrere Möglichkeiten zur Verfügung: 

#### Methode 1:

Tragen Sie die Kehrwerte der ermittelten Werte von $f$ als Funktion von $d$ auf. Passen Sie entweder das Modell einer Geraden an, aus dem Sie $f_{1}$ und $f_{2}$ aus Steigung und Achsenabschnitt bestimmen können. Alternativ können Sie (Gleichung **(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2.md)) als Modell für die Anpassung verwenden und $f_{1}$ und $f_{2}$ direkt bestimmen.

#### Methode 2:

Zur Beschreibung dieser Methode gehen wir, zur Vereinfachung, davon aus, dass Sie $X$ exakt zwischen $L_{1}$ und $L_{2}$ gewählt haben. In diesem Fall liegen die Scheitelpunkte der Linsen bei $\pm d/2$ und Sie können $f_{1}$ und $f_{2}$ aus (Gleichung **(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2.md)), wie folgt bestimmen:
$$
\begin{equation}
\begin{split}
-\frac{d}{2}-h_{x} = h_{1} = -\frac{f\,d}{f_{1}}\qquad &\longrightarrow \qquad h_{x} = \hphantom{-}\frac{f\,d}{f_{1}}-\frac{d}{2};\\
\frac{d}{2}-h_{x}' = h_{2} = \hphantom{-}\frac{f\,d}{f_{2}} \qquad &\longrightarrow \qquad h_{x}' =  -\frac{f\,d}{f_{2}} + \frac{d}{2}. \\
\end{split}
\end{equation}
$$
Wenn Sie $h_{x}$ und $h_{x}'$ in Ihrem Modell aus (Gleichung **(4)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-a.md)) entsprechend einsetzen 
$$
\begin{equation}
\begin{split}
&x(f, h_{x}) = f\left(1+\frac{1}{\beta}\right)+d\left(\frac{f}{f_{1}}-\frac{1}{2}\right); \\
&\\
&x'(f, h_{x}') = f\left(\beta+1\vphantom{\frac{1}{\beta}}\right)-d\left(\frac{f}{f_{2}}- \frac{1}{2}\right), \\
\end{split}
\end{equation}
$$
können Sie aus der Anpassung $f_{1}$, $f_{2}$ und $f$ gemeinsam bestimmen. 

Wenn Sie diese Methode zur Lösung der Aufgabe verwenden möchten sollten Sie wiederum die `MultiFit`-Funktion aus dem Programm-Paket *kafe2* zur **gleichzeitigen** Bestimmung von $f$, $f_{1}$ und $f_{2}$ verwenden, um den Vorteil nutzen zu können, dass $f$ als gemeinsamer Parameter aus den Datenpunkten beider Messreihen bestimmt werden kann. Zur Implementierung eines geeigneten Objekts der `MultiFit`-Klasse sollten Sie zwei `XYFit`-Objekte zu den Modellen $x(f, \beta, h_{x})$ und $x'(f, \beta, h'_{x})$ aus Gleichung **(2)** definieren. Gehen Sie ansonsten wie [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-b.md) beschrieben vor.

# Navigation

 [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik) | [Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-b.md) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-d.md)
