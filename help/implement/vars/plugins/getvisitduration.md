---
title: getVisitDuration
description: Verfolgen Sie, wie lange ein Besucher bis jetzt auf der Site war.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getVisitDuration

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getVisitDuration` Plug-In verfolgt die Zeit in Minuten, die der Besucher bis zu diesem Zeitpunkt auf der Site verbracht hat. Adobe empfiehlt die Verwendung dieses Plug-Ins, wenn Sie die kumulative Zeit auf der Site bis zu diesem Zeitpunkt verfolgen oder die für die Durchführung einer Aktivität benötigte Zeit verfolgen möchten. Dieses Plug-In verfolgt nicht die Zeitdauer zwischen Ereignissen. Wenn diese Funktion gewünscht wird, verwenden Sie das [`getTimeBetweenEvents`](gettimebetweenevents.md) Plug-In.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe Angebots ist eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Catalog] Schaltfläche
1. Installieren und Veröffentlichen der [!UICONTROL Common Analytics Plugins] Erweiterung
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Hinzufügen Sie eine Aktion mit der folgenden Konfiguration auf die oben stehende Regel:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: getVisitDuration initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter der Adobe Analytics-Erweiterung.
1. Erweitern Sie das [!UICONTROL Configure tracking using custom code] Akkordeon, das die [!UICONTROL Open Editor] Schaltfläche einblendet.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitDuration v2.0 */
s.getVisitDuration=function(){var d=new Date,c=d.getTime(),b=this.c_r("s_dur");if(isNaN(b)||18E5<c-b)b=c;var a=c-b;d.setTime(c+18E5); this.c_w("s_dur",b+"",d);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute": a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getVisitDuration` Methode verwendet keine Argumente. Es gibt einen der folgenden Werte zurück:

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (wobei `[x]` die Anzahl der Minuten seit der Anlandung des Besuchers auf dem Standort angegeben ist)

Dieses Plug-In erstellt ein Erstanbieter-Cookie mit dem Namen `"s_dur"`, das die Anzahl der Millisekunden angibt, die seit der Landung des Besuchers auf der Site vergangen sind. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.eVar10 = s.getVisitDuration();
```

...stellt eVar10 immer auf die Anzahl der Minuten ein, die seit der Landung des Besuchers auf der Site vergangen sind.

### Beispiel 2

Der folgende Code...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

...verwendet das Plug-in inList, um zu überprüfen, ob die Variable &quot;Ereignisses&quot;das Ereignis &quot;purchase&quot;enthält.  Ist dies der Fall, wird eVar10 auf die Anzahl der Minuten zwischen dem Beginn des Besuchers des Besuchs und dem Kaufzeitpunkt eingestellt.

### Beispiel 3

Der folgende Code...

```js
s.prop10 = s.getVisitDuration();
```

...wird immer prop10 so eingestellt, wie viele Minuten vergangen sind, seit der Besucher auf der Site gelandet ist.  Dies ist nützlich, wenn bei prop10 die Pfadsetzung aktiviert ist.  Wenn Sie die Metrik &quot;Ausstiege&quot;zum Bericht &quot;prop10&quot;hinzufügen, wird ein granularer &quot;Streudiagramm&quot;angezeigt, wie lange ein Besuch innerhalb von Minuten dauerte, bevor ein Besucher die Site verließ.

## Versionsverlauf

### 2.0 (2. Mai 2018)

* Point Release (vollständige Neuanalyse/Umschreiben des Plugins).
