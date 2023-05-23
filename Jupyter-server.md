# Arbeiten auf dem Jupyter-server

## Zugang zum Jupyter-server

Zugang zum Jupyter-server erhalten Sie über die Webadresse: [https://jupytermachine.etp.kit.edu/](https://jupytermachine.etp.kit.edu/). Als Login verwenden Sie Ihren Studierenden-Account am KIT. Wählen Sie, wenn Sie danach gefragt werden, die Option **Python** aus und starten Sie den Server. 

Falls der Zugang zum Server nicht für Sie freigeschaltet sein sollte, können Sie die Freischaltung [hier](https://comp.physik.kit.edu/Account/) veranlassen. Stellen Sie bitte **vor Praktikumsbeginn** sicher, dass Sie einen gültigen Account haben und sich entsprechend auf dem Jupyter-server einlogen können. 

## Einrichten der Versuche

Nach dem Start sollten Sie ein zweigeteiltes Fenster in Ihrer Jupyter-Umgebung vorfinden, wie im folgenden Bild gezeigt: 

<img src="./figures/JupyterAccount.png" alt="figures" style="zoom:100%;" />

Auf der linken Seite befindet sich ein Navigationsfenster mit der Verzeichnisstruktur Ihrer Jupyter-Umgebung, rechts daneben befindet sich ein Fenster (der sog. *Launcher*), in dem Sie auswählen können, welche Art von Notebook Sie öffnen möchten. Sie können, wenn Sie möchten, die Option **Notebook** und **Python 3** (das erste Icon oben links im *Launcher*) anwählen. Das rechte Fenster der Jupyter-Umgebung kann mehrere Register enthalten.  

Die jeweils aktuelle Version aller Versuchsanleitungen und die dazugehörigen Daten finden Sie auf dem gitlab-Server des SCC unter den Webadressen: 

* [https://git.scc.kit.edu/etp-lehre/p1-for-students](https://git.scc.kit.edu/etp-lehre/p1-for-students). 

* [https://git.scc.kit.edu/etp-lehre/p2-for-students](https://git.scc.kit.edu/etp-lehre/p2-for-students). 

Das folgende Bild gibt Ihnen eine Vorstellung, wie die Webseite des gitlab-Servers des SCC in etwa aussieht. Beachten Sie, dass dieses Bild nicht den aktuellen Zustand des Servers widerspiegeln muss.  

![SCC-gitlab](./figures/scc_gitlab.png)

Um das Repository aller Versuche (hier als Beispiel für die P1-Versuche) in Ihre Jupyter-Umgebung zu laden, gehen Sie z.B. wie folgt vor:

- Gehen Sie im Menü Ihrer Jupyter-Umgebung auf das Verzeichnis **Git** und wählen Sie die Option **Clone a Repository** aus.
- In einem neuen Fenster werden Sie daraufhin aufgefordert die URI-Adresse für das Repository anzugeben, das Sie klonen möchten. Diese finden Sie im [SCC Gitlab Repository](https://git.scc.kit.edu/etp-lehre/p1-for-students) (hier verlinkt für das P1).
- Öffnen Sie dazu das SCC Gitlab Repository der [P1 Versuche](https://git.scc.kit.edu/etp-lehre/p1-for-students) z.B. in einem neuen Reiter Ihres Browsers und klicken Sie den Knopf mit der Aufschrift **Clone** (blauer Knopf, rechts im obigen Bild). Wählen Sie aus dem sich öffnenden Untermenü die Option **Clone with HTTPS** aus. Die entsprechende Webadresse wird in die Zwischenablage Ihres Computers geladen.
- Wechseln Sie in Ihrem Browser wieder in den Reiter mit Ihrer Jupyter-Umgebung und geben Sie die Webadresse für das zu klonende SCC-gitlab Repository an. 
- Sie werden daraufhin nochmal gebeten sich dem SCC-gitlab Server gegenüber zu identifizieren. Verwenden Sie hierzu erneut Ihren Studierenden-Account am KIT. 

Nach erfolgreicher Durchführung sollten Sie eine Verzeichnis-Struktur **p1-for-students** in Ihrer Jupyter-Umgebung vorfinden. In diesem Verzeichnis befinden sich alle Versuche des P1 Praktikums (z.B. **Vorversuch**). Sie können in diesem Ordner die Durchführung und Auswertung des Versuchs beginnen.

Vor jedem weiteren Versuch bietet es sich an, eventuelle Änderungen in den noch ausstehenden Versuchsbeschreibungen vom Haupt-Repository zu laden. Klicken sie dazu wieder auf **Git** und wählen nun **Pull from Remote** aus. Sie müssen erneut Ihren Studierenden-Account am KIT verwenden, um sich dem  SCC-gitlab Server gegenüber zu identifizieren.

## Arbeiten mit dem Jupyter-notebook

Das Jupyter-notebook wird in Zellen bearbeitet. Es kann sich dabei um **Textzellen** (z.B. in Markdown) oder um **Code-Zellen** handeln, in die Sie direkt Python-Code eingeben können. Eine kurze Einführung in Jupyter-notebook können Sie [hier](https://www-ekp.physik.uni-karlsruhe.de/~quast/jupyter/jupyterTutorial.html) finden. Ein Jupyter-cheat sheet finden Sie z.B. [hier](https://www.edureka.co/blog/wp-content/uploads/2018/10/Jupyter_Notebook_CheatSheet_Edureka.pdf). Für die Durchführung der Versuche des P1 (oder P2) können die folgenden Jupyter-*features* von Bedeutung/Nutzen für Sie sein: 

- *Esc+m*: Wechsele Zellenmodus zu Markdown

- *Esc-y*: Wechsele Zellenmodus zu Code (d.h. Python)

- Befindet sich eine Zelle im Code-Modus können Sie direkt Kommandos in Python eingeben. Das folgende Beispiel importiert die Variable $l$ aus der Datei [*parameters_task_3.py*](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Vorversuch/params/parameters_task_3.py) aus dem *params*-Verzeichnis ihrer Jupyter-Umgebung für den Vorversuch Datenverarbeitung des P1 und gibt den Wert der Variablen auf dem Bildschirm aus, sobald Sie die Zelle ausführen. 

  ```python
  from params.parameters_task_3 import l
  print(l)
  ```

- *Strg+Enter*: Ausführen einer (Code-)Zelle.

- Sie sollten außerdem wissen, dass Sie jede in der Verzeichnisstruktur Ihrer Jupyter-Umgebung befindliche Datei per Doppelklick im rechten Fenster der Umgebung öffnen, bearbeiten und nach der Bearbeitung abspeichern können. 

- Möchten Sie ein Python-Skript aus Ihrer Jupyter-Umgebung direkt aus dem Jupyter-notebook ausführen, tun Sie dies in einer Code-Zelle mit dem  [Magic command](https://ipython.readthedocs.io/en/stable/interactive/magics.html) **%run**. Im Folgenden ist z.B. gezeigt, wie man das Skript *run_phyFit.py* aus dem *tools*-Verzeichnis Ihrer Jupyter-Umgebung direkt aus einer Code-Zelle eines Jupyter-notebooks (hier mit der Option `–-help`) aufrufen kann: 

  ```python
  %run /opt/conda/bin/run_phyFit.py --help
  ```

- Es empfiehlt sich alle angegebenen Skripte zunächst, wie oben demonstriert mit der Option `--help` aufzurufen (beachten Sie die zwei Minuszeichen). Zum einen erfahren Sie, ob sich das entsprechende Skript grundsätzlich fehlerfrei aufrufen lässt. Zum anderen erfahren Sie, wie und mit welchen weiteren Konfigurationsparametern Sie das jeweilige Skript aufrufen können. Zum Beispiel können Sie mit den folgenden weiteren Parametern das Bild der konfigurierten Anpassung direkt im Arbeitsverzeichnis Ihrer Jupyter-Umgebung in *png*-Format abspeichern:

  ```python
  %run /opt/conda/bin/run_phyFit.py -s -f png yaml/data.yaml
  ```

  Dabei steht die Option *-s* (beachten Sie das einfache Minuszeichen) für "save", also Abspeichern und die Option *-f png* für das Datenformat *png*.   

## Export von Jupyter-notebook nach *pdf*

Nach Bearbeitung sollten Sie Ihr Jupyter-notebook ins *pdf*-Format exportieren und auf ILIAS hochladen. Hierzu stehen Ihnen auf dem Jupyter-server zwei Möglichkeiten zur Verfügung. Wir empfehlen den direkten Export nach *pdf* auf dem Jupyter-server. Falls sich dies als problematisch erweisen sollte versuchen Sie den Export über *html*. Stellen Sie vor dem Export ins *pdf*-Format sicher, dass all Zellen ausgeführt wurden, so dass alle erzielten (Teil-)Ergebnisse im *pdf*-Export sichtbar sind. 

### Direkter Export nach *pdf*

Um Ihr Jupyter-notebook ins *pdf*-Format zu exportieren gehen Sie wie folgt vor: 

- Gehen Sie über den Menüpunkt *File* des Hauptmenüs des Jupyter-servers und wählen Sie den Menüpunkt *Save and Export Notebook As…* und dann den Unterpunkt *PDF* aus. Nach dem Export sollte sich eine *pdf*-Datei in Ihrem Browser öffnen, die Sie lokal abspeichern und auf ILIAS hochladen können. 
- Beachten Sie, dass Abbildungen, die explizit über Hyperlinks in die Anleitung eingebunden wurden nicht in der erzeugten *pdf*-Datei angezeigt werden. Wir haben für diesen Fall explizite Links zusätzlich in die Anleitungen eingefügt, so dass diese ihre inhaltliche Vollständigkeit bewahren. Falls Sie im Verlauf Ihrer Durchführung Bilder direkt in das Jupyter-notebook eingebunden haben sollten werden diese zusammen mit dem Jupyter-notebook exportiert und angezeigt.

### Export über *html* nach *pdf*

Falls beim direkten Export Ihres Jupyter-notebooks nach *pdf* Probleme auftreten sollten, sollte es immer noch möglich sein das Jupyter-notebook über *html* und schließlich Ihren Webbrowser nach *pdf* zu exportieren. Hierfür empfehlen wir das folgende Vorgehen: 

- Erzeugen Sie ein Verzeichnis mit dem Namen des Versuchs auf Ihrem lokalen Rechner.
- Exportieren Sie das Jupyter-notebook nach *html* und laden Sie es in dieses Verzeichnis herunter. Gehen Sie hierzu über den Menüpunkt *File* des Hauptmenüs des Jupyter-servers und wählen Sie die den Menüpunkt *Save and Export Notebook As…* und dann den Unterpunkt *HTML* aus. 
- Laden Sie sich die Bilder, die im Jupyter-notebook verlinkt wurden, zusätzlich vom Jupyter-server in das gleiche Verzeichnis herunter. Die einzubindenden Bilddateien sollten sich in der gleichen Verzeichnisstruktur, wie auf dem Jupyter-server befinden. Gegebenenfalls benötigen Sie ein Unterverzeichnis *figures*. Beachten Sie eventuelle Änderungen in den Dateiendungen (z.B. von *jpg* nach *jpeg*), die beim Herunterladen automatisch durch Ihren Browser vorgenommen worden sein könnten. 
- Sie können die *html*-Datei dann lokal, in Ihrem Browser, öffnen und von dort aus nach *pdf* exportieren. Wenn die so erzeugte *pdf*-Datei die Seiten nicht einwandfrei umbricht, ist das für uns ***kein Problem***.   
