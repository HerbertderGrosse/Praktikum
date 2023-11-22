<img src="../figures/Logo_KIT.svg" width="200" style="float:right;" />

# Fakultät für Physik

## Physikalisches Praktikum P1 für Studierende der Physik

Versuch P1-43, 44, 45 (Stand: Oktober 2023)

[Raum F1-12](https://labs.physik.kit.edu/img/Praktikum/Lageplan_P1.png)



# Lichtgeschwindigkeit

## Motivation

Die erste Person, die auf die Endlichkeit der Lichtgeschwindigkeit $c$ hinwies, war der dänische Astronom [Ole Rømer](https://de.wikipedia.org/wiki/Ole_R%C3%B8mer), der 1676 die Umlaufzeit des Jupytermondes [Io](https://de.wikipedia.org/wiki/Liste_der_Jupitermonde) vermaß. Abhängig von der Jahreszeit, in der er seine Beobachtungen machte stellte Rømer systematische Unterschiede in der Periode von Io fest, was er damit erklärte, dass die Ausbreitung des Lichtes nicht augenblicklich erfolgen kann. Rømers Messung der Lichtgeschwindigkeit wurde erst akzeptiert, als sie 1729 von [James Bradley](https://de.wikipedia.org/wiki/James_Bradley) bestätigt wurde. Im 19. Jahrhundert, führten Albert Michelson und Edward Morley das berühmte [Michelson-Morley-Experiment](https://de.wikipedia.org/wiki/Michelson-Morley-Experiment) durch. Ziel dieses Versuchs war der Nachweis der Existenz des [Äthers](https://de.wikipedia.org/wiki/Äther_(Physik)), eines postulierten Mediums in dem sich Lichtwellen ausbreiten, und dass den gesamten Raum gleichmäßig ausfüllt. **Dieser Versuch schlug fehl!** Stattdessen führte er zum Schluss, dass die Geschwindigkeit mit der sich das Licht im Vakuum ausbreitet fest und unveränderlich sein muss. 

Heute sind wir in der Lage die astronomischen Laborsysteme der Vergangenheit in den Praktikumsraum F1-12 zu bringen, um diese sehr wichtige "Naturkonstante" im Praktikum nachzumessen. Sie werden $c$ nach zwei verschiedenen Methoden bestimmen: Zum einen nach der [Drehspiegelmethode](https://de.wikipedia.org/wiki/Drehspiegelmethode) von Foucault und Michelson. Hierbei handelt es sich um eine historische Messung, die erstmals 1850/51 durchgeführt wurde. Sie werden diese Messung als Demonstrationsversuch, gemeinsam mit Ihren Kommiliton:innen und Ihrem:r Tutor:in, durchführen und auswerten. Zum anderen messen Sie $c$ mit Hilfe der Phasenverschiebung modulierter Lichtsignale (Phasenvergleichsmethode). Man kann $c$ nicht einfach mit einer Stoppuhr messen. Beide Methoden zur Messung von $c$ beruhen auf raffinierten Techniken, ohne die die jeweilige Messung nicht möglich wäre: Bei der Drehspiegelmethode ist es der Aufbau als abbildendes optisches System, bei der Phasenvergleichsmethode ist es die geschickte Modulation des Lichtstrahls zur Messung kurzer Zeitabstände.

## Lehrziele

Wir listen im Folgenden die wichtigsten **Lehrziele** auf, die wir Ihnen mit dem Versuch **Lichtgeschwindigkeit** vermitteln möchten: 

- Sie lernen zwei interessante, experimentelle Techniken zur Bestimmung einer schwierig zu messenden Größe kennen. 
- Um sich auf die Versuche vorzubereiten leiten Sie alle nötigen Zusammenhänge her und vergegenwärtigen sich die Größenordnung der zu messenden Effekte.
- Sie lernen feste Phasenbeziehungen aus der Wellenmechanik als wichtiges Werkzeug zur Messung kurzer Zeitdifferenzen kennen und wenden dieses Werkzeug in einem leicht abgewandelten Zusammenhang zur Messung des Brechungsindex optisch dichter Medien an. 
- Sie wenden das Erlernte an, um den Brechungsindex optisch dichter Medien mit handelsüblichen Gebrauchsgegenständen zu bestimmen.  

## Versuchsaufbau

Der Versuch umfasst zwei unterschiedliche Aufbauten zur Messung der Lichtgeschwindigkeit. Im Folgenden sind die wichtigsten Informationen der verwendeten Aufbauten zusammengefasst. Für ihre Auswertung wichtige technische Details finden Sie in der Datei [Datenblatt.md](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Lichtgeschwindigkeit/Datenblatt.md). Die angegebenen Größen sind zudem in [*python*](https://www.python.org/)-Modulen im Verzeichnis [*params*](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/tree/main/Lichtgeschwindigkeit/params) auf dem SCC Gitlab Server hinterlegt. 

### Drehspiegelmethode

<img src="./figures/Drehspiegelmethode.png" width="900" style="zoom:100%;" />

Das Licht eines Lasers wird auf einen Drehspiegel gerichtet und von dort auf ein System aus einem Umlenk- und einem Endspiegel reflektiert. Der Strahlengang verläuft vom Laser zum Endspiegel und wieder zurück. Vor dem Laser befindet sich ein um $45^{\circ}$ zur Strahlachse gedrehter, halbdurchlässiger Spiegel als Strahlteiler, der einen Teil des reflektierten Lichts auf einen Schirm mit Ableseskala und USB-Mikroskop umlenkt. Die Skala wird mit Hilfe des Mikroskops auf einem Bildschirm angezeigt (siehe Bild unten links in der obigen [Skizze](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Lichtgeschwindigkeit/figures/Drehspiegelmethode.png)). Zwischen Dreh- und Umlenkspiegel befindet sich eine Linse zur Verringerung der Divergenz des Lichtstrahls der auf den Endspiegel abgebildet wird. Im Zeitfenster $\Delta t$ zwischen seinem ersten und zweiten Auftreffen auf den Drehspiegel hat ein angenommenes Lichtpaket, nach den Angaben der obigen Skizze, die Wegstrecke $2\,(a+b)$ zurückgelegt. Der Drehspiegel hat sich in dieser Zeit um den Winkel $\Delta\alpha$ weiter gedreht. Dadurch erscheint der auf den Schirm gelenkte Lichtstrahl im Vergleich zum Fall des ruhenden Drehspiegels versetzt. Der Versatz hängt von der Geschwindigkeit des Lichtpakets $c$ und der Frequenz $\nu$ ab, mit der sich der Drehspiegels dreht. Die Brennweite der Linse, sowie die festen Abstände zwischen dem Laser und den jeweiligen Spiegeln sind in der obigen [Skizze](https://git.scc.kit.edu/etp-lehre/p1-for-students/-/blob/main/Lichtgeschwindigkeit/figures/Drehspiegelmethode.png) angegeben. 

### Phasenvergleichsmethode

<img src="./figures/Phasenvergleichsmethode.png" width="900" style="zoom:100%;" />

Diese Methode zur Messung der Lichtgeschwindigkeit basiert auf der Messung der Phasenverschiebung $\Delta\varphi$ zwischen einem Empfänger- und Referenzsignal. Aus $\Delta\varphi$ lässt sich bei gegebener Kreisfrequenz $\omega$ des Referenzsignals eine Zeitdifferenz $\Delta t$ bestimmen und bei bekanntem Abstand $\ell$ zwischen Sender und Empfänger so die Lichtgeschwindigkeit berechnen. Eine monochromatische Lichtquelle (Sender) ist beweglich auf eine $\approx2\,\mathrm{m}$ lange optische Bank montiert. Ihr Licht wird mit Hilfe einer Sammellinse auf eine feststehende Photodiode (Empfänger) abgebildet. Ein $60\,\mathrm{MHz}$-Frequenzgenerator erzeugt ein Referenzsignal, mit dem die Intensität der Leuchtdiode des Senders moduliert wird. Die Lichtgeschwindigkeit ergibt sich aus der Phasenverschiebung $\Delta\varphi$ zwischen dem Empfänger- und Referenzsignal als Funktion des Abstandes zwischen Sender und Empfänger. 

## Anmerkungen zum Versuch

- Die Strahlung des verwendeten Lasers der [Klasse 2](https://de.wikipedia.org/wiki/Laser#Laserklassen) für die Messung von $c$ nach der Drehspiegelmethode ist **gefährlich für Ihre Augen!** Sie sind daher angehalten während des Versuchs eine der ausgelegten Laserschutzbrillen tragen. Beachten Sie unsere [Hinweise zum sicheren Umgang mit Lasern](https://labs.physik.kit.edu/163.php?tab=%5B313%5D#tabpanel-313).
- Die Messung von $c$ nach der Drehspiegelmethode führen Sie, als **Demonstrationsversuch**, mit Ihren Kommiliton:innen und Ihrem:r Tutor:in gemeinsam durch. 

# Navigation

- Wichtige Hinweise zur Vorbereitung und  Durchführung von Aufgabe 1 finden Sie in der Datei [Hinweise-Aufgabe-1.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit/doc/Hinweise-Aufgabe-1.md).
- Wichtige Hinweise zur Vorbereitung und  Durchführung von Aufgabe 2 finden Sie in der Datei [Hinweise-Aufgabe-2.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit/doc/Hinweise-Aufgabe-2.md).
- Wichtige Hinweise zur Vorbereitung und  Durchführung von Aufgabe 3 finden Sie in der Datei [Hinweise-Aufgabe-3.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit/doc/Hinweise-Aufgabe-3.md).
- Wichtige technische Daten zum Versuch finden Sie in der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit/Datenblatt.md). 
