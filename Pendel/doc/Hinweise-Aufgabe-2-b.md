# Hinweise für den Versuch Pendel


## Aufgabe 2: Reversionspendel

### Hinweise zur Durchführung

#### Aufgabe 1.1: Funktionsweise

Beachten Sie zur Bearbeitung dieser Aufgabe die folgenden Punkte und beantworten Sie die entsprechenden Fragen: 

- Berechnen Sie aus dem einfachen Modell eines dünnen Stabs mit den Abmessungen des im Praktikum verwendeten Pendels die konkreten Werte für $\Theta$, $s$ und $\ell_{r}$. 
- Das Pendel im Praktikum besteht nicht nur aus einem dünnen Stab. Es besitzt Halterungen, um $K$ und $K'$ zu fixieren. Wie groß sind, Ihrer Erwartung nach, die Abweichungen dieses reellen Pendels von der oben gemachten, vereinfachenden Annahme eines dünnen Stabs,für die berechneten Werte? 

#### Aufgabe 1.2: Bestimmung von $g$

Gehen Sie für die Bestimmung von $\ell_{r}$ wie folgt vor: 

- Verschieben Sie $K'$ in einem Intervall um den in Aufgabe 1.1 abgeschätzten Wert von $\ell_{r}$ und messen Sie $d$, als den Abstand zwischen $K$ und $K'$ aus. 

- Bestimmen Sie für feste, so ermittelte, Werte von $d$ sowohl $T_{0}$ für das Pendel auf dem Auflagepunkt $A$ (**Skizze 1**, links), als auch $T_{0}'$ für das Pendel auf dem Auflagepunkt $A'$ (**Skizze 1**, rechts). Beschränken Sie sich auf kleine Auslenkungen des Pendels, so dass die Kleinwinkelnäherung anwendbar ist.

- Zur Messung wird eine Lichtschranke mit Zeiterfassungsgerät benutzt. Beachten Sie, dass eine Messung nur bei offener Schranke, d.h. wenn die Leuchtdiode an der Schranke rot leuchtet, gestartet werden kann. Wählen Sie als relative Unsicherheit für die Zeitmessung $\Delta t/t=\pm 0,2\%$. Hinzu zu rechnen ist noch eine weitere von der Messzeit unabhängige Unsicherheit aus der Digitalisierung, die Sie aus einer Messreihe bestimmen können, bei der Sie nur die einstellbare Anzahl der Schwingungen für die Zeitmessung an der Messautomatik verändern. Die Lichtschranke muss hierzu sorgfältig justiert werden, so dass das Schalten nahe beim Nulldurchgang erfolgt.

- Führen Sie auf diese Weise eine Messreihe für etwa 10 verschiedene Werte von $d$ durch. 

- Tragen Sie, zur Illustration die Werte von $T_{0}(d)$ und $T_{0}'(d)$ als Funktion von $d$ in das gleiche Diagramm ein. Die Kurven sollten einen Schnittpunkt aufweisen. Zeichnen Sie Unsicherheiten sowohl in $d$ als auch in $T_{0}^{(\prime)}$ in das Diagramm mit ein. 

- Zur Bestimmung von $\ell_{r}$ aus einer Anpassung an die Daten, tragen Sie die Differenz $\Delta T_{0} = T_{0}-T_{0}'$ als Funktion von $d$ in ein weiteres Diagramm ein und bestimmen Sie den Schnittpunkt mit der $x$-Achse ($\Delta T_{0}(d)=0$) aus einer Anpassung an die Daten. Bestimmen Sie auf diese Weise $\ell_{r}$ und $T_{0}(\ell_{r})$ und berechnen Sie daraus $g$. Geben Sie für die Anpassung Unsicherheiten sowohl in $d$ als auch in $\Delta T^{(\prime)}$ an.

- Hinweis: Wählen Sie ein einfaches Modell, aus dem Sie $\Delta T_{0}(d)=0$ leicht aus der Anpassung bestimmen können. Für eine lineare Anpassung ($\Delta T_{0}\propto d$) ist das Vorgehen klar. Für eine quadratische Anpassung ($\Delta T_{0}\propto d^{2}$) empfiehlt sich die Parametrisierung

  ```math
  \begin{equation*}
  \Delta T(d) = \alpha\left(\beta-d\right)^{2}+\gamma, 
  \end{equation*}
  ```

  wobei $\alpha,\beta,\gamma$ freie Parameter der Anpassung sind. So können Sie den Schnittpunkt mit der $x$-Achse als $\beta$ und die entsprechende Unsicherheit darauf als $\Delta\beta$ direkt aus der Anpassung ablesen. Überprüfen Sie die Anwendbarkeit eines solchen Modells zur Beschreibung der Daten mit Hilfe eines *goodness-of-fit* Parameters, wie dem $\chi^{2}$- oder $p$-Wert. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Pendel)

