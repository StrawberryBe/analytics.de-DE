---
title: getPercentPageViewed
description: Rufen Sie den Prozentsatz der Seite ab, die der Besucher aufgerufen hat.
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
source-git-commit: 633ba0b9a3fe40bfd1b36820949810c631597397
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 98%

---

# Adobe-Plug-in: getPercentPageViewed

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getPercentPageViewed`-Plug-in misst die Bildlaufaktivität eines Besuchers, um festzustellen, wie viel Prozent einer Seite der Benutzer ansieht, bevor er auf eine andere Seite wechselt. Dieses Plug-in ist nicht erforderlich, wenn Ihre Seiten eine geringe Höhe haben oder die Bildlaufaktivität nicht gemessen werden soll.

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
   * Aktionstyp: getPercentPageViewed initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

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
/* Adobe Consulting Plugin: getPercentPageViewed v5.0.1 */
function getPercentPageViewed(pid,ch){var n=pid,r=ch;function p(){if(window.ppvID){var a=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),b=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,d=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+b,f=Math.min(Math.round(d/a*100),100),l=Math.floor(d/b);b=Math.floor(a/b);var c="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||1==window.ppvChange&&window.cookieRead("s_tp")&&a!=window.cookieRead("s_tp")){(decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",d);if(window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");c=window.cookieRead("s_ppv");var h=-1<c.indexOf(",")?c.split(","):[];c=h[0]?h[0]:"";h=h[3]?h[3]:"";var q=window.cookieRead("s_ips");c=c+","+Math.round(h/a*100)+","+Math.round(q/a*100)+","+h+","+l}window.cookieWrite("s_tp",a)}else c=window.cookieRead("s_ppv");var k=c&&-1<c.indexOf(",")?c.split(",",6):[];a=0<k.length?k[0]:encodeURIComponent(window.ppvID);h=1<k.length?parseInt(k[1]):f;q=2<k.length?parseInt(k[2]):f;var t=3<k.length?parseInt(k[3]):d,u=4<k.length?parseInt(k[4]):l;k=5<k.length?parseInt(k[5]):b;0<f&&(c=a+","+(f>h?f:h)+","+q+","+(d>t?d:t)+","+(l>u?l:u)+","+(b>k?b:k));window.cookieWrite("s_ppv",c)}}if("-v"===n)return{plugin:"getPercentPageViewed",version:"5.0.1"};var m=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof m&&(m.contextData.getPercentPageViewed="5.0.1");window.pageName="undefined"!==typeof m&&m.pageName||"";window.cookieWrite=window.cookieWrite||function(a,b,d){if("string"===typeof a){var f=window.location.hostname,l=window.location.hostname.split(".").length-1;if(f&&!/^[0-9.]+$/.test(f)){l=2<l?l:2;var c=f.lastIndexOf(".");if(0<=c){for(;0<=c&&1<l;)c=f.lastIndexOf(".",c-1),l--;c=0<c?f.substring(c):f}}g=c;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var h=new Date;h.setTime(h.getTime()+6E4*d)}else h=d;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+h.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(a)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,d=b.indexOf(" "+a+"="),f=0>d?d:b.indexOf(";",d);return(a=0>d?"":decodeURIComponent(b.substring(d+2+a.length,0>f?b.length:f)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};var e=window.cookieRead("s_ppv");e=-1<e.indexOf(",")?e.split(","):[];n=n?n:window.pageName?window.pageName:document.location.href;e[0]=decodeURIComponent(e[0]);window.ppvChange="undefined"===typeof r||1==r?!0:!1;"undefined"!==typeof m&&m.linkType&&"o"===m.linkType||(window.ppvID&&window.ppvID===n||(window.ppvID=n,window.cookieWrite("s_ppv",""),p()),window.p_fo("s_gppvLoad")&&window.addEventListener&&(window.addEventListener("load",p,!1),window.addEventListener("click",p,!1),window.addEventListener("scroll",p,!1)),this._ppvPreviousPage=e[0]?e[0]:"",this._ppvHighestPercentViewed=e[1]?e[1]:"",this._ppvInitialPercentViewed=e[2]?e[2]:"",this._ppvHighestPixelsSeen=e[3]?e[3]:"",this._ppvFoldsSeen=e[4]?e[4]:"",this._ppvFoldsAvailable=e[5]?e[5]:"")};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPercentPageViewed`-Methode verwendet die folgenden Argumente:

* **`pid`** (optional, Zeichenfolge): Eine seitenbasierte Kennung, die Sie mit den Prozentsätzen korrelieren können, die durch die Messungen des Plug-ins bereitgestellt werden.  Ist standardmäßig die `pageName`-Variable.
* **`ch`** (optional, boolesch): Setzen Sie dies auf `false` (oder `0`), wenn Sie nicht möchten, dass das Plug-in Änderungen berücksichtigt, die nach dem ersten Laden an der Größe einer Seite vorgenommen wurden. Wenn dieses Argument weggelassen wird, wird standardmäßig `true` verwendet. Adobe empfiehlt, dieses Argument in den meisten Fällen wegzulassen.

