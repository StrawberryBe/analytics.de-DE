---
title: cleanStr
description: Entfernen oder ersetzen Sie alle unnötigen Zeichen aus einer Zeichenfolge.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in:cleanStr

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `cleanStr` Plug-In entfernt oder ersetzt alle unnötigen Zeichen aus einer Zeichenfolge, einschließlich HTML-Tag-Zeichen, zusätzliche Leerzeichen, Tabulatoren und Zeilenumbruch-/Wagenrückgaben. Es ersetzt auch einfache linke/rechte Anführungszeichen (`‘` und `’`) gerade einfache Anführungszeichen (`'`). Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie unnötige Zeichen aus Variablenwerten entfernen möchten und die Funktion &quot;Text bereinigen&quot;in Launch Ihre Implementierungsanforderungen nicht erfüllt. Dieses Plug-in ist nicht erforderlich, wenn die erfassten Daten keine unnötigen Zeichen enthalten oder die Funktion &quot;Text bereinigen&quot;in Launch ausreicht.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Fügen Sie der oben stehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialize cleanStr
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

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
/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"");str=str.trim(); str=str.replace(/[\u2018\u2019\u201A]/g,"'");str=str.replace(/\t+/g,"");for(str=str.replace(/[\n\r]/g," ");-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `cleanStr` Methode verwendet die folgenden Argumente:

* **`str`**(erforderlich, Zeichenfolge): Der Wert, den Sie löschen möchten, um HTML-Kodierung, zusätzlichen Leerzeichen, Tabulatoren oder andere unnötige Zeichen zu entfernen.

Die Methode gibt den Wert des `str` Arguments zurück, wobei alle unnötigen Zeichen entfernt werden.

## Beispiele

### Beispiel 1

Gehen Sie wie folgt vor (wobei die Punkte Leerzeichen und die Pfeile Tabstoppzeichen darstellen)

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Wenn Sie den folgenden Code ausführen...

```js
s.eVar1 = cleanStr(s.eVar1)
```

 ...eVar1 wird auf &quot;this is a messystring&quot;(dies ist ein Meldungszeichen) eingestellt (alle zusätzlichen Leerzeichen und alle Tabstoppzeichen werden entfernt)

### Beispiel 2

Wenn...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

 ...und der folgende Code wird ausgeführt...

```js
cleanStr(s.eVar1)
```

 ...Der Endwert von s.eVar1 lautet weiterhin:

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Wenn Sie das Plug-In ganz alleine ausführen (ohne den Rückgabewert einer Variablen zuzuweisen), wird die Variable, die über das str-Argument übergeben wird, nicht &quot;zurückgesetzt&quot;.

## Versionsverlauf

### 1.0 (15. April 2018)

* Erstes Release.
