---
title: prop
description: Benutzerspezifische Variablen, die Sie in Ihrer Implementierung verwenden können.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# prop

Eigenschaftsvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können.

> [!TIP] Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen. Unter [eVars](evar.md) finden Sie einen Funktionsvergleich zwischen diesen beiden benutzerdefinierten Variablentypen.

Wenn Ihr Unternehmen Props verwendet, stellen Sie sicher, dass Sie deren Verwendung und Logik in Ihrem [Lösungsdesign-Dokument](../../prepare/solution-design.md)aufzeichnen.

## Props in Adobe Experience Platform Launch

Sie können Props entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Props] section.

Sie können eine Eigenschaftsvariable auswählen, um einen Wert oder ein Datenelement festzulegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.prop1 - s.prop75 im AppMeasurement- und Starten des benutzerdefinierten Code-Editors

Jede prop-Variable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Ihre maximale Länge beträgt 100 Byte; Werte, die länger als 100 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
s.prop1 = "Example custom value";
```

## Liste-Props

Listen-Props sind eine Einstellung, die auf Props angewendet wird, mit denen die Variable mehrere Werte im selben Treffer enthalten kann. Wenn diese Einstellung nicht aktiviert ist oder das falsche Trennzeichen verwendet wird, wird die Variable als einzelner Wert behandelt.

### Liste-Props konfigurieren

Aktivieren Sie Listen-Props in den Report Suite-Einstellungen. See [Traffic variables](/help/admin/admin/c-traffic-variables/traffic-var.md) in the Admin user guide. Vergewissern Sie sich, dass das gewünschte Trennzeichen richtig konfiguriert ist. Adobe stellt kein Standardtrennzeichen bereit.

> [!TIP] Bei Implementierungen werden häufig Trennzeichen wie Komma (`,`), Doppelpunkt (`:`), Semikolon (`;`) oder Pipe (`|`) verwendet. Sie können jedes beliebige Trennzeichen verwenden, das am besten zu Ihrer Implementierung passt.

### Festlegen von Listen-Props

Nachdem Sie die Listen-Props in den Report Suite-Einstellungen mit dem gewünschten Trennzeichen konfiguriert haben, gibt es keine anderen Implementierungsunterschiede als das Trennzeichen.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

> [!IMPORTANT] Listen-Props unterliegen weiterhin der maximalen Länge von 100 Byte. Listen-Props können diesen Grenzwert leichter erreichen und abgeschnitten werden, da sie mehrere Werte enthalten können. Erwägen Sie die Verwendung von Abkürzungen oder die Verkürzung von Werten, wenn Sie diese 100-Byte-Grenze erreichen.

Wenn Sie denselben Wert mehr als einmal in einer Liste-Eigenschaft festlegen, werden diese in Berichte dedupliziert. Analyse Workspace zählt die Anzahl der Treffer, bei denen ein Wert angezeigt wird, und nicht, wie oft ein Wert in Daten vorhanden ist.
