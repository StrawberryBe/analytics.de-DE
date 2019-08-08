---
description: Die Data Connectors-Integration für appfigures verwendet Analytics-Variablen, um verschiedene appfigures-Metriken zu verfolgen.
seo-description: Die Data Connectors-Integration für appfigures verwendet Analytics-Variablen, um verschiedene appfigures-Metriken zu verfolgen.
seo-title: Analytics-Integrationsvariablen
title: Analytics-Integrationsvariablen
uuid: 08 d 5 b 714-1 c 97-4 be 6-aae 8-1 f 8192535425
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Analytics Integration Variables{#analytics-integration-variables}

Die Data Connectors-Integration für appfigures verwendet Analytics-Variablen, um verschiedene appfigures-Metriken zu verfolgen.

Die folgende Tabelle beschreibt die Analytics-Variablen, die für die appfigures-Integration automatisch aktiviert wurden.

## Erforderliche Variablen {#section-3ca8dc46bab0436cba0c9ef827c8356a}

>[!NOTE]
>
>Diese Integration verwendet spezielle Variablen für App Store-Daten. Daher müssen Sie keine benutzerspezifischen Commerce-Variablen und -ereignisse zuweisen.

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| eVar | App Store Objekt-ID | Aus appfigures importiert. | Konfigurieren Sie diese evar mit Ablauf der Besuchszeit, aktueller Zuordnung und grundlegenden Subrelationen. |
| Ereignis (numerisch) | App Store-Downloads | Aus appfigures importiert. | Anzahl der mobilen Anwendungs-Downloads. |
| Ereignis (numerisch) | App Store-Käufe (in App) | Aus appfigures importiert. | Die Anzahl der In-App-Käufe und -abonnements. |
| Ereignis (numerisch) | App Store-Platzierung | Aus appfigures importiert. | Wird verwendet, um die durchschnittliche berechnete Metrik für appfigures zu definieren. Nicht direkt verwendet. |
| Ereignis (numerisch) | App Store-Divisor-Platzierung | Aus appfigures importiert. | Wird verwendet, um die durchschnittliche berechnete Metrik für appfigures zu definieren. Nicht direkt verwendet. |
| Ereignis (numerisch) | App Store-Bewertung | Aus appfigures importiert. | Wird verwendet, um die durchschnittliche berechnete Metrik für appfigures zu definieren. Nicht direkt verwendet. |
| Ereignis (numerisch) | Divisor für App Store-Bewertung | Aus appfigures importiert. | Wird verwendet, um die durchschnittliche berechnete Metrik für appfigures zu definieren. Nicht direkt verwendet. |
| event (Währung) | App Store-Umsatz (in App) | Aus appfigures importiert. | Der In-App-Umsatz abzüglich der Store-Gebühr. |
| event (Währung) | App Store-Umsatz (1 aus) | Aus appfigures importiert. | Gesamtumsatz aus App-Käufen abzüglich der Store-Gebühr. |
| event (Währung) | App Store Premium (in App) | Aus appfigures importiert. | Nicht verwendet |
| event (Währung) | App Store Premium (1 aus) | Aus appfigures importiert. | Nicht verwendet |

