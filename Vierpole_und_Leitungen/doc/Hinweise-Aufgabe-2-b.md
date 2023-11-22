# Hinweise für den Versuch Vierpole und Leitungen

## Aufgabe 2: Drosselkette [3/4]

### Hinweise zur Durchführung

#### Aufgabe 2.1: Bestimmung der charakteristischen Impedanz $Z_{0}$

Bei dieser Messung nutzen wir den Umstand, dass das Eingangssignal für $Z_{\mathrm{A}}=Z_{0}$ am Ende der Leitung **nicht** reflektiert wird (siehe Diskussion [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Leitungen.md)). 

Für den Fall $Z_{\mathrm{A}}\neq Z_{0}$ treten Reflexionen am Leitungsende auf, so dass das beobachtete Signal am Leitungsanfang eine Überlagerung aus dem ursprünglichen Signal und ggf. sogar mehrerer Reflexionen an den Leitungsenden ist.  Wie wählen für die Messung daher eine Signalform aus, mit der wir Überlagerungen möglichst einfach erkennen können. Sobald Sie Sie bei der Reglung von $Z_{\mathrm{A}}$ die charakteristische Impedanz $Z_{\mathrm{A}}=Z_{0}$ erreichen sollten Sie das Eingangssignal unverfälscht beobachten können. Durch die Wahl einer niedrigen Frequenz $\omega\ll\omega_{0}$ bestimmen Sie auf diese Weise in guter Näherung
$$
\begin{equation*}
Z_{\mathrm{A}}=Z_{0}\approx\sqrt{\frac{L}{C}}.
\end{equation*}
$$


Gehen Sie für die Messung wie folgt vor: 

- Legen Sie eine **rechteckförmige** Wechselspannung niedriger Frequenz an. Wir schlagen $\nu\approx 20\hspace{0.05cm}\mathrm{kHz}$, $U_{0}\approx 6\hspace{0.05cm}\mathrm{V_{SS}}$ vor.

- Schließen Sie die Drosselkette mit der regelbaren Lastimpedanz $Z_{\mathrm{A}}$, als Abschlusswiderstand kurz. 

- Beobachten Sie das Eingangssignal am Oszilloskop. 

- Regeln Sie $Z_{\mathrm{A}}$ solange, bis Sie das Eingangssignal unverfälscht beobachten können und lesen Sie den so erhaltenen Wert von $Z_{\mathrm{A}}$ ab. 

#### Aufgabe 2.2: Bestimmung der Grenzfrequenz $\omega_{0}$

Bestimmen Sie $\omega_{0}$ der Drosselkette wie folgt:

- Legen Sie eine **harmonische** Wechselspannung an. Wir schlagen $\nu\lesssim 1\hspace{0.05cm}\mathrm{MHz}$, $U_{0}\approx 6\hspace{0.05cm}\mathrm{V_{SS}}$ vor. Belassen Sie $Z_{\mathrm{A}}$ auf dem zuvor bestimmten Wert für $\omega\ll\omega_{0}$.
- Beobachten Sie das Eingangssignal und überzeugen Sie sich von der Frequenzunabhängigkeit der Eingangsspannung.
- Beobachten Sie das Ausgangssignal und erhöhen Sie $\omega$ schrittweise. Regeln Sie $Z_{\mathrm{A}}$ bei steigenden Werten von $\omega$ entsprechend Ihrer Erwartung für die Frequenzabhängigkeit von $Z_{0}$ (Gleichung **(3)** [hier](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2.md)) nach, um Reflexionen in der Leitung zu vermeiden. 
- Suchen Sie die Schwelle in $\omega$ auf, ab der die Drosselkette Signale mit $\omega>\omega_{0}$ als Tiefpass unterdrückt. Bestimmen Sie $\omega_{0}$ aus der Position für $\left|U_{n}\right|/\left|U_{0}\right|=1/10$. 

#### Aufgabe 2.3: Bestimmung von $C$ und $L$ der in der Drosselkette verbauten Elemente

Bestimmen Sie $C$ und $L$ aus den zuvor bestimmten Werten für $Z_{0}$ und $\omega_{0}$. Pflanzen Sie die Unsicherheiten Ihrer Messungen von $Z_{0}$ und $\omega_{0}$ entsprechend fort und vergleichen Sie mit den technischen Angaben im [Datenblatt.mb](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Vierpole_und_Leitungen/Datenblatt.md) zu diesem Versuch. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2-a.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2-c.md)
