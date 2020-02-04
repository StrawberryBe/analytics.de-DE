---
title: p_fo (nur Seite zuerst)
description: Stellen Sie sicher, dass bestimmte Routinen nur einmal pro Seite ausgelöst werden.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in:p_fo (nur Seite zuerst)

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `p_fo` Plug-In ist ein Dienstprogramm, das prüft, ob ein bestimmtes JavaScript-Objekt vorhanden ist. Wenn das Objekt nicht vorhanden ist, erstellt das Plug-In das Objekt und gibt es zurück `true`. Wenn das JavaScript-Objekt bereits auf der Seite vorhanden ist, wird es zurückgegeben `false`. Dieses Plug-in ist nützlich, um Code exakt einmal auf einer Seite auszuführen. Einige andere Plug-Ins setzen für die Verwendung dieses Codes voraus. Dieses Plug-in ist nicht erforderlich, wenn Sie sich nicht darüber Gedanken machen, wie oft Code auf einer Seite ausgeführt wird oder wenn Sie keine abhängigen Plug-ins verwenden.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Fügen Sie für jede Startregel, bei der Sie das Plug-In verwenden möchten, eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialisieren von addProductEvar
1. Speichern und veröffentlichen Sie die Änderungen an der Regel

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
1. Erweitern Sie die [!UICONTROL Verfolgung mithilfe eines benutzerdefinierten Code] -Akkordeons, das die Schaltfläche zum [!UICONTROL Öffnen des Editors] anzeigt.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung `s_gi`). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `p_fo` Methode verwendet die folgenden Argumente:

* **on** (erforderlich, Zeichenfolge): Der Name des JavaScript-Objekts, das vom Plug-In erstellt wird, wenn das Objekt noch nicht auf der Seite vorhanden ist.

Wenn das Objekt noch nicht vorhanden ist, gibt diese Methode zurück `true` und erstellt das Objekt. Wenn das Objekt bereits vorhanden ist, gibt diese Methode zurück `false`.

## Beispielaufrufe

### Beispiel 1

Der folgende Code prüft, ob das Objekt &quot;myobject&quot;auf der Seite vorhanden ist.  Wenn das Objekt &quot;myobject&quot;nicht vorhanden ist, erstellt der Code das Objekt &quot;myobject&quot;und gibt den Wert &quot;true&quot;zurück.  Daher wird der Code innerhalb der bedingten Anweisung (z. B. Console.log(&#39;hello&#39;);) ausgeführt.

Wenn hingegen das Objekt &quot;myobject&quot;bereits vorhanden ist, wenn der Aufruf p_fo erfolgt, gibt die Funktion p_fo den Wert false zurück und die bedingte Anweisung wird daher als false betrachtet.  In diesem Fall wird der Code innerhalb der bedingten Anweisung nicht ausgeführt.

```javascript
if(s.p_fo("myobject"))
{
  console.log("hello");
}
```

**** HINWEIS: Jedes Mal, wenn ein neues Seitenobjekt/ein neues DOM geladen wird (oder die aktuelle Seite erneut geladen wird), ist das im on-Argument angegebene Objekt nicht mehr vorhanden. Daher gibt das p_fo-Plug-in nach dem ersten Laden der Seite erneut true zurück, wenn es ausgeführt wird.

## Versionsverlauf

### 2.0

* Point Release (neu kompiliert, kleinere Codegröße).
* Der Rückgabewerttyp wurde von integer in boolean geändert

### 1.0

* Erstes Release.
