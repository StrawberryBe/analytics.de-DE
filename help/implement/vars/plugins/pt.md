---
title: pt
description: Führt eine Funktion in einer Variablenliste aus.
translation-type: tm+mt
source-git-commit: 26f06adbef1608a6e01df3ab1d3ad4ba78abc28f

---


# Adobe-Plug-in: pt

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen bei der Verwendung von Adobe Analytics mehr Nutzen zu verschaffen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `pt` Plug-in führt eine Funktion oder Methode in einer Liste von Analytics-Variablen aus. Beispielsweise können Sie die `clearVars` Methode selektiv für mehrere Variablen ausführen, ohne die Methode jedes Mal manuell aufzurufen. Einige andere Plug-ins hängen von diesem Code ab, um korrekt ausgeführt zu werden. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht gleichzeitig eine bestimmte Funktion für mehrere Analytics-Variablen ausführen müssen oder wenn Sie keine abhängigen Plug-ins verwenden.

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
/* Adobe Consulting Plugin: pt v2.01 */
 s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `pt` Methode verwendet die folgenden Argumente:

* **`l`**(erforderlich, Zeichenfolge): Eine Liste von Variablen, für die die im`cf`Argument enthaltene Funktion ausgeführt werden kann.
* **`de`**(optional, Zeichenfolge): Das Trennzeichen, das die Liste der Variablen im`l`Argument trennt. Der Standardwert ist Komma (`,`).
* **`cf`**(erforderlich, Zeichenfolge): Der Name der Rückruffunktion im AppMeasurement-Objekt, die für jede der im`l`Argument enthaltenen Variablen aufgerufen werden soll.
* **`fa`**(optional, Zeichenfolge): Wenn die Funktion im`cf`Argument bei Ausführung zusätzliche Argumente benötigt, schließen Sie sie hier ein. Die Standardeinstellung ist`undefined`.

Der Aufruf dieser Methode gibt einen Wert zurück, wenn die Rückruffunktion (im `cf` Argument) einen Wert zurückgibt.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ist Teil des Plug-ins getQueryParam.  Es wird die Hilfefunktion getParameterValue für alle Schlüssel-Wert-Paare ausgeführt, die im Abfragezeichenfolgen der URL enthalten sind (fullQueryString).  Anders ausgedrückt, um jedes Schlüssel-Wert-Paar zu extrahieren, muss fullQueryString durch ein kaufmännisches Und-Zeichen (&amp;) getrennt werden. Der Parameter &quot;parameterKey&quot;bezieht sich auf den Abfragezeichenfolgenparameter, den das Plug-In speziell aus der Abfragezeichenfolge extrahieren möchte

```javascript
returnValue = s.pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

Die obige Zeile ist eine Verknüpfung zum Ausführen von Code, der wie folgt aussieht:

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = s.getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## Versionsverlauf

### 2.01 (24. September 2019)

* Geringfügige Codeänderungen zur Verringerung der Gesamtgröße

### 2.0 (17. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).
* Unterstützung für H-Code und AppMeasurement hinzugefügt.

### 1.0 (23. September 2013)

* Erstes Release.
