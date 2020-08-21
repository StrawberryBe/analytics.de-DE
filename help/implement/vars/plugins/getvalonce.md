---
title: getValOnce
description: Verhindern Sie, dass eine Analytics-Variable zweimal hintereinander auf denselben Wert gesetzt wird.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '722'
ht-degree: 100%

---


# Adobe-Plug-in: getValOnce

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getValOnce`-Plug-in verhindert, dass eine Variable mehrmals auf denselben Wert gesetzt wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Vorkommnisse deduplizieren möchten, bei denen ein Besucher eine Seite aktualisiert oder eine bestimmte Seite mehrmals besucht. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht an der Metrik „Vorkommnisse“ in Analysis Workspace interessiert sind.

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
   * Aktionstyp: getValOnce initialisieren
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
/* Adobe Consulting Plugin: getValOnce v2.01 */
s.getValOnce=function(vtc,cn,et,ep){if(vtc&&(cn=cn||"s_gvo",et=et||0,ep="m"===ep?6E4:864E5,vtc!==this.c_r(cn))){var e=new Date;e.setTime(e.getTime()+et*ep);this.c_w(cn,vtc,0===et?0:e);return vtc}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getValOnce`-Methode verwendet die folgenden Argumente:

* **`vtc`** (erforderlich, Zeichenfolge): Die Variable, die daraufhin geprüft werden soll, ob sie gerade zuvor auf einen identischen Wert gesetzt wurde
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, das den zu prüfenden Wert enthält. Die Standardeinstellung ist `"s_gvo"`
* **`et`** (optional, Ganzzahl): Der Ablauf des Cookies in Tagen (oder Minuten, je nach dem `ep`-Argument). Die Standardeinstellung ist `0`, die am Ende der Browser-Sitzung abläuft
* **`ep`** (optional, Zeichenfolge): Legen Sie dieses Argument nur fest, wenn das `et`-Argument ebenfalls festgelegt ist. Setzen Sie dieses Argument auf `"m"`, wenn Sie möchten, dass das `et`-Argument in Minuten statt in Tagen abläuft. Die Standardeinstellung ist `"d"`, die das `et`-Argument in Tagen festlegt.

Wenn das `vtc`-Argument und der Cookie-Wert übereinstimmen, gibt diese Methode eine leere Zeichenfolge zurück. Wenn das `vtc`-Argument und der Cookie-Wert nicht übereinstimmen, gibt die Methode das `vtc`-Argument als Zeichenfolge zurück.

## Beispielaufrufe

### Beispiel 1

Verwenden Sie diesen Aufruf, um zu verhindern, dass derselbe Wert für die nächsten 30 Tage mehrmals hintereinander an s.campaign weitergegeben wird:

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

Im obigen Aufruf vergleicht das Plug-in zunächst den bereits im Cookie s_campaign enthaltenen Wert mit dem Wert aus der aktuellen Variablen s.campaign.   Wenn die Werte nicht übereinstimmen, setzt das Plug-in das s_campaign-Cookie auf den neuen Wert von s.campaign und gibt dann den neuen Wert zurück.   Dieser Vergleich wird für die nächsten dreißig Tage durchgeführt.

### Beispiel 2

Mit diesem Aufruf verhindern Sie, dass derselbe Wert während der Sitzung festgelegt wird:

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

Dieser Code verhindert, dass derselbe Wert während der Sitzung eines Benutzers mehrmals hintereinander an s.eVar2 übergeben wird.  Außerdem wird der Wert „m“ im Ausdruck (am Ende des Aufrufs) ignoriert, da die Ablaufzeit auf 0 gesetzt wird.   Der Code speichert auch den Vergleichswert im s_ev2-Cookie.

## Versionsverlauf

### 2.01

* Es wurde ein Problem beim Schreiben von Cookies behoben.

### 2.0

* Zwischenversion (neu kompiliert, kleinere Code-Größe).

### 1.1

* Es wurde die Option hinzugefügt, über den `t`-Parameter Minuten oder Tage für den Ablauf auszuwählen.
* Der Umfang der verwendeten `k`-Variablen wurde korrigiert, um sie auf das Plug-in zu beschränken. Diese Änderung verhindert mögliche Interferenzen mit anderen Code auf der Seite.
