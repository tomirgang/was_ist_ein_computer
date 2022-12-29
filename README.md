# Was ist ein Computer?

Dieser Kurs soll den Teilnehmern einen Einblick in die Arbeitsweise von Computern und moderner Informationsverarbeitung geben. Nach diesem Kurs sollen alle Teilnehmer die Frage "Was ist ein Computer?" korrekt beantworten können und ein Grundverständins dafür haben wie das Internet funktioniert.

## Tag 1: Was ist ein Computer?

Der erste Teil des Kurses gibt einen Überblick über die Grundlagen heutiger IT-Systemen.

### Was ist ein Computer?

<!--Folie 4-->

Zu unserem Alltag gehören diverse elektronische Geräte, wie zum Beispiel Notebooks, Smartphones, Sprachassistenten, Single Board Computer wie der Raspberry Pi, aber auch Waschmaschinen oder Kaffeemaschinen. Was davon ist ein Computer?

<!--Folie 5-->

Wikipedia definiert einen [Computer](https://de.wikipedia.org/wiki/Computer) wie folgt:

> Ein Computer [...] ist ein Gerät, das mittels programmierbarer Rechenvorschriften Daten verarbeitet.

> Computer sind heute in allen Bereichen des täglichen Lebens vorzufinden, meistens in spezialisierten Varianten, die auf einen vorliegenden Anwendungszweck zugeschnitten sind. So dienen integrierte Kleinstcomputer [...] zur Steuerung von Alltagsgeräten wie Waschmaschinen [...]; in modernen Automobilen dienen sie [...] zur Anzeige von Fahrdaten und steuern in „Fahrassistenten“ diverse Manöver selbst.

<!--Folie 6-->

Dies bedeutet dass fast jedes moderne Gerät beinhaltet mindestens einen Computer in From eines integrierten Kleinstcomputer (Embedded Device) beinhaltet, und alle der vorher genannten Geräte auch mindestens einen Computer beinhalten.

Ein Grundverständnis des Aufbaus und der Funktionsweise von Computer hilft die Möglichkeiten und Grenzen heutiger Systeme besser einschätzen zu können, und ist die Grundlage um in vielen Situationen, vor allem in Internet, informierte Entscheidungen zu treffen.

### Computer Architektur

<!--Folie 8-->

Heutige Computer basieren auf der [Von-Neumann-Architektur](https://de.wikipedia.org/wiki/Von-Neumann-Architektur). Die zentrale, und damals revolutionäre, Idee dieser Architektur ist dass Daten und Programme in einem gemeinsamen Speicher abgelegt sind. Nach der Von-Neumann-Architektur besteht ein Computer aus einer Central Processing Unit (CPU) und über Busse angeschlossene Peripherie-Geräte, wie Speicherwerk oder I/O Geräte. 

<!--Folie 9-->

Die CPU unterteilt sich weiter in eine Control Unit (CU) und ein Rechenwerk (Arithmetic-logic Unit, ALU). Unter das Speicherwerk fallen Festplatten und SSDs, aber auch der Arbeitsspeicher (Random Access Memory, RAM). Als I/O Geräte versteht das Model zum Beispiel Tastaturen und Monitore.

<!--Folie 10-->

Heutige CPUs in PCs und Notebooks sind zum Beispiel Intel Core i, AMD Ryzen oder Apple M Cores. In Smartphones kommen SoCs (System on Chip) zum Einsatz die noch weitere Komponenten und Beschleuniger in einem Bauteil vereinen. Die CPUs dieser SoCs sind zum Beispiel Qualscomm Snapdragon, was häufig in Android Telefonen verwendet wird, oder Appels A Cores.

<!--Folie 11-->

Der RAM ist der schnellste externe Speicher in einem heutigen PC, aber er verliert seine Daten wenn der Strom abgeschaltet wird. Gewöhnlich werden Daten vor der Verarbeitung durch die CPU zuerst vom persistenten Speicher, der Festplatte, in den flüchtigen Speicher, den RAM, geladen, da auf den RAM viel schneller zugegriffen werden kann als auf die Festplatte oder SSD. Eine typische Transferrate für DDR3 RAM sind 15 GB/s. Da RAM, im Vergleich zu Festplatten oder SSDs, sehr teuer ist, ist er gewöhnlich viel kleiner dimensioniert als die Festplatte. Typische Größen für RAM in heutigen PCs sind 8 GB oder 16 GB. Wenn der RAM zu klein dimensioniert ist, was häufig bei sehr günstigen PCs oder Notebooks der Fall ist, kann dies die Gesamtleistung des Systems deutlich ausbremsen. 

Ein GigaByte (GB) sind 1000 MegaByte (MB). Ein Smartphone Foto benötigt etwa 2.5 MB Speicherplatz. Heutige Programme benötigen häufig mehrere GB Speicherplatz.

<!--Folie 12 -->

In heutigen PCs oder Notebooks kommen gewöhnlich Solid State Disks (SSD) zum Einsatz. Typische Transferraten für aktuelle SSDs liegen bei ~2.5 GB/s. Da SSDs noch relativ teuer sind, sind typische Größen heute 512GB oder 1 TerraByte (TB). Ein TerraByte sind 1000 GB. SSDs gehören zum persistenten Speicher und behalten ihre Daten auch ohne Strom.

<!--Folie 13 -->

Wenn in einem System viel Speicherplatz benötigt wird kommen zusätzlich Festplatten (Hard Disk, HDD) zum Einsatz. Festplatten sind viel langsamer als SSDs, aber auch viel günstiger pro GB, vor allem bei großen Speichergrößen. Typische Transferraten von Festplatten sind 0.5 GB/s, und typische Größen sind 2 TB oder 4 TB. Auch Festplatten gehören zum persistenten Speicher, und behalten ihre Daten auch ohne Strom. Für die Archivierung von Daten sind Festplatten besser geeignet als SSDs, da dies ihre Daten länger behalten. HDDs können ihre Daten auch ohne Strom, wenn sie richtig gelagert werden, über Jahrzehnte behalten. SSDs hingegen verlieren ihre Daten ohne Strom innerhalb von wenigen Jahren.

### Wie arbeitet ein Computer?

<!--Folie 15 -->

Computer verarbeiten Daten, aus dem Speicher oder von Eingabegeräten, durch Programme. Ein Programm ist eine Liste von Befehlen, die sequenziell von der CPU abgearbeitet wird. Programme werden auf dem persistenten Speicher abgelegt und vor der Ausführung in den RAM geladen.

<!--Folie 16 -->

Jede CPU hat einen festen Befehlssatz, d.h. eine Menge von Befehlen die sie verarbeiten kann. Befehle sind dabei Folgen von 0en und 1en, und werden linear, Speicherzelle für Speicherzelle, abgearbeitet. Die einzelnen Befehle haben eine sehr geringe Komplexität. Typische Befehle sind Addition, Subtraktion und Vergleiche.

<!--Folie 17 -->

Befehle operieren auf CPU Registern. CPU Register sind in der CPU integrierter Speicher auf den direkt zugegriffen werden kann. Dieser Speicher ist nur wenige Byte groß und stellt die Parameter für Befehle dar. Diese Register bilden den lokalen, internen Zustand der CPU. Eines dieser Register ist der Programm Counter (PC). Zur Ausführung werden Programme ins RAM, an eine bekannte Stelle geladen, und dann der Program Counter auf diese Adresse gesetzt. Der Programm Counter ist immer die Speicheradresse des nächsten Befehls. Diese Register wird durch die CPU hochgezählt, kann aber durch Befehle manipuliert werden, um Sprünge zu realisieren. In Kombination mit Vergleichsbefehlen lassen sich damit Entscheidungen in Programmen realisieren.

### Datenkodierung

<!--Folie 19 -->

Ein Computer kann nicht zwischen Bilder, Texten oder Audio unterscheiden. Computer können ausschließlich binäre Daten verarbeiten. Binäre Daten sind Folgen von 0en und 1en. Die Folge selbst nennt man dabei die Syntax, eine Bedeutung erhält sie jedoch erst durch die Semantik. Die Semantik wird durch die Programme realisiert. Dieselbe Folge von 0en und 1en kann dadurch eine unterschiedliche Bedeutung haben, und ohne Kenntnis über die Semantik sind die Daten nutzlos.

<!--Folie 20 -->

Programme interpretieren und verarbeiten Daten, und geben den Daten Bedeutung. Ein Programm ist immer auf einen oder mehrere Anwendungsfälle zugeschnitten. Die Darstellung von Daten in einem Programm richtet sich immer nach diesem Anwendungsfall und ist unvollständig. 

<!--Folie 21 -->

Welches Programm verwendet wird um die Daten darzustellen wird auf dem Betriebssystem Windows durch die Dateiendung bestimmt. Das Standard-Programm ist aber nicht das einzige Programm sein das die Daten verarbeiten kann, und andere Programme können die Daten anders darstellen oder Daten sichtbar machen die vorhanden sind, aber vom Standard-Programm nicht angezeigt werden. An Word-Dokumenten (docx) kann man dies sehr gut verdeutlichen. Word-Dokumente sind auch Zip-Archive. Wenn wir die Dateiendung eines Word-Dokuments in .zip umbenennen können wir es entpacken und das interne Datenformat betrachten. Das Word-Dokument besteht dann aus einigen XML-Dateien, zur Beschreibung der Struktur und der Text-Inhalte, und weiteren Verzeichnissen, für spezielle Daten, wie zum Beispiel "media" das die eingebetteten Bilder enthält.

<!--Folie 22 -->

Wenn man Daten mit anderen austauscht, sollte man sich bewusst sein welche unsichtbaren Daten und welche Metadaten enthalten sind. Office-Dokumente enthalten häufig eine Änderungshistorie. Wenn man ein Word-Dokument mit dem "Angebot" an einen potentiellen Kunden schickt sollte man sich bewusst sein, dass der Kunde in diesem Fall Änderungen rückgängig machen kann, und damit z.B. gelöschte Absätze wiederherstellen kann. Auch Metadaten von Dokumenten können mehr verraten als man will. Typische Office Dokumente haben in den Metadaten die benutzte Programmversion, aber auch häufig den Benutzernamen und weiter Informationen über den Computer auf dem das Dokument erstellt wurde. Zur Übermittlung bieten sich dafür spezialisierte Formate wie PDF an. Office Programme bieten fast immer einen Export als PDF an, wobei auch PDF Dokumente diverse Metadaten enthalten, jedoch zumindest keine Änderungshistorie.

### Zahlensysteme

<!--Folie 24 -->

Für das Verständnis von Daten in Computern sind Zahlensystem von zentraler Bedeutung. Das wichtigste Zahlensystem für Computer ist das Binärsystem (Dualsystem). Beim Binärsystem ist die Wertigkeit der Stellen $2^i$. Diese bedeutet, die erste Stelle von rechts ist $2^0 = 1$ wert, die zweite Stelle ist $2^1 = 2$ wert, die dritte Stelle ist $2^2 = 4$ wert. Die Dualzahl $101_2 = 1 * 4 + 0 * 2 + 1 * 1 = 5_{10}$ im Dezimalsystem, mit dem wir im Alltag arbeiten.

<!--Folie 25 -->

Da die Binärdarstellung sehr viel Platz benötigt, und schwer zu lesen ist hat, hat auch das Hexadezimalsystem im IT-Bereich große Bedeutung. Beim Hexadezimalsystem ist die Wertigkeit der Stellen $16^i$, und es werden die Ziffern 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F verwendet. Die erste Stelle von rechts ist $16^0 = 1$ wert, die zweite Stelle ist $16^1 = 16$, und die dritte Stelle ist $16^2 = 256$ wert. Die Hexadezimalzahl $10_{16} = 1 * 16 + 0 * 1 = 16_{10}$ im Dezimalsystem. Die Hexadezimalzahl $AF_{16} = 10 * 16 + 15 * 1 = 175_{10}$ im Dezimalsystem, da die Ziffer A den Wert 10 und die Ziffer F den Wert 15 hat.

<!--Folie 26 -->

Binärzahlen lassen sich kompakter und besser lesbar als Hexadezimalzahlen darstellen. Der maximale Wert einer 4stelligen Binärzahl is $8+4+2+1=15_{10}=F_{16}$, was genau einer Stelle im Hexadezimalsystem entspricht. Dadurch übersetzen sich je vier Stellen einer Binärzahl in genau eine Stelle einer Hexadezimalzahl.

<!--Folie 27 -->

Die Binärzahl $1100_{2}=12_{10}=A_{16}$. Die Binärzahl $1100 0101_{2}$ = 1100 0101 = $A5_{16}$. Die Einheit Byte, die wir von MB, GB und TB kennen, sind acht Bit. Ein Byte lasst sich als acht Binärziffern oder 2 Hexadezimalziffern darstellen, $XX_{16}$ = $XXXX.XXXX_{2}$.

<!--Folie 28 -->

CPUs werden auch nach ihrer Registergröße und Speicherbandbreite in X-Bit Systeme unterteilt. Heutige kleine Microcontroller sind 8bit oder 16bit Systeme. Aktuelle PCs sind 64bit Systeme und einige Jahre alte Rechner sind häufig noch 32bit Systeme. Diese Speicherbandbreite bestimmt die maximale RAM Größe. 32bit Systeme können maximal 4 GB RAM adressieren, 64bit Systeme können maximal 16 Exabyte, d.h. 16 Milliarden Gigabyte, RAM adressieren.

### Datenkodierung

<!--Folie 29 -->

Da Computer nur Binärzahlen verarbeiten können müssen alle Daten die mit Computern verarbeitet werden als Binärzahlen, d.h. Folgen von 0en und 1en, dargestellt werden. Für die Darstellung von Grunddatentypen haben sich Standards etabliert.

<!--Folie 30 -->

Ganzzahlen werden häufig in der sogenannten Zweierkomplement-Darstellung gespeichert. Der Zahlenraum der dargestellt werden kann ist $-2^{n-1}, ... , 0, ... -2^{n-1}$, wobei n die Anzahl der Bits sind. Dei Anzahl der Bits orientiert sich an der Registergröße der CPU, z.B. 33-Bit, da diese Größe am effizientesten verarbeitet werden kann. Bei der Verwendung von 8 Bits (1 Byte) können die Werte von -127 bis 127 dargestellt werden. Bei der Verwendung von 32 Bits sind es schon -2.147.483.648 bis 2.147.483.648 und bei 64 Bits sind es -9.223.372.036.854.775.808 bis 9.223.372.036.854.775.808. Negative Zahlen werden kodiert als invertierter Binärwert der positiven Zahl plus 1. Für -4 und 8 Bit bedeutet dies:

- 4 = 0000 0100
- invertieren: 1111 1011
- 1 addieren: 1111 1100

Eine negative Zahl in dieser Darstellung lässt sich daran erkennen dass die höchstwertige Stelle 1 ist.

<!--Folie 31 -->

Diese Kodierung kann in der Praxis zu Problemen führen. Zwei Beispiele dafür sind Youtube und Reddit. Youtube hatte Probleme als das Lied "Gangnam-Style" mehr als 2.147.483.648 betrachtet wurde, da der Zähler als vorzeichenbehaftete 32-Bit Zahl kodiert war. Reddit hatte kürzlich Probleme, nach dem 2.147.483.648sten Kommentar, da dort ein Index als vorzeichenbehaftete 32-Bit Zahl implementiert war.

<!--Folie 32 -->

Gleitkommazahlen werden gewöhnlich nach IEE 754 kodiert. Dieser Standard sieht vor dass die Zahl als $x=$ $s$ $2^e$ $m$ dargestellt wird, wobei s das Vorzeichen ist, e der Exponent und m die Mantisse. Der kodierte Exponent ist der tatsächliche Exponent plus ein Biaswert, um negative Exponenten zu realisieren.

Als 32-Bit IEE 754 Zahl wird 3.14 als $0$ $2^1$ $1.5700000524520874$ dargestellt. Binär ist das 0 1000.0000 10.0100.0111.1010.1110.00010, was zurück gerechnet 3.1399998664855957031250000 ist.

Die Gleitkommadarstellung ist fast immer mit einem sehr kleinen Fehler verbunden, womit man sich aber einen sehr großen Zahlenbereich erkauft. Als Entwickler muss man sich jedoch dessen bewusst sein, da dies eine Fehlerquelle darstellt. Für präzise Berechnungen werden deshalb gerne andere, weniger effiziente, aber dafür fehlerfrei Darstellungen gewählt.

<!--Folie 33 -->

Texte werden im Computer als Folgen von Buchstaben kodiert. Dabei wird jedem Buchstaben eine Binärzahl zugeordnet. Frühere wurde häufig ASCII als sehr einfache Zeichenkodierung gewählt. Dabei ist jedem Buchstaben eine Zahl zwischen 0 und 255 zugeordnet, d.h. jeder Buchstabe braucht 1 Byte Speicherplatz. Dies reicht für dei meisten Sprachen aus, jedoch bei weitem nicht für alle, und mehrsprachige Texte werden nur begrenzt unterstützt.

Moderne Systeme verwenden häufig eine Unicode-Darstellung. Unicode ist ein Standard der das Ziel hat alle Zeichen aller Sprachen darzustellen, und noch einige mehr, wie zum Beispiel Emoticons. Die aktuell häufigste Zeichenkodierung ist UTF8, was eine auf Speichergröße optimierte Unicode Implementierung ist. Die häufigsten Zeichen werden dabei in ein Byte codiert, aber es gibt Präfixe die längere Zeichen einleiten.

<!--Folie 34 -->

Der Text "Hallo, Welt!" ist:

- als ASCII:  48 61 6c 6c 6f 2c 20 57 65 6c 74 21
- als UTF8:   48 61 6c 6c 6f 2c 20 57 65 6c 74 21
- als UTF-16: 0048 0061 006c 006c 006f 002c 0020 0057 0065 006c 0074 0021

Das Zeichen 😊 ist:

- als ASCII nicht darstellbar
- als UTF-8: F0 9F 98 8A
- als UTF-16: D83D DE0A

Die UTF-16 Darstellung benötigt mehr Platz, ist aber effizienter zum Arbeiten mit Texten, da jedes Zeichen die selbe Länge hat und damit einfach zum x-ten Zeichen gesprungen werden kann und einzelne Zeichen unabhängig vom restlichen Text verändert werden können.

<!--Folie 35 -->

Bilder werden im einfachsten Fall als zweidimensionale Tabelle von Farbpunkten gespeichert. Dabei ist jeder Tabelleneintrag ein Farbwert für den Bildpunkt. Für die Kodierung der Farbwerte kommen verschiedene Verfahren zum Einsatz. Ein geläufiges Verfahren ist RGBA. Dabei wir die Farbe als Rot-, Grün- und Blau-Anteil gespeichert, je ein Bit, und ein Bit für den Transparenzwert. Die einfachst Datei-Bildkodierung ist BMP. Bei BMP wird eine Farbpalette erstellt und dann jeder Rasterwert als Index der Tabelle gespeichert.

Heute übliche Bild-Formate sind JPG, eine verlustbehaftete Bildkompression, die häufig für Fotos verwendet wir, und PNG, eine verlustfreie Bildkompression die Transparenz unterstützt und gerne im Internet verwendet wird.

<!--Folie 36 -->

Beim Arbeiten mit Bildern sollte man beachten dass heutige Bildformate verschiedenste Metadaten, die sogenannten EXIF-Daten, beinhalten. Diese Daten können sehr hilfreich sein für die spätere Weiterverarbeitung, können aber auch sehr leicht Informationen weitergeben die man nicht weitergeben wollte. Smartphone Bilder haben unter anderem das Telefon-Model und die GPS-Koordinaten in ihren EXIF-Daten. Mit jedem veröffentlichten Foto teilt man damit auch welches Telefon-Model man verwendet und den genauen Standort wo man das Foto aufgenommen hat.

### Was ist ein Algorithmus?

<!--Folie 38 -->

Wikipedia definiert einen Algorithmus folgendermaßen:

> Ein Algorithmus ist eine eindeutige Handlungsvorschrift zur Lösung eines Problems oder einer Klasse von Problemen.

Die Informatik hat eine Reihe von Eigenschaften die ein Algorithmus erfüllen muss, damit ein Computer ihn ausführen kann:

- Finitheit: Ein Algorithmus muss endlich beschreibbar sein.
- Ausführbarkeit: Jeder Schritt des Algorithmus muss eindeutig ausführbar sein. Das bedeutet auch jeder Schritt muss so präzise beschrieben sein dass eindeutig ist was getan werden muss.
- Dynamische Finitheit: Der Algorithmus darf nur endlich viel Speicher verwenden.
- Terminierung: Der Algorithmus darf nur endlich viele Schritte benötigen.
- Determiniertheit: Der Algorithmus muss unter denselben Voraussetzungen das gleiche Ergebnis liefern.
- Determinismus: Der nächste Schritt des Algorithmus muss zu jedem Zeitpunkt eindeutig bestimmt sein.

<!--Folie 39 -->

Wenn in den Medien von einem Algorithmus die Rede ist, geht es in der Regel um algorithmische Darstellung von Inhalten. Dies wird von den meisten Onlinediensten heute verwendet, und dabei geht es fast immer darum dass durch die Darstellung Unternehmensziele optimiert werden sollen.

Ein Beispiel dafür sind die Facebook Timeline, die Posts von Freunden und Werbung, under der Benutzung psychologischer Forschungsergebnisse, so Darstellt das die Aufenthaltsdauer auf Facebook maximiert wird und die Wahrscheinlichkeit dass ein Nutzer auf Werbung klickt optimiert wird. Dies gilt jedoch nicht nur für Facebook, sondern auch für die meisten anderen Sozialen Medien und Video-Plattformen wie Youtube oder Netflix.

### Embedded Devices, Smart Devices und IoT

<!--Folie 41 -->

Ein eingebettetes System, engl. Embedded Device, ist ein kompakter Einplatinencomputer für eine spezielle Aufgabe. Dei Eingabegeräte von embedded Devices sind häufig Sensoren, zum Beispiel Temperatursensoren in einer Kaffeemaschine oder einer Heizungssteuerung oder Radarsensoren in eine Fahrzeugassistenzsystem. Die Ausgabegeräte von Embedded Devices sind gewöhnlich Aktoren, wie zum Beispiel Motoren im Auto oder Pumpen in der Kaffeemaschine.

<!--Folie 42 -->

Smarte Geräte, engl. Smart Devices, sind eine Klasse von Geräte, aber nicht die einzigen, in denen eingebettete System verbaut sind. Diese werden verwendet um die Benutzerfreundlichkeit zu verbessern oder fortgeschrittene Funktionen zu realisieren. Smart Devices zeichnen sich häufig dadurch aus dass sie mit dem Internet verbunden sind, wodurch die Rechenleistung im Gerät gering sein kann, und das Gerät dadurch günstiger zu produzieren ist. 

Die Nachteile die man sich dadurch einhandelt realisieren sich häufig erst nach einer Weile. Für jede Software werden über die Zeit Probleme gefunden, entweder in Form von Fehlern, oder in Form von Sicherheitslücken. Gerade bei Sicherheitslücken brauchen smarte Geräte Software-Updates, was kontinuierlich kosten auf Seite des Herstellers verursacht. Auch die "Backend"-Systeme, mit denen die smarten Geräte kommunizieren um ihre Funktionen zu erfüllen verursachen fortlaufend Aufwand und Kosten auf Seite des Herstellers. Damit smarte Geräte sicher und langfristig Betrieben werden können, und wirtschaftlich für den Hersteller sind, müssen sie fortlaufend diese laufenden Kosten wieder einspielen. Dies lässt sich nur durch Abo-Modelle langfristig umsetzen. Bei günstigen smarten Geräten, ohne laufende Kosten, ist absehbar dass ihr Verwendung nur zeitlich beschränkt möglich ist, da entweder der Hersteller den Support einstellt und die Backends abschaltet, oder bankrott geht.

## Tag 2: Wie funktioniert das Internet?

Der zweite Teil des Kurses gibt einen Überblick über die Grundlagen des Internets.

### Wie funktioniert das Internet?

<!--Folie 5 -->

Das Internet ist ein Netz aus Rechnernetzen. Wikipedia definiert ein [Rechnernetz](https://de.wikipedia.org/wiki/Rechnernetz) folgendermaßen:

> Ein [...] Computernetzwerk ist ein Zusammenschluss verschiedener [...] primär selbstständiger elektronischer Systeme [...], der die Kommunikation der einzelnen Systeme untereinander ermöglicht. Ziel ist hierbei z. B. die gemeinsame Nutzung von Ressourcen wie Netzwerkdruckern, Servern, Dateien und Datenbanken. [...] Besondere Bedeutung hat heute auch die direkte Kommunikation zwischen den Netzwerknutzern (Chat, VoIP-Telefonie etc.).

Ziel eines Netzwerks ist es nach dieser Definition die Kommunikation zischen den einzelnen Teilnehmern zu ermöglichen, um Ressourcen gemeinsam zu Nutzen. Diese Ressourcen werden von sogenannten Servern bereitgestellt. Server sind Computer, die darauf optimiert sind eine Ressourcen zur Verfügung zu stellen. Das kann ein Post von anderen Benutzern sein, im Fall von Sozialen Netzwerken, oder ein Film, im Fall von Videodiensten wie Netflix, oder ein gemeinsamer Drucker im Firmennetzwerk, oder auch Telefonie, im Fall von Voice over IP (VoIP).

<!--Folie 6 -->

In vielen dieser Fälle erfolgt die Kommunikation der Geräte nach dem [Client-Server-Modell](https://de.wikipedia.org/wiki/Client-Server-Modell). Wikipedia definiert das Client-Server-Modell folgendermaßen:

> Das Client-Server-Modell [...] beschreibt eine Möglichkeit, Aufgaben und Dienstleistungen innerhalb eines Netzwerkes zu verteilen. [...] Der Client kann auf Wunsch einen Dienst vom Server anfordern [...]. Der Server [...] beantwortet die Anforderung [...]; üblicherweise kann ein Server gleichzeitig für mehrere Clients arbeiten.

In diesem Modell muss der Server für die Client erreichbar sein, d.h. eine IP-Adresse haben die im Netz bekannt ist. Für Dienste im Internet bedeutet dies dass der Server öffentlich erreichbar sein muss. Die Client-Anwendungen der Benutzer kontaktieren über das Netzwerk diesen Server um die Dienste anzufordern.

<!--Folie 7 -->

Das [Internet](https://de.wikipedia.org/wiki/Internet) ist ein globales Netzwerk das lokale Netze verbindet. Wikipedia definiert das Client-Server-Modell folgendermaßen:

> Das Internet [...] ist ein weltweiter Verbund von Rechnernetzwerken [...]. Es ermöglicht die Nutzung von Internetdiensten wie WWW, E-Mail, [...] Der Datenaustausch zwischen den über das Internet verbundenen Rechnern erfolgt über die technisch normierten Internetprotokolle.

Nach dieser Definition ist ein zentraler Punkt des Internets Datenaustausch. Dieser Datenaustausch wird in vielen Fällen über Webseiten realisiert, die von einem Browser, als Client, von einem Webserver abgerufen werden. Zur Beschreibung von Webseiten wird die [Hypertext Markup Language](https://de.wikipedia.org/wiki/Hypertext_Markup_Language) (HTML) verwendet. Wikipedia definiert das HTML folgendermaßen:

<!--Folie 8 -->

> Die Hypertext Markup Language [...] ist eine textbasierte Auszeichnungssprache zur Strukturierung elektronischer Dokumente [...]. HTML-Dokumente sind die Grundlage des World Wide Web und werden von Webbrowsern dargestellt.

HTML dient zur statischen Beschreibung der Inhalte, d.h. HTML definiert verschiedene Element wie z.B. Überschriften und Absätze, die dann vom Browser interpretiert werden um den Inhalt darzustellen. HTML sieht dabei keine Formatierung der Inhalte vor, d.h. z.B. Farben oder Schriftgrößen. Jeder Browser bringt eingene Standards dafür mit, fast immer wird jedoch parallel zum HTML auch ein [Cascading Style Sheet](https://de.wikipedia.org/wiki/Cascading_Style_Sheets) (CSS) geliefert, das definiert wie die einzelnen Elemente dargestellt werden. Mit modernem CSS lassen sich auch einfache Animationen realisieren, dynamische Inhalte werden aber fast immer mit [JavaScript](https://de.wikipedia.org/wiki/JavaScript) (JS) realisiert. Wikipedia definiert JavaScript folgendermaßen:

<!--Folie 9 -->

> JavaScript [...] ist eine Skriptsprache, die ursprünglich [...] für dynamisches HTML in Webbrowsern entwickelt wurde, um Benutzerinteraktionen auszuwerten, Inhalte zu verändern, nachzuladen oder zu generieren und so die Möglichkeiten von HTML zu erweitern.

In dieser Definition stecken drei wesentliche Aussagen. JavaScript ist ein Programm, das vom Server heruntergeladen und auf dem Rechner des Clients ausgeführt wird. Das Programm kann die Inhalte der Browser-Darstellung dynamisch verändern, um z.B. auf Benutzereingaben zu reagieren, und das Programm kann mit dem Server kommunizieren, z.B. um Inhalte nachzuladen.

<!--Folie 10 -->

JavaScript Programme können aber nicht nur vom Server kommen. Browser können das vom Server geladene JavaScript manipulieren oder teilweise oder gar nicht ausführen. Dies kann auch durch den Benutzer und Plugins konfiguriert werden, und wird z.B. für Werbe-Blocker verwendet. Moderne Browser erlauben es dem Nutzer über die Plugins Greasemonkey oder Tampermonkey in Webseiten eigene Programme einzuschleusen. Das folgende Skript ersetzt auf der [Heise](http://heise.de) alle vorkommen des Worts "Wirtschaft" durch ein grün markiertes "Hohoho":

```JavaScript
// ==UserScript==
// @name         Replace Wirtschaft
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Replace Wirtschaft
// @author       You
// @match        https://www.heise.de/
// @icon         https://www.google.com/s2/favicons?sz=64&domain=heise.de
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    var content = document.getElementsByTagName('body')[0];
    if (content) {
        console.log('replace');
        content.innerHTML = content.innerHTML.replaceAll('Wirtschaft', '<span style="background-color:lightgreen">Hohoho</span>');
    }
})();
```

Diese Änderungen sind nur lokal, d.h. nur im eigenen Browser sichtbar, da die Manipulation im Browser, bei der Darstellung der Inhalte, und nicht auf dem Server stattfindet.

### Wie funktioniert Verschlüsselung?

<!--Folie 11 -->

Verschlüsselung wird verwendet um Inhalte vor fremden Augen zu schützen. Verschlüsselung kann nicht vor Manipulation der Inhalte schützen, sie macht es jedoch schwierig Inhalte gezielt zu verändern. Zur Überprüfung von Inhalten können Signaturen eingesetzt werden.

<!--Folie 12 -->

Im einfachsten Szenario wird eine symmetrische Verschlüsselung verwendet, d.h. zum ver- und entschlüsseln wird dasselbe Passwort benötigt, und Alice will Bob eine geheime Nachricht zukommen lassen. Malloy würde gerne den Inhalt kennen, vor ihm soll er jedoch verborgen werden, obwohl er die übermittelte Nachricht lesen kann. Um dies zu erreichen müssen sich in diesem Fall Alice und Bob vorher bereits auf einen Verschlüsselungsalgorithmus und ein Passwort geeinigt haben. Alice verschlüsselt dann die Nachricht, unter Verwendung des Algorithmus und des Passworts und sendet sie an Bob. Nach dem die Nachricht verschlüsselt ist, ist diese unlesbar. Da Bob den Algorithmus und das Passwort kennt kann er jedoch die Nachricht wiederherstellen und lesen.

Der wichtigste Grundsatz bei Verschlüsselung ist dass der Algorithmus immer öffentlich sein sollte. Einen guten Verschlüsselungsalgorithmus zu schreiben, der wirklich sicherstellen kann dass die Daten geschützt sind, ist eine sehr schwierige Aufgabe, und lässt sich nur durch Reviews und Analysen von Experten auf dem Gebiet der Verschlüsselung erreichen. Es sollte niemals eine eigene Verschlüsselung erfunden werden, da diese mit Sicherheit sehr einfach gebrochen werden kann. Es gibt für jeden Anwendungsfall Verschlüsselungsalgorithmen, die öffentlich bekannt sind, und von namhaften Experten und Institutionen überprüft wurden.

<!--Folie 13 -->

HTTP ist unverschlüsselt, d.h. der Internetanbieter und jeder weiter Besitzer eines Geräts auf dem Weg kann die Daten lesen, auswerten und einfach manipulieren. HTTP sollte heute nicht mehr verwendet werden. Um die Kommunikation zwischen dem Client und dem Server wird heute, im Fall von HTTPS, [Transport Layer Security](ttps://de.wikipedia.org/wiki/Transport_Layer_Security) (TLS) eingesetzt. Wikipedia definiert TLS folgendermaßen:

> Transport Layer Security [...], auch bekannt unter der Vorgängerbezeichnung Secure Sockets Layer (SSL), ist ein Verschlüsselungsprotokoll zur sicheren Datenübertragung im Internet.

Wichtig dabei ist dass TLS die Daten nur auf dem Weg zum Server schützt. Der Server kann, und muss in vielen Fällen, die Daten lesen und verarbeiten. Mit Hilfe von TLS lassen sich nur die Inhalte schützen, nicht jedoch die Metadaten. Unter Metadaten versteht man hier Informationen wie z.B. wer hat wann mit wem kommuniziert. Im Fall von Alice und Bob bedeutet dies dass Malloy nicht lesen kann was Alice an Bob geschrieben hat, er weiß jedoch dass Alice mit Bob kommuniziert hat, und in vielen Fällen reicht das schon aus. Im realen Leben bedeutet dies, dass dein Internetanbieter nicht herausfinden kann welche Pornos du angeschaut hast, aber dass du eine Porno-Seite besucht hast weiß er schon. Auch für benutzerspezifische Werbung oder Strafverfolgung ist die Information wer hat wann und die häufig mit wem kommuniziert viel wichtiger sein als die konkreten Inhalte der Nachrichten, und kann viel einfacher automatisiert ausgewertet werden.

<!--Folie 14 -->

Auch heute noch sind eMail nach wie vor unverschlüsselt, d.h. jeder Teilnehmer auf dem Kommunikationsweg kann die Inhalte mitlesen. Weiter sollte man sich bewusst sein dass eMail selbst keine Authentifizierung des Kommunikationspartners hat, d.h. der Absender einer eMail kann sehr einfach "gefälscht" werden, da der Client den Absender festlegt. Zum senden von eMails wir das [Simple Mail Transfer Protocol](https://de.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) (SMTP) verwendet. Diese Protokoll stammt noch aus den Anfängen des Internets, als nur eine kleine Anzahl von Hochschulen verbunden waren, und alle Teilnehmer als vertrauenswürdig angesehen wurden. Zum Abrufen von eMails aus seinem eigenen Postfach würde früher [POP3](https://de.wikipedia.org/wiki/Post_Office_Protocol) verwendet, heute wird fast ausschließlich [IMAP](https://de.wikipedia.org/wiki/Internet_Message_Access_Protocol) verwendet. Sowohl beim Senden als auch beim Empfangen von Nachrichten kann heute TLS verwendet werden, wenn der eMail Client richtig konfiguriert ist. Diese schützt jedoch nicht auf dem Transport der eMails zwischen den eMail Servern. Auch dort kann TLS zum Einsatz kommen, und seriöse Anbieter nutzen dies auch, als Nutzer kann man sich jedoch nicht darauf verlassen.

<!--Folie 15 -->

Selbst wenn für Nachrichten TLS verwendet wird können die involvierten Server-Betreiber die Nachrichten dennoch lesen, da TLS nur auf dem Transportweg, jedoch nicht auf dem Server schützt. Um Nachrichten sicher zu schützen muss eine [Ende-zu-Ende-Verschlüsselung](https://de.wikipedia.org/wiki/Ende-zu-Ende-Verschl%C3%BCsselung) verwendet werden. Für eMails gibt es [PGP/MIME](https://de.wikipedia.org/wiki/PGP/MIME), das ein Public-Key-Verfahren nutzt, und [S/MIME](https://de.wikipedia.org/wiki/S/MIME), das Zertifikate verwendet. S/MIME wird häufig von größeren Firmen eingesetzt, ist jedoch mit Aufwand und häufig auch Kosten für die Zertifikate verbunden. PGP/MIME kann ohne Kosten benutzt werden, ist jedoch mit Aufwand verbunden und es gibt keine einheitliche und öffentliche Infrastruktur für den Schlüsselaustausch.

<!--Folie 17 -->

In den aktuellen politischen Diskussionen geht es häufig auch um Metadaten. Das Bundesamt für Sicherheit in der Informationstechnik beschreibt [Metadaten](ttps://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Onlinekommunikation/Chat-Messenger/Messenger/messenger_node.html#:~:text=Nachrichten%2C%20die%20%C3%BCber%20Messenger%20verschickt,das%20Datum%20und%20die%20Uhrzeit.) folgendermaßen:

> Nachrichten, die über Messenger verschickt werden, bestehen aus dem Text der Nachricht [...] und sogenannten Metadaten. Zu den Metadaten zählen die Kennung des Absenders, häufig in der Form der Telefonnummer, die Kennung des Adressaten, das Datum und die Uhrzeit.  [...] Solche Daten dienen nicht nur der korrekten Zuleitung der Nachricht, sondern können auch zur Analyse von Vorlieben und ähnlichem genutzt werden. Auf diese Weise lassen sich Profile erstellen, die für personalisierte Werbung genutzt werden können.

<!--Folie 18 -->

Als Nutzer muss man sich bewusst sein dass man durch Kenntnis solcher Profile sehr einfach manipuliert werden kann, und selbst das Bewusstsein darüber schützt nur begrenzt. Aus Metadaten lassen sich. mit Hilfe von Data Science, auch Information gewinnen die man im ersten Moment für unmöglich hält. David Kiesel zeigt dies sehr schön im [Vortag Spiegel Mining](https://media.ccc.de/v/33c3-7912-spiegelmining_reverse_engineering_von_spiegel-online) und der dazugehörigen [Artikel-Serie](https://www.dkriesel.com/spiegelmining). Allein durch die Auswertung der öffentlichen Metddaten der Spiegel Homepage, wenn ein Artikel von welchen Redakteuren veröffentlicht wurde, rekonstruiert er die interne Struktur von Spiegel Online, und kann am Ende sogar darauf schließen welche Mitarbeiter eine private Beziehung pflegen.

### Was ist Public Key Infrastruktur?

<!--Folie 20 -->

Ich habe den Begriff Public Key Infrastruktur bereits im Kontext von HTTPS erwähnt, ich will dieses Thema aber hier ausführlicher Darstellen, une es ist einen eigenen Abschnitt wert. Public Key Verschlüsselung fällt in den Bereich der asymmetrischen Verschlüsselungsverfahren, die in den letzten Jahren sehr an Bedeutung gewonnen haben. Wikipedia definiert ein [Asymmetrisches Kryptosystem](https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem) folgendermaßen:

> Das „asymmetrische Kryptosystem“ oder „Public-Key-Kryptosystem“ ist ein kryptographisches Verfahren, bei dem [...]  die kommunizierenden Parteien keinen gemeinsamen geheimen Schlüssel zu kennen brauchen. Jeder Benutzer erzeugt sein eigenes Schlüsselpaar, das aus einem geheimen Teil (privater Schlüssel) und einem nicht geheimen Teil (öffentlicher Schlüssel) besteht. Der öffentliche Schlüssel ermöglicht es jedem, Daten für den Besitzer des privaten Schlüssels zu verschlüsseln, [...]. Der private Schlüssel ermöglicht es seinem Besitzer, mit dem öffentlichen Schlüssel verschlüsselte Daten zu entschlüsseln, [...].

<!--Folie 21 -->

Diese Verfahren beruhen auf mathematischen Problemen die es erlauben eine Richtung sehr einfach und effizient zu berechnen, die Rückrichtung ist jedoch nicht in machbarem Aufwand berechenbar, d.h. die Rückrichtung zu berechnen würde mindestens mehrere hunderttausend Jahre benötigen mit aktuellen Computern. Auf Basis von asymmetrischer Verschlüsselung lassen sich [Public-Key-Infrastrukturen](https://de.wikipedia.org/wiki/Public-Key-Infrastruktur) aufbauen. Wikipedia definiert eine Public-Key-Infrastruktur folgendermaßen:

> Mit Public-Key-Infrastruktur [...] bezeichnet man in der Kryptologie ein System, das digitale Zertifikate ausstellen, verteilen und prüfen kann. Die innerhalb einer PKI ausgestellten Zertifikate werden zur Absicherung rechnergestützter Kommunikation verwendet.

Public-Key-Infrastrukturen sind nicht nur die Basis von HTTPS und anderen TLS Verfahren, sondern sind auch die Grundlage der Corona Impfzertifikate. Sie erlauben neben der Verschlüsselung von Inhalten auch die Signatur von Daten. Durch Signaturen kann ein Anwender, oder ein Programm, überprüfen ob die Daten valide sind, in dem zusammen mit den Daten auch eine Prüfsumme übermittelt wird. Diese Prüfsumme wurde mit dem privaten Schlüssel des Ausstellers berechnet, und kann mit dessen öffentlichem Schlüssel überprüft werden. Diese Signatur zu fälschen ist ähnlich schwierig wie das zugrunde liegende Verschlüsselungsverfahren zu brechen.

### Was ist die Cloud?

<!--Folie 23 -->

Die Daten die wir auf dem Transport mit Verschlüsselung und Signaturen schützen liegen am Ende häufig in sogenannten Clouds. Der Begriff Cloud hat keinen technischen Hintergrund, sonder kommt von Management-Präsentation in denen externe, unbekannte Systeme häufig als Wolke (engl. Cloud) dargestellt wurden. Die Wikipedia definiert die [Cloud](https://de.wikipedia.org/wiki/Cloud_Computing) folgendermaßen:

> Cloud Computing [...] beschreibt ein Modell, das bei Bedarf [...] zeitnah und mit wenig Aufwand geteilte Computerressourcen als Dienstleistung [...] bereitstellt und nach Nutzung abrechnet.

Dies heißt im Kern, die Cloud sind Server von anderen Anbietern. Dies impliziert auch dass der Cloud-Anbieter vollen Zugriff auf die Daten in der Cloud hat, wenn diese nicht verschlüsselt sind. Praktisch bedeutet dies, dass jeder Mitarbeiter mit entsprechenden Rechten, zum Beispiel bei DropBox, alle Dateien aller Kunden sehen, verändern und löschen kann. Seriöse Anbieter versuchen diesen Personenkreis klein zu halten, und versuchen mit Firmenrichtlinien Missbrauch zu vermeiden, Sicherheit bietet jedoch nur Verschlüsselung. Wichtige Daten sollten nie nur an einem Ort abgespeichert werden, auch nicht nur in der Cloud, da ein technischer Defekt oder eine Einstellung des Dienstes so zum Verlust der Daten führen kann. Als weiter Kopie biete sich die Cloud als Ablageort für verschlüsselte Daten an. Bei der Auswahl des Cloud-Anbieters sollte man auch die für den Anbieter lokale Gesetzgebung betrachten. Auch der seriöseste Cloud-Anbieter kann wenig gegen einen Gerichtsbeschluss an seinem Firmensitz ausrichten.

### Was ist ein Hacker Angriff?

<!--Folie 25 -->

Ein weiter Aspekt des Internets, der gerne in der Presse und Politik auftaucht, sind Hacker Angriffe. Um Hacker Angriffe zu verstehen muss man zunächst verstehen was ein ["Black-Hat Hacker"](ttps://de.wikipedia.org/wiki/Hacker_(Computersicherheit)#Black-Hats) ist. Wikipedia definiert Black-Hats folgendermaßen:

> Black-Hats [...] handeln mit krimineller Energie [...] und beabsichtigen [...] das Zielsystem zu beschädigen oder Daten zu stehlen[...].

Black-Hats sind also Kriminelle, oder staatliche Akteure, deren Ziel es ist fremde Computer zu manipulieren. Dabei kommen fast immer folgende Angriffswege zum Einsatz:

[Phishing](https://de.wikipedia.org/wiki/Phishing) ist eine Falschinformationskampagne, deren Ziel es ist einen Nutzer des fremden Rechners so zu manipulieren dass er dem Angreifer Zugang gewährt. dies können z.B. eMails mit gefälschtem Absender und manipulierten Anhängen sein, die beim Öffnen dem Angreifer Zugriff geben. Phishing ist eine von vielen [Social Engineering](https://de.wikipedia.org/wiki/Social_Engineering_(Sicherheit)) Methoden die nicht den Computer sondern den Nutzer angreift. Gerade Kriminelle nutzen häufig Social Engineering da diese Angriffe einfach breit gestreut werden können, und viel günstiger, risikoloser und schneller sind als technische Angriffe. Bei hoch-gesicherten technischen Systemen kann Social Engineering der einzige Angriffsweg sein.

Ein weiterer Angriffsweg sind schlecht konfigurierte System, die z.B. Standard-Passwörter des Herstellers verwenden. Diese betrifft häufig Privatpersonen und kleine Unternehmen. Kriminelle benutzen Programme um alle aus dem Internet erreichbaren Geräte auf bekannte unsichere Konfiguration und Standardpasswörter zu überprüfen, und dann z.B. durch Verschlüsselung der Daten und Erpressung des Besitzers Gewinn zu erzielen. Diese Angriffe werden auch zunehmend voll-automatisiert ausgeführt, wodurch auch Privatepersonen und geringe Erpressungssummen lukrativ werden.

Softwarefehler und bekannte Sicherheitslücken (CVE, [Common Vulnerabilities and Exposures](https://de.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) sind ein weiterer technischer Angriffsweg. Hier gibt es vor allem zwei Szenarien. Staatliche Akteure, mit nahezu unbegrenzten Ressourcen, oder Kriminelle können über bekannte oder noch unbekannte Sicherheitslücken gezielt bestimmte Ziele angreifen, was dann auch Stoff für Hollywood ist, und aus der Ferne Industriespionage betreiben. Diese Szenario ist nur für sehr wichtige Ziele lukrativ, da diese Art der Angriffe sehr teuer und zeitaufwändig sind. Im Gegensatz zu Hollywood, bleiben solche Angriffe fast immer lange unentdeckt, da die Angreifer sehr geschickt und vorsichtig agieren, um ihren Zugang nicht zu gefährden. Ein wichtiger werdendes zweites Szenario ist die massenhafte Ausnutzung einer öffentlich bekannten Sicherheitslücke, wie z.B. im Fall von [EternalBlue](https://de.wikipedia.org/wiki/EternalBlue) und [WannaCry](https://de.wikipedia.org/wiki/WannaCry). Dabei hat ein Angreifer automatisiert alle Systeme mit der Schwachstelle angegriffen und verschlüsselt, um dann Lösegeld für die Daten zu erpressen. Diese Art von Angriff wird auch für Privatpersonen zunehmend relevant, da gerade günstige IoT Geräte und Smartphones häufig nicht oder schlecht vom Hersteller gewartet werden, und dadurch leicht automatisiert über bekannte Schwachstellen angegriffen werden können.

<!--Folie 26 -->

Egal welchen der obigen Wege genutzt wurde, läuft ein Hacker-Angriff fast immer nach folgendem Schema ab:

- Der Angreifer erlangt Zugriff auf das Zielsystem.
- Der Angreifer sichert seinen Zugriff, z.B. durch das installieren von Schadsoftware. Dieser Schritt ist für das Opfer, d.h. den Nutzer des angegriffenen Geräts oft nicht erkennbar.
- Der Angreifer nutzt eine erlangten Zugriffsrechte um diese auszuweiten, in der er z.B. andere Geräte im internen Netzwerk angreift die nicht von aussen erreichbar sind.
- Diese ersten Schritte dauern gewöhnlich Tage bis Monate, und werden vom Opfer i.A. nicht entdeckt. Jetzt unterscheiden sich die nächsten Schritte, je nach Ziel und Motivation des Angreifers.
    - Ein Krimineller könnte jetzt seine erlangten Rechte nutzen um entweder unerkannt Informationen zu stehlen und zu verkaufen, oder er könnte durch gestohlene Daten und/oder verschlüsseln der System deren Besitzer erpressen.
    - Für staatliche Akteure ist gewöhnlich das Ziel unerkannt zu bleiben. Durch den Zugriff können wichtige und geheime Daten erlangt werden und dieser Zugriff ist die Grundlage für einen "Hack-back-Angriff". Um dem angreifenden Staat im Fall eine offenen Cyber-Angriffs schaden zu können muss man i.A. diesen bereits zuvor verdeckt angegriffen haben, und damit Zugriff auf kritische Systeme erlangt haben.

Eine weitere Angriffsart, die es häufig in die Medien schafft, sind sogenannte ["Denial of Service"](https://de.wikipedia.org/wiki/Denial_of_Service) (DoS) Angriffe. Wenn dieser Angriff von Menschen durchgeführt wird, ist er das digitale Äquivalent eines Sitzstreiks. Das angegriffenen System wird durch die schiere Anzahl der Anfragen für andere Nutzer unbenutzbar gemacht. Im kriminellen Kontext werden diese Angriffe fast immer durch Bot-Netze durchgeführt. Bot-Netze sind Gruppen von Geräten auf die, unbemerkt von deren Besitzern, Zugriff erlangt wurde, und die vom Angreifer ferngesteuert werden können. Kriminell Motiviert funktioniert dieser Angriff nur für kommerzielle Anbieter denen ein nennenswerter Schaden durch diesen Angriff entsteht. Der Betreiber des angegriffenen Dienstes wird wieder Lösegeld erpresst.

Auch kleine Anbieter können sich mit Hilfe von [Content Delivery Networks](https://de.wikipedia.org/wiki/Content_Delivery_Network) (CDN) günstig vor DoS Angriffen schützen. CDNs betreiben global verteilte Infrastruktur, über die nicht dynamisch generierte Inhalte ausgeliefert werden. Dadurch sind diese Inhalte für die Nutzer schneller abrufbar, und die Inhalte bleiben auch bei einem Ausfall des Server des Betreibers erreichbar. 

<!--Folie 27 -->

Ein weiter Begriff im Kontext von Hacker Angriffen, der auch hier schon mehrfach ohne genaue Erklärung verwendet wurde, ist Ransomware. Ransomware, oder Erpressungssoftware, wird ausschließlich von Kriminellen eingesetzt. Die Ransomware wird, nachdem Zugriff auf das fremde System erlangt wurde, verwendet um die Daten auf diesem System zu verschlüsseln und den Benutzer damit zu erpressen. Durch automatisierte Angriffe bekannter Schwachstellen werden auch Privatpersonen und kleine Firmen, die nur bereit sind einen geringen Betrag zu bezahlen, lukrative Ziele. Im Fall von größeren Unternehmen erfordern diese Angriffe häufig viel Vorlauf und Aufwand, da zuerst die Firmen-IT, inklusive der Backups, in weiten Teilen infiltriert werden muss damit der Angriff wirksam ist. Da vor allem große Firmen zunehmend besser auf diese Art von Angriffen vorbereitet sind, werden aktuell diese Angriffe auch mit Datendiebstahl und der Drohung diese Daten zu veröffentlichen ergänzt.
