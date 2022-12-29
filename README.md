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

### Datenkodierung

...








## Tag 2: Wie funktioniert das Internet?

Der zweite Teil des Kurses gibt einen Überblick über die Grundlagen des Internets.