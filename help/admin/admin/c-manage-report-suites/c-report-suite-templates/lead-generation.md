---
description: Definiert allgemeine Einstellungen für eine Website, auf der Informationen zu Dienstleistungen und Produkten bereitgestellt werden, die üblicherweise erst nach weiterführender Interaktion verkauft werden.
title: Lead-Generierung
feature: Report Suite Settings
exl-id: 4a629908-2bb4-4d61-a934-42906edff9df
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: ht
source-wordcount: '193'
ht-degree: 100%

---

# Lead-Generierung

Definiert allgemeine Einstellungen für eine Website, auf der Informationen zu Dienstleistungen und Produkten bereitgestellt werden, die üblicherweise erst nach weiterführender Interaktion verkauft werden.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
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
| Warenkörbe | Zähler | `scOpen` |
| Warenkorbansichten | Zähler | `scView` |
| Instanzen | Zähler | nicht angegeben |
| Checkouts | Zähler | `scCheckout` |
| Zusatz zum Warenkorb | Zähler | `scAdd` |
| Entnahme aus Warenkorb | Zähler | `scRemove` |
| Besuche | Zähler (keine Subrelationen) | nicht angegeben |
| Seitenansichten | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors pro Tag | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors | Zähler (keine Subrelationen) | nicht angegeben |
