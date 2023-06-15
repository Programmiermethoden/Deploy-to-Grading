---
title: Testmetriken
---

Eine Auflistung an möglichen Metriken, mit denen die Abgaben bewertet werden sollen. Die Metriken sind unterteilt in Metriken, die von Studierenden selbst ausgeführt werden können (durch die GH-Action) und Metriken, die nur bei der endgültigen Bewertung eingesetzt werden können, da sie z.B. Gruppenübergreifend arbeiten.

**Für alle (insbesondere Studierende)**

|Metrik|Erläuterung|Einordnung|Tool|
|--|--|--|--|
|Kompilierung|Die erste Anforderung an eine Abgabe sollte sein, dass es erfolgreich kompiliert werden kann. Gleichzeitig können wir hiermit und dem `depends_on` in der Aufgabendefinition verhindern, dass andere Tests unnötig ausgeführt werden.|Muss|javac|
|Unittests|Zum Testen der konkreten Implementierung verwenden wir offensichtlicherweise Unittests. Dazu kann auch das Testen über Logging genutzt werden.|Muss|[JUnit](https://junit.org/junit5/) / [JGrade](https://github.com/espertus/jgrade)|
|CLI-Tests (Blackbox Testing)|Für alle möglichen Testfälle, die sich nicht mit Unittests umsetzen lassen, stellen wir noch eine zweite Variante bereit. Hiermit sollte auch die Nelson-Methode aus Programmiermethoden/Dungeon#337 abgedeckt sein. Falls Logging-Tests nicht direkt über Unittests durchgeführt werden sollen, können auch CLI-Tests dafür genutzt werden.|Muss|(noch offen) / [JGrade](https://github.com/espertus/jgrade)|
|Code Format|Zum Prüfen, ob der Code korrekt formatiert ist bzw. der Formatierungsprozess korrekt angestoßen wurde.|Muss|[Spotless](https://github.com/diffplug/spotless)|
|JavaDoc Documentation|Zum Prüfen, ob JavaDoc mit abgegeben und korrekt eingesetzt wurde.|Muss|[Checkstyle](https://checkstyle.sourceforge.io/)|
|Code Coverage|Zum Prüfen von Aufgaben, in denen Studierende Tests schreiben sollen. Insbesondere im Hinblick, ob Methoden vergessen wurden.|Sollte|[https://emma.sourceforge.net/intro.html](https://emma.sourceforge.net/intro.html)|
|Coding-Style und Softwaremetriken|Sammelmetrik für alle Coding-Style Sachen. Je nachdem, was für Checkstyle definiert wurde.|Sollte|[Checkstyle](https://checkstyle.sourceforge.io/) (alternativ [PMD](https://pmd.github.io/))|
|Bug Checking|Prüfen auf Bugs. Wenn nicht eh bereits über Unittests abgedeckt.|Kann|[SpotBugs](https://spotbugs.github.io/)|
|Effizienz (z.B. Ausführungszeiten)|Wahrscheinlich nicht überall anwendbar, aber vielleicht findet man ein paar Fälle, in denen sich das Prüfen auf Effizienz lohnt.|Kann|(offen)|
|Dungeon|Damit alle Ergebnisse an einer Stelle gesammelt sind, könnte man hier auch die Dungeon-Ergebnisse auswerten.|Kann|(eigene Anwendung)|
|GUI Testing|Falls überhaupt relevant.|Kann|(offen)|
|PR Check|In Programmiermethoden/Dungeon#334 ist eine Checkliste mit Punkten, die ein PR erfüllen muss. Das könnte man auch überprüfen. Folgende Punkte sind genannt: Titel, Beschreibung, Assignes, ggf. Review, Mehrere kleine Commit, Nur relevante Dateien, Sortiertes Repo. Basierend auf dieser Definition ist eine eigenständige Aufgabe für den PR Check notwendig.|Kann|(offen)|

**Nur für die endgültige Bewertung**

|Metrik|Erläuterung|Einordnung|Tool|
|--|--|--|--|
|Plagiats-/Abschreibeerkennung|Gerade bei der automatischen Bewertung kann leicht dieselbe Lösung von unterschiedlichen Studis eingereicht werden. Nach dem Motto: Schaut sich doch eh keiner mehr an. Um dies zu verhindern, sollte eine Abschreibeerkennung eingefügt werden.|Muss|JPlag|
|Dungeon|Damit alle Ergebnisse an einer Stelle gesammelt sind, könnte man hier auch die Dungeon-Ergebnisse auswerten. (Doppelnennung, da Studierende vermutlich schon im Dungeon eine Rückmeldung bekommen sollten. Hier dann nur zur Zusammenfassung der Ergebnisse.)|Kann|(eigene Anwendung)|
|Manuelle Bewertung|Falls die Bewertung angepasst werden muss, z.B. weil die automatischen Tools etwas nicht abdecken oder ein Fehler bei den Tools gefunden werden, wird diese zusätzliche "Metrik" benötigt. Hierbei besteht bei dem bisherigen Konzept noch das Problem, dass die manuelle Bewertung nicht für Studierende sichtbar ist.|Kann|(offen)|
