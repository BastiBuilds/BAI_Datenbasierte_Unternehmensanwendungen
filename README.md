# BAI_Datenbasierte_Unternehmensanwendungen

## Projektaufgaben Abfolgerung
Die Projektarbeit gliedert sich thematisch in folgende vier Phasen (siehe Details in der 
Semesterplanung):
1. Verstehen und arbeiten mit strukturierten «Daten» unter Verwendung von 
«Spreadsheets».
2. Erstellung eines konzeptuellen Modells (Entity-Relationship-Modell) und Generierung der 
Datenbank.
3. SQL-Abfragen: SQL (Structured Query Language) ist eine Sprache, die für relationale 
Datenbanken konzipiert wurde.
4. Interagieren mit Datenbanken mit «Jupyter Notebooks», z.B. Deepnote.
Konkrete Aufgaben, die Teil des Projektberichts sind, werden im Semesterplan als 
«Deliverables» gekennzeichnet


## Aufgabe
Ein Besitzer kann ein oder mehrere Hotels in der Schweiz besitzen. Jedes Hotel offeriert 
mindestens ein Zimmer für Kunden. Jedes Zimmer hat einen bestimmten Zimmerpreis und 
einen Typ (z.B. EZ, DZ, Studio, …). Für ein Hotel können beliebig viele Buchungen durch 
einen Kunden vorgenommen werden. Bei einer Buchung wird das Startdatum, das Enddatum
des Aufenthaltes sowie das Buchungsdatum im System vermerkt. Eine Buchung kann auch 
wieder storniert werden. Für jede realisierte Buchung wird nach Beendigung des Aufenthaltes 
eine Rechnung fällig (Ausnahme ist eine stornierte Buchung). Die Rechnung besteht i.d.R. aus 
mehreren Positionen wie Nächtigung, Getränke, Reinigung, Skipass etc. Für eine Rechnung 
werden auch die Zahlungsart wie Kreditkarte (VISA, AMEX, …), Twint, Paypal, 
Einzahlungsschein, Cash sowie das Rechnungsdatum und die Währung vermerkt. Es kann 
auch vorkommen, dass eine Rechnung nie bezahlt wird. Hotels, sowie deren Kunden haben 
jeweils genau eine Adresse mit Strasse (incl. Nummer), Postleitzahl, Ortsname und Land.


## User Stories
### Als Benutzer:
1. **Als Benutzer möchte ich die verfügbaren Hotels durchsuchen, damit ich dasjenige 
auswählen kann, welches meinen Wünschen entspricht.**
    - Ich möchte alle Hotels in einer Stadt durchsuchen, damit ich das Hotel nach 
meinem bevorzugten Standort (Stadt) auswählen kann.
    - Ich möchte alle Hotels in einer Stadt nach der Anzahl der Sterne durchsuchen.
    - Ich möchte alle Hotels in einer Stadt durchsuchen, die Zimmer haben, die 
meiner Gästezahl entsprechen (nur 1 Zimmer pro Buchung), entweder mit oder 
ohne Anzahl der Sterne.
    - Ich möchte alle Hotels in einer Stadt durchsuchen, die während meines 
Aufenthaltes ("von" (start_date) und "bis" (end_date)) Zimmer für meine 
Gästezahl zur Verfügung haben, entweder mit oder ohne Anzahl der Sterne, 
damit ich nur relevante Ergebnisse sehe.
    - Ich möchte die folgenden Informationen pro Hotel sehen: Name, Adresse, 
Anzahl der Sterne.
    - Ich möchte ein Hotel auswählen, um die Details zu sehen (z.B. verfügbare 
Zimmer [siehe 2]).
2. **Als Benutzer möchte ich Details zu verschiedenen Zimmertypen (EZ, DZ, 
Familienzimmer), die in einem Hotel verfügbar sind, sehen, einschliesslich der 
maximalen Anzahl von Gästen für dieses Zimmer, Beschreibung, Preis und 
Ausstattung, um eine fundierte Entscheidung zu treffen.**
    - Ich möchte die folgenden Informationen pro Zimmer sehen: Zimmertyp, max. 
Anzahl der Gäste, Beschreibung, Ausstattung, Preis pro Nacht.
    - Ich möchte nur die verfügbaren Zimmer sehen.
3. **Als Benutzer möchte ich ein Zimmer in einem bestimmten Hotel buchen, um meinen 
Urlaub zu planen.**

### Als Admin-Nutzer:
1. **Als Admin-Nutzer des Buchungssystems möchte ich die Möglichkeit haben, 
Hotelinformationen zu pflegen, um aktuelle Informationen im System zu haben.**
    - Ich möchte neue Hotels zum System hinzufügen
    - Ich möchte Hotels aus dem System entfernen
    - Ich möchte die Informationen bestimmter Hotels aktualisieren, z. B. den 
Namen, die Sterne usw.
2. **Als Admin-Nutzer des Buchungssystems möchte ich alle Buchungen aller Hotels 
sehen können, um eine Übersicht zu erhalten.**
3. **Ich möchte alle Buchungen bearbeiten können, um fehlende Informationen zu 
ergänzen (z.B. Telefonnummer).**
