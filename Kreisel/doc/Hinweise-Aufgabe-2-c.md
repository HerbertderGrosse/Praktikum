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
&\omega_{N} = \mu_{i}\,\omega; \\
&\\
&\mu_{1} = \frac{\theta_{z}'}{\sqrt{\theta_{x}'\,\theta_{y}'}}; \qquad 
\mu_{2} = \frac{\theta_{z}'}{\sqrt{(\theta_{x}'+\theta_{\mathrm{Z}})\,\theta_{y}'}}; \\
&\\
&\text{mit dem bekannten Tr\"agheitsmoment:} \\
&\\
&\theta_{\mathrm{Z}} = 2\,\left(\frac{1}{2}m_{\mathrm{Z}}\,r_{\mathrm{Z}}^{2}+m\,\ell^{2}\right),
\end{split}
\end{equation*}
$$
wobei $m_{\mathrm{Z}}$ der Masse und und $r_{\mathrm{Z}}$ dem Radius der jeweils baugleichen Zusatzgewichte und $\ell$ dem Abstand der Schwerpunkte der Zusatzgewichte von der Symmetrieachse des Kreisels entsprechen. 

Aus dem Quotienten 
$$
\begin{equation*}
\begin{split}
&\frac{\mu_{1}}{\mu_{2}}=\sqrt{\frac{\theta_{x}'}{\theta_{x}'+\theta_{\mathrm{Z}}}}; \\
&\\
&\theta_{x}' = \frac{\theta_{\mathrm{Z}}}{\frac{\mu_{2}^{2}}{\mu_{1}^{2}}-1} \\
\end{split}
\end{equation*}
$$
 lässt sich $\theta_{x}'$ bestimmen.

###### Schritt-2:

Das Trägheitsmoment $\theta_{z}'$ lässt sich aus der Messung aus **Aufgabe 2.3** nach Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) bestimmen:
$$
\begin{equation}
T(\omega) = \frac{2\pi\,\theta_{z}'}{m_{\mathrm{Stab}}\,g\,s}\,\omega = \kappa \,\omega,
\end{equation}
$$
wobei $m_{\mathrm{Stab}}$ der Masse und und $s$ dem Abstand des Schwerpunkts des Stabs vom Schwerpunkt des Kreisels und $g$ der Erdbeschleunigung entsprechen. Aus $\kappa$ erhalten Sie $\theta_{z}'$ aus der Gleichung: 

$$
\begin{equation*}
\theta_{z}' = \frac{m_{\mathrm{Stab}}\,g\,s\,\kappa}{2\pi}.
\end{equation*}
$$

###### Schritt-3: 

Mit dem Wissen um $\theta_{x}'$ und $\theta_{z}'$ können Sie nun $\theta_{y}'$ am einfachsten aus der zuvor bestimmten Steigung $\mu_{1}$ bestimmen: 
$$
\begin{equation*}
\begin{split}
& \mu_{1} = \frac{\theta_{z}'}{\sqrt{\theta_{x}'\,\theta_{y}'}}; \qquad
\theta_{y}' = \frac{\theta_{z}^{\prime\,2}}{\mu_{1}^{2}\,\theta_{x}'}. \\
\end{split}
\end{equation*}
$$
**Beachten Sie, bei einer Berechnung der Trägheitsmomente auf diese Weise die Fortpflanzung der Unsicherheiten einschließlich der Bestimmung systematischer Unsicherheiten!**

##### Methode-2:

Für die Bestimmung von $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ nach Methode-2 übergeben Sie die Datenpunkte aus den **Aufgaben 2.2** und **2.3** an die `MultiFit`-Funktion aus dem Programm-Paket *kafe2* und definieren die Modelle direkt nach Gleichung (**(1)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)) und Gleichung (**(3)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-a.md)). Ein Beispiel für die Nutzung finden Sie in der offiziellen Dokumentation des Programmpakets [hier](https://kafe2.readthedocs.io/en/latest/parts/beginners_guide.html#multifit). Eine lauffähige Adaption mit weiteren Erklärungen finden im `tools`-Verzeichnis dieses Repositories [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/tools/kafe2_example_MultiFit.ipynb).

Zur Implementierung eines geeigneten Objekts der `MultiFit`-Klasse sollten Sie zwei `XYFit`-Objekte zu den Modellen $\omega_{N}^{(1)}(\omega, \theta_{z}', \theta_{y}', \theta_{z}')$ und $\omega_N^{(2)}(\omega, \theta_{z}', \theta_{y}', \theta_{z}', \theta_{\mathrm{Z}})$ für die Messungen der Nutation und $i$ `XYFit`-Objekte zu den Modellen $T^{(i)}(\omega, \theta_{z}', m_{\mathrm{Stab}}^{(i)}, s^{(i)}, g)$ für die Messung(en) der Präzession definieren, wobei $i$ den verwendeten Konfigurationen mit zusätzlichem Gewicht am Stahlstab entsprechen. Geben Sie für jedes `XYFit`-Objekt auch die Unsicherheiten auf $\omega$ individuell an. Da es sich für jede Messung um neu aufgenommene Messpunkte handelt sind die Unsicherheiten zu verschiedenen `XYFit`-Objekten (im Gegensatz zum oben verlinkten Beispiel einer Strom-Spannungs Kennlinie) **nicht korreliert**. 

Nach erfolgreicher Implementierung erhalten Sie die Zentralwerte und Unsicherheiten auf $\theta_{x}'$, $\theta_{y}'$ und $\theta_{z}'$ aus der Anpassung. 

##### Bestimmung der Masse des Rotors

Die Masse des Rotors können Sie aus der Annahme abschätzen, dass dieser in erster Näherung einem flachen Zylinder entspricht. Daraus besteht der folgende Zusammenhang
$$
\begin{equation*}
\theta_{z}' = \frac{1}{2}M_{\mathrm{Rotor}}\left(\frac{d_{\mathrm{Rotor}}}{2}\right)^{2},
\end{equation*}
$$
 wobei $M_{\mathrm{Rotor}}$ der Masse und $d_{\mathrm{Rotor}}$ dem Durchmesser des Rotors entsprechen. aus der Kenntnis von $\theta_{z}'$ und $d_{\mathrm{Rotor}}$ lässt sich so $M_{\mathrm{Rotor}}$ abschätzen.

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Kreisel/doc/Hinweise-Aufgabe-2-b.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel)
