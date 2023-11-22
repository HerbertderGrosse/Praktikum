# Hinweise für den Versuch Vierpole und Leitungen

## Aufgabe 2: Drosselkette [4/4]

### Hinweise zur Durchführung

#### Aufgabe 2.4: Bestimmung der Phasendifferenz $\Delta\varphi$

Betreiben Sie für diese Aufgabe das Oszilloskop im Zweikanalmodus. 

- Legen Sie eine harmonische Wechselspannung als Eingangssignal an die Drosselkette.
- Bestimmen Sie für 6–8 verschiedene Frequenzen zwischen $10$–$650\hspace{0.05cm}\mathrm{kHz}$, $\Delta\varphi(\omega)$. Sorgen Sie dabei für einen reflexionsfreien Abschluss der Messanordnung am Leitungsende, wie für Aufgabe 2.2. Für die Einstellungen am Frequenzgenerator bieten sich z.B. die folgenden Werte an: $\nu=10,100,300,500,600,650,690\,\mathrm{kHz}$ an. 
- Die vorliegende Schaltung erlaubt es Ihnen auch ein Signal nach Durchlaufen nur eines einzelnen $\pi$-Glieds auszulesen. Führen Sie die gleiche Messreihe **sowohl für die gesamte Drosselkette, als auch für ein einzelnes $\pi$-Glied** durch. 

Bestimmen Sie abschließend nochmals $\omega_{0}$, diesmal aber aus $\Delta\varphi$. Gehen Sie dabei wie folgt vor:

- Betreiben Sie das Oszilloskop im Zweikanalmodus. Legen Sie dabei $U_{0}$ auf einen und $U_{1}$ auf den anderen Eingang. So können Sie den Verlauf beider Signale als [Lissajous-Figur](https://de.wikipedia.org/wiki/Lissajous-Figur) darstellen und Vielfache von $\Delta\varphi=n\hspace{0.05cm}\pi,\hspace{0.15cm}n\in\mathbb{N}$ leicht aus den sich einstellenden Diagonalen ablesen.

- Für das $\pi$-Glied gilt $\Delta\varphi(\omega_{0})=\pi$. Für die sechsgliedrige Drosselkette ist $\Delta\varphi$ um den Faktor $n=6$ relativ zum $\pi$-Glied verstärkt (siehe Diskussion [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2.md)). Bestimmen Sie $\omega$ für die am Oszilloskop ermittelten Werte von $\Delta\varphi=1\pi,2\pi,3\pi,4\pi,5\pi$. 
- Tragen Sie die ermittelten Werte für $\omega$ gegen $n\cdot\pi/6, \hspace{0.15cm}n=1\ldots5$ auf und passen Sie eine Gerade an den Verlauf der Messwerte an. Aus der Steigung der Geraden erhalten Sie eine Messung für $\omega_{0}$. Beurteilen sie die Güte der Anpassung. 

Vergleichen den so ermittelten Wert und dessen Unsicherheit mit Ihrem Ergebnis aus Aufgabe 2.2.  

#### Aufgabe 2.5: Reflexionen

- Schließen Sie für diesen Versuchsteil das Ende der Drosselkette kurz ($Z_{0}=0\,\Omega$). Dadurch wird das Signal am Kettenende mit einem Phasensprung von $\pi$ reflektiert (siehe Diskussion [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Leitungen.md)). 
- Vermeiden Sie Reflexionen am Leitungsanfang, indem Sie einen Steckwiderstand $Z_{\mathrm{E}}\approx Z_{0}$ zwischen Signalgenerator und Kettenanfang schalten. Ersetzen Sie hierzu den Kurzschlussstecker zwischen Generator und Kettenanfang durch den zur Verfügung stehenden $200\hspace{0.05cm}\Omega$-Vorwiderstand.  
- Schließen Sie eine rechteckförmige Wechselspannung ($\nu\approx20\hspace{0.05cm}\mathrm{kHz}$) an. Welche Signalform beobachten Sie am Kettenanfang? Entspricht dies Ihrer Erwartung?   

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2-b.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen)
