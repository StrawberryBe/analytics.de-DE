---
title: cleanStr
description: Entfernen oder ersetzen Sie alle unnötigen Zeichen aus einer Zeichenfolge.
translation-type: tm+mt
source-git-commit: c1a19f79eba3e992747a14146ca93306f84b355b
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 98%

---


# Adobe-Plug-in: cleanStr

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `cleanStr`-Plug-in entfernt oder ersetzt alle unnötigen Zeichen aus einer Zeichenfolge, einschließlich HTML-Tag-Zeichen, zusätzliche Leerzeichen, Tabulatoren und Zeilenumbrüche/Zeilenumschalter. Es ersetzt auch einfache linke/rechte Anführungszeichen (`‘` und `’`) durch gerade einfache Anführungszeichen (`'`). Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie unnötige Zeichen aus Variablenwerten entfernen möchten und die Funktion „Text bereinigen“ in Launch Ihre Implementierungsanforderungen nicht erfüllt. Dieses Plug-in ist nicht erforderlich, wenn die erfassten Daten keine unnötigen Zeichen enthalten oder die Funktion „Text bereinigen“ in Launch ausreicht.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: cleanStr initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: cleanStr v2.0 (No Prerequisites Required) */
function cleanStr(str){var a=str;if("-v"===a)return{plugin:"cleanStr",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}"undefined"!==typeof b&&(b.contextData.cleanStr="2.0");if("string"===typeof a){a=a.replace(/<\/?[^>]+(>|$)/g,"");a=a.trim();a=a.replace(/[\u2018\u2019\u201A]/g,"'");a=a.replace(/\t+/g,"");for(a=a.replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `cleanStr`-Methode verwendet die folgenden Argumente:

* **`str`** (erforderlich, Zeichenfolge): Der Wert, den Sie von der HTML-Codierung, zusätzlichen Leerzeichen, Tabulatoren oder anderen unnötigen Zeichen bereinigen möchten.

Die Methode gibt den Wert des `str`-Arguments zurück, wobei alle unnötigen Zeichen entfernt werden.

## Beispiele

### Beispiel 1

Gehen Sie wie folgt vor (wobei die Punkte für Leerzeichen und die Pfeile für Tabulatorzeichen stehen)

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Wenn Sie den folgenden Code ausführen ...

```js
s.eVar1 = cleanStr(s.eVar1)
```

... wird eVar1 auf „this is a messystring“(dies ist eine chaotische Zeichenfolge) gesetzt (mit allen zusätzlichen Leerzeichen und allen Tabulatorzeichen entfernt)

### Beispiel 2

Wenn ...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

 ... und der folgende Code ausgeführt wird ...

```js
cleanStr(s.eVar1)
```

... lautet der Endwert von s.eVar1 weiterhin:

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Wenn Sie das Plug-in allein ausführen (ohne den Rückgabewert einer Variablen zuzuweisen), wird die Variable, die über das str-Argument übergeben wird, nicht zurückgesetzt.

## Versionsverlauf

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (15. April 2018)

* Erste Version.
