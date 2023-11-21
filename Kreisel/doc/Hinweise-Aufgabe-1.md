# Hinweise für den Versuch Kreisel

## Aufgabe 1: Physik starrer Körper [1/3]

### Winkelgeschwindigkeit und Trägheitstensor

In der Mechanik verwenden wir zur Beschreibung der Dynamik eines Massepunkts die physikalischen Größen Geschwindigkeit ($\vec{v}$), Impuls ($\vec{p}$) und Kraft ($\vec{F}$). Mit dem Kreisel betrachten wir einen rotierenden, [starren Körper](https://de.wikipedia.org/wiki/Starrer_K%C3%B6rper), mit endlicher Ausdehnung, zu dessen Beschreibung wir zu $\vec{v}$, $\vec{p}$ und $\vec{F}$ äquivalente Größen heranziehen:  

- Das Äquivalent zu $\vec{v}$ ist die **Winkelgeschwindigkeit** $\vec{\omega}$; 
- das Äquivalent zu $\vec{p}$ ist der **Drehimpuls** $\vec{L}$; und 
- das Äquivalent zu $\vec{F}$ ist das **Drehmoment** $\vec{M}$.  

Für ein gegebenes (infinitesimales) Massenelement $\mathrm{d}m$ wird der Zusammenhang dieser Größen zueinander durch das äußere Produkt ([Kreuzprodukt](https://de.wikipedia.org/wiki/Kreuzprodukt)) "$\times$" mit dem Ortsvektor $\vec{r}$ des Massenelements hergestellt: 
$$
\begin{equation*}
\vec{v} = \vec{r}\times \vec{\omega}; \qquad
\vec{L} = \vec{r}\times \vec{p}; \qquad
\vec{M} = \vec{r}\times \vec{F}. \\
\end{equation*}
$$
Der Zusammenhang zwischen $\vec{L}$ und $\vec{\omega}$ ergibt sich daraus zu 
$$
\begin{equation}
\vec{L} = \vec{r}\times\vec{p} = \mathrm{d}m \left(\vec{r}\times\vec{v}\right) = \mathrm{d}m \left(\vec{r}\times\left(\vec{r}\times\vec{\omega}\right)\right).
\end{equation}
$$
Um das doppelte Kreuzprodukt in Gleichung **(1)** weiter zu diskutieren, greifen wir auf eine Regel aus der [analytischen Geometrie](https://de.wikipedia.org/wiki/Analytische_Geometrie) (die sog. "bac-cab"-Regel) zurück:
$$
\begin{equation*}
\vec{a}\times\vec{b}\times\vec{c} = \big(\vec{b}\cdot\vec{a}\big)\,\vec{c} - \big(\vec{c}\cdot\vec{a}\big)\,\vec{b}
\end{equation*}
$$
Das Kreuzprodukt $\vec{b}\times\vec{c}$ kann durch einen Vektor $\vec{\kappa}$ beschrieben werden, der senkrecht auf die aus $\vec{b}$ und $\vec{c}$ aufgespannte Ebene steht. Das erneute Kreuzprodukt $\vec{a}\times\vec{\kappa}$ führt auf einen Vektor, der wieder in diese Ebene zurückfällt. Als Konsequenz kann der resultierende Vektor als eine Linearkombination aus $\vec{b}$ und $\vec{c}$ geschrieben werden. Diese Linearkombination ergibt sich aus den vorangestellten [Skalarprodukten](https://de.wikipedia.org/wiki/Skalarprodukt). 

Anwendung auf Gleichung **(1)** führt auf: 
$$
\begin{equation}
\begin{split}
&\vec{L} = \mathrm{d}m \left(r^{2}\vec{\omega} - \big(\vec{\omega}\cdot\vec{r}\big)\vec{r}\right)\\
&\\
&L_{i} = \underbrace{\mathrm{d}m \left(r^{2}\delta_{ij} - r_{i}r_{j}\right)}\omega_{j}.\\
&\hphantom{L_{i} = \mathrm{d}m \,r^{2}\,}\equiv \Theta_{ij}\\
\end{split}
\end{equation}
$$
In der zweiten Zeile von Gleichung **(2)** haben wir die Vektoren komponentenweise ausgeschrieben, wobei $i$ und $j$ jeweils unabhängigen Indizes entsprechen. Die komponentenweise Darstellung von Gleichung **(2)** zeigt, dass sich die Komponenten $L_{i}$ durch die lineare Abbildung
$$
\begin{equation*}
L_{i} = \Theta_{ij}\,\omega_{j}
\end{equation*}
$$
aus den Komponenten $\omega_{j}$ ergeben. Dabei kann, je nach Struktur von $\Theta_{ij}$ **jede Komponente** von $\vec{\omega}$ zum Wert jeder Komponente von $\vec{L}$ beitragen. Die Größe
$$
\begin{equation*}
\boldsymbol{\Theta} \equiv \left(\Theta_{ij}\right)
\end{equation*}
$$
bezeichnen wir als [Trägheitstensor](https://de.wikipedia.org/wiki/Tr%C3%A4gheitstensor). Aufgrund seines Transformationsverhaltens unter Drehungen im Raum handelt es sich um einen Tensor 2. Stufe. Konkret als Matrix ausgeschrieben hat $\boldsymbol{\Theta}$ die Form: 
$$
\begin{equation}
\boldsymbol{\Theta} = \mathrm{d}m
\left(
\begin{array}{ccc}
r^{2}-x^{2} & x\,y & x\,z \\
y\,x & r^{2}-y^{2} & y\,z \\
z\,x & z\,y & r^{2}-z^{2} \\
\end{array}
\right).
\end{equation}
$$
Der Trägheitstensor ist durch seine Konstruktion symmetrisch ($\Theta_{ij}=\Theta_{ji}$). Die drei Diagonalelemente von $\boldsymbol{\Theta}$ (die wir im Folgenden auch mit $(\theta_{i};\hspace{0.1cm}i=x,y,z)$ bezeichnen werden) heissen [Trähgeitsmomente](https://de.wikipedia.org/wiki/Tr%C3%A4gheitsmoment). Die drei nicht-diagonalen Elemente heissen [Deviationsmomente](https://de.wikipedia.org/wiki/Deviationsmoment).

### Eigenwertproblem  

Schreibt man Gleichung **(2)** aus erhält man ein gekoppeltes [lineares Gleichungssystem](https://de.wikipedia.org/wiki/Lineares_Gleichungssystem) der Form
$$
\begin{equation}
\left(
\begin{array}{c}
L_{x} \\
L_{y} \\
L_{z} \\
\end{array}
\right)
=
\left(
\begin{array}{ccc}
\Theta_{xx} & \Theta_{xy} & \Theta_{xz} \\
\Theta_{yx} & \Theta_{yy} & \Theta_{yz} \\
\Theta_{zx} & \Theta_{zy} & \Theta_{zz} \\
\end{array}
\right)
\cdot
\left(
\begin{array}{c}
\omega_{x} \\
\omega_{y} \\
\omega_{z} \\
\end{array}
\right),
\end{equation}
$$
wofür wir $\boldsymbol{\Theta}$ als $3\times3$-Matrix dargestellt haben. In bestimmten Fällen kann ein solches Gleichungssystem, durch eine Transformation $\bold{U}$ auf eine geeignete Basis 
$$
\begin{equation*}
\boldsymbol{\widetilde{\Theta}} = \bold{U}\cdot\boldsymbol{\Theta}\cdot\bold{U}^{-1}
\end{equation*}
$$
mit $\bold{U^{-1}U=\mathbb{1}}$, entkoppelt werden, so dass $\boldsymbol{\widetilde{\Theta}}$ die Form einer [Diagonalmatrix](https://de.wikipedia.org/wiki/Diagonalmatrix) annimmt. Die Suche nach solchen Abbildungen $\bold{U}$ bezeichnet man als [Eigenwertproblem](https://de.wikipedia.org/wiki/Eigenwerte_und_Eigenvektoren). Die Matrix $\boldsymbol{\widetilde{\Theta}}$ führt die Basisvektoren des Vektors 
$$
\begin{equation*}
\vec{\tilde{\omega}} \equiv \bold{U}\cdot\vec{\omega}
\end{equation*}
$$
bis auf die Multiplikation mit dem Eigenwert $\theta_{i}$ in sich selbst über. Die Transformation $\bold{U}$ entspricht also einem Wechsel von einer beliebigen [Orthonormalbasis](https://de.wikipedia.org/wiki/Orthonormalbasis) in eine Orthonormalbasis, die durch $\boldsymbol{\widetilde{\Theta}}$ in sich selbst abgebildet wird. 

### Hauptachsentransformation

Die Eigenschaft, dass der Trägheitstensor aus Gleichung **(3)** **symmetrisch** ist, hat für die Lösung des Eigenwertproblems die folgenden weitreichenden Konsequenzen: 

- Für symmetrische Abbildung ist das Eigenwertproblem **immer lösbar**. Die Eigenwerte können allerdings n-fach [entartet](https://de.wikipedia.org/wiki/Eigenwerte_und_Eigenvektoren#Berechnung_der_Eigenwerte) vorliegen. 
- Die Eigenwerte sind **immer reell**.
- Die durch die zugehörigen Eigenvektoren aufgespannten Unterräume stehen **immer senkrecht aufeinander**.

Die Matrizen $\bold{U}$ zur Diagonalisierung von $\boldsymbol{\Theta}$ sind in diesem Fall Rotationsmatrizen mit der (definierenden) Eigenschaft: 
$$
\begin{equation*}
\bold{R}^{-1} = \bold{R}^{\intercal},
\end{equation*}
$$
wobei $\bold{R}^{\intercal}$ der Transponierten von $\bold{R}$ entspricht. Die Lösung des Eigenwertproblems gewinnt dadurch eine **anschauliche geometrische Bedeutung**: 

Es handelt sich um die Drehung von einem allgemeinen in ein spezielles Bezugssystem, in dem die Eigenvektoren des Problems aus Gleichung **(2)** parallel zu den [Hauptträgheitsachsen](https://de.wikipedia.org/wiki/Haupttr%C3%A4gheitsachse) des starren Körpers verlaufen. Diese Achsen sind durch die Form und Massenbelegung des Körpers vorgegeben. 

Das Eigenwertproblem erhält aufgrund dieser Besonderheiten den eigenen Namen [Hauptachsentransformation](https://de.wikipedia.org/wiki/Hauptachsentransformation). Nach Hauptachsentransformation hat Gleichung **(4)** die einfache Form: 
$$
\begin{equation}
\left(
\begin{array}{c}
L_{x} \\L_{y} \\L_{z} \\
\end{array}
\right)
=
\left(
\begin{array}{ccc}
\theta_{x} & 0 & 0 \\
0 & \theta_{y} & 0 \\
0 & 0 & \theta_{z}\\
\end{array}
\right)
\cdot
\left(
\begin{array}{c}
\omega_{x} \\
\omega_{y} \\
\omega_{z} \\
\end{array}
\right),
\end{equation}
$$
oder in Komponentenschreibweise
$$
\begin{equation*}
L_{i} = \theta_{i}\,\delta_{ij}\,\omega_{j}.
\end{equation*}
$$
Die $\{\theta_{i}\}$ heißen in diesem Fall **Hauptträgheitsmomente**.

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel/doc/Hinweise-Aufgabe-1-a.md)

