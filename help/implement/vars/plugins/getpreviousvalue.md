---
title: getPreviousValue
description: Rufen Sie den letzten Wert ab, der an eine Variable übergeben wird.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getPreviousValue

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getPreviousValue` Plug-In können Sie eine Variable auf einen Wert einstellen, der bei einem vorherigen Treffer festgelegt wurde. Dieses Plug-in ist nicht erforderlich, wenn Ihre Implementierung alle gewünschten Werte im aktuellen Treffer enthält.

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
   * Aktionstyp: getPreviousValue initialisieren
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
/* Adobe Consulting Plugin: getPreviousValue v2.0 */
s.getPreviousValue=function(v,c){var s=this,d;c=c||"s_gpv";var b=new Date;b.setTime(b.getTime()+18E5);s.c_r(c)&&(d=s.c_r(c)); v?s.c_w(c,v,b):s.c_w(c,d,b);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getPreviousValue` Methode verwendet die folgenden Argumente:

* **`v`** (Zeichenfolge, erforderlich): Die Variable mit dem Wert, der an die nächste Bildanforderung übergeben werden soll. Eine häufig verwendete Variable ist `s.pageName` das Abrufen des vorherigen Seitenwerts.
* **`c`** (Zeichenfolge, optional): Der Name des Cookies, in dem der Wert gespeichert wird.  Wenn dieses Argument nicht festgelegt ist, wird standardmäßig `"s_gpv"`verwendet.

Wenn Sie diese Methode aufrufen, wird der im Cookie enthaltene Zeichenfolgenwert zurückgegeben. Das Plug-In setzt dann den Ablauf des Cookies zurück und weist ihm den Variablenwert aus dem `v` Argument zu. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* Legt s.prop7 den Wert fest, der in der vorherigen Bildanforderung an s.pageName übergeben wurde (d. h. den Wert, der im Cookie &quot;gpv_Page&quot; gespeichert wurde)
* Der Code setzt dann das Cookie &quot;gpv_Page&quot;zurück, sodass es dem aktuellen Wert von s.pageName entspricht
* Wenn s.pageName nicht zum Zeitpunkt der Ausführung dieses Codes eingestellt ist, setzt der Code den Ablauf für den aktuellen Wert des Cookies zurück

### Beispiel 2

Im folgenden Code wird s.prop7 auf den letzten Wert eingestellt, der an s.pageName übergeben wird, jedoch nur, wenn Ereignis1 zum Zeitpunkt des Aufrufs auch in s.Ereignisses enthalten ist, wie über das InList-Plug-In bestimmt.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Beispiel 3

Im folgenden Code wird s.prop7 auf den letzten Wert eingestellt, der an s.pageName übergeben wird, jedoch nur, wenn s.pageName derzeit gleichzeitig auf der Seite eingestellt ist.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Beispiel 4

Im folgenden Code wird s.eVar10 auf den Wert gesetzt, der in der vorherigen Bildanforderung an s.eVar1 übergeben wurde.   Der vorherige eVar1-Wert wäre im Cookie &quot;s_gpv&quot;enthalten gewesen.  Der Code setzt dann das Cookie &quot;s_gpv&quot;gleich dem aktuellen Wert von s.eVar1.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## Unwahrscheinliche Quirts

Wenn die mit dem v-Argument verknüpfte Variable auf einen neuen Wert eingestellt ist und das getPreviousValue-Plug-In ausgeführt wird, aber ein Analytics-Server-Aufruf NICHT gleichzeitig gesendet wird, wird der neue v-Argumentwert bei der nächsten Ausführung des Plug-Ins weiterhin als &quot;vorheriger Wert&quot;betrachtet.
Angenommen, der folgende Code wird auf der ersten Seite des Besuchs ausgeführt:

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Dieser Code erzeugt einen Server-Aufruf, bei dem das Argument pageName mit &quot;home&quot;identisch ist und das Argument p7 (prop7) nicht eingestellt ist.  Der Aufruf von s.getPreviousValue speichert jedoch den Wert von s.pageName (d.h. &quot;home&quot;) in dem im Aufruf angegebenen Cookie (d. h. das &quot;gpv_Page&quot;-Cookie).
Nehmen Sie jetzt an, dass unmittelbar danach auf derselben Seite der folgende Code ausgeführt wird (aus welchem Grund auch immer):

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

Da die Funktion s.t() in diesem Codeblock nicht ausgeführt wird, wird keine weitere Bildanforderung erstellt.  Wenn jedoch der Funktionscode s.getPreviousValue() dieses Mal ausgeführt wird, wird s.prop7 gleich dem vorherigen Wert von s.pageName (d. h. &quot;home&quot;) und speichert dann den neuen Wert von s.pageName (d.h. &quot;zufriedener Wert&quot;) im Cookie &quot;gpv_Page&quot;.
Angenommen, der Besucher navigiert zu einer anderen Seite und der folgende Code wird auf dieser Seite ausgeführt:

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Wenn die s.t()-Aufruffunktion ausgeführt wird, wird eine Bildanforderung erstellt, bei der s.pageName=&quot;Seite 2&quot; und s.prop7 gleich &quot;fröhlicher Wert&quot;sind. Dies war der Wert von s.pageName, als der letzte Aufruf von getPreviousValue stattfand.   Der s.prop7-Wert von &quot;home&quot;war nie in einer echten Bildanforderung enthalten, obwohl &quot;home&quot;der erste Wert war, der an s.pageName übergeben wurde.

## Versionsverlauf

### v2.0 (7. Oktober 2019)

* Point Release (vollständige Logik umschreiben).
