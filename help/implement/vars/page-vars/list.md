---
title: list
description: Benutzerdefinierte Variablen, die mehrere Werte im selben Treffer enthalten.
feature: Variables
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 87%

---

# list

Listenvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen Listenvariablen und deren Logik in Ihrem [Lösungs-Design-Dokument](../../prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>Listenvariablen speichern die letzten 250 Werte pro Besucher. Wenn mehr als 250 eindeutige Werte für einen bestimmten Besucher vorhanden sind, werden die ältesten Werte nicht den Metriken zugeordnet.

## Einrichten von Listenvariablen in den Report Suite-Einstellungen

Stellen Sie sicher, dass Sie jede Listenvariable in den Report Suite-Einstellungen konfigurieren, bevor Sie sie in Ihrer Implementierung verwenden. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). Dieser Schritt gilt für alle Implementierungsmethoden.

## Listenvariablen, die das Web SDK verwenden

Wenn Sie die [**XDM-Objekt**](/help/implement/aep-edge/xdm-var-mapping.md), verwenden Listenvariablen die XDM-Felder `xdm._experience.analytics.customDimensions.lists.list1.list[]` nach `xdm._experience.analytics.customDimensions.lists.list3.list[]`. Jedes Array-Element enthält ein `"value"`-Objekt, das jede Zeichenfolge enthält. Es ist nicht erforderlich, ein Trennzeichen anzugeben. Adobe-Datenerfassungsserver erkennen automatisch das richtige Trennzeichen, das in [Report Suite-Einstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md).

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
>Das Adobe-XDM-Schema enthält `key`-Objekte zusätzlich zu `value`-Objekten in jedem `list[]`-Array. Adobe verwendet diese `key`-Objekte nicht beim Senden von Daten an Adobe Analytics.

Wenn Sie die [**Datenobjekt**](/help/implement/aep-edge/data-var-mapping.md), Listenvariablen verwenden `data.__adobe.analytics.list1` - `data.adobe.analytics.list3` nach AppMeasurement-Syntax. Stellen Sie sicher, dass Sie das richtige Trennzeichen verwenden, das in [Report Suite-Einstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md).

```json
"data": {
  "__adobe": {
    "analytics": {
      "list1": "Example value 1,Example value 2,Example value 3"
    }
  }
}
```

## Listenvariablen, die die Adobe Analytics-Erweiterung verwenden

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.list1 – s.list3 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Listenvariable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Sie haben keine maximale Byte-Anzahl; jeder einzelne Wert hat jedoch ein Maximum von 255 Byte. Das Trennzeichen, das Sie verwenden, wird beim Einrichten der Variablen in den [Report Suite-Einstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) festgelegt. Verwenden Sie keine Leerzeichen, wenn Sie mehrere Elemente trennen.

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
