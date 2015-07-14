QPM Compilation
===============

[https://github.com/devfoo-one/QPM-Klausurvorbereitung](https://github.com/devfoo-one/QPM-Klausurvorbereitung)

Qualität
========

Was ist Qualität?
-----------------

> Qualität ist die Gesamtheit der **Eigenschaften** und **Merkmale** eines **Produkts** oder einer **Tätigkeit**, die sich auf deren Eignung zur Erfüllung gegebener Erfordernisse bezieht.

5 Ansätze um Qualität zu erklären:

1.	transzendentaler (übernatürlicher) Ansatz

	-	Qualität ist universell erkennbar, absolut, einzigartig und vollkommen.
	-	Qualität kann nicht exakt definiert oder gemessen werden.

2.	produktbezogener Ansatz

	-	Qualität ist eine messbare, genau spezifizierte Größe, die das Produkt beschreibt und durch die man Qualitätsunterschiede aufzeigen kann.
	-	Subjektive Beobachtungen und Wahrnehmungen werden nicht berücksichtigt.

3.	benutzerbezogener Ansatz

	-	Qualität wird durch den Produktbenutzer festgelegt.
	-	Benutzer entscheidet, ob es sich um ein Qualitätsprodukt handelt oder nicht
	-	da verschiedene Benutzer unterschiedliche Wünsche haben, werden diejenigen Produkte als qualitativ hochwertig angesehen, die die Bedürfnisse einer Vielzahl von Benutzern am besten befriedigen

4.	prozessbezogener Ansatz

	-	Qualität entsteht durch die richtige Erstellung des Produkts

5.	Kosten-/Nutzenbezogener Ansatz

	-	Qualität ist eine Funktion von Kosten und Nutzen
	-	Ein Qualitätsprodukt ist ein Erzeugnis, das einen bestimmten Nutzen zu einem akzeptablen Preis erbringt

Softwarequalität
----------------

DIN ISO 9126:

> Softwarequalität ist die Gesamtheit der **Merkmale** und **Merkmalswerte** eines Softwareprodukts, die sich auf die **Eignung** beziehen, festgelegte oder vorausgesetzte **Erfordernisse** zu erfüllen.

Sechs Qualitätsmerkmale werden allgemin unterschieden. Diese können auf jede Art von Software angewandt werden:

-	**Funktionalität**
	-	*Richtigkeit*
		-	liefert die richtigen oder vereinbarten Ergebnisse
	-	*Sicherheit*
		-	beabsichtigten oder unbeabsichtigten unberechtigten Zugriff verhindern
	-	...
-	**Zuverlässigkeit**
	-	*Reife*
		-	geringe Versagenshäufigkeit durch Fehlerzustände
	-	*Wiederherstellbarkeit*
		-	bei einem Versagen das Leistungsniveau wiederherstellen und die direkt betroffenen Daten wiedergewinnen
	-	...
-	**Benutzbarkeit**
	-	*Verständlichkeit*
		-	Aufwand für den Benutzer, das Konzept und die Anwendung zu verstehen
	-	*Erlernbarkeit*
		-	Aufwand für den Benutzer, die Anwendung zu erlernen
	-	...
-	**Effizienz**
	-	*Zeitverhalten*
		-	Antwort- und Verarbeitungszeiten sowie Durchsatz bei der Funktionsausführung
	-	*Verbrauchsverhalten*
		-	Anzahl und Dauer der benötigten Betriebsmittel (Ressourcen) für die Erfüllung der Funktionen
	-	...
-	**Änderbarkeit**
	-	*Analysierbarkeit*
		-	Aufwand, um Mängel oder Ursachen von Versagen zu diagnostizieren
	-	*Modifizierbarkeit*
		-	Aufwand zur Ausführung von Verbesserungen, zur Fehlerbeseitigung oder Anpassung an Umgebungsänderungen
	-	*Prüfbarkeit*
		-	Aufwand, der zur Prüfung der geänderten Software notwendig ist
	-	...
-	**Übertragbarkeit**
	-	*Anpassbarkeit*
		-	Möglichkeiten, die Software an verschiedene, festgelegte Umgebungen anzupassen
	-	*Installierbarkeit*
		-	Aufwand, der zum Installieren der Software in einer festgelegten Umgebung notwendig ist
	-	...

Qualitätssicherungsmaßnahmen
----------------------------

***kommen lt. Klausurvorbereitung nicht dran, da wir diese in der VL nicht abgehandelt hatten***

### konstruktive Qualitätssicherung

### analytische Qualitätssicherung

Qualitätsmanagement
-------------------

> **Qualitätsmanagement** umfasst alle Tätigkeiten der Gesamtführungsaufgabe, welche die **Qualitätspolitik, Ziele und Verantwortungen festlegen** sowie diese durch Mittel wie Qualitätsplanung, Qualitätslenkung, Qualitätssicherung und Qualitätsverbesserung im Rahmen des Qualitätsmanagementsystems **verwirklichen** (DIN EN ISO 8402)

Qualitätssicherung
------------------

### Analytische Verfahren zur Qualitätssicherung

1.	Testende Verfahren (haben das **Ziel, Fehler zu erkennen.** )
	-	Dynamische Testverfahren
		-	Die Systemkomponente **wird ausgeführt** um Fehler zu finden.
	-	Statische Testverfahren
		-	Systemkomponente wird nicht ausgeführt, sondern **der Quellcode wird analysiert** um Fehler zu finden
2.	Verifizierende Verfahren (**beweisen die Korrektheit einer Systemkomponente** )
	-	Verifikation
		-	beweist mit mathematischen Mitteln die Konsistenz zwischen der Spezifikation und der Implementierung einer Systemkomponente
	-	Symbolische Ausführung
		-	Ein Quellprogramm wird mit allgemeinen symbolischen Eingabewerten durch einen Interpreter ausgeführt

Dynamische Testverfahren
========================

Dynamische Testverfahren, bei denen Fehler in Systemkomponenten durch die Ausführung des entsprechenden Codes identifiziert werden, können noch weiter klassifiziert werden. Sie haben das Ziel **Fehler zu erkennen** mittels:

-	Zufallstests
-	Test spezieller Werte
-	Funktionale Äquivalenzklassenbildung
-	Grenzwertanalyse
-	Parallelalgorithmen

Allgemeines:

-	spezielle Werte des Datentyps berücksichtigen
	-	`0,1,2` bei int, sowie die negativen Werte
	-	`MAX_VALUE` und `MIN_VALUE`
-	Strings
	-	Übergabe von `null` testen
	-	Leerstring
	-	Strings mit nur einem Zeichen
	-	Strings mit einem Steuerzeichen, z.B. `\n`
	-	sehr lange Strings

Äquivalenzklasse und Grenzwertanalyse
-------------------------------------

Die *Definitionsbereiche der Eingabeparameter* und die *Wertebereiche der Ausgabeparameter* werden in **Äquivalenzklassen** zerlegt.

-	Es wird davon ausgegangen, dass ein Programm bei der **Verarbeitung eines Repräsentanten aus einer Äquivalenzklasse so reagiert wie bei allen anderen Werten aus dieser Klasse.**
-	Wenn das Programm mit dem **repräsentativen Wert aus der Äquivalenzklasse** fehlerfrei läuft, dann ist zu erwarten, dass es auch für andere Werte aus dieser Klasse **korrekt funktioniert.**

Testfälle die die **Grenzwerte der Äquivalenzklassen abdecken** oder in unmittelbarer Umgebung dieser Grenzen liegen, sind besonders effektiv und decken besonders häufig Fehler auf.

![](img/aequivalenzklasse.jpg)

Modultest
---------

-	untersuchen stets einen **möglichst kleinen, für sich allein funktionierenden Code-Ausschnitt**, etwa eine einzelne Methode oder Klasse
-	Entwickler können hier bereits preiswert Detailfehler aufdecken und beseitigen bevor die Testabteilung oder der Kunde darauf stößt
-	Stichwort **Test Driven Design, Test First**
-	Das Schreiben von Modultests setzt ein hohes Verständnis guten Softwaredesigns voraus.

Parallelalgorithmen
-------------------

Ist ein **alternativer Algorithmus** mit den (zumindest theoretisch erwarteten) identischen Ergebnissen. Er dient zum parallelen Vergleich des zu testenden Algorithmus.

Black-Box Tests
---------------

Black-Box-Tests (auch **funktionale Tests** genannt) verwenden nur die **offengelegten Schnittstellen** eines Testmoduls um dieses mit Eingaben zu versorgen und das Ergebnis auszuwerten. Syntax und Semantik des der implementierten Methode zugrundeliegenden Algorithmus wird nicht interpretiert.

Glass-Box-Tests
---------------

Wie Black-Box-Tests, nur mit zusätzlicher Kenntnis des Quellcodes.

weitere Testverfahren
---------------------

-	GUI Tests
-	Inhalts- und Pixelvergleich

Softwaremetriken
================
