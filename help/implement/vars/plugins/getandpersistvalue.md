---
title: getAndPersistValue
description: Speichern Sie einen Wert, der später jederzeit abgerufen werden kann.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-Plug-in: getAndPersistValue

>[!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getAndPersistValue`-Plug-in können Sie einen Wert in einem Cookie speichern, das später während eines Besuchs abgerufen werden kann. Es erfüllt eine ähnliche Rolle wie die Funktion [!UICONTROL Speicherdauer] in Adobe Experience Platform Launch. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie eine Analytics-Variable bei nachfolgenden Treffern automatisch auf dem gleichen Wert belassen wollen, nachdem die Variable gesetzt wurde. Dieses Plug-in ist nicht erforderlich, wenn die Funktion [!UICONTROL Speicherdauer] von Launch ausreicht oder Sie Variablen in nachfolgenden Treffern nicht auf denselben Wert setzen und beibehalten müssen. Die integrierte Persistenz von eVars erfordert nicht die Verwendung dieses Plug-ins, da diese Variablen Server-seitig von Adobe beibehalten werden.

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
   * Aktionstyp: getAndPersistValue initialisieren
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
/* Adobe Consulting Plugin: getAndPersistValue v2.0 */
s.getAndPersistValue=function(vtp,cn,ex){var b=new Date;cn=cn?cn:"s_gapv";(ex=ex?ex:0)?b.setTime(b.getTime()+864E5*ex): b.setTime(b.getTime()+18E5);vtp||(vtp=this.c_r(cn));this.c_w(cn,vtp,b);return vtp};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getAndPersist`-Methode verwendet die folgenden Argumente:

* **`vtp`** (erforderlich): Der Wert, der von Seite zu Seite beibehalten werden soll
* **`cn`** (optional): Der Name des Cookies, in dem der Wert gespeichert werden soll. Wenn dieses Argument nicht gesetzt ist, heißt Das Cookie `"s_gapv"`
* **`ex`** (optional): Die Anzahl der Tage vor Ablauf des Cookies. Wenn dieses Argument `0` oder nicht gesetzt ist, läuft das Cookie am Ende des Besuchs ab (30 Minuten Inaktivität).

Wenn die Variable im `vtp`-Argument festgelegt ist, setzt das Plug-in das Cookie und gibt dann den Cookie-Wert zurück. Wenn die Variable im `vtp`-Argument nicht festgelegt ist, gibt das Plug-in nur den Cookie-Wert zurück.

## Beispiele

### Beispiel 1

Der folgende Code setzt eVar21 auf den Wert von „hello“.  Der Code setzt dann das ev21gapv-Cookie, das in 28 Tagen abläuft, auf den Wert von eVar21 (d. h. „hello“).  Der Code setzt dann eVar21 (erneut) auf den Wert des ev21gapv-Cookies.

```js
s.eVar21 = "hello";
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 2

Nehmen wir an, dass eVar21 noch nicht auf der aktuellen Seite gesetzt wurde, aber innerhalb der letzten 28 Tage auf einer vorherigen Seite auf „hello“ gesetzt wurde.   Der folgende Code setzt nur eVar21 auf den Wert des ev21gapv-Cookies (d. h. „hello“).  Das ev21gapv-Cookie wird nicht zurückgesetzt, da eVar21 nicht auf der aktuellen Seite gesetzt wurde, bevor die Funktion aufgerufen wurde.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 3

Nehmen wir an, dass eVar21 noch nicht auf der aktuellen Seite gesetzt wurde, aber innerhalb der letzten 28 Tage auf einer vorherigen Seite auf „hello“ gesetzt wurde.  Der folgende Code setzt nur prop35 auf den Wert des ev21gapv-Cookies (d. h. „hello“).  eVar21 wird nicht gesetzt.

```js
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 4

Der folgende Code setzt eVar21 auf den Wert von „howdy“.  Der Code setzt dann das ev21gapv-Cookie, das in 28 Tagen abläuft, auf den Wert von eVar21 (d. h. „howdy“) (oder setzt es darauf zurück).  Der Code setzt dann prop35 auf den Wert des ev21gapv-Cookies (d. h. „howdy“).

```js
s.eVar21 = "howdy";
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 5

Angenommen, s.eVar21 wurde innerhalb der letzten 28 Tage auf keiner Seite gesetzt.  Der folgende Code setzt s.eVar21 auf null, da das ev21gapv-Cookie 28 Tage nach seinem letzten Setzen abgelaufen wäre.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Beispiel 6

Der folgende Code setzt eVar30 auf „shopping“.  Anschließend wird das Cookie s_gapv gesetzt, das am Ende der Browser-Sitzung abläuft und dem Wert von s.eVar30 entspricht (d. h. „shopping“).  Anschließend wird s.eVar30 auf den Wert des Cookies s_gapv gesetzt (d. h., der getAndPersistValue-Aufruf gibt den Wert des Cookies s_gapv zurück, der in diesem Fall „shopping“ ist).

```js
s.eVar30 = "shopping";
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

Wenn s.eVar30 auf keinen zusätzlichen Seiten, die während der Sitzung angezeigt werden, auf einen expliziten Wert festgelegt wird, sondern (in doPlugins) über den folgenden Code gesetzt wird ...

```js
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

... wird s.eVar30 auf „shopping“ gesetzt (d. h. den beibehaltenen Wert des s_gapv-Cookies)

## Versionsverlauf

### 2.0 (16. April 2018)

* Zwischenversion (kleinere Code-Größe)
* Die Übergabe von „0“ in das `ex`-Argument erzwingt nun den Ablauf nach 30 Minuten Inaktivität und nicht mehr den Ablauf am Ende der Browser-Sitzung.

### 1.0 (18. Januar 2016)

* Erste Version.
