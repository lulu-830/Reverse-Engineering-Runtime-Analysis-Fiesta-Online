# Reverse-Engineering-Runtime-Analysis-Fiesta-Online
Dieses Projekt entstand im Rahmen meiner Ausbildung zum Fachinformatiker und diente ausschließlich dem Erlernen von Reverse Engineering, Binary Patching und Laufzeitanalyse. Mit x64dbg und Cheat Engine analysierte ich Programmabläufe und testete temporäre Änderungen zu Lern- und Demonstrationszwecken.


## Hinweis

Dieses Projekt wurde ausschließlich zu Ausbildungs-, Lern- und Forschungszwecken erstellt.

Ziel war es, Kenntnisse im Bereich Reverse Engineering, Debugging und Laufzeitanalyse zu vertiefen. Das Projekt wurde **nicht für den Einsatz auf offiziellen Servern oder im produktiven Betrieb entwickelt**.

---

# Projektziel

Im Rahmen dieses Projekts habe ich mich intensiv mit der Analyse eines Windows-Programms beschäftigt. Der Fokus lag darauf, Programmabläufe zu verstehen, relevante Funktionen zu identifizieren und deren Verhalten während der Laufzeit temporär zu verändern.

Dabei wurden unter anderem folgende Werkzeuge eingesetzt:

* **x64dbg** zur Analyse des Programmablaufs
* **Cheat Engine** zur Speicheranalyse und zum Testen temporärer Änderungen
* Erstellung einer **Cheat Engine Table (.CEM)**, um untersuchte Änderungen reproduzierbar während der Laufzeit anwenden zu können

---

# Lerninhalte

Während des Projekts konnte ich praktische Erfahrungen in folgenden Bereichen sammeln:

* Analyse von x86/x64-Assemblercode
* Arbeiten mit Breakpoints und Debugging
* Identifikation relevanter Funktionen
* Analyse von Kontrollflüssen
* Binary Patching
* Laufzeitmanipulation von Programmen
* Speicheranalyse
* Verständnis von Funktionsaufrufen und Parameterübergaben
* Entwicklung reproduzierbarer Testumgebungen mit Cheat Engine

---

# Untersuchte Programmmechaniken

Als Analyseobjekt diente das MMORPG **Fiesta Online**.

Im Rahmen der Untersuchung wurden verschiedene interne Prüfmechanismen analysiert und temporär verändert, um deren Auswirkungen auf das Programmverhalten besser nachvollziehen zu können.

Dazu gehörten unter anderem:

### Skill-Zielrestriktionen

Analyse der internen Zielprüfungen von Fähigkeiten.

Dadurch konnte nachvollzogen werden, wie unterschiedliche Zieltypen technisch verarbeitet werden, beispielsweise:

* Einzelziel-Fähigkeiten
* Flächenfähigkeiten (AoE)
* Selbstzauber
* Fähigkeiten mit auswählbaren Zielen

---

### Reichweitenprüfung

Untersuchung der internen Distanzprüfungen.

Hierbei wurde analysiert, an welcher Stelle maximale Wirkungsreichweiten überprüft werden und wie diese Logik innerhalb des Programms umgesetzt ist.

---

### Zauberunterbrechung durch Bewegung

Analyse der Mechanik, welche laufende Zaubervorgänge beim Bewegen der Spielfigur unterbricht.

Dabei wurde untersucht, welche internen Bedingungen für einen Abbruch verantwortlich sind und wie sich Änderungen dieser Prüfungen auf das Laufzeitverhalten auswirken.

---

# Cheat Engine Table

Zusätzlich wurde eine Cheat Engine Table erstellt.

Diese dient ausschließlich dazu, die während der Analyse entwickelten temporären Speicheränderungen reproduzierbar anzuwenden, ohne den Programmcode dauerhaft zu verändern.

Alle Änderungen erfolgen ausschließlich im Arbeitsspeicher und sind nach einem Neustart des Programms wieder verworfen.

---

# Verwendete Werkzeuge

* x64dbg
* Cheat Engine
* Windows Debugging
* Assembler (x86/x64)
* Binary Patching
* Memory Analysis

---

# Ziel des Projekts

Dieses Repository dokumentiert meinen Lernfortschritt während meiner Ausbildung zum Fachinformatiker und zeigt den praktischen Umgang mit Reverse Engineering und der Analyse von Windows-Anwendungen.

Der Schwerpunkt liegt auf dem Verständnis interner Programmabläufe, dem Debugging sowie der Analyse von Binärdateien und Speicherstrukturen.

---

# Haftungsausschluss

Dieses Projekt dient ausschließlich Bildungs-, Forschungs- und Dokumentationszwecken. Es dokumentiert Methoden und Erkenntnisse aus der Analyse einer Windows-Anwendung und soll den Lernfortschritt im Bereich Reverse Engineering und Debugging veranschaulichen.
