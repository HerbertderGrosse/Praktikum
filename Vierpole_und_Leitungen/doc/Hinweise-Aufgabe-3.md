# Hinweise für den Versuch Vierpole und Leitungen

## Aufgabe 3: Koaxialkabel

Das [Koaxialkabel](https://de.wikipedia.org/wiki/Koaxialkabel) ist ein typisches Beispiel für eine homogene Leitung zur stromleitungsgebundenen Signalübertragung. Es ist ein zweipoliges Kabel mit konzentrischem Aufbau, bestehend aus einem *Innenleiter* (meist aus Kupfer, auch *Seele* genannt), der in konstantem Abstand von einem hohlzylindrischen *Außenleiter* (ebenfalls aus Kupfer) umgeben ist. Üblicherweise wird das Signal über den Innenleiter übertragen, während der Außenleiter als geerdeter Rückleiter fungiert und den Innenleiter zusätzlich vor [Störstrahlung](https://de.wikipedia.org/wiki/Störausstrahlung_(EMV)) [abschirmt](https://de.wikipedia.org/wiki/Abschirmung_(Elektrotechnik)). Der Raum zwischen Innen- und Außenleiter wird durch ein [Dielektrikum](https://de.wikipedia.org/wiki/Dielektrikum) gefüllt, das anteilig oder vollständig aus Luft bestehen kann. Der Außenleiter ist nochmals durch einen robusten, isolierenden Mantel, z.B. aus PVC, vor der Umgebung geschützt.

Für die Bestimmung der Leitungseigenschaften werden $R'$ und $G'$ meist vernachlässigt. Die Kapazitäts- und Induktivitätsbeläge hängen von der Geometrie des Kabels und der Wahl des Dielektrikums (meist Polyethylen, PE) ab. Es gilt: 
$$
\begin{equation}
L' = \frac{\mu\,\mu_{0}}{2\pi}\ln\left(\frac{d_{a}}{d_{i}}\right); \qquad
C' = \frac{2\pi\,\epsilon\,\epsilon_{0}}{\ln\left(\frac{d_{a}}{d_{i}}\right)}
\end{equation}
$$
wobei $\mu$ der [Permiabilität](https://de.wikipedia.org/wiki/Permeabilit%C3%A4t_(Magnetismus)) und $\epsilon$ der [Permittivität](https://de.wikipedia.org/wiki/Permittivit%C3%A4t) des Dielektrikums, $d_{i}$ dem Durchmesser des Innenleiters uns $d_{a}$ dem Innendurchmesser des Außenleiters entsprechen. Sowohl für Luft, als auch für viele Kunststoffe (wie PE) können Sie in sehr guter Näherung $\mu=1$ annehmen. Beim verlustfreien, idealen Koaxialkabel erfolgt die Leitung des Signals im Dielektrikum, während Innen- und Außenleiter nur die Randbedingungen für die Leitung vorgeben. 

Für den **Wellenleitungswiderstand** gilt: 
$$
\begin{equation}
Z_{0} = \sqrt{\frac{L'}{C'}}=\sqrt{\vphantom{\frac{L'}{C'}}\frac{\mu\,\mu_{0}}{4\pi^{2}\epsilon\,\epsilon_{0}}}\,\ln\left(\frac{d_{a}}{d_{i}}\right).
\end{equation}
$$
Er sollte im Frequenzbereich von einigen $\mathrm{kHz}$ bis zu einigen $\mathrm{GHz}$ (für $\omega\ll\omega_{0}$), in dem Koaxialkabel angewendet werden, weitestgehend frequenzunabhängig sein.  

### Hinweise zur Durchführung

#### Aufgabe 3.1: Bestimmung von $Z_{0}$

Bestimmen Sie $Z_{0}$ analog zu Aufgabe 3.1. Verwenden Sie hierzu eine rechteckförmige Wechselspannung mit $\nu\approx 1,1\hspace{0.05cm}\mathrm{MHz}$. 

#### Aufgabe 3.2: Bestimmung der Verzögerungszeit pro Länge $\tau'$

Bestimmen Sie die Verzögerungszeit pro Länge $\tau'$ des Kabels auf **zwei Arten**:

- Indem Sie das Signal, mit dem Oszilloskop im Zweikanalmodus, gleichzeitig am Anfang und Ende des Kabels betrachten. Wählen Sie eine rechteckförmige Wechselspannung und die Zeitachsendehnung am Oszilloskop maximal. Sie müssen dabei nicht auf Reflexionsfreiheit achten, warum?  
- Indem Sie das Kabelende mit $Z_{\mathrm{A}}=0\hspace{0.05cm}\Omega$ kurzschließen und am Kabelanfang das am Kabelende reflektierte Signal mit dem Referenzsignal des Frequenzgenerators vergleichen. Wählen Sie auch hier eine rechteckige Wechselspannung.
- Vergleichen Sie beide Ergebnisse im Rahmen der bestimmten Unsicherheiten. 

Bei $\tau'$ handelt es sich um den Kehrwert der Gruppengeschwindigkeit $v$ im Kabel.

#### Aufgabe 3.3: Bestimmung von $\epsilon$

Bestimmen Sie $\epsilon$ aus den Werten, die Sie in den Aufgaben 4.1 und 4.2 bestimmt haben:

- Die Bestimmung aus dem gemessenen Wert von $Z_{0}$ erfolgt über Gleichung **(2)**, unter Verwendung der Parameter $d_{a}$ und $d_{i}$.
- Bestimmen Sie für jeden Wert von $\epsilon$ auch die entsprechende Unsicherheit durch Fehlerfortpflanzung. 
- Vergleichen Sie die von Ihnen bestimmten Werte untereinander und vergleichen Sie sie mit der Erwartung aus den Angaben zu diesem Versuch (siehe [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/Datenblatt.md)). 

Die Bestimmung aus $\tau'$ erfolgt aus der Gruppengeschwindigkeit des Signals im Kabel:
$$
\begin{equation*}
\begin{split}
&v = \frac{c}{\sqrt{\epsilon\,\mu}}; \\
&\\
&\epsilon = \frac{c^{2}}{v^{2}\,\mu} = \frac{c^{2}\tau^{\prime 2}}{\mu}
\end{split}
\end{equation*}
$$
wobei $c$ der Lichtgeschwindigkeit (im Vakuum) entspricht. Berechnen Sie $\epsilon$ **aus beiden Messungen aus Aufgabe 3.2**. 

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen)

