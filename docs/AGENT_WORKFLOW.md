# Agenten-Workflow — sparsam und zuverlässig

## Standardablauf
Ein zentraler Agent führt Anforderungen, Planung, Umsetzung, passende Tests und Status zusammen. Nutzer müssen keine Rollenberichte zwischen Chats kopieren. Der Hauptagent darf seine Selbstprüfung nicht als unabhängig bezeichnen.

1. Bestehenden Repo-/Branch-/Commitstand einmal für den Arbeitsbeginn feststellen.
2. Nur Konzept, relevante Dateien und offene Findings lesen.
3. Aufgabe als klein, normal oder kritisch einstufen und nötige Prüfungen kurz benennen.
4. Kleine Aufgabe: kurz planen, umsetzen, gezielt testen, knapp berichten.
5. Normales Feature: Hauptagent plant und implementiert; ein unabhängiger Prüfer kontrolliert den relevanten Diff und die Funktion.
6. Kritische Änderungen an Autorität, Netzwerk, Datenschutz oder gemeinsamem Gameplay: Architekturentscheidung plus gezielte unabhängige Funktions- und Sicherheitsprüfung; in der Regel höchstens zwei Prüfer.
7. Nach Fixes nur betroffene Akzeptanzkriterien, ursprüngliche Reproduktionen und notwendige Abschluss-Tests erneut prüfen.
8. Ergebnis und offene nächste Schritte in den passenden Quelldateien dokumentieren.

## Kosten- und Kontextregeln
- Keine automatisch gestarteten Subagents.
- Keine vollständige Historien- oder Gesamtcodelektüre für jede Aufgabe.
- Bestehende CI- und Testnachweise wiederverwenden, solange sie für denselben geprüften Code gelten.
- Vollständige Testläufe für einen Kandidaten am sinnvollen Abschluss; unterwegs fokussierte Tests.
- Alte Testergebnisse bleiben an ihren Commit gebunden. Nach relevantem Codewechsel gezielte Retests.
- Große Rohlogs nicht in den Hauptkontext kopieren; kurze Zusammenfassung mit Pfad/Beleg.
- Bei wiederholt gescheiterten Fixes derselben Ursache erst die Ursache neu bewerten, statt dieselbe Schleife fortzuführen.

## Status und Entscheidungen
Für jede Aufgabe knapp festhalten: Ziel, Risikoklasse, betroffene Bereiche, Branch/Commit, geänderte Dateien, ausgeführte Tests, Findings, offene Entscheidung und nächster Schritt.
PASS nur für tatsächlich ausgeführte Prüfungen und den genannten Commit. Fehlende Geräte-/Browserprüfung klar als offen benennen.
Neue Produkt- oder Architekturentscheidungen mit Tim klären, wenn sie das gewünschte Spielerlebnis oder zentrale Verträge ändern.

## Sicherheits-/Produktgrenzen
- Änderungen betreffen nur dieses Repository.
- Kein Merge, Push, Render-Deployment oder Release ohne ausdrücklichen Auftrag.
- Keine echte Spieler- oder Produktionsdaten verwenden.
- Keine Tests entfernen oder abschwächen, um einen grünen Lauf zu erzielen.
