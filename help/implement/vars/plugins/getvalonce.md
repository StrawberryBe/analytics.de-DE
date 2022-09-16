---
title: getValOnce
description: Verhindern Sie, dass eine Analytics-Variable zweimal hintereinander auf denselben Wert gesetzt wird.
feature: Variables
exl-id: 23bc5750-43a2-4693-8fe4-d6b31bc34154
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 97%

---

# Adobe-Plug-in: getValOnce

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getValOnce`-Plug-in verhindert, dass eine Variable mehrmals auf denselben Wert gesetzt wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Vorkommnisse deduplizieren möchten, bei denen ein Besucher eine Seite aktualisiert oder eine bestimmte Seite mehrmals besucht. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht an der Metrik „Vorkommnisse“ in Analysis Workspace interessiert sind.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize getValOnce
1. Save and publish the changes to the rule.-->

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getValOnce v3.0 (Requires AppMeasurement) */
function getValOnce(vtc,cn,et,ep){var e=vtc,k=cn,l=et,m=ep;if(arguments&&"-v"===arguments[0])return{plugin:"getValOnce",version:"3.0"};var c=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,a;b<window.s_c_il.length;b++)if(a=window.s_c_il[b],a._c&&"s_c"===a._c)return a}();"undefined"!==typeof c&&(c.contextData.getValOnce="3.0");window.cookieWrite=window.cookieWrite||function(b,a,d){if("string"===typeof b){var h=window.location.hostname,c=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){c=2<c?
c:2;var f=h.lastIndexOf(".");if(0<=f){for(;0<=f&&1<c;)f=h.lastIndexOf(".",f-1),c--;f=0<f?h.substring(f):h}}g=f;a="undefined"!==typeof a?""+a:"";if(d||""===a)if(""===a&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return b&&(document.cookie=encodeURIComponent(b)+"="+encodeURIComponent(a)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(b)===a:!1}};window.cookieRead=window.cookieRead||function(b){if("string"===
typeof b)b=encodeURIComponent(b);else return"";var a=" "+document.cookie,d=a.indexOf(" "+b+"="),c=0>d?d:a.indexOf(";",d);return(b=0>d?"":decodeURIComponent(a.substring(d+2+b.length,0>c?a.length:c)))?b:""};return e&&(k=k||"s_gvo",l=l||0,m="m"===m?6E4:864E5,e!==this.c_r(k))?(c=new Date,c.setTime(c.getTime()+l*m),cookieWrite(k,e,0===l?0:m),e):""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getValOnce`-Funktion verwendet die folgenden Argumente:

* **`vtc`** (erforderlich, Zeichenfolge): Die Variable, die daraufhin geprüft werden soll, ob sie gerade zuvor auf einen identischen Wert gesetzt wurde
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, das den zu prüfenden Wert enthält. Die Standardeinstellung ist `"s_gvo"`
* **`et`** (optional, Ganzzahl): Der Ablauf des Cookies in Tagen (oder Minuten, je nach dem `ep`-Argument). Die Standardeinstellung ist `0`, die am Ende der Browser-Sitzung abläuft
* **`ep`** (optional, Zeichenfolge): Legen Sie dieses Argument nur fest, wenn das `et`-Argument ebenfalls festgelegt ist. Setzen Sie dieses Argument auf `"m"`, wenn Sie möchten, dass das `et`-Argument in Minuten statt in Tagen abläuft. Die Standardeinstellung ist `"d"`, die das `et`-Argument in Tagen festlegt.

Wenn das Argument `vtc` und der Cookie-Wert übereinstimmen, gibt diese Funktion eine leere Zeichenfolge zurück. Wenn das Argument `vtc` und der Cookie-Wert nicht übereinstimmen, gibt die Funktion das Argument `vtc` als Zeichenfolge zurück.

## Beispiele

```js
// Prevent the same value from being passed in to the campaign variable more than once in a row for next 30 days
s.campaign = getValOnce(s.campaign,"s_campaign",30);

// Prevent the same value from being passed in to eVar2 more than once in a row for the browser session
s.eVar2 = getValOnce(s.eVar2,"s_ev2");

// Prevent the same value from being passed in to eVar8 more than once in a row for 10 minutes
s.eVar8 = getValOnce(s.eVar8,"s_ev8",10,"m");
```

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.01

* Es wurde ein Problem beim Schreiben von Cookies behoben.

### 2.0

* Zwischenversion (neu kompiliert, kleinere Code-Größe).

### 1.1

* Es wurde die Option hinzugefügt, über den `t`-Parameter Minuten oder Tage für den Ablauf auszuwählen.
* Der Umfang der verwendeten `k`-Variablen wurde korrigiert, um sie auf das Plug-in zu beschränken. Diese Änderung verhindert mögliche Interferenzen mit anderen Code auf der Seite.
