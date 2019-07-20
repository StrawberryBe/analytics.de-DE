---
description: Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.
seo-description: Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.
seo-title: Inhalt und Medien
solution: Analytics
title: Inhalt und Medien
topic: Admin Tools
uuid: 281 b 0 bf 8-59 dc -46 dc-b 5 d 5-5 e 42827 b 785 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Inhalt und Medien

Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Ablauf | `s_code` festlegen |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Handelsvariable 3 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |

| Erfolgsereignisse | Typ | `s_code` festlegen |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| E-Mail-Registrierungen | Zähler (keine Subrelationen) | `event2` |
| Abonnements | Zähler (keine Subrelationen) | `event3` |
| Seitenansichten | Zähler (keine Subrelationen) | `event4` |
| Anzeigenimpressionen | Zähler (keine Subrelationen) | `event5` |
| Anzeigenklicks | Zähler (keine Subrelationen) | `event6` |

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

