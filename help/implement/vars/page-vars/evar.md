---
title: eVar
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# eVar

*Auf dieser Hilfeseite wird die Implementierung von eVars beschrieben. Informationen dazu, wie eVars als Dimension funktionieren, finden Sie unter[eVars](../../../components/c-variables/dimensionslist/reports-conversion.md)im Komponenten-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können.

>[!TIP] Adobe empfiehlt in den meisten Fällen die Verwendung von eVars anstelle von Props. In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen eVars und deren Logik in Ihrem [Lösungsdesigndokument](../../prepare/solution-design.md) aufzeichnen.

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede eVar in den Report Suite-Einstellungen konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

## eVars in Adobe Experience Platform Launch

Sie können eVars entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL eVars] section.

Sie können eine eVar auswählen, um einen Wert oder ein Datenelement festzulegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.eVar1 – s.eVar250 in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Jede eVar ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Die maximale Länge beträgt 255 Byte. Werte, die länger als 255 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
s.eVar1 = "Example custom value";
```

## Zähler-eVars

eVar-Werte enthalten normalerweise einen Zeichenfolgenwert. Sie können eVars jedoch so konfigurieren, dass sie stattdessen einen Zähler enthalten. Sie möchten beispielsweise die Anzahl der internen Suchen zählen, die vor einem Kauf durchgeführt wurden. Anstatt einen Textwert festzulegen, verwenden Sie folgende Syntax:

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

Wenn mehr als zwei Dezimalstellen angegeben sind, wird die Zähler-eVar auf zwei Dezimalstellen gerundet. Ein eVar-Zähler kann keine negativen Zahlen enthalten.

>[!IMPORTANT] Bevor Sie Zähler-eVars verwenden können, müssen Sie eVars zunächst in der Admin-Konsole auf &quot;Zähler&quot;konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

## Vorteile von Props oder eVars

In der aktuellen Version von Adobe Analytics sind Props und eVars benutzerdefinierte Variablen mit ähnlichen Funktionen. Sie haben jedoch einige große Unterschiede:

* Die Daten in Props sind innerhalb von Minuten in der Berichterstellung verfügbar. Bei eVars kann es bis zu 30 Minuten dauern, bis die Daten in der Berichterstellung angezeigt werden.
* Props haben in Berichten eine Beschränkung von 100 Byte. eVars sind auf 255 Byte begrenzt.
* Props können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Props bleiben standardmäßig nicht über den festgelegten Treffer hinaus erhalten. eVars haben eine benutzerdefinierte Gültigkeit, mit der Sie feststellen können, wann einer eVar ein nachfolgendes Ereignis nicht mehr gutgeschrieben wird. Wenn Sie jedoch die [Berichtszeitverarbeitung](../../../components/vrs/vrs-report-time-processing.md)verwenden, können sowohl props als auch eVars ein benutzerdefiniertes Zuordnungsmodell verwenden.
