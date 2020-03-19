---
title: getAndPersistValue
description: Speichern Sie einen Wert, der zu einem späteren Zeitpunkt abgerufen werden kann.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getAndPersistValue

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getAndPersistValue` Plug-In können Sie einen Wert in einem Cookie speichern, das später während eines Besuchs abgerufen werden kann. Es erfüllt eine ähnliche Rolle wie die [!UICONTROL Storage duration] Funktion in Adobe Experience Platform Launch. Adobe empfiehlt die Verwendung dieses Plug-Ins, wenn Sie eine Analytics-Variable bei nachfolgenden Treffern nach dem Festlegen der Variablen automatisch auf denselben Wert beibehalten möchten. Dieses Plug-in ist nicht erforderlich, wenn die [!UICONTROL Storage duration] Funktion von Launch ausreicht oder Sie Variablen bei nachfolgenden Treffern nicht auf denselben Wert setzen und beibehalten müssen. Die integrierte Persistenz von eVars erfordert nicht die Verwendung dieses Plug-Ins, da diese Variablen serverseitig von Adobe beibehalten werden.

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
   * Aktionstyp: Initialize getAndPersistValue
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
/* Adobe Consulting Plugin: getAndPersistValue v2.0 */
s.getAndPersistValue=function(vtp,cn,ex){var b=new Date;cn=cn?cn:"s_gapv";(ex=ex?ex:0)?b.setTime(b.getTime()+864E5*ex): b.setTime(b.getTime()+18E5);vtp||(vtp=this.c_r(cn));this.c_w(cn,vtp,b);return vtp};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getAndPersist` Methode verwendet die folgenden Argumente:

* **`vtp`** (erforderlich): Der Wert, der von Seite zu Seite bestehen bleibt
* **`cn`** (optional): Der Name des Cookies, in dem der Wert gespeichert werden soll. Wenn dieses Argument nicht festgelegt ist, wird das Cookie mit `"s_gapv"`
* **`ex`** (optional): Die Anzahl der Tage vor Ablauf des Cookies. Wenn dieses Argument festgelegt ist `0` oder nicht, läuft das Cookie am Ende des Besuchs ab (30 Minuten Inaktivität).

Wenn die Variable im `vtp` Argument festgelegt ist, setzt das Plug-In das Cookie und gibt dann den Cookie-Wert zurück. Wenn die Variable im `vtp` Argument nicht festgelegt ist, gibt das Plug-In nur den Wert des Cookies zurück.

## Beispiele

### Beispiel 1

Im folgenden Code wird eVar21 auf den Wert von &quot;hello&quot;gesetzt.  Der Code legt dann das ev21gapv-Cookie fest, das in 28 Tagen abläuft und dem Wert von eVar21 entspricht (d.h. &quot;hello&quot;).  Der Code setzt dann (erneut) eVar21 gleich dem Wert des ev21gapv-Cookies.

```js
s.eVar21 = "hello";
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 2

Nehmen Sie an, dass eVar21 auf der aktuellen Seite noch nicht eingestellt wurde, aber auf einer vorherigen Seite innerhalb der letzten 28 Tage gleich &quot;hello&quot;war.   Der folgende Code setzt eVar21 nur auf den Wert des ev21gapv-Cookies (d.h. &quot;hello&quot;).  Das ev21gapv-Cookie wird nicht zurückgesetzt, da eVar21 nicht auf der aktuellen Seite eingestellt wurde, bevor die Funktion aufgerufen wurde.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 3

Nehmen Sie an, dass eVar21 auf der aktuellen Seite noch nicht eingestellt wurde, aber auf einer vorherigen Seite innerhalb der letzten 28 Tage gleich &quot;hello&quot;war.  Im folgenden Code wird nur prop35 eingestellt, der dem Wert des ev21gapv-Cookies entspricht (d.h. &quot;hello&quot;).  eVar21 wird nicht eingestellt.

```js
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 4

Im folgenden Code wird eVar21 mit dem Wert &quot;howdy&quot;eingestellt.  Der Code setzt dann das ev21gapv-Cookie, das in 28 Tagen abläuft, entsprechend dem Wert von eVar21 (d.h. &quot;howdy&quot;).  Der Code setzt dann prop35 gleich dem Wert des ev21gapv-Cookies (d.h. &quot;howdy&quot;).

```js
s.eVar21 = "howdy";
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 5

Angenommen, s.eVar21 wurde innerhalb der letzten 28 Tage auf keiner Seite eingestellt.  Der folgende Code setzt s.eVar21 gleich Null, da das ev21gapv-Cookie 28 Tage nach dem letzten Setzen abgelaufen wäre.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 6

Der folgende Code setzt eVar30 gleich &quot;shopping&quot;.  Anschließend wird das Cookie s_gapv gesetzt, das am Ende der Browsersitzung abläuft und dem Wert von s.eVar30 entspricht (d. h. &quot;einkaufen&quot;).  Anschließend wird s.eVar30 auf den Wert des Cookies s_gapv gesetzt (d. h. der getAndPersistValue-Aufruf gibt den Wert des Cookies s_gapv zurück, das in diesem Fall &quot;shopping&quot;ist).

```js
s.eVar30 = "shopping";
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

Wenn s.eVar30 nicht auf einen expliziten Wert für zusätzliche Seiten festgelegt ist, die während der Sitzung gesehen werden, sondern über den folgenden Code (in doPlugins) festgelegt wird...

```js
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

...s.eVar30 wird gleich &quot;shopping&quot;(d. h. der beibehaltene Wert des s_gapv-Cookies) eingestellt

## Versionsverlauf

### 2.0 (16. April 2018)

* Point Release (kleinere Codegröße)
* Durch Übergabe von 0 in das `ex` Argument wird nun der Ablauf nach 30 Minuten Inaktivität erzwungen und nicht nach Ablauf am Ende der Browsersitzung.

### 1.0 (18. Januar 2016)

* Erstes Release.
