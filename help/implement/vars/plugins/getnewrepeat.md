---
title: getNewRepeat
description: Verfolgen Sie die Aktivitäten neuer oder rückkehrender Besucher.
translation-type: tm+mt
source-git-commit: aa4e1e71b8962fca8c880b9efe2b0a2b8b9e1360

---


# Adobe-Plug-in: getNewRepeat

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen bei der Verwendung von Adobe Analytics mehr Nutzen zu verschaffen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getNewRepeat` Plug-in können Sie innerhalb einer bestimmten Anzahl von Tagen feststellen, ob es sich bei einem Besucher um einen neuen Besucher oder einen wiederholten Besucher handelt. Adobe empfiehlt die Verwendung dieses Plugins, wenn Sie Besucher anhand einer benutzerdefinierten Anzahl von Tagen als &quot;neu&quot;identifizieren möchten. Dieses Plug-in ist nicht erforderlich, wenn die Dimensionen &quot;Neu/Wiederholte Besucher&quot;im Analysis Workspace den Anforderungen Ihres Unternehmens entsprechen.

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
/* Adobe Consulting Plugin: getNewRepeat v2.1 */
s.getNewRepeat=function(d){d=d?d:30;var s=this,p="s_nr"+d,b=new Date,e=s.c_r(p),f=e.split("-"),c=b.getTime();b.setTime(c+864E5*d); if(""===e||18E4>c-f[0]&&"New"===f[1])return s.c_w(p,c+"-New",b),"New";s.c_w(p,c+"-Repeat",b);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getNewRepeat` Methode verwendet die folgenden Argumente:

* **`d`**(integer, optional): Die erforderliche Mindestanzahl von Tagen zwischen Besuchen, an denen Besucher zurückgesetzt werden`"New"`. Wenn dieses Argument nicht festgelegt ist, wird der Standardwert 30 Tage verwendet.

Diese Methode gibt den Wert zurück, `"New"` wenn das vom Plug-In eingestellte Cookie nicht vorhanden oder abgelaufen ist. Gibt den Wert zurück, `"Repeat"` wenn das vom Plug-In eingestellte Cookie vorhanden ist, sowie die Zeitdauer seit dem aktuellen Treffer und der im Cookie eingestellte Zeitraum über 30 Minuten. Diese Methode gibt denselben Wert für den gesamten Besuch zurück.

Dieses Plug-In verwendet ein Cookie mit dem Namen `"s_nr[LENGTH]"` , bei dem `[LENGTH]` es mit dem `d` Argument übereinstimmt. Das Cookie enthält einen Unix-Zeitstempel, der die aktuelle Zeit und den aktuellen Status des Besuchers (`"New"` oder `"Repeat"`) darstellt.

## Beispielaufrufe

### Beispiel 1

Im folgenden Code wird s.eVar1 gleich dem Wert &quot;New&quot;für neue Besucher eingestellt und s.eVar1 wird während des restlichen Besuchs des Besuchers auf der Site weiterhin mit dem Wert &quot;New&quot;(mit jedem neuen Aufruf) eingestellt.

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 2

Wenn der Besucher nach dem letzten Aufruf von s.getNewRepeat() 31 Minuten bis 30 Tage zurück zur Site zurückkehrt, setzt der folgende Code s.eVar1 auf den Wert &quot;Repeat&quot;und setzt während des restlichen Besuchs des Besuchers auf s.eVar1 den Wert &quot;Repeat&quot;(mit jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 3

Wenn der Besucher seit dem letzten Aufruf von s.getNewRepeat() seit mindestens 30 Tagen nicht auf der Site war, setzt der folgende Code s.eVar1 gleich dem Wert von &quot;New&quot;und setzt s.eVar1 weiterhin den Wert &quot;New&quot;(mit jedem neuen Aufruf) während des restlichen Besuchs auf der Site fest.

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 4

Wenn der Besucher nach dem letzten Aufruf von s.getNewRepeat() 31 Minuten bis 365 Tage (d.h. 1 Jahr) zur Site zurückkehrt, setzt der folgende Code s.eVar1 gleich dem Wert von &quot;Repeat&quot;und setzt s.eVar1 während des verbleibenden Zeitraums auf den Wert von &quot;Repeat&quot;(mit jedem neuen Aufruf) Besuch der Site.

```js
s.eVar1=s.getNewRepeat(365);
```

### Beispiel 5

Wenn der Besucher seit dem letzten Aufruf von s.getNewRepeat() seit mindestens 365 Tagen (d. h. 1 Jahr) nicht auf der Site war, setzt der folgende Code s.eVar1 auf den Wert von &quot;New&quot;und setzt s.eVar1 weiterhin auf den Wert &quot;New&quot;(mit jedem neuen Aufruf) während des verbleibenden Teils des Besuchers ein Besuche der Site.

```js
s.eVar1=s.getNewRepeat(365);
```

## Versionsverlauf

### 2.1 (30. September 2019)

* Neuanordnung der JavaScript-Logik zur Reduzierung der Plugin-Größe

### 2.0 (16. April 2018)

* Neu kompiliert mit kleinerer Codegröße
* Die Möglichkeit, das Cookie zum Speichern der Besuchsinformationen zu benennen, wurde entfernt. Das Plug-In benennt das Cookie nun dynamisch basierend auf dem Wert, der an das `d` Argument übergeben wird.
