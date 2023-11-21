# Hinweise für den Versuch Kreisel

## Aufgabe 2: Kardanisch gelagerter Kreisel

### Hinweise zur Durchführung

#### Antrieb des Kreisels

Der Kreisel wird mit einem regelbaren Antriebsmotor mit biegsamer Welle in Schwung gebracht. 

- Stellen Sie die Drehzahlsteuerung vor jedem Kreiselanwurf auf Null zurück. 
- Der Antriebsmotor sollte immer im Rechtslauf und im Drehzahlbereich zwischen $0-3500\,\text{Umdrehungen pro min}$ betrieben werden. 
- Vergewissern Sie sich vor jedem Kreiselanwurf, dass die biegsame Welle am Motorflansch fest aufsitzt und dass sie möglichst wenig gebogen
  ist. 
- Sorgen Sie durch geeigneten Druck für einen guten mechanischen Kontakt mit der Sägezahnkupplung.
- Es bietet sich an, dass eine Person die Welle hält, während eine andere Person die Drehzahl des Motors langsam hochregelt. 
- Wenn Sie die biegsame Welle nicht benötigen, lagern Sie diese bitte in gestreckter Haltung.

#### Frequenzbestimmung am Kreisel

Zur Frequenzbestimmung am Kardankreisel gibt es zwei auf Schwanenhalshalterungen montierte Bewegungssensoren. Die periodischen Bewegungen der Rotation ($\vec{\omega}$) und der Nutation ($\vec{\omega}_{N}$) werden durch Fototransistoren in elektrische Pulse umgesetzt, die über Pulszähler direkt als Frequenzen angezeigt werden. 

Zur Bestimmung von $\vec{\omega}$ befindet sich ein reflektierender Streifen auf den Rotor. Biegen Sie die Schwanenhalshalterung so, dass sich das Dioden/Fototransistorelement fast senkrecht etwa $1\,\mathrm{cm}$ über der Rotationsfläche befindet. Zwei LED-Leuchten an der Schwanenhalshalterung geben Aufschluss über eine gute Positionierung:

- LED-1 sollte bei Betriebsbereitschaft immer an sein.
- LED-2 sollte regelmäßig mit aufgenommenen Frequenz blinken. 

Wenn LED-2 dunkel bleibt, ist der Lichtreflex zu schwach; bei Dauerlicht ist er zu intensiv. Als Regelparameter verwenden Sie den Abstand und den Winkel
des Dioden/Fototransistorelements zur Oberfläche des Rotors.

Die Nickbewegung des inneren Kardanrahmens aufgrund der Nutation mit der Frequenz $\vec{\omega}_{N}$ wird mit Hilfe der zweiten Schwanenhalhalterung erfasst. Positionieren Sie hierzu das Dioden/Fototransistorelement so, dass der auf dem Rand des inneren Kardanrahmen befindliche Reflektorstreifen periodisch erfasst werden kann. 

Die Frequenzzähler werden über den A-Eingang gespeist. Die Funktion „FA“ (Frequenz an A) sollte beim Einschalten der Geräte standardmäßig aktiviert sein. Mit den weiteren Einstellungen „Auto“-Triggerung und Dämpfung „1-25“ sollte ein sorgloser Messbetrieb gewährleistet sein. Die Frequenzzählung erfolgt kontinuierlich. Für die Ablesung können beide Frequenzzähler gleichzeitig mit
einem Schalter am Kontrollkästchen angehalten werden.

Die Präzessionsbewegung sollten Sie per Hand mit einer Stoppuhr aufnehmen.

#### Aufgabe 2.1 Dämpfung

Bringen Sie den Kreisel für diese Messung mit Hilfe des Motors auf etwa $2000\,\text{Umdrehungen pro min}$. Bis der Kreisel zum Stillstand kommt, vergehen daraufhin etwa $35\,\mathrm{min}$. Sie können die Dämpfungskurve auf zweierlei Wese aufnehmen: 

