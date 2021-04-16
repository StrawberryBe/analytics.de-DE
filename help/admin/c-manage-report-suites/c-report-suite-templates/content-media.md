---
description: Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.
title: Inhalte und Medien
feature: Admin Tools
uuid: 281b0bf8-59dc-46dc-b5d5-5e42827b785d
exl-id: 9983ff86-9341-4b01-b4f3-41042874a9fb
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 100%

---

# Inhalte und Medien

Definiert die allgemeinen Einstellungen für eine Website, für die Originalinhalte entwickelt und auf der Artikel und Videos präsentiert werden.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Handelsvariable 3 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |

| Erfolgsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| E-Mail-Registrierungen | Zähler (keine Subrelationen) | `event2` |
| Abonnements | Zähler (keine Subrelationen) | `event3` |
| Seitenansichten | Zähler (keine Subrelationen) | `event4` |
| Anzeigenimpressionen | Zähler (keine Subrelationen) | `event5` |
| Anzeigenklicks | Zähler (keine Subrelationen) | `event6` |

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Traffic-Eigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Verkaufsereignisse. Die Anfangskonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen gleich. Ereignisse mit einer N/A Variablen „s_code“ müssen nicht eingestellt werden, da sie automatisch bereitgestellt werden.

| Standard-Verkaufsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Umsatz | Zähler | `purchase` |
| Bestellungen | Zähler | `purchase` |
| Einheiten | Zähler | `purchase` |
| Warenkorb | Zähler | `scOpen` |
| Warenkorbansichten | Zähler | `scView` |
| Instanzen | Zähler | nicht angegeben |
| Checkouts | Zähler | `scCheckout` |
| Zusatz zum Warenkorb | Zähler | `scAdd` |
| Entnahme aus Warenkorb | Zähler | `scRemove` |
| Besuche | Zähler (keine Subrelationen) | nicht angegeben |
| Seitenansichten | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors pro Tag | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors | Zähler (keine Subrelationen) | nicht angegeben |
