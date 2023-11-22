# Hinweise für den Versuch Kreisel

## Aufgabe 2: Kardanisch gelagerter Kreisel [3/4]

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
- Sie verwenden eine Messbox, die die Messwerte automatisch aufnimmt. Hierzu benötigen Sie einen Laptop mit Windows Betriebssystem zur Auslese via USB-Verbindung und die Möglichkeit `python` aus einem Terminal auszuführen. Die Software zur Auslese der  Messbox finden Sie unter [diesem Link](https://github.com/Xraydylan/MessBox). Wenn Sie die Messbox für die Auslese der Daten verwenden möchten sollte diese Software lokal auf dem entsprechenden Laptop installiert sein.

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
- Ohne Gewichte können Sie $\omega_{N}$ bis zu Frequenzen von $\omega/2\pi\approx 10\,\mathrm{Hz}$ noch einigermaßen verlässlich bestimmen; mit Gewichten bis zu Frequenzen von $\omega/2\pi\approx 15\,\mathrm{Hz}$.

Passen die an sich ergebenden Kurven jeweils ein Modell nach Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) an. 

#### Aufgabe 2.3 Präzession

Die Messung von $\Omega$ gleicht im Prinzip der Messung von $\omega_{N}$. Das für die Präzession nötige Drehmoment wird durch ein zusätzliches Gewicht am inneren Kardanrahmen verursacht, das durch einen Stahlstab eingebracht wird, der auf der dem Antriebsflansch gegenüberliegenden Seite, aufgeschraubt wird. 

Messen Sie dann $T=2\pi/\Omega$ mit einer Stoppuhr. Achten Sie darauf vor dem Start jeder Messung alle Nutationsbewegungen am inneren Kardanrahmen sachte abzudämpfen und die Schwanenhalshalterungen aus dem Schwenkbereich des sich drehenden Stabs zu räumen. Kontrollieren $\omega$ sowohl vor, als auch nach der Messung von $T$.

Wiederholen Sie die Messreihe mit verschiedenen Positionen des zusätzlichen Gewichts am Stab und tragen Sie $T(\omega)$ jeweils als Funktion von $\omega$ auf. Sie sollten mindestens 30 Messpunkte aufnehmen, die Sie auf verschiedene Messreihen mit verschiedenen Positionen des Gewichts am Stab aufteilen können. 

Passen Sie an die sich ergebenden Kurven jeweils ein Modell nach Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) an. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-c.md)
