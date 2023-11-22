# Verwendung der PhyPraKit Module

Für diejenigen unter Ihnen, die sich in der Verwendung der Programmiersprache [python](https://www.python.org/) nicht sicher fühlen, aber dennoch nicht auf die korrekte Anwendung statistischer Methoden zur Parameterschätzung in den P1- und P2-Praktika verzichten wollen hat Prof. Günter Quast am Institut für Experimentelle Teilchenphysik (ETP) die Python Modulsammlung [PhyPraKit](https://etpwww.etp.kit.edu/~quast/PhyPraKit/htmldoc/) entwickelt.

Aus dieser Modulsammlung werden Sie voraussichtlich nur die Skripte `run_phyFit.py`, `csv2yml.py` und ggf. `plotData.py` benötigen. Auf dem Jupyter-Server können Sie diese Skripte sowohl aus einem Terminal, als auch direkt aus einer Code-Zelle eines Juypter-notebooks aufrufen. Der Aufruf des Skripts `run_phyFit.py` aus einem Terminal Ihrer Jupyter-Umgebung sieht z.B. so aus: 

`run_PhyFit.py –-help`

Der Aufruf des gleichen Skripts direkt aus einer Code-Zelle eines Jupyter-notebooks sieht z.B. so aus:[^1] 

`%run /opt/conda/bin/run_phyFit.py --help`

Beachten Sie die Angabe **des vollen Pfades** (`/opt/conda/bin/`) zum Skript, wenn Sie es mit Hilfe des [Magic commands](https://ipython.readthedocs.io/en/stable/interactive/magics.html) `%run` aus einer Code-Zelle des Jupyter-notebooks aufrufen. 

Mit der Option `–-help` in diesen Beispielen, rufen Sie den "Hilfe"-Text mit Erklärungen zur Anwendung des Skripts auf. Wenn Sie eine Parameteranpassung an Daten durchführen wollen müssen Sie dem Skript *run_phyFit.py* sowohl die Daten, als auch das anzupassende Modell mit den entsprechenden Parametern bekannt machen. Dies erreichen Sie mit Hilfe einer Konfigurationsdatei, die im [`yaml`](https://de.wikipedia.org/wiki/YAML)-Format abgefasst ist. Wir werden Ihnen im Folgenden die wichtigsten Eigenschaften einer solchen Konfigurationsdatei anhand der Verwendung mit dem Skript `run_phyFit.py` erklären. 

Alle in diesem Text verwendeten Code-Beispiele sollten Sie in jedem SCC gitlab-Repository zu jedem der P1- und P2-Versuche direkt ausführen können.

[^1]: Beachten Sie die Verwendung des [Magic commands](https://ipython.readthedocs.io/en/stable/interactive/magics.html) **%run** zur Ausführung des Skripts aus einer Code-Zelle des Jupyter-notebooks. Weitere Hinweise hierzu erhalten Sie im Dokument [Arbeiten auf dem Jupyter-Server](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/doc/JupyterServer.md).

## Parameteranpassung mit dem Skript *run_phyFit.py*

Wenn Sie sich für die Verwendung der Modulsammlung PhyPraKit entschieden haben empfiehlt es sich, sich mit der Nutzung des Skripts `run_phyFit.py` und der Struktur der notwendigen `yaml`-Datei zu dessen Steuerung vertraut zu machen. Im Folgenden ist die Durchführung einer Parameteranpassung an einen Beispieldatensatz, bestehend aus 14 freigewählten Datenpunkten, mit Hilfe der Datei [`PhyPraKit_example.yaml`](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/tools/PhyPraKit_example.yaml) gezeigt: 

Die wichtigsten Strukturelemente der `yaml`-Datei sind in den folgenden Kommentarzeilen in dieser Datei kurz erklärt: 

```yaml
# Das ist eine Kommentarzeile schreiben Sie so viele Kommentare in Ihre yaml-
# Dateien, wie sie möchten! Falls sie diese Datei für Ihre Auswertung nutzen 
# möchten legen Sie am besten eine Kopie dieser Datei (z.B. mit dem Namen 
# my_model.yaml) in Ihrer Arbeitsumgebung an und passen Sie die Datenpunkte, 
# Unsicherheiten und die Modell-Funktion, die Sie anpassen möchten an Ihre 
# Messung an. Sie können dann eine Anpassung an die Daten mit Hilfe des 
# python-Skripts run_phyFit.py vornehmen wie im Dokument "Verwendung der 
# PhyPraKit Module" 

# Hier geben Sie den Titel des plots an, der nach der Anpassung des Modells an 
# die Daten angezeigt werden wird.
title: "Beispiel aus Datei 'PhyPraKit_example.yaml'"
# Hier geben Sie den Titel auf der x-Achse an.
x_label: 'x-Werte'
# Hier geben Sie den titel auf der y-Achse an.
y_label: 'y-Werte'
# Dieses Label wird in der Legende angezeigt. 
label: Zufallsdaten
# Dies sind die Werte der Beispieldaten auf der x-Achse.
x_data: [0., 0.2, 0.4, 0.6, 0.8, 1., 1.2, 1.4, 1.6, 1.8, 2., 2.2, 2.4, 2.6]
# Dies sind die Unsicherheiten der Werte auf der x-Achse. 
x_errors: [0.01,0.015,0.02,0.025,0.03,0.035,0.04,0.045,0.05,0.055,0.06,
           0.065,0.07,0.075]
# Dies sind die Werte der Beispieldaten auf der y-Achse.  
y_data: [1.149, 0.712, 0.803, 0.464, 0.398, 0.355, 0.148,
         0.328, 0.181, 0.140, 0.0651, 0.005, -0.005, 0.116]
# Hier sehen Sie nur einen Eintrag für die Unsicherheiten der Werte auf der 
# y-Achse. Geben Sie nur eine einzige Zahl an, gilt diese als Unsicherheit für 
# alle Werte. 
y_errors: 0.07
# Dies ist ein Namenslabel für das Modell, das Sie an die Daten anpassen 
# möchten.
model_label: 'Exponential'
# Dies ist die Modell-Funktion, die Sie an die Daten anpassen möchten. Beachten 
# Sie das "|"-Symbol nach dem yaml-Schlüsselwort "model_function". Danach folgt 
# die Definition der Funktion in python. Sie können alle vorinstallerten 
# Bibliotheken, wie z.B. numpy (np) für die Definition der Modell-Funktion ver-
# wenden. 
model_function: |
    def exp_model(x, A=1., x0=1.):
      return A*np.exp(-x/x0)
```

Wenn Sie das Skript mit der Konfigurationsdatei `PhyPraKit_example.yaml` aus einer Code-Zelle eines Jupyter-notebook in Ihrer Jupyter-Umgebung ausführen wollen, geben Sie in der Code-Zelle den folgenden Text ein und führen Sie die Code-Zelle z.B. mit der Tastenkombination *Strg+Enter* aus:

`%run /opt/conda/bin/run_phyFit.py tools/PhyPraKit_example.yaml`

Daraufhin sollten Sie das folgende Bild erhalten:     

![](../figures/xyData_and_Model.png)

Sie sehen, dass das Modell einer Exponentialfunktion mit den Parametern $A$ und $x_{0}$ an die Datenpunkte angepasst wurde.

Sie sollten die angepassten Parameter $A$ und $x_{0}$ der Modell-Funktion, das Datenlabel, das Label der Modell-Funktion und die Achsenbeschriftungen mit den entsprechenden Schlüsselworten in der `yaml`-Datei identifizieren können. 

Ein voll funktionsfähiges Beispiel Jupyter-notebook finden Sie unter [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/tools/PhyPraKit_example.ipynb).

## Ein paar Tipps für Anfänger:innen auf diesem Gebiet: 

- `yaml` ist ein Strukturformat, das aus Paaren von beliebigen "Schlüsselworten" und "Werten" (*key-value* Paaren) besteht. Diese sind grundsätzlich durch einen Doppelpunkt voneinander getrennt. 
- Die Schlüsselworte, die wir in der oben gezeigten Datei verwenden, haben nichts mit dem `yaml`-Format an sich zu tun. Das Format ist nur das Medium, das wir verwenden um das Skript `run_phyFit.py` zu konfigurieren. Es handelt sich um **Schlüsselworte, die das Skript erwartet**. 
- Innerhalb des Skripts gibt es Code-Stellen in denen solche Schlüsselworte in der `yaml`-Konfigurationsdatei gesucht und die dazugehörigen Parameter ausgelesen werden. Wenn für die Anwendung essentielle Schlüsselworte nicht gefunden werden können, oder wenn das ausgeführte Skript mit den übergebenen Parametern nichts anfangen kann, wird durch das Skript ein Fehler ausgegeben.  
- Sie können keine Anpassung einer Funktion an Daten durchführen, wenn Sie dem Skript die Daten nicht als Werte, hier zu den Schlüsselworten *x_data* und *y_data*, bekannt machen. Ebenso erwartet das Skript Werte für die Unsicherheiten auf die Datenpunkte, die man mit den Schlüsselworten *x_errors* und *y_errors* übergibt, und eine anzupassende Modellfunktion. Diese einfachen Anforderungen erklären die Schlüsselworte, für die Sie in der `yaml`-Datei Werte **zur Verfügung stellen müssen**.
- Halten Sie sich exakt an die Syntax der Schlüsselworte. Die Worte *x-data*, *x_Data* oder *x_data* sind **nicht identisch**. Beachten Sie Groß- und Kleinschreibung!
- Wenn Sie für einen Wert (einfache oder doppelte) Anführungsstriche öffnen, müssen Sie diese auch mit gleichartigen Anführungsstrichen wieder schließen. Das sind klassische Tippfehler bei Programmieranfänger:innen. 

Sie werden sehen, dass Sie den Bogen mit etwas Übung schnell raus bekommen werden. Falls Sie im Laufe der Versuche mit Ihren eigenen `yaml`-Dateien mal nicht klarkommen sollten vergleichen Sie sie mit der Beispieldatei oder jeder anderen funktionierenden `yaml`-Datei aus Ihrem wachsenden Fundus, bis Sie den Unterschied gefunden haben. Bei anhaltenden Problemen wenden Sie sich an Ihre Tutor:innen oder die Dozenten des Praktikums. Wir helfen Ihnen jederzeit gerne weiter.  

**Anm.:** Mit der gleichen `yaml`-Datei können Sie das Skript *plotData.py* ausführen.  

# Navigation

[Zurück zu P1-Praktikum](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students)

