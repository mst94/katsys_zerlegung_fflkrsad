# katsys_zerlegung_fflkrsad

FE2-Zerlegung für die Katsys-Schnittstelle des Landkreises Schwandorf für die Feuerwehren, um die Einsatzmittel einfach und schnell zu extrahieren.

## Vorbereitungen ##
- Zerlegung - Jar-Datei herunterladen und unter Config/extern/ einfügen. FE2 neustarten.
- In den Einstellungen der Einheit diese Zerlegung als de.stelzer.KatsysFFLkrSADv1.jar auswählen und speichern.
- Katsys Alarmeingang anpassen.

## Alarmeingang Mapping ##
Die Einsatzmittel müssen wie folgt gemapped werden:
...
katsys_einsatzmittel;einsatzmittel_original
...

## Ergebnis Parameter in Alarmdaten ##
### einsatzmittel ###
FL Musterstadt 30/1
FF Musterstadt
FL Musterhausen Land 1/6
FL Musterstadt 40/1
FL Musterstadt 41/1

### einsatzmittel_formatiert ###
🚒 FL Musterstadt 30/1
→
🏠 FF Musterstadt
FL Musterhausen Land 1/6
🚒 FL Musterstadt 40/1
→ Gruppe (Takt. Einheit, Dispo)
🚒 FL Musterstadt 41/1
→ Pressluftatmer (Gerät + Maske)

### einsatzmittel_kurz	###
FL Musterstadt 30/1
FF Musterstadt
FL Musterhausen Land 1/6
FL Musterstadt 40/1
FL Musterstadt 41/1

### einsatzmittel_mit_dispoinfo ###
FL Musterstadt 30/1 ()
FF Musterstadt
FL Musterhausen Land 1/6
FL Musterstadt 40/1 (Gruppe (Takt. Einheit, Dispo))
FL Musterstadt 41/1 (Pressluftatmer (Gerät + Maske))
