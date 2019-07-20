---
description: Definiert allgemeine Einstellungen für ein Jobportal oder eine Website zur Stellensuche.
seo-description: Definiert allgemeine Einstellungen für ein Jobportal oder eine Website zur Stellensuche.
seo-title: Job Portal
solution: Analytics
title: Job Portal
topic: Admin Tools
uuid: c 33 a 8 e 30-eea 6-45 f 5-9568-d 64 c 6753855 e
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Job Portal

Definiert allgemeine Einstellungen für ein Jobportal oder eine Website zur Stellensuche.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festlegen |
|---|---|---|---|---|---|
| Interne Promotion | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Self-Service-Ereignistyp | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

Mit dieser Report Suite-Vorlage werden keine Erfolgsereignisse konfiguriert.

| Benutzerspezifische Insight-Variablen | `s_code` festlegen |
|---|---|
| Sicher/Nicht-Sicher | `prop1` |
| Trafficeigenschaft 2–5 | `prop2, prop3, prop4, prop5` |

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

