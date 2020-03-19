---
title: getValOnce
description: Verhindern, dass eine Analytics-Variable zweimal hintereinander auf denselben Wert gesetzt wird.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getValOnce

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getValOnce` Plug-In verhindert, dass eine Variable mehrmals auf denselben Wert gesetzt wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Vorfälle deduplizieren möchten, bei denen ein Besucher eine Seite aktualisiert oder eine bestimmte Seite mehrmals besucht. Dieses Plug-in ist nicht erforderlich, wenn Sie sich keine Sorgen um die Metrik &quot;Vorfälle&quot;in Analyse Workspace machen.

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
   * Aktionstyp: getValOnce initialisieren
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
/* Adobe Consulting Plugin: getValOnce v2.0 */
s.getValOnce=function(vtc,cn,et,ep){if(vtc&&(cn=cn||"s_gvo",et=et||0,ep="m"===ep?6E4:864E5,vtc!==this.c_r(cn))){var e=new Date;e.setTime(e.getTime()+et*ep);this.c_w(cn,vtc,0===et?0:ep);return vtc}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getValOnce` Methode verwendet die folgenden Argumente:

* **`vtc`** (erforderlich, Zeichenfolge): Zu prüfende Variable, ob sie zuvor auf einen identischen Wert gesetzt wurde
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, das den zu prüfenden Wert enthält. Standard ist `"s_gvo"`
* **`et`** (optional, integer): Der Ablauf des Cookies in Tagen (oder Minuten, je nach `ep` Argument). Die Standardeinstellung ist `0`, die am Ende der Browsersitzung abläuft.
* **`ep`** (optional, Zeichenfolge): Legen Sie dieses Argument nur fest, wenn das `et` Argument ebenfalls festgelegt ist. Legen Sie dieses Argument fest, `"m"` wenn das `et` Argument in Minuten und nicht in Tagen ablaufen soll. Die Standardeinstellung ist `"d"`der Wert, der das `et` Argument in Tagen festlegt.

Wenn das `vtc` Argument und der Cookie-Wert übereinstimmen, gibt diese Methode eine leere Zeichenfolge zurück. Wenn das `vtc` Argument und der Cookie-Wert nicht übereinstimmen, gibt die Methode das `vtc` Argument als Zeichenfolge zurück.

## Beispielaufrufe

### Beispiel 1

Verwenden Sie diesen Aufruf, um zu verhindern, dass derselbe Wert für die nächsten 30 Tage mehrmals hintereinander an s.Campaign weitergegeben wird:

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

Im obigen Aufruf vergleicht das Plug-in zunächst den bereits im Cookie s_Campaign enthaltenen Wert mit dem Wert aus der aktuellen Variablen s.Campaign.   Wenn keine Übereinstimmung erfolgt, setzt das Plug-In das Cookie s_Campaign auf den neuen Wert von s.Campaign und gibt dann den neuen Wert zurück.   Dieser Vergleich findet für die nächsten dreißig Tage statt.

### Beispiel 2

Verwenden Sie diesen Aufruf, um zu verhindern, dass derselbe Wert während der Sitzung festgelegt wird:

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

Dieser Code verhindert, dass derselbe Wert während der Sitzung eines Benutzers mehrmals hintereinander an s.eVar2 übergeben wird.  Außerdem wird der Wert &quot;m&quot;im Ausdruck (am Ende des Aufrufs) ignoriert, da die Ablaufzeit auf 0 gesetzt wird.   Der Code speichert auch den Vergleichswert im s_ev2-Cookie.

## Versionsverlauf

### 2.0

* Point Release (neu kompiliert, kleinere Codegröße).

### 1.1

* Die Option zur Auswahl von Minuten oder Tagen für den Ablauf über den `t` Parameter wurde hinzugefügt.
* Der Umfang der `k` Variablen, die verwendet wird, um sie auf das Plug-In zu beschränken, wurde korrigiert. Diese Änderung verhindert mögliche Störungen mit anderen Code auf der Seite.
