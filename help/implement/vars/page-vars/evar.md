---
title: eVar
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 100%

---


# eVar

*Auf dieser Hilfeseite wird die Implementierung von eVars beschrieben. Informationen dazu, wie eVars als Dimension funktionieren, finden Sie unter [eVars](/help/components/dimensions/evar.md) im Komponenten-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsdesigndokument](/help/implement/prepare/solution-design.md) verfügen, werden die meisten für Ihr Unternehmen spezifischen Dimensionen als eVars angezeigt. Standardmäßig bleiben eVars über den Treffer hinaus bestehen, auf den sie gesetzt wurden. Sie können ihre Gültigkeit und Zuordnung unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen anpassen.

Die Anzahl der verfügbaren eVars hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 250 eVars verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede eVar in den Report Suite-Einstellungen konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

## eVars in Adobe Experience Platform Launch

Sie können eVars entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL eVars].

Sie können eine eVar auf einen Wert oder ein Datenelement festlegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

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

>[!IMPORTANT]
>
>Bevor Sie Zähler-eVars verwenden können, müssen Sie eVars in der Admin Console zuerst in „Zähler“ konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).
