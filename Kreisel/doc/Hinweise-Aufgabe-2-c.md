# Hinweise für den Versuch Kreisel

## Aufgabe 2: Kardanisch gelagerter Kreisel [4/4]

### Hinweise zur Durchführung

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

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-b.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel)
