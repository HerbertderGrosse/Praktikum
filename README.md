# Arbeiten in den P1 und P2 Praktika

## Ziele der P1 und P2 Praktika

Ziele der P1 und P2 Praktika sind es Ihnen die Möglichkeit zu bieten: 

- Experimente unter Laborbedingungen durchzuführen; 
- Daten mit naturwissenschaftlichem Anspruch zu erheben und weiter zu verarbeiten; 
- physikalische Gesetzmäßigkeiten experimentell zu überprüfen.  

Sie werden feststellen, dass die durchzuführenden Versuche und die zu  untersuchenden Gesetzmäßigkeiten noch nicht in allen Fällen aus den Vorlesungen bekannt sein werden. Dies lässt sich aufgrund der Organisation des Praktikums, im Rotationsverfahren, nicht vermeiden. Bei einem so breiten Anwendungsgebiet, wie den Grundlagen der Physik, können Sie darüber hinaus grundsätzlich nicht davon ausgehen, immer auf bekannten Stoff zu stoßen. Es ist daher auch ein wichtiger Lehrinhalt der P1 und P2 Praktika, sich neue Themen und Versuche der Physik *eigenständig* zu erschließen.  

### Durchführung eines Versuchs

Zur **Durchführung** eines Versuchs gehört es, *zielgerichtet* zu experimentieren und Messungen und Teilergebnisse in den Kontext des Experiments *einzuordnen*. Sie sollten also mit einer klaren Vorstellung darüber, was Sie im anstehenden Versuch erwartet, im Praktikum eintreffen und die physikalische Aufgabenstellung vollumfänglich verstanden haben. Dies wird durch die Vorbesprechung zum Versuch sichergestellt. 

### Erhebung der Daten

Zur **Erhebung der Daten** gehört die *systematische*, *reproduzierbare* Aufnahme von Messwerten einschließlich der Einschätzung der damit verbundenen wichtigsten Unsicherheiten. Grundsätzlich gilt in der Physik: **"Keine Messung ohne Einschätzung der damit verbundenen wichtigsten Unsicherheiten!"** 

### Protokoll und Auswertung

Ein zentraler Bestandteil der Datenerhebung ist das *gewissenhaft*, *vollständig* und *sachlich* geführte **Protokoll der Versuchsdurchführung**, das in die Auswertung des Experiments mündet. 

Das wissenschaftlich geführte Protokoll setzt voraus, das sich der Durchführende der einzelnen Schritte des Experiments bewusst ist und diese für sich und Außenstehende klar, verständlich und reproduzierbar dokumentiert. Das Protokoll erklärt, *wie* Sie zu einem Messergebnis gekommen sind. Sollte Ihnen beim Experimentieren ein Fehler unterlaufen sein, sollte dies aus dem Protokoll nachträglich nachvollziehbar und ggf. in der Einschätzung der Ergebnisse durch Sie und Außenstehende zu berücksichtigen sein. 

Die gewissenhafte Erhebung und Dokumentation Ihrer Daten begründet Ihren guten Ruf als Wissenschaftler:innen. Ein Fehler in der Durchführung eines Experiments kann zur Entwertung Ihrer Ergebnisse und/oder zur Neuauflage eines –dann verbesserten– Experiments führen. Das ist Bestandteil des wissenschaftlichen Erkenntnisgewinns. Die mangelhafte *Dokumentation* und daher von außen nicht mehr nachvollziehbare Ergebnisse machen Ihr Experiment von vornherein und *unwiederbringlich* unbrauchbar. 

