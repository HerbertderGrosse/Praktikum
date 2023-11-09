<img src="../figures/Logo_KIT.svg"  width=200px style="float:right;" />

# Fakultät für Physik 

## Physikalisches Praktikum P1 für Studierende der Physik



Praktikumsvorversuch (Stand: Oktober 2023)





# Datenverarbeitung am Beispiel des Pendels



## Motivation

Im Mittelpunkt jedes physikalischen Experiments steht die **[Messung](https://de.wikipedia.org/wiki/Messung), d.h. die nachvollziehbare Erfassung und Weiterverarbeitung primärer [Daten](https://de.wikipedia.org/wiki/Daten), unter Laborbedingungen**. 

Mit diesem Praktikumsvorversuch, den alle Praktikumsteilnehmer:innen, am ersten Tag des P1, gemeinsam mit Ihren Tutor:innen durchführen, werden wir Sie anhand eines einfachen physikalischen Vorgangs mit den wichtigsten Methoden der computergestützten Datenverarbeitung in der modernen Physik vertraut machen. Im Laufe des P1 werden Sie erfahren, dass geschicktes Messen, mit Hilfe einer intelligenten Anordnung zur Erfassung und Weiterverarbeitung der Daten, schnell zur Messkunst avancieren kann, und dass die physikalische Messung untrennbar mit den Methoden der [Parameterschätzung in der Statistik](https://de.wikipedia.org/wiki/Sch%C3%A4tzfunktion) verbunden ist. Wir gehen davon aus, dass diejenigen unter Ihnen, die Physik als Hauptfach studieren den einführenden Kurs *Computergestützte Datenauswertung* (GgDa) am KIT besucht haben. Das P1 (sowie das P2 im folgenden Semester) bietet Ihnen eine Plattform, die Methoden, die Sie dort kennengelernt haben wiederholt für reelle, physikalische Messungen einzusetzen. Weiterführende Kurse, um die Methoden der Datenanalyse, wie Sie sie in der Physik benötigen, von Grund auf zu erlernen, werden im weiteren Verlauf des Physikstudiums am KIT angeboten. Für diejenigen unter Ihnen, die Physik im Nebenfach studieren, sollen dieser und die folgenden Versuche des P1 einen unverstellten Einblick in den Messalltag eines Physikers geben. Sie erhalten zur Bewältigung gesonderte Unterstützung  durch unsere Tutor:innen und die Dozenten.

Als Aufgabe wählen wir die Bestimmung der [Erdbeschleunigung](https://de.wikipedia.org/wiki/Schwerefeld) $g$ mit Hilfe eines Pendels, wie Sie sie im P1-Versuch [Pendel](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/tree/main/Pendel) selbst durchführen werden. Wir haben mit Hilfe der kostenfreien Anwendung [phyphox](https://phyphox.org/de/home-de/) der RWTH Aachen einen reellen Datensatz vorbereitet den Sie, im Rahmen dieses Vorversuchs, weiterverarbeiten werden. Zur Aufzeichnung der Daten bestanden bis auf den Besitz eines Smartphones kaum apparative Voraussetzungen. Sie könnten das hier vorgestellte Experiment also auch bei sich zu Hause wiederholen und Ihre Ergebnisse mit denen aus diesem und dem P1-Versuch Pendel vergleichen.

## Lehrziele

Wir listen im Folgenden die wichtigsten **Lehrziele** auf, die wir Ihnen mit dem **Vorversuch Datenverarbeitung am Beispiel des Pendels** vermitteln möchten: 

- Sie machen sich bewusst, dass in der modernen Physik jeder Messung ein Modell zugrunde liegt. 
- Sie lernen verschiedene Wege kennen Modellparameter zu bestimmen und erhalten einen Einblick darin, welche Stärken und Schwächen diese haben.
- Sie üben sich in der Anwendung statistischer Methoden zur exakten numerischen Bestimmung von Modellparametern. Sie können dabei Softwarepakete nutzen, die Ihnen die Fakultät [frei und offen](https://de.wikipedia.org/wiki/Open_Source) zur Verfügung stellt.
- In der Diskussion machen Sie sich den Unterschied zwischen Unsicherheiten, die statistischer Natur sind, und Unsicherheiten, die auf dem Mangel an Kenntnis der dem Experiment zugrunde liegenden Prozesse und Randbedingungen beruhen, bewusst. 
- Sie erkennen den Unterschied zwischen Messunsicherheiten und Messfehlern. 

## Versuchsaufbau

Wir haben die Anwendung [phyphox](https://phyphox.org/de/home-de/) auf ein Smartphone geladen und das Smartphone mit Klebestreifen auf eines der [Reversionspendel](https://de.wikipedia.org/wiki/Reversionspendel) aus dem P1-Versuch [Pendel](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/tree/main/Pendel) montiert. Für die Messung haben wir die Anwendung **Beschleunigung (ohne $g$)** verwendet. Der Versuchsaufbau ist im folgenden Bild skizziert:

<img src="./figures/PendelVorversuch.png" style="zoom:100%;" />

Wir haben das Pendel in Schwingung versetzt, die resultierende Bewegung mit Hilfe der im Smartphone eingebauten Beschleunigungssensoren ausgelesen und uns die resultierenden Datensätze im [*csv*-Format](https://de.wikipedia.org/wiki/CSV_(Dateiformat)) per Mail zugeschickt. Außerdem haben wir alle für unsere Messung relevanten äußeren Parameter mit Unsicherheiten festgehalten. Alle wichtigen Informationen zu Pendel und Smartphone haben wir aus der Anleitung des P1-Versuchs [Pendel](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/tree/main/Pendel) und den im Internet verfügbaren Datenblättern des Smartphones bezogen. Zum Teil haben wir die Abmessungen des Smartphones noch einmal mit einfachen Mitteln nachvollzogen. Dort, wo uns keine Informationen zu Unsicherheiten vorlagen haben wir sie abgeschätzt. Die Datensätze, die wir aufgenommen haben finden Sie nach dem *Download* des Versuchs in Ihrer Arbeitsumgebung auf dem Jupyter-Server. 

## Wichtige Hinweise zum Versuch

- Beim [*csv*-Format](https://de.wikipedia.org/wiki/CSV_(Dateiformat)) handelt es sich um ein einfaches, sowohl von Menschen als auch Maschinen lesbares Dateiformat, um Daten in Spalten und Zeilen organisiert abzulegen.
- Bevor Sie sich an die Auswertung der Daten und die Extraktion physikalischer Parameter machen können ist es im Messalltag notwendig die Daten zunächst aufzubereiten und geeignet zu präparieren. Dazu gehört z.B. die Anpassung des Datenformats, die Überprüfung auf unerkannte Störeffekte, Nullstellenkorrekturen und vieles mehr.  

# Navigation

- Wichtige Hinweise zu den Aspekten einer Messung und den von der Fakultät zur Verfügung gestellten Werkzeugen zur Datenanalyse finden Sie in der Datei [Hinweise-Datenverarbeitung.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Datenverarbeitung.md).
- Wichtige Hinweise zur Vorbereitung und Durchführung von Aufgabe 1 finden Sie in der Datei [Hinweise-Aufgabe-1.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-1.md).
- Wichtige Hinweise zur Vorbereitung und Durchführung von Aufgabe 2 finden Sie in der Datei [Hinweise-Aufgabe-2.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-2.md).
- Wichtige Hinweise zur Vorbereitung und Durchführung von Aufgabe 3 finden Sie in der Datei [Hinweise-Aufgabe-3.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/doc/Hinweise-Aufgabe-3.md).
- Wichtige technische Daten zum Versuch finden Sie in der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/blob/main/Vorversuch/Datenblatt.md).  
