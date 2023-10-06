# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 2: Mathematisches Pendel

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

Die Größe $\hat{\chi}^{2}/n_{\mathrm{dof}}$ und die Werte und Unsicherheiten der angepassten Parameter $\hat{A}$, $\hat{\omega}$ und $\hat{\phi}$ sind Ausgaben der Anpassung. Gehen Sie bei der Bearbeitung dieses Aufgabenteils wie folgt vor: 

- Ermitteln Sie $g^{(2.2)}\pm\Delta g_{\Delta T}^{(2.2)}$ mit Hilfe der Anpassung und vergleichen Sie Ihr Ergebnis im Rahmen seiner Unsicherheiten zu $g_{\mathrm{exp}}\pm\Delta g_{\mathrm{exp}}$. 
- Diskutieren und erklären Sie alle Beobachtungen, die Sie dabei machen. Wie kommt es, dass $\Delta g_{\Delta T}^{(2.2)}$ so viel kleiner ist, als $\Delta g_{\Delta T}^{(2.1)}$ und wie steht es um den Vergleich mit $g_{\mathrm{exp}}$?

###  Aufgabe 2.3: Zweite Erweiterung der Methodik

Sie können $g\pm\Delta g$ auch direkt als Modellparameter bestimmen. Unter Verwendung von *PhyPraKit* könnte der Funktionsblock für ein entsprechend verändertes Modell so aussehen: 

```yaml
model_label: "HARMONIC_G"
model_function: |
  def model(t, A=0.8, g=9.8, phi=0):
      return x0*np.cos(np.sqrt(g/0.6285)*t+phi)
```

Dabei handelt es sich bei der Zahl `0.6385` um die Länge $\ell$ des Pendels (siehe [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md)), die wir als **äußeren Parameter** bestimmt haben und als solchen ins Modell einbringen. 

Aus dieser Modifikation ergeben sich tiefere Einsichten in die Diskussion der berücksichtigten Unsicherheiten:

Die Größe $\ell$ hat selbst eine Unsicherheit $\Delta\ell$, die wir in der Bestimmung von $\Delta g$ berücksichtigen sollten. Da $\ell$, als *von außen eingebrachter* Parameter, nicht immanent, d.h. nicht aus der Anpassung selbst, bestimmt werden kann, müssen wir $\Delta\ell$ ebenfalls von außen in die Bestimmung von $g$ einbringen.  Am einfachsten erreichen wir dies, indem wir $\ell$ um $\pm\Delta\ell$ variieren und die Anpassung erneut (insgesamt also $3\times$) durchführen. Die Unsicherheit $\Delta\ell$ wird entsprechend auf $g$ propagiert und führt so zu einer Unsicherheit $\Delta g_{\Delta\ell}^{(2.2)}$ unter Variation von $\ell$ um den Betrag $\pm\Delta\ell$. 

Die Unsicherheit $\Delta g_{\Delta\ell}$, die sich aus der ungenügenden Kenntnis von $\ell$ ergibt bezeichnet man in diesem Zusammenhang als epistemische, oder **systematische Unsicherheit**. In der Physik sind systematische Unsicherheiten i.d.R. mit *systematischen Variationen* verbunden. Im Gegensatz dazu bezeichnet man $\Delta g_{\Delta T}$, das die Unsicherheiten der Datenpunkte, an die das Modell angepasst wurde und damit die eigentliche Messung repräsentiert, als **statistische Unsicherheit** der Messung.

Nach der Anpassung an die Daten können Sie $g^{(2.3)}$ direkt als Ausgabewert der Anpassung ablesen. Es handelt sich lediglich um eine Umparametrisierung des Modells aus Aufgabe 2.1 für die Sie die folgenden Eigenschaften feststellen sollten: 

- Der Wert von $g^{(2.3)}$ ist der gleiche, wie für $g^{(2.2)}$ aus Aufgabe 2.2;
- Der Wert von $\Delta g_{\Delta T}^{(2.3)}$ ist der gleiche, wie für $\Delta g_{\Delta T}^{(2.2)}$ aus Aufgabe 2.2;
- Der Wert von $\chi^{2}/n_{\mathrm{dof}}$ für die Güte der Anpassung ist der gleiche, wie aus Aufgabe 2.2.

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-b.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch)
