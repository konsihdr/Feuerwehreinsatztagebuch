# Feuerwehreinsatztagebuch

Ein digitales Einsatztagebuch für die Einsatzstelle – als **einzelne HTML-Datei**, ganz ohne
Installation, Server oder Internetverbindung. `index.html` im Browser öffnen und loslegen.

Alle Daten bleiben auf dem Gerät: Sie werden im `localStorage` des Browsers gespeichert und
können als JSON-Datei gesichert bzw. wieder geladen werden. Es werden keine Daten übertragen.

## Funktionen

- **Einsatzdaten** – Bezeichnung, Ort, Stichwort, Einsatznummer, Einsatzleiter/in, Datum, Alarmzeit
- **Einsatztagebuch** – Ereignis eintippen, Enter drücken, fertig: der Eintrag wird mit
  sekundengenauem Zeitstempel protokolliert. Volltextsuche über alle Einträge.
- **Eingesetzte Kräfte** – Mitglieder und Gegenstände (Fahrzeuge, Geräte) per Häkchen als
  „eingesetzt" bzw. „abgerückt" protokollieren, jeweils mit Zeitstempel; optional mit Kommentar.
- **Revisionssicher** – Einträge werden nie überschrieben oder gelöscht: Beim Bearbeiten bleibt
  die alte Fassung als Historie sichtbar, „gelöschte" Einträge werden nur durchgestrichen.
- **Autosave** – jede Änderung wird sofort lokal gespeichert (Statusanzeige in der Kopfzeile).
- **Export** – vollständiges Tagebuch als JSON (zum Weiterarbeiten) oder als PDF (zum Ablegen).

## Bedienung

### Einsatz beginnen

1. `index.html` im Browser öffnen (Doppelklick genügt).
2. Links unter **Einsatzdaten** die Kopfdaten des Einsatzes eintragen.
3. Der Cursor steht direkt im Eingabefeld des Tagebuchs – losprotokollieren.

### Tagebuch führen

| Aktion | Bedienung |
| --- | --- |
| Ereignis erfassen | Text eingeben, **Enter** – Zeitstempel wird automatisch gesetzt |
| Eingabe verwerfen | **Esc** im Eingabefeld |
| Eintrag korrigieren | **✎** in der Zeile, neuen Text eingeben, **Enter** (alte Fassung bleibt sichtbar) |
| Eintrag zurücknehmen | **✕** – der Eintrag wird durchgestrichen, nicht entfernt |
| Wiederherstellen | **Wiederherstellen** in der durchgestrichenen Zeile |
| Suchen | Suchfeld über der Tabelle; **Esc** leert die Suche |

### Kräfte und Gerät

- Häkchen bei einem Mitglied oder Gegenstand setzen → Eintrag „*Name* – eingesetzt" mit Zeitstempel.
- Häkchen wieder entfernen → Eintrag „*Name* – abgerückt" mit Zeitstempel.
- **💬** an einer Zeile ergänzt einen Kommentar (z. B. Auftrag oder Abschnitt).
- Über die Eingabefelder unter den Listen lassen sich eigene Mitglieder und Gegenstände ergänzen,
  über **×** wieder aus der Auswahlliste entfernen (bereits protokollierte Einträge bleiben erhalten).
- **CSV ↑ / CSV ↓** importiert bzw. exportiert die Listen – eine Angabe pro Zeile.
  So lässt sich die Mitgliederliste der eigenen Wehr einmalig vorbereiten und auf allen Geräten nutzen.

Die Listen von Mitgliedern und Gegenständen werden getrennt vom Einsatz gespeichert und bleiben
beim Anlegen eines neuen Einsatzes erhalten.

### Sichern und exportieren

| Schaltfläche | Wirkung |
| --- | --- |
| **Neuer Einsatz** | Setzt den aktuellen Einsatz zurück (mit Rückfrage) – vorher speichern! |
| **Laden (JSON)** | Lädt einen zuvor gespeicherten Einsatz zurück in die Oberfläche |
| **Speichern (JSON)** | Lädt den kompletten Einsatz als JSON-Datei herunter |
| **PDF Export** | Öffnet den Druckdialog mit einem aufbereiteten Protokoll – dort „Als PDF sichern" |

Der Dateiname enthält Einsatzbezeichnung und Zeitstempel, z. B.
`Einsatztagebuch_Wohnungsbrand_Musterstrasse_20260817_1432.json`.

> **Hinweis:** Die lokale Browser-Speicherung ersetzt keine Sicherung. Nach dem Einsatz – und bei
> längeren Lagen auch zwischendurch – den Stand als JSON und/oder PDF exportieren. Wird der Browser-
> Speicher gelöscht (privater Modus, „Websitedaten löschen"), sind die Daten sonst verloren.

## Betrieb

- **Lokal:** `index.html` auf den Rechner, USB-Stick oder das Tablet kopieren und öffnen.
  Funktioniert vollständig offline.
- **Gehostet:** Die Datei kann unverändert z. B. über GitHub Pages bereitgestellt werden.
- **Online:** Einfach per [https://einsatztagebuch.hoerder.cloud](https://einsatztagebuch.hoerder.cloud) verwenden
 
Voraussetzung ist lediglich ein aktueller Browser (Chrome, Edge, Firefox, Safari). Für die
Bedienung an der Einsatzstelle empfiehlt sich ein möglichst breiter Bildschirm, da die Oberfläche
in drei Spalten aufgebaut ist.
