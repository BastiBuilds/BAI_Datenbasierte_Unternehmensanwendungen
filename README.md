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

# 4.1 Eigene User Stories
## Als Benutzer
1. **Buchungen und Rechnungen anzeigen**
    - (EBUS1a) Als Benutzer möchte ich all meine Buchungen und die dazugehörigen Rechnungen sehen, damit ich einen Überblick über meine bisherigen Transaktionen habe.

2. **Zahlungsmittel einsehen**
    - (EBUS2a) Als Benutzer möchte ich alle verfügbaren Zahlungsmittel sehen, um zu prüfen, ob ich mit Twint bezahlen kann.

3. **Pensionsarten in Basel Hotels anzeigen**
    - (EBUS3a) Als Benutzer möchte ich alle Pensionsarten von Hotels in Basel sehen, um eine informierte Wahl treffen zu können.
  
## Als Admin
1. **Unbezahlte Rechnungen und Buchungen mit Kundendetails**
    - (EAUS1a) Als Admin möchte ich alle Rechnungen und Buchungen inklusive der dazugehörigen Kundendaten sehen, bei denen die Rechnung noch nicht bezahlt wurde, um offene Zahlungen nachzuverfolgen.

2. **Top 10 Hotels nach Grösse und Angestelltenzahl**
    - (EAUS2a)Als Admin möchte ich die 10 grössten Hotels inklusive ihrer Adresse sehen, geordnet nach der maximalen Gästeaufnahme und anschliessend eine zusätzliche Anzeige anhand der Anzahl der Angestellten, um eine Übersicht zu haben.

3. **Stornierte Buchungen mit Details**
    - (EAUS3a) Als Admin möchte ich alle stornierte Buchungen inklusive Gästeinformationen, Raum- und Hoteldetails sehen, um sehen zu können, welche Hotel und Räume am schlechtesten laufen und ob es einen Zusammenhang mit den Gästen gibt.