- Sie protokollieren $\omega(t)$ alle $30\,\mathrm{s}$. Auf diese Weise erhalten Sie etwa 60 Messwerte;
- Sie verwenden eine Messbox, die die Messwerte automatisch aufnimmt. Hierzu benötigen Sie einen Laptop mit einem Windows Betriebssystem zur Auslese der Messbox via USB-Verbindung.

Tragen Sie die Messwerte als Funktion von $t$ auf. Es empfiehlt sich ein phänomenologisches Modell der Art
$$
\begin{equation*}
\omega(t, \omega_{0}, \alpha, \beta, \gamma) = \omega_{0}\,e^{-\alpha\,t} + \beta\,t^{\gamma}
\end{equation*}
$$
mit den freien Parametern $\omega_{0}$, $\alpha$, $\beta$ und $\gamma$ an die Daten anzupassen. Der Term $t^{\gamma}$ des Modells beinhaltet Reibungseffekte in der Lagerung des Rotors. 

#### Aufgabe 2.2 Nutation

Bringen Sie den Kreisel für diese Messung mit Hilfe des Motors auf etwa $1000\,\text{Umdrehungen pro min}$. Aufgrund der Konstruktion treiben Sie den Kreisel in seiner Figurenachse (d.h. mit $\vec{L}\parallel\vec{\omega}$) an.  Um eine Nutationsbewegung zu erhalten müssen Sie $\vec{\omega}$ aus der Figurenachse auslenken. Dies erreichen Sie durch einen kräftigen Stoß mit der Faust auf den inneren Kardanrahmen. 

Positionieren Sie zur Bestimmung von $\omega_{N}$ eine der Schwanenhalshalterungen so, dass sie die Reflektor-beklebte Kante des inneren Kardanrahmens periodisch erfasst. Durch die Reibung in den Lagern des inneren Kardanrahmens wird die Nutationsbewegung relativ schnell gedämpft. 

Gehen Sie dann wie folgt vor:

- Schlagen Sie den inneren Kardanrahmen zur Bestimmung eines Stichprobenmittels (und entsprechender Unsicherheiten) einige Male an. 
- Beginnen Sie mit der jeweils nächsten Messung, wenn $|\vec{\omega}/2\pi|$ um etwa $0,5\,\mathrm{Hz}$ gesunken ist. Auf diese Weise können Sie bis zu 30 Messungen aufnehmen. 
- Tragen Sie dann $\omega_{N}$ als Funktion von $\omega$ auf. Beachten Sie hierzu, dass Sie die Wiedergabe von $\omega_{N}$ und $\omega$ zum Ablesen der Werte an beiden Frequenzzählern gleichzeitig anhalten können (siehe oben).
- Führen Sie eine Messreihe ohne und eine zweite Messreihe mit Zusatzgewichten an den Enden des inneren Kardanrahmens durch. 
- Schrauben Sie hierzu die Zusatzgewichte zusammen mit zwei $0,5\,\mathrm{mm}$ dicken Unterlegscheiben aus Teflon auf die überstehenden Gewinde der inneren Kardanachse auf. Positionieren Sie die Zylinder so, dass deren Symmetrieachsen parallel zur Senkrechten (und damit parallel zur Drehachse des äußeren Kardanrahmens) stehen, um die Berechnung der durch die Gewichte zusätzlich eingebrachten Trägheitsmomente in $\theta_{x}^{(a)}$ nicht unnötig zu erschweren. Schrauben Sie die Gewichte gerade so fest, dass sie durch die Nutationsbewegung nicht aus ihrer variablen Lage gebracht werden; die Teflonscheiben sind flexibel und sollten den nötigen Spielraum hierzu bieten.
- Die zylindrischen Zusatzgewichte führen zu einem wesentlich höherem Trägheitsmoment des äußeren Kardanrahmens um die Senkrechte, woraus eine entsprechend veränderte Abhängigkeit zwischen $\omega_{N}$ und $\omega$ resultiert. 
- Ohne Gewichte können Sie $\omega_{N}$ bis zu Frequenzen von $\omega/2\pi\approx 10\,\mathrm{Hz}$ noch einigermaßen verlässlich bestimmen; mit Gewichten bis zu Frequenzen von $\omega/2\pi\approx 25\,\mathrm{Hz}$.

