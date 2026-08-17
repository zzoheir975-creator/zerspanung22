# Zerspanungsrechner – Android

Deutschsprachiger Android-Rechner für Fräsen und Drehen.

## Enthalten
- Fräsen: Drehzahl n und Vorschub Vf
- Werkstoffsuche
- Offline-Werkstoffdaten
- Button „Werkstoffdaten aktualisieren“
- Vorbereitung für Online-JSON-Datenbank
- Dark Industrial UI
- „Entwickelt von Afkir Zoheir“

## Online-Datenbank aktivieren

1. Lade `materials.json` auf einen HTTPS-Webserver oder GitHub.
2. Öffne `app/src/main/java/de/afkirzoheir/zerspanungsrechner/MainActivity.kt`.
3. Ändere:
   `MaterialRepository.UPDATE_URL`
   auf deine HTTPS-JSON-Adresse.
4. Baue die App neu.

Beispielstruktur:
[
  {
    "name": "C45",
    "nummer": "1.0503",
    "gruppe": "Vergütungsstahl (unlegiert)",
    "rm": 725,
    "vcFraesen": 125,
    "fz": 0.07,
    "vcDrehen": 180,
    "f": 0.18
  }
]

Wichtig: Schnittdaten sind Richtwerte. Für eine kommerzielle Version sollten Quellen, Werkzeughersteller-Daten und technische Normen geprüft werden.

## Android Studio

Projektordner `Zerspanungsrechner` in Android Studio öffnen und Gradle synchronisieren.
Anschließend `app` auf einem Gerät/Emulator starten.

Für Google Play:
- Release-Keystore erstellen
- signiertes Android App Bundle (.aab) bauen
- Store Listing, Datenschutz/Impressum und ggf. Testanforderungen vorbereiten


## Build-Fix (Version 1.0.1)

Java und Kotlin verwenden beide JVM 17. Damit wird der Fehler "Inconsistent JVM-target compatibility detected" vermieden.

Wenn Android Studio fragt, welches Gradle-JDK verwendet werden soll, bitte ein **JDK 17 oder neuer** auswählen.

## Start

1. Projekt in Android Studio öffnen.
2. Gradle Sync abwarten.
3. Android-Gerät per USB mit aktivem USB-Debugging verbinden oder einen Emulator auswählen.
4. `app` auswählen und **Run (▶)** drücken.
