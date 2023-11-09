# Hinweise für den Versuch Datenverarbeitung am Beispiel des Pendels

## Aufgabe 2: Mathematisches Pendel

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

Die Größe $\ell$ hat selbst eine Unsicherheit $\Delta\ell$, die wir in der Bestimmung von $\Delta g$ berücksichtigen sollten. Da $\ell$, als *von außen eingebrachter* Parameter, nicht immanent, d.h. nicht aus der Anpassung selbst, bestimmt werden kann, müssen wir $\Delta\ell$ ebenfalls von außen in die Bestimmung von $\Delta g$ einbringen.  Am einfachsten erreichen wir dies, indem wir $\ell$ um $\pm\Delta\ell$ variieren und die Anpassung erneut (insgesamt also $3\times$) durchführen. Die Unsicherheit $\Delta\ell$ wird entsprechend auf $g$ propagiert und führt so zu einer Unsicherheit $\Delta g_{\Delta\ell}^{(2.2)}$ unter Variation von $\ell$ um den Betrag $\pm\Delta\ell$. 

Die Unsicherheit $\Delta g_{\Delta\ell}$, die sich aus der ungenügenden Kenntnis von $\ell$ ergibt bezeichnet man in diesem Zusammenhang als epistemische, oder **systematische Unsicherheit**. In der Physik sind systematische Unsicherheiten i.d.R. mit *systematischen Variationen* verbunden. Im Gegensatz dazu bezeichnet man $\Delta g_{\Delta T}$, das die Unsicherheiten der konkreten Messung, an die das Modell angepasst wurde repräsentiert, als **statistische Unsicherheit** der Messung.

Nach der Anpassung an die Daten können Sie $g^{(2.3)}$ direkt als Ausgabewert der Anpassung ablesen. Es handelt sich lediglich um eine Umparametrisierung des Modells aus Aufgabe 2.1 für die Sie die folgenden Eigenschaften feststellen sollten: 

- Der Wert von $g^{(2.3)}$ ist der gleiche, wie für $g^{(2.2)}$ aus Aufgabe 2.2;
- Der Wert von $\Delta g_{\Delta T}^{(2.3)}$ ist der gleiche, wie für $\Delta g_{\Delta T}^{(2.2)}$ aus Aufgabe 2.2;
- Der Wert von $\hat{z}/n_{\mathrm{dof}}$ für die Güte der Anpassung ist der gleiche, wie aus Aufgabe 2.2.

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2-c.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vorversuch)

