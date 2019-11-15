---
description: Definiert allgemeine Einstellungen für eine E-Commerce-Website.
solution: Analytics
title: Handel
topic: Admin tools
uuid: 85fc235d-0180-4245-b831-0243ebe3c40c
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Handel

Definiert allgemeine Einstellungen für eine E-Commerce-Website.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festgelegt |
|---|---|---|---|---|---|
| Interne Promotions | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Merchandising-Kategorie | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |
| Handelsvariable 5 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar5` |

| Erfolgsereignisse | Typ | `s_code` festgelegt |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| Benutzerspezifische Ereignisse 1-5 | Zähler (keine Subrelationen) | `event1, event2, event3, event4, event5` |

| Benutzerspezifische Insight-Variablen | `s_code` festgelegt |
|---|---|
| Trafficeigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

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