Vor der Digitalisierung wurden Protokolle in Form von Laborbüchern geführt. Für die P1 und P2 Praktika wird das Laborbuch durch das **Jupyter-notebook** ersetzt, das Sie auf dem [Jupyter-server](https://jupytermachine.etp.kit.edu/) der Fakultät anlegen können. Sie sollten darin zielgerichtet und für sich und Außenstehende nachvollziehbar 

- die Ziele des Experiments; 
- die Bedingungen der Durchführung; 
- *alle* Messwerte, einschließlich der Einschätzung ihrer Unsicherheiten; 
- die Weiterverarbeitung der Daten und daraus resultierende Teilergebnisse dokumentieren. 

**Am Ende des Praktikumstages mündet das Protokoll in die Auswertung des Versuchs**. Eine Anleitung zu jedem Versuch als Jupyter-notebook sollte Ihnen bei der Erstellung des Protokolls als Vorlage dienen können. Praktische Hinweise zur Arbeit mit dem Jupyter-notebook finden Sie im Dokument [Praktische Hinweise zur Durchführung und Auswertung der Versuche](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/PraktischeHinweise.md). 

### Wichtige Begriffsklärungen

#### Versuchsausgang

Niemand erwartet von Ihnen, dass Sie die von Ihnen durchgeführten Versuche bereits am ersten Tag des P1 perfekt dokumentieren können. Vielmehr sollen Sie das Experimentieren und die wissenschaftlich-sachliche Einschätzung Ihres Experimentierens anhand gut verstandener physikalischer Prozesse im Verlauf der P1 und P2 Praktika *erlernen*. 

Wir erwarten nicht, dass ein von Ihnen durchgeführtes Experiment zu Ergebnissen mit "Veröffentlichungsreife" führt oder nach den Standards physikalischer Veröffentlichungen formatiert ist. Insbesondere erwarten wir nicht, dass Sie mit Ihrem Ergebnis einen existierenden Literaturwert so exakt wie möglich reproduzieren.  

Eine Aussage wie: "Meine Messung stimmt innerhalb von 10% mit dem Literaturwert überein" ist für uns im Allgemeinen *irrelevant*. Die Frage, die Sie mit Ihrem Versuch zu beantworten haben ist: **"Stimmt meine Messung innerhalb der von mir abgeschätzten Unsicherheiten mit meiner Erwartung überein?"**. Ihre Erwartung kann dabei durch einen Literaturwert gespeist sein.

Bei der Beantwortung der obigen Frage ist die adäquate *numerische* Einschätzung der Unsicherheiten der Messung mitunter wichtiger, als der ermittelte Zentralwert.   

#### Einschätzung des eigenen Experimentierens

Auf dem [Jupyter-server](https://jupytermachine.etp.kit.edu/) der Fakultät stehen Ihnen alle nötigen Werkzeuge zur Anwendung von Methoden zur **statistischen Parameterschätzung**, wie sie von der Fakultät empfohlen werden, zur Verfügung. Dadurch sollte sich in vielen Fällen eine, oft nicht auf ihre Anwendbarkeit hin überprüfte "händische" Fehlerabschätzung durch Gaußsche Fehlerfortpflanzung erübrigen. 

Selbst, wenn Sie sich für die Anwendung Gaußscher Fehlerfortpflanzung entscheiden sollten müssen Sie dies nicht "händisch" mit Hilfe eines Taschenrechners oder einer Excel-Tabelle tun; Sie können eine einfache Funktion in Python-Code direkt in Ihr Versuchsprotokoll im Jupyter-notebook integrieren. Falls Ihnen dabei ein Fehler unterlaufen sollte, ist dies mit der Funktion, als Bestandteil des Protokolls nachvollziehbar dokumentiert und zu jeder Zeit nachträglich korrigierbar. Der [Vorversuch Datenverarbeitung](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/tree/main/Vorversuch) des P1 bietet Ihnen die Möglichkeit Ihr Wissen und Ihre Erfahrung auf diesem Gebiet in Vorbereitung auf das P1 aufzufrischen und/oder zu vertiefen. 

Als Physiker:innen müssen Sie in die Situation hineinwachsen, dass Sie selbstverständlich **die Unsicherheiten der von Ihnen weiterverarbeiteten Daten bewusst ein- oder abschätzen**. Sie sollten *nach Möglichkeit* keinen Messwert oder Parameter ohne entsprechende *quantitative* Abschätzung seiner Unsicherheiten weiterverarbeiten. Die Einschätzung von Unsicherheiten gehört zu Ihrem Handwerk als Wissenschaftler:innen. In einer numerischen Parameterschätzung erhalten Sie *verlässliche* Konfidenzintervalle für die von Ihnen bestimmten Messgrößen aus der angewandten Anpassung (dem *fit*) ohne notwendige eigene Fehlerfortpflanzung. Nutzen Sie die von der Fakultät angebotenen Möglichkeiten zur Parameterschätzung daher am besten wo immer möglich, um von den von Ihnen aufgenommenen primären Daten direkt zum Messergebnis zu gelangen. 

## Ein Praktikumstag im P1 oder P2

Ein Praktikumstag im P1 oder P2 verläuft von **13:30 – 19:00**. Wir gehen davon aus, dass Sie sich vor Versuchsantritt mit den grundlegenden Fragestellungen des aktuellen Versuchs vertraut gemacht haben, und dass Sie den Versuch der Vorwoche abgeschlossen und ausgewertet haben. Unter diesen Voraussetzung sollte Ihr Tag im P1 oder P2 wie folgt aussehen: 

### Vorbesprechung des aktuellen Versuchs

Von **13:30 – 14:00** besprechen Sie Ziele und Durchführung Ihres aktuellen Versuchs mit dem/der entsprechenden Tutor:in. Im Rahmen dieser Vorbesprechung klären Sie ab, 

- ob Sie die physikalische Fragestellung oder den zu untersuchenden physikalischen Sachverhalt ausreichend verstanden haben; 
- ob Sie Ziele und Strategie zur Durchführung des Versuchs verstanden haben;  
- ob Sie die für die Versuchsdurchführung notwendigen Apparaturen identifizieren und sachgerecht bedienen können. 

Diese Besprechung sollten Sie nicht als Prüfung verstehen. Natürlich wollen wir wissen, ob Sie wissen worum es in den 5,5 Stunden dieses Versuchstages für Sie gehen soll. Sollte dies nicht der Fall sein, können Sie aus dem Versuchstag nichts lernen. Vorrangiges Ziel der Vorbesprechung ist es aber, Sie in die Position zu versetzen, dass Sie mit einer klaren Idee den Versuch weitestgehend *selbstständig* durchführen können. Bei anspruchsvollen Versuchen und gerade zu Beginn des P1 kann dies eine schwere Aufgabe sein. Sie haben nach der Vorbesprechung 3,5 Stunden Zeit, diese Aufgabe in Ihrem Sinne bestmöglich zu lösen. Der/Die Tutor:in ist dazu da, Ihnen dabei zu helfen. 

### Versuchsdurchführung

Von **14:00 – 17:30** haben Sie Zeit den aktuellen Versuch durchzuführen. Der/Die Tutor:in sollte über die gesamte Zeitspanne zur Beantwortung von Fragen zu Ihrer Verfügung stehen. Manche Versuchsaufbauten müssen aus Sicherheitsgründen vor Inbetriebnahme von dem/der Tutor:in abgenommen werden. Bemühen Sie sich den Versuch *als Team* so *selbstständig* wie möglich durchzuführen, aber stellen Sie gemeinsam mit dem/der Tutor:in sicher, dass Ihre Durchführung zielgerichtet ist und erzielte Zwischenergebnisse im Zusammenhang des gesamten Versuchs für Sie Sinn ergeben. Hierfür empfehlen wir Ihnen dringend **Teilauswertungen im Jupyter-notebook** durchzufüren. Sie können so nach Ihren Möglichkeiten die Qualität der aufgenommenen Daten sicherstellen. 

Von **15:30 – 16:00**, nachdem Sie sich mit dem Versuch vertraut gemacht und sich eine entsprechende Übersicht über de Versuch verschafft haben, suchen Sie Ihre:n Tutor:in zur **Nachbesprechung des vorangegangenen Versuchs** auf. Besprechen Sie sowohl die Durchführung als auch die Auswertung des vorangegangenen Versuchs *im Team* und *persönlich* bei dem/der entsprechenden Tutor:in. Dabei vertreten Sie Ihre Ergebnisse und klären, ob es resultierende Beanstandungen zur Auswertung gibt. Sie finden den/die Tutor:in in den Räumlichkeiten des vorangegangen Versuchs. Dieser Teil entfällt bei der Durchführung des ersten Versuchs im Praktikum.

Falls Sie vor 17:30 mit der Durchführung der Versuchs fertig sein sollten, können Sie bereits mit der Auswertung beginnen und die Auswertung ggf. auch am Tag der Versuchsdurchführung fertigstellen. 

### Einführung in den nächsten Versuch durch Kommiliton:innen

Von **17:30 – 18:00** nutzen Sie die Zeit sich mit dem nächsten Versuch persönlich vertraut zu machen: Teilen Sie sich hierzu in zwei Gruppen A und B auf. Gruppe A verbleibt zunächst beim aktuellen Versuch. Gruppe B sucht den Raum des nächsten Versuchs auf und lässt sich von Gruppe A des dortigen Versuchs etwa 10 min lang erklären, worum es bei diesem Versuch geht und wie er ablaufen wird. Gruppe A sollte nach 3,5 Stunden des Experimentierens in der Lage sein, den Kommiliton:innen aus Gruppe B erklären zu können, was sie im aktuellen Versuch gemacht haben. Der/Die entsprechende Tutor:in unterstützt Sie dabei gegebenenfalls. Nach dieser Zeit kehrt Gruppe B zu ihrem aktuellen Versuch zurück und die Gruppen A und B tauschen die Rollen. 

### Abschluss des aktuellen Versuchs

Von **18:00 – 19:00** haben Sie die Möglichkeit verbleibende Messungen des aktuellen Versuchs abzuschließen. Sie führen damit Ihr Protokoll zu einem wohldefinierten Endpunkt. Der Praktikumstag endet aus organisatorischen Gründen pünktlich um 19:00, selbst wenn Sie den Versuch noch nicht vollständig durchgeführt haben sollten. Geben Sie in einem solchen Fall in Ihrem Protokoll an, woran es lag, dass Sie nicht rechtzeitig fertig geworden sind. Sprechen Sie Ihre Messungen und Zwischenergebnisse nochmal abschließend mit dem/der Tutor:in durch, bevor Sie gehen. 

Formatieren Sie Ihr Protokoll in *pdf*-Format und laden Sie Ihr Protokoll sowohl als Jupyter-notebook, als auch in *pdf*-Format (als Version $\mathrm{v0}$) auf das ILIAS-System hoch. 

### Auswertung 

Die Auswertung des Versuchs erfolgt auf Grundlage Ihres Protokolls vorzugsweise im Jupyter-notebook. Zu Ihrer Orientierung bzgl. des Umfangs gehen Sie davon aus, dass Sie **nicht mehr als 2 Stunden** für die verbleibende Auswertung des aktuellen Versuchs benötigen sollten. Beachten Sie, dass es das vorrangige Ziel der Auswertung ist, Ihre Messung und die erzielten Ergebnisse mit einer sinnvollen persönlichen Einschätzung einschließlich entsprechender *quantifizierter* Unsicherheiten für Sie und Außenstehende verständlich zu dokumentieren. Ihr Protokoll und die entsprechende Auswertung sollten *übersichtlich*, *nachvollziehbar* und *vollständig* sein. Wir verlangen explizit **keine Formatierung in Latex**. 

Die Abgabe erfolgt durch das Hochladen einer *pdf*-Version des Jupyter-notebooks (als Version $\mathrm{v1}$) ins ILIAS-System. Beachten Sie hierzu die Hinweise die wir für Sie in den Dokumenten [Praktische Hinweise zur Durchführung und Auswertung der Versuche](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/PraktischeHinweise.md) und [Arbeiten auf dem Jupyter-server](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Jupyter-server.md) bereitgestellt haben.  

## Einordnung des Praktikums und ECTS-Regelung

Das P1 und P2 entsprechen in der Bewertung des damit verbundenen Arbeitsaufwands jeweils **6 ECTS-Punkten**. Es handelt sich dabei um rund 1/5 Ihrer Arbeit für das Physikstudium im jeweils laufenden Semester. Diese Leistung erbringen Sie **konzentriert auf 10 Wochen des Semesters**. Sie sollten diese Zeit für die Praktika bei der Gestaltung Ihres Semesterplans dringend einplanen. 

Die Praktika der Physik bieten Ihnen die Möglichkeit zu Experimentieren, physikalische Gesetzmäßigkeiten experimentell zu überprüfen, physikalische Sachverhalte, die aus einer Vorlesung nicht immer intuitiv und klar sind, am Experiment nachzuvollziehen und sich in der Aufzeichnung, Dokumentation und Weiterverarbeitung von Messdaten mit wissenschaftlichem Anspruch auszubilden. Dies ist ein wesentlicher Bestandteil jedes Physikstudiums und damit Ihrer Ausbildung zum wissenschaftlichen Arbeiten. 

Bei der Berechnung der ECTS-Punkte für die Praktika legen wir das folgende Modell zugrunde: 

- **4–6 Stunden Versuchsvorbereitung**, in denen Sie sicherstellen, dass Sie nach Ihrer eigenen Einschätzung optimal auf den kommenden Versuch vorbereitet sind.
- **6 Stunden Versuchsbesprechung und -durchführung**.
- **2–4 Stunden Versuchsnachbereitung** (einschließlich potentieller Beanstandungen durch die Tutor:innen).      

Damit ergeben sich bis zu **160 Stunden** Arbeitsaufwand im laufenden Semester. 

Beachten Sie bei der Beurteilung des Arbeitsaufwands, dass die Praktika aus organisatorischen Gründen, bereits nach 10 Wochen und somit deutlich vor dem offiziellen Ende der Vorlesungszeit des Semesters enden. Dies räumt Ihnen die Möglichkeit ein sich gegen Ende der Vorlesungszeit angemessen auf anstehende Abschlussprüfungen vorzubereiten. Der Preis hierfür ist, dass sich der Arbeitsaufwand während des laufenden Praktikums entsprechend erhöht.

