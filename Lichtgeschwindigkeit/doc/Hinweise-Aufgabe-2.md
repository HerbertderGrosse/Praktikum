# Hinweise für den Versuch Lichtgeschwindigkeit

## Aufgabe 2: Phasenvergleichmethode

### Prinzip der Messung

Diese Methode zur Messung von $c$ basiert auf der Messung der Phasenverschiebung $\Delta\varphi$ zwischen einem Empfänger- und einem Referenzsignal. Aus $\Delta\varphi$ lässt sich bei gegebener Kreisfrequenz $\omega$ des Referenzsignals eine Zeitdifferenz $\Delta t$ bestimmen und bei bekanntem Abstand $\ell$ zwischen Sender und Empfänger so die *Phasengeschwindigkeit* berechnen. 

Bei der Bestimmung von $c$ mit Hilfe einer [Lissajous](https://de.wikipedia.org/wiki/Lissajous-Figur)-Figur messen Sie bei vorgegebenem $\Delta\varphi$ die Wegdifferenz $\Delta\ell$ des verschobenen Senders. In allen anderen Fällen bestimmen Sie $\Delta\varphi$ für vorgebenene Werte von $\ell$.   

### Messbereichserweiterung des Oszilloskops

Mit der Zeitauflösung eines einfachen Oszilloskops ist die beabsichtigte Messung mit dem vorliegenden Aufbau nicht ohne weiteres möglich. Sie können die Messung trotzdem mit den im Praktikum zur Verfügung stehenden Mitteln durchführen. Hierzu nutzen wir eines der [Additionstheoreme](https://de.wikipedia.org/wiki/Formelsammlung_Trigonometrie#Produkte_der_Winkelfunktionen) der Kosinus-Funktion: 

$$
\begin{equation}
\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta,
\end{equation}
$$
woraus sich der folgende Zusammenhang leicht ableiten lässt: 

$$
\begin{equation}
\cos\alpha\cos\beta = \frac{1}{2}\Bigl(\cos(\alpha+\beta)+\cos(\alpha-\beta)\Bigr).
\end{equation}
$$
Wir wählen zur Beschreibung des funktionalen Zusammenhangs des (ursprünglichen) Referenzsignals eine Kosinus-Funktion $\cos(\omega\,t+\varphi)$, wobei $\omega$ der Kreisfrequenz und $\varphi$ einer freien Phase entsprechen. Wir modulieren (mit Hilfe der in das Hauptnetzgerät eingebauten Mischstufen) die Amplitude des Referenzsignals multiplikativ mit einem gleichen Signal mit geringfügig niedrigerer Frequenz $\omega'\lesssim\omega$. Für das so veränderte (endgültige) Referenzsignal ergibt sich dadurch der folgende funktionale Zusammenhang zur Beschreibung seiner Amplitude: 

$$
\begin{equation}
\cos(\omega\,t+\varphi)\cos(\omega'\,t) = \frac{1}{2}\Bigl(\cos((\omega+\omega')\,t+\varphi) + \cos((\omega-\omega')\,t+\varphi)\Bigr).
\end{equation}
$$
Wir interessieren uns für den zweiten Term in der Klammer auf der rechten Seite der Gleichung, der den Verlauf $\cos((\omega-\omega')\,t+\varphi)$ aufweist. Der hochfrequente Term $\cos((\omega+\omega')\,t+\varphi)$ kann durch einen [Tiefpassfilter](https://de.wikipedia.org/wiki/Tiefpass) unterdrückt werden. 

Sie können feststellen, dass die Phase $\varphi$ unverändert vom ursprünglichen Referenzsignal (der Form $\cos(\omega\,t+\varphi)$) auf den Term $\cos((\omega-\omega')\,t+\varphi)$ übertragen wird, so dass auch die später zu messende Phasendifferenz $\Delta\varphi$ zwischen Empfänger- und Referenzsignal erhalten bleibt, d.h. eine Phasendifferenz $\Delta\varphi$ im nicht modulierten Eingangssignal entspricht der gleichen Phasendifferenz $\Delta\overline{\varphi}$ in der späteren Darstellung auf dem Oszilloskop. Zur Unterscheidung stellen wir die auf dem Oszilloskop dargestellten Größen überstrichen dar. 

Es gilt zwar $\Delta\varphi=\Delta\overline{\varphi}$, die Frequenzen $\omega$ und $\overline{\omega}\equiv\omega-\omega^{\prime}$ unterscheiden sich jedoch. Der Verlauf auf der Zeitachse des Oszilloskops erscheint daher um den Faktor $\omega/\overline{\omega}$  gedehnt:

$$
\begin{equation}
\Delta \overline{\varphi} = \Delta \varphi;\qquad
\overline{\omega}\,\Delta\overline{t} = \omega\,\Delta t;\qquad
\Delta \overline{t} = \omega/\overline{\omega}\,\Delta t,
\end{equation}
$$
wobei $\Delta \overline{t}$ einem auf dem Oszilloskop dargestellten Zeitfenster (mit dem Verlauf $\cos((\overline{\omega})\,t+\varphi)$) und $\Delta t$ einem Zeitfenster des ursprünglichen Signals (mit dem Verlauf $\cos(\omega\,t+\varphi)$) entsprechen. Durch den gedehnten Maßstab können auch sehr kurze Zeitdifferenzen im Eingangssignal aufgelöst werden. Es handelt sich also effektiv um eine **"Messbereichserweiterung" des Oszilloskops hin zu kürzeren Zeitabständen**.

Um $\Delta\varphi$ deutlich sichtbar zu machen wird das Referenzsignal mit einem Störsignal der Frequenz $59,9\,\mathrm{MHz}$ multiplikativ gemischt. Mittels eines [Tiefpassfilters](https://de.wikipedia.org/wiki/Tiefpass) werden die hochfrequenten Anteile des gemischten Signals unterdrückt und die niederfrequenten Anteile auf einem einfachen computergestützten Oszilloskop, als Funktion der Zeit dargestellt.

### Hinweise zur Durchführung

- Bestimmen Sie $\Delta\overline{\varphi}$ für mindestens fünf verschiedene Werte von $\ell$. Beachten Sie den Zeit Dehnungsfaktor $\omega/\overline{\omega}$ bei der Bestimmung von $\Delta t$. 
- Tragen Sie die Wertepaare graphisch auf und nehmen Sie eine geeignete Anpassung vor. Begründen Sie das der Anpassung zu Grunde gelegte Modell.
- Geben Sie ein Maß für die Güte der Anpassung (*goodness of fit*) als $\chi^{2}/\mathrm{ndof}$ und als $p$-Wert an und bewerten Sie die Anpassung. 
- Überlegen Sie welche äußeren Parameter Sie für die Bestimmung von $c$ noch kontrollieren müssen und wie gut dies der Fall ist.
- Geben Sie Ihr Ergebnis aus der Anpassung mit statistischen und systematischen Unsicherheiten an.

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit)

