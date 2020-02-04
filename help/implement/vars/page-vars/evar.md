---
title: eVar
description: Benutzerspezifische Variablen, die Sie in Ihrer Implementierung verwenden können.
translation-type: tm+mt
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# eVar

eVars sind benutzerspezifische Variablen, die Sie beliebig verwenden können.

> [!TIP] Adobe empfiehlt in den meisten Fällen, eVars über Props zu verwenden. In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen eVars und deren Logik in Ihrem [Lösungsdesigndokument](../../prepare/solution-design.md)aufzeichnen.

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede eVar in den Report Suite-Einstellungen konfigurieren. See [Conversion variables](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in the Admin guide.

## eVars beim Start der Adobe Experience Platform

Sie können eVars entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL eVars] .

Sie können eine eVar auswählen, um einen Wert oder ein Datenelement festzulegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.eVar1 - s.eVar250 in AppMeasurement und Benutzerdefinierter Code-Editor starten

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

Wenn mehr als zwei Dezimalstellen angegeben sind, wird die Zähler-eVar auf zwei Dezimalstellen gerundet. Ein eVar-Zähler darf keine negativen Zahlen enthalten.

## Exklusive Vorteile für Props oder eVars

In der aktuellen Version von Adobe Analytics sind Props und eVars benutzerdefinierte Variablen mit ähnlichen Funktionen. Es gibt jedoch mehrere große Unterschiede:

* Daten in Eigenschaftsvariablen stehen in wenigen Minuten zur Verfügung. eVars können bis zu 30 Minuten dauern, bis sie in Berichten angezeigt werden.
* Props haben in Berichten eine Beschränkung von 100 Byte. eVars sind auf 255 Byte begrenzt.
* Eigenschaften können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Eigenschaften bleiben standardmäßig nicht über den festgelegten Treffer hinaus erhalten. eVars haben einen benutzerdefinierten Ablauf, mit dem Sie feststellen können, wann eine eVar nicht mehr für ein nachfolgendes Ereignis gutgeschrieben wird. Wenn Sie die [Berichtszeitverarbeitung](../../../components/vrs/vrs-report-time-processing.md)verwenden, können sowohl Eigenschaftsvariablen als auch eVars beliebige Zuordnungsmodelle verwenden.
