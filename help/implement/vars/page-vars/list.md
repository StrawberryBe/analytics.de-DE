---
title: list
description: Benutzerdefinierte Variablen, die mehrere Werte im selben Treffer enthalten.
feature: Variables
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
source-git-commit: 50e57e30a50d9c010e8b25b5a7d0afc8926525f5
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 67%

---

# Liste

Listenvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen Listenvariablen und deren Logik in Ihrem [Lösungsdesigndokument](../../prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>Listenvariablen speichern die letzten 250 Werte pro Besucher. Wenn mehr als 250 eindeutige Werte für einen bestimmten Besucher vorhanden sind, werden die ältesten Werte nicht den Metriken zugeordnet.

## Einrichten von Listenvariablen in den Report Suite-Einstellungen

Stellen Sie sicher, dass Sie jede Listenvariable in den Report Suite-Einstellungen konfigurieren, bevor Sie sie in Ihrer Implementierung verwenden. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen. ](/help/admin/admin/conversion-var-admin/list-var-admin.md) Dieser Schritt gilt für alle Implementierungsmethoden.

## Listenvariablen mit dem Web SDK

Listenvariablen sind [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) unter den XDM-Feldern `_experience.analytics.customDimensions.lists.list1.list[]` nach `_experience.analytics.customDimensions.lists.list3.list[]`. Jedes Array-Element enthält eine `"value"` -Objekt, das jede Zeichenfolge enthält. Es ist nicht erforderlich, ein Trennzeichen anzugeben. Es wird automatisch unter Verwendung des in [Report Suite-Einstellungen](/help/admin/admin/conversion-var-admin/list-var-admin.md). Wenn beispielsweise ein Komma (&#39;`,`&#39;) als Trennzeichen für die Listenvariable 1 konfiguriert ist, füllt das folgende XDM-Objekt die `list1` Variable mit `"Example value 1,Example value 2,Example value 3"`.

```json
"xdm": {
    "_experience": {
        "analytics": {
            "customDimensions": {
                "lists": {
                    "list1": {
                        "list": [
                            {
                                "value": "Example value 1"
                            },
                            {
                                "value": "Example value 2"
                            },
                            {
                                "value": "Example value 3"
                            }
                        ]
                    }
                }
            }
        }
    }
}
```

>[!NOTE]
>
>Das Adobe-XDM-Schema enthält `key` Objekte zusätzlich zu `value` Objekte in jedem `list[]` Array. Adobe verwendet diese `key` Objekte beim Senden von Daten an Adobe Analytics.

## Listenvariablen mit der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.list1 - s.list3 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Listenvariable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Sie haben keine maximale Byte-Anzahl; jeder einzelne Wert hat jedoch ein Maximum von 255 Byte. Das Trennzeichen, das Sie verwenden, wird beim Einrichten der Variablen in [Report Suite-Einstellungen](/help/admin/admin/conversion-var-admin/list-var-admin.md). Verwenden Sie keine Leerzeichen, wenn Sie mehrere Elemente trennen.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Wenn Sie im selben Treffer doppelte Werte festlegen, dedupliziert Adobe alle Instanzen dieser Werte. Wenn Sie z. B. `s.list1 = "Brick,Brick";` festlegen, wird eine Instanz in Berichten gezählt.

## Vergleich von Listen-Props mit Listenvariablen

Listen-Props und Listenvariablen können beide im selben Treffer mehrere Werte enthalten. Zwischen diesen beiden Variablentypen gibt es jedoch einige wichtige Unterschiede.

* Jede Prop kann eine Listen-Prop werden. Sie können bis zu 75 Listen-Props haben, wenn jede Prop eine Listen-Prop ist. Es sind nur drei Listenvariablen verfügbar.
* Listen-Props haben eine 100-Byte-Grenze für die gesamte Variable. Listenvariablen haben eine 255-Byte-Grenze pro Wert und keine Gesamt-Byte-Grenze.
* Listen-Props bleiben nicht über den festgelegten Treffer hinaus erhalten. Für Listenvariablen gelten die gewünschten Gültigkeitseinstellungen. Bei der [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md) können Sie jedoch sowohl auf Listen-Props als auch auf Listenvariablen eine benutzerdefinierte Attribution anwenden.
