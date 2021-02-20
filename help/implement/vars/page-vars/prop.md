---
title: prop
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 100%

---


# prop

*Auf dieser Hilfeseite wird die Implementierung von Props beschrieben. Informationen dazu, wie Props als Dimension funktionieren, finden Sie unter [Props](/help/components/dimensions/prop.md) im Komponenten-Benutzerhandbuch.*

Props sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen.

>[!TIP]
>
>Adobe empfiehlt in den meisten Fällen die Verwendung von [eVars](evar.md). In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 75 Props verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Props in Adobe Experience Platform Launch

Sie können Props entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Props].

Sie können eine Prop auf einen Wert oder ein Datenelement festlegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.prop1 – s.prop75 in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Jede Prop-Variable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Die maximale Länge beträgt 100 Byte. Werte, die länger als 100 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
s.prop1 = "Example custom value";
```

## Listen-Props

Listen-Props sind eine Einstellung, die auf Props angewendet wird, mit denen die Variable mehrere Werte im selben Treffer enthalten kann. Wenn diese Einstellung nicht aktiviert ist oder das falsche Trennzeichen verwendet wird, wird die Variable als einzelner Wert behandelt.

### Konfigurieren von Listen-Props

Aktivieren Sie Listen-Props in den Report Suite-Einstellungen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md). Vergewissern Sie sich, dass das gewünschte Trennzeichen richtig konfiguriert ist. Adobe stellt kein Standardtrennzeichen bereit.

>[!TIP]
>
>Bei Implementierungen werden häufig Trennzeichen wie Komma (`,`), Doppelpunkt (`:`), Semikolon (`;`) oder der senkrechte Strich (`|`) verwendet. Sie können jedes beliebige Trennzeichen verwenden, das am besten zu Ihrer Implementierung passt.

### Festlegen von Listen-Props

Sobald Sie Listen-Props in den Report Suite-Einstellungen mit dem gewünschten Trennzeichen konfigurieren, gibt es außer der Verwendung des Trennzeichens keine weiteren Implementierungsunterschiede.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

>[!IMPORTANT]
>
>Listen-Props unterliegen weiterhin der maximalen Länge von 100 Byte. Listen-Props können diese Grenze leichter erreichen und abgeschnitten werden, da sie mehrere Werte enthalten können. Erwägen Sie die Verwendung von Abkürzungen oder die Verkürzung von Werten, wenn Sie diesen Grenzwert von 100 Byte erreichen.

Wenn Sie denselben Wert mehr als einmal in einer Listen-Prop festlegen, werden diese Werte in Berichten dedupliziert. Analysis Workspace zählt die Anzahl der Treffer, bei denen ein Wert angezeigt wird, und nicht, wie oft ein Wert in Daten vorhanden ist.
