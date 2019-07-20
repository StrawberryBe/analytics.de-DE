---
description: Definiert allgemeine Einstellungen für eine Website, die Inhalte zusammenträgt, z. B. ein Nachrichtenportal.
seo-description: Definiert allgemeine Einstellungen für eine Website, die Inhalte zusammenträgt, z. B. ein Nachrichtenportal.
seo-title: Aggregator-Portal
solution: Analytics
title: Aggregator-Portal
topic: Admin Tools
uuid: d 227 c 209-4 d 88-4 server-b 126-994 b 2 a 179 c 51
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Aggregator-Portal

Definiert allgemeine Einstellungen für eine Website, die Inhalte zusammenträgt, z. B. ein Nachrichtenportal.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festlegen |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Referrer-Kategorie | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

| Erfolgsereignisse | Typ | `s_code` festlegen |
|---|---|---|
| Anmelden | Zähler (keine Subrelationen) | `event1` |
| Referrer-Ansicht | Zähler (keine Subrelationen) | `event2` |
| Referrer-Klicks | Zähler (keine Subrelationen) | `event3` |

| Benutzerspezifische Insight-Variablen | `s_code` festlegen |
|---|---|
| Trafficeigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Verkaufsereignisse. Die Anfangskonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen gleich. Ereignisse mit einer N/A Variablen „s_code“ müssen nicht eingestellt werden, da sie automatisch bereitgestellt werden.

| Standard-Verkaufsereignisse | Typ | `s_code` festlegen |
|---|---|---|
| Umsatz | Zähler | `purchase` |
| Bestellungen | Zähler | `purchase` |
| Einheiten | Zähler | `purchase` |
| Warenkorb | Zähler | `scOpen` |
| Warenkorbansicht | Zähler | `scView` |
| Instanzen | Zähler | Keine |
| Checkouts | Zähler | `scCheckout` |
| Zusatz zum Warenkorb | Zähler | `scAdd` |
| Entnahme aus Warenkorb | Zähler | `scRemove` |
| Besuche | Zähler (keine Subrelationen) | Keine |
| Seitenansichten | Zähler (keine Subrelationen) | Keine |
| Unique Visitors pro Tag | Zähler (keine Subrelationen) | Keine |
| Unique Visitors | Zähler (keine Subrelationen) | Keine |

