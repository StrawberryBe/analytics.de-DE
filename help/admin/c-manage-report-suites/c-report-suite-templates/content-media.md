---
description: Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.
seo-description: Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.
seo-title: Inhalte und Medien
solution: Analytics
title: Inhalte und Medien
topic: Admin Tools
uuid: 281b0bf8-59dc-46dc-b5d5-5e42827b785d
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Inhalte und Medien

Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festgelegt |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Handelsvariable 3 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |

| Erfolgsereignisse | Typ | `s_code` festgelegt |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| E-Mail-Registrierungen | Zähler (keine Subrelationen) | `event2` |
| Abonnements | Zähler (keine Subrelationen) | `event3` |
| Seitenansichten | Zähler (keine Subrelationen) | `event4` |
| Anzeigenimpressionen | Zähler (keine Subrelationen) | `event5` |
| Anzeigenklicks | Zähler (keine Subrelationen) | `event6` |

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

