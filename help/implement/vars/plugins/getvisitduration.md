---
title: getVisitDuration
description: Verfolgen Sie, wie lange ein Besucher bis jetzt auf der Site war.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in:getVisitDuration

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getVisitDuration` Plug-In verfolgt die Zeit in Minuten, die der Besucher bis zu diesem Zeitpunkt auf der Site verbracht hat. Adobe empfiehlt die Verwendung dieses Plug-Ins, wenn Sie die kumulative Zeit auf der Site bis zu diesem Zeitpunkt verfolgen oder die für die Durchführung einer Aktivität benötigte Zeit verfolgen möchten. Dieses Plug-In verfolgt nicht die Zeitspanne zwischen Ereignissen. Wenn diese Funktion gewünscht wird, verwenden Sie das `getTimeBetweenEvents` Plug-In.

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
/* Adobe Consulting Plugin: getVisitDuration v2.0 */
s.getVisitDuration=function(){var d=new Date,c=d.getTime(),b=this.c_r("s_dur");if(isNaN(b)||18E5<c-b)b=c;var a=c-b;d.setTime(c+18E5); this.c_w("s_dur",b+"",d);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute": a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getVisitDuration` Methode verwendet keine Argumente. Es gibt einen der folgenden Werte zurück:

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (wobei `[x]` die Anzahl der Minuten seit der Besucher auf der Site vergangen ist)

Dieses Plug-In erstellt ein Erstanbieter-Cookie mit dem Namen `"s_dur"`, das die Anzahl der Millisekunden angibt, die vergangen sind, seit der Besucher auf der Site gelandet ist. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.eVar10 = s.getVisitDuration();
```

 ...stellt eVar10 immer auf die Anzahl der Minuten ein, die vergangen sind, seit der Besucher auf der Site gelandet ist.

### Beispiel 2

Der folgende Code...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

 ...prüft mithilfe des InList-Plug-Ins, ob die Ereignisvariable das Kaufereignis enthält.  Ist dies der Fall, wird eVar10 auf die Anzahl der Minuten zwischen dem Beginn des Besuchs und dem Kaufzeitpunkt des Besuchers eingestellt.

### Beispiel 3

Der folgende Code...

```js
s.prop10 = s.getVisitDuration();
```

 ...wird immer prop10 so eingestellt, wie viele Minuten vergangen sind, seit der Besucher auf der Site gelandet ist.  Dies ist nützlich, wenn bei prop10 die Pfadsetzung aktiviert ist.  Wenn Sie die Metrik &quot;Ausstiege&quot;zum Bericht &quot;prop10&quot;hinzufügen, wird ein granularer Streudiagramm-Bericht angezeigt, wie lange ein Besuch innerhalb von Minuten dauerte, bevor ein Besucher die Site verließ.

## Versionsverlauf

### 2.0 (2. Mai 2018)

* Point Release (vollständige Neuanalyse/Umschreiben des Plugins).
