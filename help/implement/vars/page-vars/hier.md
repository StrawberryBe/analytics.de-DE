---
title: hier
description: Implementieren Sie Hierarchievariablen in Adobe Analytics.
feature: Variables
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
source-git-commit: f435453f655caef89460de42ebecf489b021dc47
workflow-type: ht
source-wordcount: '352'
ht-degree: 100%

---

# hier

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Klassifizierungen.

Hierarchievariablen sind benutzerdefinierte Variablen, mit denen Sie die Struktur einer Website sehen können. Adobe unterstützt bis zu fünf Hierarchievariablen in Ihrer Implementierung.

Diese Variable ist nützlich bei Sites mit mehr als drei Ebenen in der Site-Struktur. Eine Medien-Site kann beispielsweise vier Ebenen zum Abschnitt „Sport“ haben: `Sports`, `Local Sports`, `Baseball` und `Team name`. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ wiedergegeben.

Bevor Sie Hierarchien in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede Hierarchie in den Report Suite-Einstellungen konfigurieren.

## Hierarchien, die das Web SDK verwenden

Hierarchien sind [für Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) unter den XDM-Feldern `_experience.analytics.customDimensions.hierarchies.hier1` bis `_experience.analytics.customDimensions.hierarchies.hier5` zugeordnet.

## Hierarchien, die die Adobe Analytics-Erweiterung verwenden

Sie können Hierarchien entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Hierarchie].

Sie können einen Hierarchiewert auf eine statische Zeichenfolge setzen oder auf ein Datenelement verweisen. Sie können auch das gewünschte Trennzeichen festlegen. Stellen Sie sicher, dass das hier definierte Trennzeichen mit dem in den Report Suite-Einstellungen festgelegten Trennzeichen übereinstimmt.

## s.hier1 – s.hier5 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Hierarchie ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Die maximale Länge beträgt 255 Byte. Werte, die länger als 255 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn beispielsweise einer Ihrer Abschnitte `Coach Griffin, Jim` heißt, wählen Sie ein anderes Trennzeichen als ein Komma. Die maximale Variablenanzahl beträgt 255 Byte. Trennzeichen können aus mehreren Zeichen bestehen, z. B. `||` oder `/|\`, die in Variablenwerten mit geringerer Wahrscheinlichkeit auftreten.

```js
s.hier1 = "Toys|Boys 6+|Legos|Super Block Tub";

s.hier3 = "Sports/Local Sports/Baseball";
```