Passen die an sich ergebenden Kurven jeweils ein Modell nach Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) an. 

#### Aufgabe 2.3 Präzession

Die Messung von $\Omega$ gleicht im Prinzip der Messung von $\omega_{N}$. Das für die Präzession nötige Drehmoment wird durch ein zusätzliches Gewicht am inneren Kardanrahmen verursacht, das durch eine Stahlstange eingebracht wird, die auf der dem Antriebsflansch gegenüberliegenden Seite, aufgeschraubt wird. 

Die Messung von $\Omega$ erfolgt dann per Hand, mit einer Stoppuhr. Achten Sie darauf vor dem Start jeder Messung alle Nutationsbewegungen am inneren Kardanrahmen sachte abzudämpfen und die Schwanenhalshalterungen aus dem Schwenkbereich der sich drehenden Stahlstange zu räumen. Kontrollieren $\omega$ sowohl vor, als auch nach der Messung von $\Omega$.

Wiederholen Sie die Messreihe mit verschiedenen Gewichten an der Metallstange und tragen Sie $\Omega$ jeweils als Funktion von $\omega$ auf. Sie sollten mindestens 30 Messpunkte aufnehmen, die Sie auf verschiedene Messreihen mit verschiedenen Gewichten am Stab aufteilen können. 

Passen die an sich ergebenden Kurven jeweils ein Modell nach Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) an. 

#### Aufgabe 2.4

Die Trägheitsmomente $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ lassen sich aus den Messungen der **Aufgaben 2.2** und **2.3** auf zweierlei Art und Weise bestimmen: 

- Zum einen, indem an alle Messungen als unabhängig betrachtet und die gesuchten Größen daraus Schritt für Schritt extrahiert (**Methode-1**). 
- Zum anderen, indem man, mit Hilfe der *Multifit* Methode aus *kafe2*, ein gemeinsames zugrundeliegendes Modell gleichzeitig an alle Messungen anpasst (**Methode-2**). 

Methode-2 ist zwar technisch anspruchsvoller, es ist jedoch die bessere Methode, weil sie es erlaubt, alle Messpunkte gleichzeitig für die Bestimmung von drei gesuchten Parametern zu nutzen. Nach Methode-1 kann man immer nur einen Bruchteil der aufgezeichneten Messpunkte zur Bestimmung einzelner Parameter nutzen, deren individuelle statistische Unsicherheiten dadurch größer sind. 

##### Methode-1

###### Schritt-1:

Hierbei nutzen Sie zunächst die Messung von $\omega_{N}$ als Funktion von $\omega$ zur Berechnung von $\theta_{x}'$ nach Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md))
$$
\begin{equation}
\omega_{N} = \omega\,\frac{\theta_{z}^{\prime}}{\sqrt{\theta_{x}^{\prime}\,\theta_{y}^{\prime}}}.
\end{equation}
$$
Dabei nutzen Sie die Messung **einmal mit** und **einmal ohne Zusatzgewichte**, um die Ambiguität zwischen $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ in der Steigung der jeweiligen Ursprungsgeraden aufzuheben. 

