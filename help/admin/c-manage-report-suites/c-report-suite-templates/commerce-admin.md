---
description: Definiert allgemeine Einstellungen für eine E-Commerce-Website.
seo-description: Definiert allgemeine Einstellungen für eine E-Commerce-Website.
seo-title: Commerce
solution: Analytics
title: Commerce
topic: Admin Tools
uuid: 85 fc 235 d -0180-4245-b 831-0243 ebe 3 c 40 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Commerce

Definiert allgemeine Einstellungen für eine E-Commerce-Website.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festlegen |
|---|---|---|---|---|---|
| Interne Promotions | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Merchandising-Kategorie | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |
| Handelsvariable 5 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar5` |

| Erfolgsereignisse | Typ | `s_code` festlegen |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| Benutzerspezifische Ereignisse 1-5 | Zähler (keine Subrelationen) | `event1, event2, event3, event4, event5` |

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

