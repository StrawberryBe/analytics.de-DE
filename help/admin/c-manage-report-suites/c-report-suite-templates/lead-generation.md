---
description: Definiert allgemeine Einstellungen für eine Website, auf der Informationen zu Dienstleistungen und Produkten bereitgestellt werden, die üblicherweise erst nach weiterführender Interaktion verkauft werden.
seo-description: Definiert allgemeine Einstellungen für eine Website, auf der Informationen zu Dienstleistungen und Produkten bereitgestellt werden, die üblicherweise erst nach weiterführendem Engagement verkauft werden.
seo-title: Lead-Generierung
solution: Analytics
title: Lead-Generierung
topic: Admin Tools
uuid: e7d3cc4a-1bee-4722-92c1-4454f7613d39
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Lead-Generierung

Definiert allgemeine Einstellungen für eine Website, auf der Informationen zu Dienstleistungen und Produkten bereitgestellt werden, die üblicherweise erst nach weiterführender Interaktion verkauft werden.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festgelegt |
|---|---|---|---|---|---|
| Interne Promotion | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Self-Service-Ereignistyp | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

Mit dieser Report Suite-Vorlage werden keine Erfolgsereignisse konfiguriert.

| Benutzerspezifische Insight-Variablen | `s_code` festgelegt |
|---|---|
| Sicher/Nicht-Sicher | `prop1` |
| Trafficeigenschaft 2–5 | `prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Verkaufsereignisse. Die Anfangskonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen gleich. Ereignisse mit einer N/A Variablen „s_code“ müssen nicht eingestellt werden, da sie automatisch bereitgestellt werden.

| Standard-Verkaufsereignisse | Typ | `s_code` festgelegt |
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

