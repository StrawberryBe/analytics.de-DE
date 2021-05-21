---
title: getPercentPageViewed
description: Rufen Sie den Prozentsatz der Seite ab, die der Besucher aufgerufen hat.
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '892'
ht-degree: 100%

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
/* Adobe Consulting Plugin: getPercentPageViewed v5.0 w/handlePPVevents helper function (Requires AppMeasurement and the p_fo plugin) */
function getPercentPageViewed(pid,ch){var l=pid,p=ch;function m(){if(window.ppvID){var c=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),b=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,k=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+b,a=Math.min(Math.round(k/c*100),100),n=Math.floor(k/b);b=Math.floor(c/b);var d="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||1==window.ppvChange&&window.cookieRead("s_tp")&&c!=window.cookieRead("s_tp")){(decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",k);if(window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");d=window.cookieRead("s_ppv");var f=-1<d.indexOf(",")?d.split(","):[];d=f[0]?f[0]:"";f=f[3]?f[3]:"";var e=window.cookieRead("s_ips");d=d+","+Math.round(f/c*100)+","+Math.round(e/c*100)+","+f+","+n}window.cookieWrite("s_tp",c)}else d=window.cookieRead("s_ppv");var h=d&&-1<d.indexOf(",")?d.split(",",6):[];c=0<h.length?h[0]:escape(window.ppvID);f=1<h.length?parseInt(h[1]):a;e=2<h.length?parseInt(h[2]):a;var l=3<h.length?parseInt(h[3]):k,m=4<h.length?parseInt(h[4]):n;h=5<h.length?parseInt(h[5]):b;0<a&&(d=c+","+(a>f?a:f)+","+e+","+(k>l?k:l)+","+(n>m?n:m)+","+(b>h?b:h));window.cookieWrite("s_ppv",d)}}if("-v"===l)return{plugin:"getPercentPageViewed",version:"5.0"};var e=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof e&&(e.contextData.getPercentPageViewed="5.0");window.pageName="undefined"!==typeof e&&e.pageName||"";window.cookieWrite=window.cookieWrite||function(c,b,a){if("string"===typeof c){var k=window.location.hostname,e=window.location.hostname.split(".").length-1;if(k&&!/^[0-9.]+$/.test(k)){e=2<e?e:2;var d=k.lastIndexOf(".");if(0<=d){for(;0<=d&&1<e;)d=k.lastIndexOf(".",d-1),e--;d=0<d?k.substring(d):k}}g=d;b="undefined"!==typeof b?""+b:"";if(a||""===b)if(""===b&&(a=-60),"number"===typeof a){var f=new Date;f.setTime(f.getTime()+6E4*a)}else f=a;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(a?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,c=b.indexOf(" "+a+"="),e=0>c?c:b.indexOf(";",c);return(a=0>c?"":decodeURIComponent(b.substring(c+2+a.length,0>e?b.length:e)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};var a=window.cookieRead("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];l=l?l:window.pageName?window.pageName:document.location.href;a[0]=decodeURIComponent(a[0]);window.ppvChange="undefined"===typeof p||1==p?!0:!1;"undefined"!==typeof e&&e.linkType&&"o"===e.linkType||(window.ppvID&&window.ppvID===l||(window.ppvID=l,window.cookieWrite("s_ppv",""),m()),window.p_fo("s_gppvLoad")&&window.addEventListener&&(window.addEventListener("load",m,!1),window.addEventListener("click",m,!1),window.addEventListener("scroll",m,!1)),window._ppvPreviousPage=a[0]?a[0]:"",window._ppvHighestPercentViewed=a[1]?a[1]:"",window._ppvInitialPercentViewed=a[2]?a[2]:"",window._ppvHighestPixelsSeen=a[3]?a[3]:"",window._ppvFoldsSeen=a[4]?a[4]:"",window._ppvFoldsAvailable=a[5]?a[5]:"")};
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

### 5.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### v4.0 (7. Oktober 2019)

* `s._ppvFoldsSeen`- und `s._ppvFoldsAvailable`-Lösungen hinzugefügt

### v3.01 (13. August 2018)

* Es wurde ein Problem bei Seiten behoben, die mehrere AppMeasurement-Objekte auf einer Seite haben

### v3.0 (13. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe)
* Das Plug-in erstellt jetzt Variablen, die Adobe Analytics-Variablen anstelle von Rückgabewerten zugewiesen werden