Zunächst bestimmen Sie die Steigungen $m_{1}$ und $m_{2}$ mit und ohne Zusatzgewichte: 
$$
\begin{equation*}
\begin{split}
&\omega_{N} = m_{i}\,\omega; \\
&\\
&m_{1} = \frac{\theta_{z}'}{\sqrt{\theta_{x}'\,\theta_{y}'}}; \qquad 
m_{2} = \frac{\theta_{z}'}{\sqrt{(\theta_{x}'+\theta_{\mathrm{Zylinder}})\,\theta_{y}'}}; \\
&\\
&\text{mit dem bekannten Tr\"agheitsmoment:} \\
&\\
&\theta_{\mathrm{Zylinder}} = 2\,\left(\frac{1}{2}m\,r^{2}+m\,\ell^{2}\right),
\end{split}
\end{equation*}
$$
wobei $m$ der Masse und und $r$ dem Radius der jeweils baugleichen Zusatzgewichte und $\ell$ dem Abstand der Schwerpunkte der Zusatzgewichte von der Symmetrieachse des Kreisels entsprechen. 

Aus dem Quotienten 
$$
\begin{equation*}
\begin{split}
&\frac{m_{1}}{m_{2}}=\sqrt{\frac{\theta_{x}'}{\theta_{x}'+\theta_{\mathrm{Zylinder}}}}; \\
&\\
&\theta_{x}' = \frac{\theta_{\mathrm{Zylinder}}}{\frac{m_{2}^{2}}{m_{1}^{2}}-1} \\
\end{split}
\end{equation*}
$$
 lässt sich $\theta_{x}'$ bestimmen.

###### Schritt-2:

Das Trägheitsmoment $\theta_{z}'$ lässt sich aus der Messung aus **Aufgabe 2.3** nach Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) bestimmen:
$$
\begin{equation}
\Omega = \frac{M\,g\,s}{\theta_{z}'}\,\frac{1}{\omega} = \kappa \,\frac{1}{\omega},
\end{equation}
$$
wobei $M$ der Masse und und $s$ dem Abstand des Schwerpunkts des Stabs vom Schwerpunkt des Kreisels und $g$ der Erdbeschleunigung entsprechen. Sie können zur Bestimmung von $\kappa$ die Präzessionsfrequenz $\Omega$ gegen $1/\omega$ auftragen und $\kappa$ als Steigung einer Geraden bestimmen. Besser ist jedoch der Auftrag von $\Omega$ gegen $\omega$ und die direkte Anpassung der Hyperbelgleichung aus Gleichung **(2)**. Letzteres Vorgehen belässt die Grundannahme normalverteilter Unsicherheiten $\Delta\omega_{i}$ auf die Messwerte $\omega_{i}$ entlang der $x$-Achse **unverzerrt**. 

Aus $\kappa$ erhalten Sie $\theta_{z}'$ aus der Gleichung: 
$$
\begin{equation*}
\theta_{z}' = \frac{M\,g\,d}{\kappa}.
\end{equation*}
$$

###### Schritt-3: 

Mit dem Wissen um $\theta_{x}'$ und $\theta_{z}'$ können Sie nun $\theta_{y}'$ am einfachsten aus der zuvor bestimmten Steigung $m_{1}$ bestimmen: 
$$
\begin{equation*}
\begin{split}
& m_{1} = \frac{\theta_{z}'}{\sqrt{\theta_{x}'\,\theta_{y}'}}; \qquad
\theta_{y}' = \frac{\theta_{z}^{\prime\,2}}{m_{1}^{2}\,\theta_{x}'}. \\
\end{split}
\end{equation*}
$$
**Beachten Sie, bei einer Berechnung der Trägheitsmomente auf diese Weise die Fortpflanzung der Unsicherheiten einschließlich der Bestimmung systematischer Unsicherheiten!**

##### Methode-2:

Für die Bestimmung von $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ nach Methode-2 übergeben Sie die Datenpunkte aus den **Aufgaben 2.2** und **2.3** geeignet an die *Mutifit*-Funktion aus *kafe2* und definieren die Modelle direkt nach Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) und Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)). 

Nach erfolgreicher Implementierung erhalten Sie die Zentralwerte und Unsicherheiten auf $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ aus der Anpassung. 

##### Bestimmung der Masse des Rotors

Die Masse des Rotors können Sie aus der Annahme abschätzen, dass dieser in erster Näherung einem flachen Zylinder entspricht. Daraus besteht der folgende Zusammenhang
$$
\begin{equation*}
\theta_{z}' = \frac{1}{2}M_{\mathrm{Rotor}}\left(\frac{d}{2}\right)^{2},
\end{equation*}
$$
 wobei $M_{\mathrm{Rotor}}$ der Masse und $d$ dem Durchmesser des Rotors entsprechen. aus der Kenntnis von $\theta_{z}'$ und $d$ lässt sich so $M_{\mathrm{Rotor}}$ abschätzen.

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel)
