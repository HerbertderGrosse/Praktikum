# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 2: Mathematisches Pendel

### Lineare Fehlerfortpflanzung nach Gauß

Als lineare [Fehlerfortpflanzung](https://de.wikipedia.org/wiki/Fehlerfortpflanzung) bezeichnet man den Vorgang, bei dem die Unsicherheit $\Delta\hat{\theta}$ auf einen bestimmten Wert $\hat{\theta}$ eines Parameters $\theta$, z.B. im Rahmen einer Abbildung
$$
\begin{equation*}
X\to Y: \quad \theta\to f(\theta)
\end{equation*}
$$
als Unsicherheit $\Delta f(\hat{\theta})$ auf den Funktionswert $f(\hat{\theta})$ übertragen wird. Handelt es sich bei $f(\theta)$ um eine in $\theta$ stetig differenzierbare Abbildung, innerhalb der reellen Zahlen, erhält man $\Delta f(\hat{\theta})$ z.B. durch Entwicklung der [Taylorreihe](https://de.wikipedia.org/wiki/Taylorreihe):
$$
\begin{equation*}
\begin{split}
&f(\theta) = f(\hat{\theta}) + \underbrace{\frac{\partial f}{\partial\theta}(\hat{\theta})\,\Delta\hat{\theta}}+\ldots\\
&\hphantom{f(\theta) = f(\hat{\theta}) +,}\equiv\Delta f(\hat{\theta})
\end{split}
\end{equation*}
$$
Dem Umstand, dass die Taylorreihe bereits nach dem ersten Term abbricht tragen wir durch das Attribut *lineare* Fehlerfortpflanzung Rechnung. 

Liegen Unsicherheiten auf mehrere Parameter $\{\hat{\theta}_{j}:\hspace{0.05cm}j=1\ldots n\}$ vor, muss in $n$ Dimensionen gerechnet werden: 
$$
\begin{equation}
\begin{split}
&\Delta f(\boldsymbol{\theta}) = 
\left(\begin{array}{cccc} \partial_{\theta_{0}}f & \partial_{\theta_{1}}f & \ldots & \partial_{\theta_{n}}f
\end{array}\right)\cdot
\underbrace{
\left(\begin{array}{cccc} 
\sigma_{1}^{2} & \sigma_{12} & \ldots & \sigma_{1n} \\
\sigma_{21} & \sigma_{2}^{2} & \ldots & \sigma_{2n}f \\
\vdots &  & \ddots & \vdots \\
\sigma_{n1} & \sigma_{n2} & \ldots & \sigma_{n}^{2} \\
\end{array}\right)}
\cdot
\left(\begin{array}{c} \partial_{\theta_{0}}f \\\partial_{\theta_{1}}f \\ \vdots \\ \partial_{\theta_{n}}f
\end{array}\right).\\
&\hphantom{\Delta f(\boldsymbol{\theta}) =\left(\begin{array}{cccc} \Delta\theta_{0} & \Delta\theta_{1} & \Delta\theta_{1} & \Delta\theta_{1} & \ldots & \Delta\theta
\end{array}\right)}\equiv \Sigma\\
\end{split}
\end{equation}
$$
Dabei entspricht $\boldsymbol{\theta}=\{\theta_{j}\}$ und $\Sigma$ der [Kovarianzmatrix](https://de.wikipedia.org/wiki/Kovarianzmatrix) des Problems, die die Unsicherheiten und [linearen Korrelationen](https://de.wikipedia.org/wiki/Korrelation) der $\{\hat{\theta}_{j}\}$ abbildet.  

Gebräuchlicher ist Gleichung **(1)** in der Gestalt
$$
\begin{equation}
\begin{split}
&\Delta f(\boldsymbol{\theta}) = \sqrt{\sum\limits_{j=1}^{n}\left(\frac{\partial f(\boldsymbol{\theta})}{\partial\theta_{j}}\,\Delta\hat{\theta}_{j}\right)^{2}}, \\
&\text{mit:}\\
&\\
&\Delta\hat{\theta}_{j}^{2} = \sigma_{j}^{2},\\
\end{split}
\end{equation}
$$
die dem Spezialfall entspricht, dass die $\{\theta_{j}\}$ alle paarweise unabhängig sind, wofür $\Sigma$ die Form einer [Diagonalmatrix](https://de.wikipedia.org/wiki/Diagonalmatrix) annimmt. 

Schwierigkeiten bei der linearen Fehlerfortpflanzung bestehen darin, dass die $\{\theta_{j}\}$ i.a. nicht unabhängig und die Korrelationen zwischen den $\{\theta_{j}\}$ nicht bekannt sind. Auch kann es nicht-triviale Korrelationen zwischen den $\{\theta_{j}\}$ geben, für die $\sigma_{ij}=0$ gilt. 

Bei der Anwendung von Gleichung **(2)** sollten Sie sicherstellen (und entsprechend argumentieren), warum Sie annehmen (können), dass die $\{\theta_{j}\}$ paarweise unabhängig sind. Wenn Sie die Möglichkeit haben, einen Parameter $\theta_{j}\pm\Delta \theta_{j}$ direkt und ohne weitere Fehlerfortpflanzung aus einer Parameteranpassung zu bestimmen sollten Sie dieses Vorgehen der linearen Fehlerfortpflanzung nach Möglichkeit vorziehen. 

## Hinweise zur Durchführung

Die zusätzlichen Angaben der Parameter, die Sie zur Lösung dieser Aufgabe benötigen, finden Sie in den Dateien [`parameters_Aufgabe_2.py`](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/params/parameters_Aufgabe_2.py) oder [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md).

### Aufgabe 2.1 Referenzmessung von $T$

- Wählen Sie zur Bestimmung der Referenzmessung einen kurzen Abschnitt aus dem vorliegenden Datensatz frei aus. Dieser Abschnitt sollte ungefähr eine Periode der Pendelschwingung einschließen. Bestimmen Sie daraus $T\pm\Delta T$. 
- Berechnen Sie, mit Hilfe von Gleichung (**(2)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md)), aus $T$ den Wert $g^{(2.1)}\pm\Delta g_{\Delta T}^{(2.1)}$. Den Wert der Größe $\ell$, den Sie für diese Berechnung ebenfalls benötigen, finden Sie z.B. in der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md). 
- Berücksichtigen Sie den Einfluss der Unsicherheit $\Delta\ell$ auf die Bestimmung von $g^{(2.1)}$ als zusätzliche Komponente $\Delta g_{\Delta\ell}^{(2.1)}$, **durch lineare Fehlerfortpflanzung**. 
- Da die Messung von $\ell$ sicher unabhängig von der Erhebung der vorliegenden Messreihe erfolgte ist es legitim $\Delta g_{\Delta\ell}^{(2.1)}$ (als unkorrelierte Unsicherheitsquelle) quadratisch zu $\Delta g_{\Delta T}^{(2.1)}$ zu addieren, um eine Gesamtunsicherheit $\Delta g^{(2.1)}$ zu erhalten.
- Vergleichen Sie Ihr Ergebnis von $g^{(2.1)}\pm\Delta g^{(2.1)}$ im Rahmen seiner Unsicherheiten zu $g_{\mathrm{exp}}\pm\Delta g_{\mathrm{exp}}$. 

### Aufgabe 2.2: Erste Erweiterung der Methodik

Das Modell zur Beschreibung der Daten ist durch Gleichung (**(2)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md)) gegeben. Bei der Verwendung von *PhyPraKit* können Sie ein solches Modell zur Anpassung an die Daten z.B. durch einen "Funktionsblock", wie den im Folgenden gezeigten, in der `yaml`-Datei zur Ansteuerung des Skripts *run_phyFit.py* definieren:

```yaml
model_label: "HARMONIC_PLAIN"
model_function: |
  def my_model(t, A=0.8, T=1.6, phi=0.):
      return A*np.cos(2*np.pi/T*t+phi)
```

Der Funktionsname `my_model` oder das Label `HARMONIC_PLAIN` sind dabei frei gewählt. Beachten Sie, dass die `yaml`-Datei mit diesem Modell auch mit dem Skript *plotData.py* verwendet werden kann. In diesem Fall wird das Modell einfach zusammen mit den Daten dargestellt. Die dabei verwendeten Modellparameter entsprechen den Defaultwerten der Funktionsargumente im oben gezeigten Funktionsblock. 

Wenn Sie das Modell *an die Daten anpassen* möchten führen Sie das Skript *run_phyFit.py* mit der gleichen `yaml`-Datei aus. Aus einer Code-Zelle des Jupyter-notebook könnte dies z.B. so aussehen:

```shell
%run /opt/conda/bin/run_phyFit.py foo.yaml 
```

Die Größe $\hat{z}/n_{\mathrm{dof}}$ und die Werte und Unsicherheiten der angepassten Parameter $\hat{A}$, $\hat{\omega}$ und $\hat{\phi}$ sind Ausgaben der Anpassung. Gehen Sie bei der Bearbeitung dieses Aufgabenteils wie folgt vor: 

- Ermitteln Sie $g^{(2.2)}\pm\Delta g_{\Delta T}^{(2.2)}$ mit Hilfe der Anpassung und vergleichen Sie Ihr Ergebnis im Rahmen seiner Unsicherheiten zu $g_{\mathrm{exp}}\pm\Delta g_{\mathrm{exp}}$. 
- Diskutieren und erklären Sie alle Beobachtungen, die Sie dabei machen. Wie kommt es, dass $\Delta g_{\Delta T}^{(2.2)}$ so viel kleiner ist, als $\Delta g_{\Delta T}^{(2.1)}$ und wie steht es um den Vergleich mit $g_{\mathrm{exp}}$?

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-b.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-d.md)

