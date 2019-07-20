---
description: Definiert häufige Einstellungen für Banken und andere Institutionen, die Zugriff auf Onlinedienste bieten.
seo-description: Definiert häufige Einstellungen für Banken und andere Institutionen, die Zugriff auf Onlinedienste bieten.
seo-title: Finanzdienste
solution: Analytics
title: Finanzdienste
topic: Admin Tools
uuid: a 321 b 409-24 a 4-4 d 9 f -9 aac -65761261 e 991
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Finanzdienste

Definiert häufige Einstellungen für Banken und andere Institutionen, die Zugriff auf Onlinedienste bieten.

| Konversionsvariablen (eVars) | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festlegen |
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

