<img src="../figures/Logo_KIT.svg" width="200" style="float:right;" />

# Fakultät für Physik

## Physikalisches Praktikum P1 für Studierende der Physik

Versuch P1-26, 27, 28 (Stand: Oktober 2023)

[Raum F1-15](https://labs.physik.kit.edu/img/Praktikum/Lageplan_P1.png)



# Kreisel

## Motivation

Die uns umgebende Natur ist i.a. weder geradlinig noch punktförmig, wie in der Schule oder den ersten Einführungsvorlesungen der Mechanik oft vorausgesetzt. Physikalische Körper bewegen sich im dreidimensionalen Raum und haben eine endliche Ausdehnung. Als erste Konsequenz erfolgt die Beschreibung der Bewegung physikalischer Körper nicht allein mit der Hilfe [skalarer](https://de.wikipedia.org/wiki/Skalar_(Mathematik)) Größen, wie der Masse $m$, sondern zusätzlich mit der Hilfe von [Vektoren](https://de.wikipedia.org/wiki/Vektor), mehr-komponentigen mathematischen Darstellungen, wie dem Ortsvektor $\vec{r}$, mit einem fest vorgegebenen Verhalten unter Transformationen im Raum. Ausgedehnte Körper, bei denen einzelne Punkte im Raum in festen Beziehungen zueinander stehen werden zudem mit Hilfe von [Tensoren](https://de.wikipedia.org/wiki/Tensor) beschrieben. Die Welt der [analytischen Geometrie](https://de.wikipedia.org/wiki/Analytische_Geometrie) wird durch komplizierte Verknüpfungen wie das [innere](https://de.wikipedia.org/wiki/Skalarprodukt), [äußere](https://de.wikipedia.org/wiki/Kreuzprodukt) oder das [Tensorprodukt](https://de.wikipedia.org/wiki/Tensorprodukt) bestimmt. Wichtige mathematische Gebilde, wie der [Hilbertraum](https://de.wikipedia.org/wiki/Hilbertraum), sind der Natur abgeschaut. 

Ausgedehnte Körper können manchmal nicht-intuitive, zum Teil verrückt anmutende Bewegungen ausführen, die durch die Sprache der analytischen Geometrie genau beschrieben und vorhergesagt werden können. Gerade aufgrund seiner bemerkenswerten Bewegungsformen ist der Kreisel vielen von Ihnen, als *physikalisches* Spielzeug, seit Kindesbein wohl bekannt. In der Physik ist der Kreisel ein niemals langweiliges Studienobjekt, um die manchmal nicht-intuitive Erfahrungswelt der uns umgebenden Realität mit der manchmal nicht besonders anschaulichen Welt der Mathematik in Verbindung zu bringen. Mit dem Versuch Kreisel, haben Sie Gelegenheit hierzu.   

## Lehrziele

Wir listen im Folgenden die wichtigsten **Lehrziele** auf, die wir Ihnen mit dem Versuch **Kreisel** vermitteln möchten: 

- Sie vergegenwärtigen sich die Bedeutung von Skalaren, Vektoren und Tensoren. 
- Mit dem [Trägheitstensor](https://de.wikipedia.org/wiki/Tr%C3%A4gheitstensor) $\boldsymbol{\Theta}$ beschäftigen Sie sich mit einer der experimentell zugänglichsten und noch anschaulichsten Tensorgrößen in der klassischen Physik. Dabei haben Sie die Möglichkeit mathematisch abstrakte Konzepte, wie [Eigenwert](https://de.wikipedia.org/wiki/Eigenwerte_und_Eigenvektoren), [Eigenvektor](https://de.wikipedia.org/wiki/Eigenwerte_und_Eigenvektoren) oder [Hauptachsentransformation](https://de.wikipedia.org/wiki/Hauptachsentransformation), die Sie aus der [linearen Algebra](https://de.wikipedia.org/wiki/Lineare_Algebra) kennen physikalisch mit Leben zu füllen. [Eigenwertprobleme](https://de.wikipedia.org/wiki/Verallgemeinertes_Eigenwertproblem) sind von entscheidender Bedeutung bei der Beschreibung stationärer Zustände in der Physik. 
- Sie untersuchen wichtige, nicht-alltägliche und zunächst nicht-intuitiv anmutende Eigenschaften des [symmetrischen Kreisels](https://de.wikipedia.org/wiki/Symmetrischer_Kreisel), wie [Nutation](https://de.wikipedia.org/wiki/Nutation_(Physik)) und [Präzession](https://de.wikipedia.org/wiki/Pr%C3%A4zession) und bestimmen daraus die [Trägheitsmomente](https://de.wikipedia.org/wiki/Tr%C3%A4gheitsmoment) $\Theta_{i}$ entlang der [Hauptträgheitsachsen](https://de.wikipedia.org/wiki/Haupttr%C3%A4gheitsachse) eines [kardanisch gelagerten](https://de.wikipedia.org/wiki/Kardanische_Aufh%C3%A4ngung) Kreisels. 
- Als historische Anwendung diskutieren Sie die Funktionsweise des [Kreiselkompass](https://de.wikipedia.org/wiki/Kreiselkompass).  

## Versuchsaufbau

Dieser Versuch ist zweigeteilt. Im Folgenden sind die verwendeten Aufbauten kurz beschrieben. Eine Auflistung der für ihre Auswertung wichtigen Bauteile und deren Eigenschaften finden Sie in der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel/Datenblatt.md).

### Physik starrer Körper

Im ersten Versuchsteil machen Sie ganz persönliche Erfahrungen mit der Physik starrer Körper, bei denen z.T. *Sie selbst* das Versuchsobjekt sind. 

<img src="./figures/VektorGeometrie.png" width="900" style="zoom:100%;" />

<img src="./figures/Kreiselkompass.png" width="900" style="zoom:100%;" />

Hierzu stehen Ihnen die folgenden Utensilien zur Verfügung: 

- Ein Drehschemel und ein Rad mit Zugband und Griffen (im Folgenden auch als Fahrradkreisel bezeichnet).
- Eine Sammlung von Holzquadern, die Sie in ihren Schwerpunkten zu jeder Grundfläche an einem Draht aufhängen können. Der Draht kann mit Hilfe eines externen Elektromotors in Drehung versetzt werden, so dass Sie das Verhalten der Holzquader bezüglich jeder Ihrer Hauptachsen untersuchen können. 
- Ein [kardanisch gelagerter](https://de.wikipedia.org/wiki/Kardanische_Aufh%C3%A4ngung) [Kreiselkompass](https://de.wikipedia.org/wiki/Kreiselkompass) auf einer drehbahren tellerförmigen Standfläche. Die Standfläche dient als Ersatz für die rotierende Erde. Der Kreisel lässt sich gegen die Standfläche verkippen, um variierende Breitengrade nachzustellen. Der innere Kardanrahmen des Kreisels ist mit Schraubenfedern in der angenommenen Tangential- (Horizontal-)ebene des eingestellten Breitengrads fixiert. Der Rotor des Kreisels kann mit Hilfe einer aufsetzbaren Antriebskurbel in Rotation versetzt werden. Die Standfläche wiederum kann mit Hilfe eines externen Elektromotors in eine langsame gleichmäßige Rotation versetzt werden, um die Revolution der Erde zu simulieren. 

### Kardanisch gelagerter Kreisel

Im zweiten Versuchsteil nehmen Sie quantitative Untersuchungen an einem kardanisch gelagerten Kreisel vor, den Sie mit Hilfe eines externen Elektromotors antreiben können. 

<img src="./figures/KardanischerKreisel.png" width="900" style="zoom:100%;" />

Der Rotor des Kreisels wird durch zwei Kardanrahmen gehalten. An den äußeren Kardanrahmen lassen sich (beidseitig) zwei Zylinder oder (einseitig) ein Metallstab, als zusätzliche Gewichte anbringen. Mit Hilfe der symmetrisch zu montierenden Zylinder erhöhen Sie das Trägheitsmoment entlang einer der Hauptträgheitsachsen des Kreisels. Mithilfe des Stabs sorgen Sie dafür, dass ein resultierendes Drehmoment auf den Kreisel wirkt, der dadurch nicht mehr momentenfrei lagert und in [Präzession](https://de.wikipedia.org/wiki/Pr%C3%A4zession) versetzt wird. Frequenzmessungen nehmen Sie mit Hilfe von Photosensoren mit eingebauten Lichtquellen vor, die zur flexibleren Handhabe auf [Schwanenhalshalterungen](https://de.wikipedia.org/wiki/Schwanenhals_(Halterung)) montiert sind. Aus den durchgeführten Messungen können Sie auf geschickte Weise die Trägheitsmomente entlang der Hauptträgheitsachsen des Kreisels experimentell bestimmen und die Masse des Rotors abschätzen.

## Wichtige Hinweise zum Versuch

- Rotierende Körper können sehr viel Energie aufnehmen, die man ihnen zunächst nicht ansieht. **Lassen Sie daher im Umgang mit den Kreiseln besondere Vorsicht walten.** Achten Sie z.B. darauf, dass sich lange Haare nicht im Kreisel verfangen. 
- Bei den Apparaturen handelt es sich z.T. um sehr teure Spezialanfertigungen zu pädagogischen Zwecken. Verwenden Sie zum Abbremsen der Kreisel die bereitliegenden Stofflappen und gehen Sie achtsam mit den Gerätschaften um. 

# Navigation

- Wichtige Hinweise zur Vorbereitung und  Durchführung von Aufgabe 1 finden Sie in der Datei [Hinweise-Aufgabe-1.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel/doc/Hinweise-Aufgabe-1.md).
- Wichtige Hinweise zur Vorbereitung und  Durchführung von Aufgabe 2 finden Sie in der Datei [Hinweise-Aufgabe-2.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel/doc/Hinweise-Aufgabe-2.md).
- Wichtige technische Daten zum Versuch finden Sie in der Datei [Datenblatt.md](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Kreisel/Datenblatt.md). 

