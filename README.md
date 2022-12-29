# Was ist ein Computer?

Dieser Kurs soll den Teilnehmern einen Einblick in die Arbeitsweise von Computern und moderner Informationsverarbeitung geben. Nach diesem Kurs sollen alle Teilnehmer die Frage "Was ist ein Computer?" korrekt beantworten können und ein Grundverständins dafür haben wie das Internet funktioniert.

## Tag 1: Was ist ein Computer?

Der erste Teil des Kurses gibt einen Überblick über die Grundlagen heutiger IT-Systemen.

### Was ist ein Computer?

Zu unserem Alltag gehören diverse elektronische Geräte, wie zum Beispiel Notebooks, Smartphones, Sprachassistenten, Single Board Computer wie der Raspberry Pi, aber auch Waschmaschinen oder Kaffeemaschinen. Was davon ist ein Computer?

Wikipedia definiert einen [Computer](https://de.wikipedia.org/wiki/Computer) wie folgt:

> Ein Computer [...] ist ein Gerät, das mittels programmierbarer Rechenvorschriften Daten verarbeitet.

> Computer sind heute in allen Bereichen des täglichen Lebens vorzufinden, meistens in spezialisierten Varianten, die auf einen vorliegenden Anwendungszweck zugeschnitten sind. So dienen integrierte Kleinstcomputer [...] zur Steuerung von Alltagsgeräten wie Waschmaschinen [...]; in modernen Automobilen dienen sie [...] zur Anzeige von Fahrdaten und steuern in „Fahrassistenten“ diverse Manöver selbst.

Dies bedeutet dass fast jedes moderne Gerät beinhaltet mindestens einen Computer in From eines integrierten Kleinstcomputer (Embedded Device) beinhaltet, und alle der vorher genannten Geräte auch mindestens einen Computer beinhalten.

Ein Grundverständnis des Aufbaus und der Funktionsweise von Computer hilft die Möglichkeiten und Grenzen heutiger Systeme besser einschätzen zu können, und ist die Grundlage um in vielen Situationen, vor allem in Internet, informierte Entscheidungen zu treffen.

### Computer Architektur

Heutige Computer basieren auf der [Von-Neumann-Architektur](https://de.wikipedia.org/wiki/Von-Neumann-Architektur). Die zentrale, und damals revolutionäre, Idee dieser Architektur ist dass Daten und Programme in einem gemeinsamen Speicher abgelegt sind. Nach der Von-Neumann-Architektur besteht ein Computer aus einer Central Processing Unit (CPU) und über Busse angeschlossene Peripherie-Geräte, wie Speicherwerk oder I/O Geräte. Die CPU unterteilt sich weiter in eine Control Unit (CU) und ein Rechenwerk (Arithmetic-logic Unit, ALU). Unter das Speicherwerk fallen Festplatten und SSDs, aber auch der Arbeitsspeicher (Random Access Memory, RAM). Als I/O Geräte versteht das Model zum Beispiel Tastaturen und Monitore.

Heutige CPUs in PCs und Notebooks sind zum Beispiel Intel Core i, AMD Ryzen oder Apple M Cores. In Smartphones kommen SoCs (System on Chip) zum Einsatz die noch weitere Komponenten und Beschleuniger in einem Bauteil vereinen. Die CPUs dieser SoCs sind zum Beispiel Qualscomm Snapdragon, was häufig in Android Telefonen verwendet wird, oder Appels A Cores.

Der RAM ist der schnellste externe Speicher in einem heutigen PC, aber er verliert seine Daten wenn der Strom abgeschaltet wird. Gewöhnlich werden Daten vor der Verarbeitung durch die CPU zuerst vom persistenten Speicher, der Festplatte, in den flüchtigen Speicher, den RAM, geladen, da auf den RAM viel schneller zugegriffen werden kann als auf die Festplatte oder SSD. Eine typische Transferrate für DDR3 RAM sind 15 GB/s. Da RAM, im Vergleich zu Festplatten oder SSDs, sehr teuer ist, ist er gewöhnlich viel kleiner dimensioniert als die Festplatte. Typische Größen für RAM in heutigen PCs sind 8 GB oder 16 GB. Wenn der RAM zu klein dimensioniert ist, was häufig bei sehr günstigen PCs oder Notebooks der Fall ist, kann dies die Gesamtleistung des Systems deutlich ausbremsen. 

Ein GigaByte (GB) sind 1000 MegaByte (MB). Ein Smartphone Foto benötigt etwa 2.5 MB Speicherplatz. Heutige Programme benötigen häufig mehrere GB Speicherplatz.

In heutigen PCs oder Notebooks kommen gewöhnlich Solid State Disks (SSD) zum Einsatz. Typische Transferraten für aktuelle SSDs liegen bei ~2.5 GB/s. Da SSDs noch relativ teuer sind, sind typische Größen heute 512GB oder 1 TerraByte (TB). Ein TerraByte sind 1000 GB. SSDs gehören zum persistenten Speicher und behalten ihre Daten auch ohne Strom.

Wenn in einem System viel Speicherplatz benötigt wird kommen zusätzlich Festplatten (Hard Disk, HDD) zum Einsatz. Festplatten sind viel langsamer als SSDs, aber auch viel günstiger pro GB, vor allem bei großen Speichergrößen. Typische Transferraten von Festplatten sind 0.5 GB/s, und typische Größen sind 2 TB oder 4 TB. Auch Festplatten gehören zum persistenten Speicher, und behalten ihre Daten auch ohne Strom. Für die Archivierung von Daten sind Festplatten besser geeignet als SSDs, da dies ihre Daten länger behalten. HDDs können ihre Daten auch ohne Strom, wenn sie richtig gelagert werden, über Jahrzehnte behalten. SSDs hingegen verlieren ihre Daten ohne Strom innerhalb von wenigen Jahren.

### Wie arbeitet ein Computer?

Computer verarbeiten Daten, aus dem Speicher oder von Eingabegeräten, durch Programme. Ein Programm ist eine Liste von Befehlen, die sequenziell von der CPU abgearbeitet wird. Programme werden auf dem persistenten Speicher abgelegt und vor der Ausführung in den RAM geladen.

Jede CPU hat einen festen Befehlssatz, d.h. eine Menge von Befehlen die sie verarbeiten kann. Befehle sind dabei Folgen von 0en und 1en, und werden linear, Speicherzelle für Speicherzelle, abgearbeitet. Die einzelnen Befehle haben eine sehr geringe Komplexität. Typische Befehle sind Addition, Subtraktion und Vergleiche.

Befehle operieren auf CPU Registern. CPU Register sind in der CPU integrierter Speicher auf den direkt zugegriffen werden kann. Dieser Speicher ist nur wenige Byte groß und stellt die Parameter für Befehle dar. Diese Register bilden den lokalen, internen Zustand der CPU. Eines dieser Register ist der Programm Counter (PC). Zur Ausführung werden Programme ins RAM, an eine bekannte Stelle geladen, und dann der Program Counter auf diese Adresse gesetzt. Der Programm Counter ist immer die Speicheradresse des nächsten Befehls. Diese Register wird durch die CPU hochgezählt, kann aber durch Befehle manipuliert werden, um Sprünge zu realisieren. In Kombination mit Vergleichsbefehlen lassen sich damit Entscheidungen in Programmen realisieren.

### Datenkodierung

Ein Computer kann nicht zwischen Bilder, Texten oder Audio unterscheiden. Computer können ausschließlich binäre Daten verarbeiten. Binäre Daten sind Folgen von 0en und 1en. Die Folge selbst nennt man dabei die Syntax, eine Bedeutung erhält sie jedoch erst durch die Semantik. Die Semantik wird durch die Programme realisiert. Dieselbe Folge von 0en und 1en kann dadurch eine unterschiedliche Bedeutung haben, und ohne Kenntnis über die Semantik sind die Daten nutzlos.

Programme interpretieren und verarbeiten Daten, und geben den Daten Bedeutung. Ein Programm ist immer auf einen oder mehrere Anwendungsfälle zugeschnitten. Die Darstellung von Daten in einem Programm richtet sich immer nach diesem Anwendungsfall und ist unvollständig. 

Welches Programm verwendet wird um die Daten darzustellen wird auf dem Betriebssystem Windows durch die Dateiendung bestimmt. Das Standard-Programm ist aber nicht das einzige Programm sein das die Daten verarbeiten kann, und andere Programme können die Daten anders darstellen oder Daten sichtbar machen die vorhanden sind, aber vom Standard-Programm nicht angezeigt werden. An Word-Dokumenten (docx) kann man dies sehr gut verdeutlichen. Word-Dokumente sind auch Zip-Archive. Wenn wir die Dateiendung eines Word-Dokuments in .zip umbenennen können wir es entpacken und das interne Datenformat betrachten. Das Word-Dokument besteht dann aus einigen XML-Dateien, zur Beschreibung der Struktur und der Text-Inhalte, und weiteren Verzeichnissen, für spezielle Daten, wie zum Beispiel "media" das die eingebetteten Bilder enthält.

Wenn man Daten mit anderen austauscht, sollte man sich bewusst sein welche unsichtbaren Daten und welche Metadaten enthalten sind. Office-Dokumente enthalten häufig eine Änderungshistorie. Wenn man ein Word-Dokument mit dem "Angebot" an einen potentiellen Kunden schickt sollte man sich bewusst sein, dass der Kunde in diesem Fall Änderungen rückgängig machen kann, und damit z.B. gelöschte Absätze wiederherstellen kann. Auch Metadaten von Dokumenten können mehr verraten als man will. Typische Office Dokumente haben in den Metadaten die benutzte Programmversion, aber auch häufig den Benutzernamen und weiter Informationen über den Computer auf dem das Dokument erstellt wurde. Zur Übermittlung bieten sich dafür spezialisierte Formate wie PDF an. Office Programme bieten fast immer einen Export als PDF an, wobei auch PDF Dokumente diverse Metadaten enthalten, jedoch zumindest keine Änderungshistorie.

### Zahlensysteme

Für das Verständnis von Daten in Computern sind Zahlensystem von zentraler Bedeutung. Das wichtigste Zahlensystem für Computer ist das Binärsystem (Dualsystem). Beim Binärsystem ist die Wertigkeit der Stellen $2^i$. Diese bedeutet, die erste Stelle von rechts ist $2^0 = 1$ wert, die zweite Stelle ist $2^1 = 2$ wert, die dritte Stelle ist $2^2 = 4$ wert. Die Dualzahl $101_2 = 1 * 4 + 0 * 2 + 1 * 1 = 5_{10}$ im Dezimalsystem, mit dem wir im Alltag arbeiten.

Da die Binärdarstellung sehr viel Platz benötigt, und schwer zu lesen ist hat, hat auch das Hexadezimalsystem im IT-Bereich große Bedeutung. Beim Hexadezimalsystem ist die Wertigkeit der Stellen $16^i$, und es werden die Ziffern 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F verwendet. Die erste Stelle von rechts ist $16^0 = 1$ wert, die zweite Stelle ist $16^1 = 16$, und die dritte Stelle ist $16^2 = 256$ wert. Die Hexadezimalzahl $10_{16} = 1 * 16 + 0 * 1 = 16_{10}$ im Dezimalsystem. Die Hexadezimalzahl $AF_{16} = 10 * 16 + 15 * 1 = 175_{10}$ im Dezimalsystem, da die Ziffer A den Wert 10 und die Ziffer F den Wert 15 hat.

Binärzahlen lassen sich kompakter und besser lesbar als Hexadezimalzahlen darstellen. Der maximale Wert einer 4stelligen Binärzahl is $8+4+2+1=15_{10}=F_{16}$, was genau einer Stelle im Hexadezimalsystem entspricht. Dadurch übersetzen sich je vier Stellen einer Binärzahl in genau eine Stelle einer Hexadezimalzahl.

Die Binärzahl $1100_{2}=12_{10}=A_{16}$. Die Binärzahl $1100 0101_{2}$ = 1100 0101 = $A5_{16}$. Die Einheit Byte, die wir von MB, GB und TB kennen, sind acht Bit. Ein Byte lasst sich als acht Binärziffern oder 2 Hexadezimalziffern darstellen, $XX_{16}$ = $XXXX.XXXX_{2}$.

CPUs werden auch nach ihrer Registergröße und Speicherbandbreite in X-Bit Systeme unterteilt. Heutige kleine Microcontroller sind 8bit oder 16bit Systeme. Aktuelle PCs sind 64bit Systeme und einige Jahre alte Rechner sind häufig noch 32bit Systeme. Diese Speicherbandbreite bestimmt die maximale RAM Größe. 32bit Systeme können maximal 4 GB RAM adressieren, 64bit Systeme können maximal 16 Exabyte, d.h. 16 Milliarden Gigabyte, RAM adressieren.

### Datenkodierung

Da Computer nur Binärzahlen verarbeiten können müssen alle Daten die mit Computern verarbeitet werden als Binärzahlen, d.h. Folgen von 0en und 1en, dargestellt werden. Für die Darstellung von Grunddatentypen haben sich Standards etabliert.

Ganzzahlen werden häufig in der sogenannten Zweierkomplement-Darstellung gespeichert. Der Zahlenraum der dargestellt werden kann ist $-2^{n-1}, ... , 0, ... -2^{n-1}$, wobei n die Anzahl der Bits sind. Dei Anzahl der Bits orientiert sich an der Registergröße der CPU, z.B. 33-Bit, da diese Größe am effizientesten verarbeitet werden kann. Bei der Verwendung von 8 Bits (1 Byte) können die Werte von -127 bis 127 dargestellt werden. Bei der Verwendung von 32 Bits sind es schon -2.147.483.648 bis 2.147.483.648 und bei 64 Bits sind es -9.223.372.036.854.775.808 bis 9.223.372.036.854.775.808. Negative Zahlen werden kodiert als invertierter Binärwert der positiven Zahl plus 1. Für -4 und 8 Bit bedeutet dies:

- 4 = 0000 0100
- invertieren: 1111 1011
- 1 addieren: 1111 1100

Eine negative Zahl in dieser Darstellung lässt sich daran erkennen dass die höchstwertige Stelle 1 ist.

Diese Kodierung kann in der Praxis zu Problemen führen. Zwei Beispiele dafür sind Youtube und Reddit. Youtube hatte Probleme als das Lied "Gangnam-Style" mehr als 2.147.483.648 betrachtet wurde, da der Zähler als vorzeichenbehaftete 32-Bit Zahl kodiert war. Reddit hatte kürzlich Probleme, nach dem 2.147.483.648sten Kommentar, da dort ein Index als vorzeichenbehaftete 32-Bit Zahl implementiert war.

Gleitkommazahlen werden gewöhnlich nach IEE 754 kodiert. Dieser Standard sieht vor dass die Zahl als $x=$ $s$ $2^e$ $m$ dargestellt wird, wobei s das Vorzeichen ist, e der Exponent und m die Mantisse. Der kodierte Exponent ist der tatsächliche Exponent plus ein Biaswert, um negative Exponenten zu realisieren.

Als 32-Bit IEE 754 Zahl wird 3.14 als $0$ $2^1$ $1.5700000524520874$ dargestellt. Binär ist das 0 1000.0000 10.0100.0111.1010.1110.00010, was zurück gerechnet 3.1399998664855957031250000 ist.

Die Gleitkommadarstellung ist fast immer mit einem sehr kleinen Fehler verbunden, womit man sich aber einen sehr großen Zahlenbereich erkauft. Als Entwickler muss man sich jedoch dessen bewusst sein, da dies eine Fehlerquelle darstellt. Für präzise Berechnungen werden deshalb gerne andere, weniger effiziente, aber dafür fehlerfrei Darstellungen gewählt.

Texte werden im Computer als Folgen von Buchstaben kodiert. Dabei wird jedem Buchstaben eine Binärzahl zugeordnet. Frühere wurde häufig ASCII als sehr einfache Zeichenkodierung gewählt. Dabei ist jedem Buchstaben eine Zahl zwischen 0 und 255 zugeordnet, d.h. jeder Buchstabe braucht 1 Byte Speicherplatz. Dies reicht für dei meisten Sprachen aus, jedoch bei weitem nicht für alle, und mehrsprachige Texte werden nur begrenzt unterstützt.

Moderne Systeme verwenden häufig eine Unicode-Darstellung. Unicode ist ein Standard der das Ziel hat alle Zeichen aller Sprachen darzustellen, und noch einige mehr, wie zum Beispiel Emoticons. Die aktuell häufigste Zeichenkodierung ist UTF8, was eine auf Speichergröße optimierte Unicode Implementierung ist. Die häufigsten Zeichen werden dabei in ein Byte codiert, aber es gibt Präfixe die längere Zeichen einleiten.

Der Text "Hallo, Welt!" ist:

- als ASCII:  48 61 6c 6c 6f 2c 20 57 65 6c 74 21
- als UTF8:   48 61 6c 6c 6f 2c 20 57 65 6c 74 21
- als UTF-16: 0048 0061 006c 006c 006f 002c 0020 0057 0065 006c 0074 0021

Das Zeichen 😊 ist:

- als ASCII nicht darstellbar
- als UTF-8: F0 9F 98 8A
- als UTF-16: D83D DE0A

Die UTF-16 Darstellung benötigt mehr Platz, ist aber effizienter zum Arbeiten mit Texten, da jedes Zeichen die selbe Länge hat und damit einfach zum x-ten Zeichen gesprungen werden kann und einzelne Zeichen unabhängig vom restlichen Text verändert werden können.

Bilder werden im einfachsten Fall als zweidimensionale Tabelle von Farbpunkten gespeichert. Dabei ist jeder Tabelleneintrag ein Farbwert für den Bildpunkt. Für die Kodierung der Farbwerte kommen verschiedene Verfahren zum Einsatz. Ein geläufiges Verfahren ist RGBA. Dabei wir die Farbe als Rot-, Grün- und Blau-Anteil gespeichert, je ein Bit, und ein Bit für den Transparenzwert. Die einfachst Datei-Bildkodierung ist BMP. Bei BMP wird eine Farbpalette erstellt und dann jeder Rasterwert als Index der Tabelle gespeichert.

Heute übliche Bild-Formate sind JPG, eine verlustbehaftete Bildkompression, die häufig für Fotos verwendet wir, und PNG, eine verlustfreie Bildkompression die Transparenz unterstützt und gerne im Internet verwendet wird.

Beim Arbeiten mit Bildern sollte man beachten dass heutige Bildformate verschiedenste Metadaten, die sogenannten EXIF-Daten, beinhalten. Diese Daten können sehr hilfreich sein für die spätere Weiterverarbeitung, können aber auch sehr leicht Informationen weitergeben die man nicht weitergeben wollte. Smartphone Bilder haben unter anderem das Telefon-Model und die GPS-Koordinaten in ihren EXIF-Daten. Mit jedem veröffentlichten Foto teilt man damit auch welches Telefon-Model man verwendet und den genauen Standort wo man das Foto aufgenommen hat.

### Was ist ein Algorithmus?

Wikipedia definiert einen Algorithmus folgendermaßen:

> Ein Algorithmus ist eine eindeutige Handlungsvorschrift zur Lösung eines Problems oder einer Klasse von Problemen.

Die Informatik hat eine Reihe von Eigenschaften die ein Algorithmus erfüllen muss, damit ein Computer ihn ausführen kann:

- Finitheit: Ein Algorithmus muss endlich beschreibbar sein.
- Ausführbarkeit: Jeder Schritt des Algorithmus muss eindeutig ausführbar sein. Das bedeutet auch jeder Schritt muss so präzise beschrieben sein dass eindeutig ist was getan werden muss.
- Dynamische Finitheit: Der Algorithmus darf nur endlich viel Speicher verwenden.
- Terminierung: Der Algorithmus darf nur endlich viele Schritte benötigen.
- Determiniertheit: Der Algorithmus muss unter denselben Voraussetzungen das gleiche Ergebnis liefern.
- Determinismus: Der nächste Schritt des Algorithmus muss zu jedem Zeitpunkt eindeutig bestimmt sein.

Wenn in den Medien von einem Algorithmus die Rede ist, geht es in der Regel um algorithmische Darstellung von Inhalten. Dies wird von den meisten Onlinediensten heute verwendet, und dabei geht es fast immer darum dass durch die Darstellung Unternehmensziele optimiert werden sollen.

Ein Beispiel dafür sind die Facebook Timeline, die Posts von Freunden und Werbung, under der Benutzung psychologischer Forschungsergebnisse, so Darstellt das die Aufenthaltsdauer auf Facebook maximiert wird und die Wahrscheinlichkeit dass ein Nutzer auf Werbung klickt optimiert wird. Dies gilt jedoch nicht nur für Facebook, sondern auch für die meisten anderen Sozialen Medien und Video-Plattformen wie Youtube oder Netflix.

### Embedded Devices, Smart Devices und IoT

Ein eingebettetes System, engl. Embedded Device, ist ein kompakter Einplatinencomputer für eine spezielle Aufgabe. Dei Eingabegeräte von embedded Devices sind häufig Sensoren, zum Beispiel Temperatursensoren in einer Kaffeemaschine oder einer Heizungssteuerung oder Radarsensoren in eine Fahrzeugassistenzsystem. Die Ausgabegeräte von Embedded Devices sind gewöhnlich Aktoren, wie zum Beispiel Motoren im Auto oder Pumpen in der Kaffeemaschine.

Smarte Geräte, engl. Smart Devices, sind eine Klasse von Geräte, aber nicht die einzigen, in denen eingebettete System verbaut sind. Diese werden verwendet um die Benutzerfreundlichkeit zu verbessern oder fortgeschrittene Funktionen zu realisieren. Smart Devices zeichnen sich häufig dadurch aus dass sie mit dem Internet verbunden sind, wodurch die Rechenleistung im Gerät gering sein kann, und das Gerät dadurch günstiger zu produzieren ist. 

Die Nachteile die man sich dadurch einhandelt realisieren sich häufig erst nach einer Weile. Für jede Software werden über die Zeit Probleme gefunden, entweder in Form von Fehlern, oder in Form von Sicherheitslücken. Gerade bei Sicherheitslücken brauchen smarte Geräte Software-Updates, was kontinuierlich kosten auf Seite des Herstellers verursacht. Auch die "Backend"-Systeme, mit denen die smarten Geräte kommunizieren um ihre Funktionen zu erfüllen verursachen fortlaufend Aufwand und Kosten auf Seite des Herstellers. Damit smarte Geräte sicher und langfristig Betrieben werden können, und wirtschaftlich für den Hersteller sind, müssen sie fortlaufend diese laufenden Kosten wieder einspielen. Dies lässt sich nur durch Abo-Modelle langfristig umsetzen. Bei günstigen smarten Geräten, ohne laufende Kosten, ist absehbar dass ihr Verwendung nur zeitlich beschränkt möglich ist, da entweder der Hersteller den Support einstellt und die Backends abschaltet, oder bankrott geht.

## Tag 2: Wie funktioniert das Internet?

Der zweite Teil des Kurses gibt einen Überblick über die Grundlagen des Internets.

