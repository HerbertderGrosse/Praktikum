# Hinweise für den Versuch Geometrische Optik

## Aufgabe 2: Vermessung eines Zweilinsensystems $L$ [3/5]

### Bestimmung von $H_{1}$, $H_{2}$ und $f$

Die Bestimmung von $f$, $h_{x}$ und $h_{x}'$ läuft nun wie folgt ab: 

- Sie variieren den Abstand $x$. Dabei variieren Sie effektiv $g$, während $h_{x}$ durch die feste Wahl von $X$ immer gleich bleibt. Beachten Sie die Lage des Nullpunkts in $X$, demnach ist $x$ mit negativem und $x'$ mit positivem Vorzeichen zu messen.
- Justieren Sie zu jedem gewählten Wert von $x$ den Abstand des Schirms $x'$, so dass $B$ wieder scharf darauf abgebildet wird. Beachten Sie die Unsicherheiten auf $x$ und $x'$.  
- Bestimmen Sie den Abbildungsmaßstab $\beta$ zu jedem Wertepaar, bestehend aus $x$ und $x'$. Berechnen Sie die Unsicherheiten auf $\beta$ in jedem Punkt aus den Unsicherheiten auf $G$ und $B$, mittels linearer Fehlerfortpflanzung. 

Zwar sind $g$ und $b$ nicht bekannt, $\beta$ kann aber aus $G$ und $B$ bestimmt werden. Dazu können können Sie zwei mögliche Wege der Auswertung beschreiten: 

#### Methode 1:

Trägt man $x(f, h_{x})$ als Funktion von $(1+1/\beta)$ und $x^\prime(f, h^\prime_{x})$ als Funktion von $(\beta+1)$ auf sollte sich jeweils ein linearer Zusammenhang ergeben, aus dem sich $f$ als Steigung und $h_{x}$ ($h'_{x}$) als Achsenabschnitt ablesen lassen. durch Anpassung zweier unabhängiger Modelle nach Gleichung (**(4)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-a.md)) erhalten Sie jeweils einen Wert für $h_x$ und $h^\prime_x$ und zwei unabhängige Werte für $f$. Die Werte für $f$ sollten innerhalb ihrer Unsicherheiten übereinstimmen.  

#### Methode 2:

Mit Hilfe der `MultiFit`-Funktion aus dem Programm-Paket *kafe2* können Sie $f$, $h_x$ und $h_x^\prime$ **gleichzeitig** anpassen. Sie nutzen dabei den Vorteil, dass beide Messreihen zur Bestimmung des gemeinsamen Parameters $f$ beitragen können. Ein Beispiel für die Nutzung finden Sie in der offiziellen Dokumentation des Programmpakets *kafe2* [hier](https://kafe2.readthedocs.io/en/latest/parts/beginners_guide.html#multifit). Eine lauffähige Adaption mit weiteren Erklärungen finden im `tools`-Verzeichnis dieses Repositories [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/tools/kafe2_example_MultiFit.ipynb).

Zur Implementierung eines geeigneten Objekts der `MultiFit`-Klasse sollten, wie oben beschrieben zwei `XYFit`-Objekte zu den Modellen $x(f, \beta, h_x)$ und $x^\prime(f, \beta, h^\prime_x)$ aus Gleichung (**(4)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-a.md)) definieren. Geben Sie für jedes `XYFit`-Objekt auch die Unsicherheiten auf $\beta$ individuell an. Da es sich für jede Messung um neu aufgenommene Messpunkte handelt sind die Unsicherheiten zu verschiedenen `XYFit`-Objekten (im Gegensatz zum oben verlinkten Beispiel einer Strom-Spannungs Kennlinie) **nicht korreliert**. 

Sowohl $h_x$ als auch $h_x^\prime$ können sowohl positive als auch negative Werte annehmen, je nachdem ob sich die entsprechende Hauptebene links oder rechts von $X$ befindet. Aus $h_x$ und $h_x^\prime$ lässt sich der Abstand der Hauptebenen $a=h_x^\prime-h_x$ bestimmen, der von der Wahl von $X$ unabhängig ist. Sie können $a$ auch direkt in Ihrem Modell implementieren, indem Sie z.B.  $h_x^\prime$ als $h_x^\prime=a+h_x$ ausdrücken. 

# Navigation

 [Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Geometrische_Optik/doc/Hinweise-Aufgabe-2-c.md)