Der Aufruf dieser Methode gibt nichts zurück. Stattdessen werden die folgenden Variablen festgelegt:

* `s._ppvPreviousPage`: Der Name der vorherigen angezeigten Seite. Abschließende Bildlaufmessungen für die aktuelle Seite sind erst verfügbar, nachdem eine neue Seite geladen wurde.
* `s._ppvHighestPercentViewed`: Der höchste Prozentsatz der vorherigen Seite, die der Besucher angezeigt hat (in der Höhe). Der am weitesten entfernte Punkt, zu dem der Besucher auf der vorherigen Seite gescrollt hat.
* `s._ppvInitialPercentViewed`: Der Prozentsatz der vorherigen Seite, der beim ersten Laden der vorherigen Seite sichtbar war.
* `s._ppvHighestPixelsSeen`: Die höchste Anzahl der insgesamt angesehenen Pixel (in der Höhe), während der Besucher einen Bildlauf auf der vorherigen Seite ausgeführt hat.
* `s._ppvFoldsSeen`: Die höchste Anzahl von „Seitenfalten“, die erreicht wurde, als der Besucher die vorherige Seite nach unten gescrollt hat. Diese Variable enthält die Falte „Seitenanfang“.
* `s._ppvFoldsAvailable`: Die Anzahl der insgesamt verfügbaren „Seitenfalten“, die zum Scrollen auf der vorherigen Seite verfügbar sind.

Weisen Sie eine oder mehrere dieser Variablen eVars zu, um Dimensionsdaten in Berichten anzuzeigen.

Dieses Plug-in erstellt ein Erstanbieter-Cookie mit dem Namen `s_ppv`, das die oben genannten Werte enthält. Es läuft am Ende der Browser-Sitzung ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed + " + | foldsSeen=" + s._ppvFoldsSeen + " | foldsAvailable=" + s._ppvFoldsAvailable;
}
```

* Bestimmt, ob s.pageName festgelegt ist und wenn ja, wird die Funktion getPercentPageViewed vom Code ausgeführt
* Wenn die Funktion „getPercentPageViewed“ ausgeführt wird, erstellt sie die Variablen, die im Abschnitt „Rückgaben“ oben beschrieben sind
* Wenn die „Rückgaben“-Variablen erfolgreich eingestellt wurden:
   * Der Code setzt s.prop1 gleich dem Wert von s._ppvPreviousPage (d. h. dem vorherigen Wert von s.pageName oder der vorherigen Seite).
   * Der Code setzt außerdem s.prop2 gleich dem höchsten angezeigten Prozentsatz der vorherigen Seite und dem anfänglichen angezeigten Prozentsatz der vorherigen Seite, zusammen mit der Anzahl der vom Besucher erreichten Falten und der Anzahl der verfügbaren Falten

**Hinweis**:  Wenn beim ersten Laden eine ganze Seite sichtbar ist, sind sowohl die Dimensionen „Höchster Prozentsatz angezeigt“ als auch „Anfänglicher Prozentsatz angezeigt“ gleich 100 und sowohl die Dimension „Angezeigte Falten“ als auch „Verfügbare Falten“ gleich 1.   Wenn beim ersten Laden eine ganze Seite NICHT sichtbar ist, der Besucher jedoch nie nach unten scrollt, bevor er zur nächsten Seite wechselt, sind sowohl die Dimension „Höchster Prozentsatz angezeigt“ als auch die Dimension „Anfänglicher Prozentsatz angezeigt“ gleich demselben Wert.

### Beispiel 2

Angenommen, s.prop5 wurde so eingestellt, dass anstelle des gesamten Seitennamens ein aggregierter „Seitentyp“ erfasst wird.

Der folgende Code bestimmt, ob s.prop5 eingestellt wurde, und speichert in diesem Fall seinen Wert als „vorherige Seite“, um ihn mit den Dimensionen „Höchster Prozentsatz angezeigt“ und „Anfänglicher Prozentsatz angezeigt“ zu korrelieren.  Der Wert wird weiterhin in der Variablen „s._ppvPreviousPage“ gespeichert, kann jedoch so behandelt werden, als wäre er der vorherige Seitentyp und nicht der vorherige Seitenname.

```js
if(s.prop5) s.getPercentPageViewed(s.prop5);
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}
```

## Versionsverlauf

### 5.0.1 (22. Juni 2021)

* Es wurde ein Problem behoben, bei dem bestimmte Sonderzeichen dazu führten, dass das Plug-in beschädigt wurde.

### 5.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### v4.0 (7. Oktober 2019)

* `s._ppvFoldsSeen`- und `s._ppvFoldsAvailable`-Lösungen hinzugefügt

### v3.01 (13. August 2018)

* Es wurde ein Problem bei Seiten behoben, die mehrere AppMeasurement-Objekte auf einer Seite haben

### v3.0 (13. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe)
* Das Plug-in erstellt jetzt Variablen, die Adobe Analytics-Variablen anstelle von Rückgabewerten zugewiesen werden
