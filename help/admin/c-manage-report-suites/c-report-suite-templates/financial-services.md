---
description: Definiert häufige Einstellungen für Banken und andere Institutionen, die Zugriff auf Onlinedienste bieten.
title: Finanzdienste
topic: Admin tools
uuid: a321b409-24a4-4d9f-9aac-65761261e991
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 100%

---


# Finanzdienste

Definiert häufige Einstellungen für Banken und andere Institutionen, die Zugriff auf Onlinedienste bieten.

| Konversionsvariablen (eVars) | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Promotion | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Self-Service-Ereignistyp | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

Mit dieser Report Suite-Vorlage werden keine Erfolgsereignisse konfiguriert.

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Sicher/Nicht sicher | `prop1` |
| Traffic-Eigenschaft 2-5 | `prop2, prop3, prop4, prop5` |

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

