# HA Blueprints

Eigene Blueprints für Home Assistant.

## PV-Überschuss → Steckdose schalten (Auto laden)

[![Blueprint in Home Assistant importieren](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Frtaucher%2Fha_blueprint%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fpv_ueberschuss_steckdose.yaml)

Schaltet eine Steckdose (z. B. zum Laden eines E-Autos), sobald die PV-Anlage Überschuss hat und einspeisen würde.

**Funktionen**

- Ein-/Ausschaltschwelle mit Hysterese und einstellbaren Verzögerungen
- Mindestlaufzeit nach dem Einschalten
- Eigenverbrauch der Steckdose wird zum Netzwert dazugerechnet (über Leistungssensor oder festen Wert), damit das Laden den Überschuss nicht "auffrisst"
- Optional: Hausbatterie-Priorität (Start-/Stop-Ladestand)
- Optional: Auto-Ladestand mit Ziel-SoC und "Auto angesteckt"-Prüfung
- Zeitfenster (Standard 06:00–20:00)
- Optional: eigene Aktionen nach dem Ein- und Ausschalten (z. B. Benachrichtigung)

**Installation**

- Mit dem Button oben importieren, oder
- Datei `blueprints/automation/pv_ueberschuss_steckdose.yaml` nach `config/blueprints/automation/` kopieren.

Danach unter *Einstellungen → Automatisierungen → Neue Automatisierung → Blueprint verwenden* anlegen.

Benötigt Home Assistant 2024.10 oder neuer.
