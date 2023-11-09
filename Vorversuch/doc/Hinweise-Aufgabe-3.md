# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 3: Schrittweise Erweiterung des Modells

### Das physikalische Pendel

Das Modell des [mathematischen Pendels](https://de.wikipedia.org/wiki/Mathematisches_Pendel) stellt eine starke Vereinfachung der Realität dar: der Faden wird als masselos und die gesamte Masse des Pendels in einem Punkt konzentriert angenommen. Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md)) beschreibt die Bewegung dieses Massepunkts unter Einwirkung des [Schwerefelds](https://de.wikipedia.org/wiki/Schwerefeld) $g$. 

Möchte man die endliche Ausdehnung des Pendels berücksichtigen muss man die physikalischen Eigenschaften starrer Körper berücksichtigen und das Modell des [physikalischen Pendels](https://de.wikipedia.org/wiki/Physikalisches_Pendel) zugrunde legen. Die zugehörige Bewegungsgleichung hat die Form 
$$
\begin{equation}
\Theta\,\,\ddot{\varphi} + Mgs\,\varphi = 0,
\end{equation}
$$
wobei $M$ der gesamten Masse, $s$ dem Abstand zwischen Schwerpunkt und Aufhängung und $\Theta$ dem Trägheitsmoment des Pendels entsprechen.

Während die mathematische Lösung, ihrer Form nach, gleich bleibt nimmt Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md)) die folgende Form an:
$$
\begin{equation}
g = \frac{4\,\pi^{2}}{T^{2}}\frac{\Theta}{Ms}.
\end{equation}
$$
### Die linear [gedämpfte Schwingung](https://de.wikipedia.org/wiki/Schwingung#Linear_ged%C3%A4mpfte_Schwingung)

Legen wir der Messung das Modell einer linearer gedämpften Schwingung zugrunde verändert sich Gleichung **(2)** zur Bestimmung von $g$ wie folgt: 
$$
g = \left(\frac{4\,\pi^{2}}{T^{2}}+\frac{1}{\tau^{2}}\right)\frac{\Theta}{Ms},
$$
wobei $\tau$ einer Abklingzeit in Sekunden entspricht. Wie Sie sehen handelt es sich um eine Korrektur, die die Abschätzung von $g$ zu größeren Werten hin verändert.  

Die Dämpfung hat nicht nur Einfluss auf die Bestimmung von $g$ sondern auch auf die Lösung der (modifizierten) Bewegungsgleichung, die sich wie folgt ändert:
$$
\begin{equation}
\varphi(t) = A\,e^{-t/\tau}\cos(\omega t+\phi);\qquad
\omega=\sqrt{\frac{gMs}{\Theta}-\frac{1}{\tau^{2}}}.
\end{equation}
$$

## Hinweise zur Durchführung

### Aufgabe 3.1: Erste Erweiterung des Modells

Der Übergang zu dieser vermeintlich wahrheitsgetreueren Beschreibung der Realität durch Gleichung **(2)** besitzt einige bemerkenswerte Aspekte, die Sie in Ihrer Auswertung diskutieren sollten: 

- Die mathematische Lösung der Bewegungsgleichung ist zunächst zu der aus **Aufgabe 2** (Gleichung **(2)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md)) äquivalent. Welche Verbesserung der Messung haben Sie also zu erwarten?
- Es fällt auf, dass mit $M$ erstmals die Masse des Pendels selbst in der Formel zur Berechnung von $g$ auftaucht. Das scheint zunächst im Widersprich zu den 1602 gemachten Beobachtungen von [Galileio Galilei](https://de.wikipedia.org/wiki/Galileo_Galilei) zu stehen (siehe Motivation zum P1-Versuch [Pendel](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel)). Wie löst sich dieser Widerspruch auf? 
- Zusätzlich tauchen die Größen $\Theta$ und $s$, in der Formel zur Berechnung von $g$ auf, die mit nicht geringen Unsicherheiten behaftet sind (siehe [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md)). Es kann also passieren, dass die unzureichende Kenntnis von $\Theta$ und $s$ den Wert von $\Delta g^{(3.1)}$ und somit die Sensitivität der Messung auf die Messgröße $g$ **quantitativ *verschlechtert***. Ist das ein Widerspruch zur Annahme, dass es sich um ein besseres Modell zur Beschreibung der Daten handeln sollte?
- Mit diesem Modell stehen Sie vor der Herausforderung **systematische Unsicherheiten** auf $\Delta\Theta$, $\Delta M$ und $\Delta s$ zu einer Gesamtunsicherheit zu kombinieren. Wir haben z.B. zur Berechnung von $\Theta$ (nach dem [Satz von Steiner](https://de.wikipedia.org/wiki/Steinerscher_Satz)) für das Smartphone eine homogene Massenverteilung angenommen. Bedenken Sie hierzu die folgenden Punkte:
  - Wie könnte man testen, wie sehr die Annahme einer homogenen Massenverteilung von der Realität abweicht? 
  - Eine falsche Annahme für die Massenverteilung des Smartphones wirkt sich *gleichzeitig* auf die Bestimmung sowohl von $\Theta$, als auch auf $s$ aus. Die Annahme, das $\Theta$ und $s$ unabhängig sind ist, ist bei einer solchen Vorgehensweise also nicht gerechtfertigt. Wie würden Sie dies in Ihrem Modell für die Kombination der Unsicherheiten berücksichtigen?
  - Wie könnten Sie es experimentell einrichten, dass beide Unsicherheiten paarweise unabhängig sind? 

### Aufgabe 3.2: Zweite Erweiterung des Modells

- Berechnen Sie die Größe der Korrektur 

  ```math
  \begin{equation*}
  \delta g = \frac{\Theta}{Ms\tau^{2}}
  \end{equation*}
  ```

  aus Gleichung **(3)** und den Angaben aus der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md) und beurteilen Sie, ob das bestehende Modell in dieser Hinsicht modifiziert werden sollte oder nicht. 

- Verändern Sie ihr Modell gemäß Gleichung **(4)** (mit oder ohne Korrektur auf $\omega$), passen Sie dieses veränderte Modell an die Daten an und beantworten Sie die folgenden Fragen: 

  - Wie verändert sich die Ausgabe von $n_{\mathrm{dof}}$ und warum?

  - Wie verändert sich die Ausgabe von $\hat{z}/n_{\mathrm{dof}}$?

  - Ist das zugrundeliegende Modell mit den Daten kompatibel? 
  
  - Wie könnten Sie die Hypothese, das das zugrundeliegende Modell die Daten beschreiben kann, einem stärkeren Test unterziehen?


# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch)

