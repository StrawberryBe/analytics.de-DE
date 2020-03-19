---
title: getPercentPageViewed
description: Rufen Sie den Prozentsatz der Seite ab, die der Besucher angezeigt hat.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getPercentPageViewed

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

The `getPercentPageViewed` plug-in measures a visitor&#39;s scroll activity to see how much of a page they view before moving on to another page. Dieses Plug-in ist nicht erforderlich, wenn Ihre Seiten klein sind oder die Aktivität des Bildlaufs nicht gemessen werden soll.

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
/* Adobe Consulting Plugin: getPercentPageViewed v4.0 w/handlePPVevents helper function (Requires p_fo plug-in) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange="undefined"===typeof ch||!0==ch?!0:!1;if("undefined"=== typeof s.linkType||"o"!==s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()), s.p_fo("s_gppvLoad") &&window.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1)),s._ppvPreviousPage=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:"",s._ppvFoldsSeen=a[4]?a[4]:"",s._ppvFoldsAvailable=a[5]?a[5]:""};

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v4.0 Plugin) */
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,g=s_c_il.length;c<g;c++)if(s_c_il[c]&& (s_c_il[c].getPercentPageViewed||s_c_il[c].getPreviousPageActivity)){var s=s_c_il[c];break}if(s&&s.ppvID){var f=Math.max (Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight, document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),h= window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight;c=(window.pageYOffset|| window.document.documentElement.scrollTop||window.document.body.scrollTop)+h;g=Math.min(Math.round(c/f*100),100);var k=Math.floor(c/h);h=Math.floor(f/h);var d="";if(!s.c_r("s_tp")||s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID) ||1==s.ppvChange&&s.c_r("s_tp")&&f!=s.c_r("s_tp")){(s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID+"1"))&&s.c_w("s_ips",c);if(s.c_r("s_tp")&&s.unescape(s.c_r("s_ppv").split(",")[0])===s.ppvID){s.c_r("s_tp");d=s.c_r("s_ppv");var e=-1< d.indexOf(",")?d.split(","):[];d=e[0]?e[0]:"";e=e[3]?e[3]:"";var l=s.c_r("s_ips");d=d+","+Math.round(e/f*100)+","+Math.round(l/ f*100)+","+e+","+k}s.c_w("s_tp",f)}else d=s.c_r("s_ppv");var b=d&&-1<d.indexOf(",")?d.split(",",6):[];f=0<b.length?b[0]: escape(s.ppvID);e=1<b.length?parseInt(b[1]):g;l=2<b.length?parseInt(b[2]):g;var m=3<b.length?parseInt(b[3]):c,n=4<b.length? parseInt(b[4]):k;b=5<b.length?parseInt(b[5]):h;0<g&&(d=f+","+(g>e?g:e)+","+l+","+(c>m?c:m)+","+(k>n?k:n)+","+(h>b?h:b)); s.c_w("s_ppv",d)}}};

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getPercentPageViewed` Methode verwendet die folgenden Argumente:

* **`pid`** (optional, Zeichenfolge):  Ein seitenbasierter Identifikator, den Sie mit den Prozentsätzen korrelieren können, die durch die Messungen des Plug-Ins bereitgestellt werden.  Die Standardeinstellung ist die `pageName` Variable.
* **`ch`** (optional, boolean):  Setzen Sie dies auf `false` (oder `0`), wenn Sie nicht möchten, dass das Plug-In Änderungen berücksichtigt, die nach dem ersten Laden an der Größe einer Seite vorgenommen wurden. Wenn dieses Argument weggelassen wird, wird standardmäßig `true`verwendet. Adobe empfiehlt, dieses Argument in den meisten Fällen wegzulassen.

Der Aufruf dieser Methode gibt nichts zurück. Stattdessen werden die folgenden Variablen festgelegt:

* `s._ppvPreviousPage`: Der Name der vorherigen angezeigten Seite. Abschließende Bildlaufmessungen für die aktuelle Seite sind erst verfügbar, nachdem eine neue Seite geladen wurde.
* `s._ppvHighestPercentViewed`: Der höchste Prozentsatz der vorherigen Seite, die der Besucher angezeigt hat (im Höhenbereich). Der am weitesten entfernte Punkt, zu dem der Besucher auf der vorherigen Seite einen Bildlauf durchgeführt hat.
* `s._ppvInitialPercentViewed`: Der Prozentsatz der vorherigen Seite, der beim ersten Laden der vorherigen Seite angezeigt wurde.
* `s._ppvHighestPixelsSeen`: Die höchste Anzahl der insgesamt angesehenen Pixel (in der Höhe), während der Besucher einen Bildlauf auf der vorherigen Seite ausgeführt hat.
* `s._ppvFoldsSeen`: Die höchste Anzahl an &quot;Seitenfalten&quot;wurde erreicht, als der Besucher auf der vorherigen Seite einen Bildlauf nach unten durchlief. Diese Variable enthält den &quot;Anfang der Seite&quot;.
* `s._ppvFoldsAvailable`: Die Anzahl der insgesamt verfügbaren &quot;Seitenfalts&quot;, die auf der vorherigen Seite nach unten durchlaufen werden können.

Weisen Sie eine oder mehrere dieser Variablen eVars zu, um Dimensionsdaten in Berichten anzuzeigen.

Dieses Plug-In erstellt ein Erstanbieter-Cookie mit dem Namen `s_ppv` , das die oben genannten Werte enthält. Er läuft am Ende der Browsersitzung ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed + " + | foldsSeen=" + s._ppvFoldsSeen + " | foldsAvailable=" + s._ppvFoldsAvailable;
}
```

* Bestimmt, ob s.pageName festgelegt ist und wenn ja, wird die Funktion getPercentPageViewed vom Code ausgeführt
* Wenn die Funktion getPercentPageViewed ausgeführt wird, erstellt sie die Variablen, die oben im Abschnitt &quot;Rückgaben&quot;beschrieben werden
* Wenn die Variablen &quot;Rückgaben&quot;erfolgreich eingestellt wurden:
   * Der Code setzt s.prop1 gleich dem Wert von s._ppvPreviousPage (d. h. dem vorherigen Wert von s.pageName oder der vorherigen Seite)
   * Der Code legt außerdem s.prop2 so fest, dass er dem höchsten Prozentsatz der vorherigen Seite und dem ersten Prozent der vorherigen Seite entspricht, zusammen mit der Anzahl der Ordner, die der Besucher erreicht hat, und der Anzahl der verfügbaren Falten

**Hinweis**:  Wenn beim ersten Laden eine ganze Seite sichtbar ist, sind sowohl die Dimensionen &quot;Höchster Prozentsatz angezeigt&quot;als auch &quot;Anfänglicher Prozentsatz angezeigt&quot;gleich 100 und sowohl die Dimensionen &quot;Angezeigte Ordner&quot;als auch &quot;Verfügbare Ordner&quot;gleich 1.   Wenn eine ganze Seite beim ersten Laden NICHT sichtbar ist, der Besucher jedoch nie nach unten scrollt, bevor er zur nächsten Seite wechselt, dann sind sowohl die Dimensionen &quot;Höchster Prozent angezeigt&quot;als auch &quot;Anfänglicher Prozentsatz angezeigt&quot;gleich demselben Wert.

### Beispiel 2

Angenommen, s.prop5 wurde so eingestellt, dass anstelle des gesamten Seitennamens ein aggregierter „Seitentyp“ erfasst wird.

Der folgende Code bestimmt, ob s.prop5 eingestellt wurde. Wenn ja, speichert er seinen Wert als &quot;vorherige Seite&quot;, um ihn mit den Dimensionen &quot;Höchster angezeigter Prozentsatz&quot;und &quot;Anfänglicher Prozentsatz angezeigt&quot;zu korrelieren.  Der Wert wird weiterhin in der Variablen s._ppvPreviousPage gespeichert, kann jedoch so behandelt werden, als wäre er der vorherige Seitentyp und nicht der vorherige Seitenname.

```js
if(s.prop5) s.getPercentPageViewed(s.prop5);
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}
```

## Versionsverlauf

### v4.0 (7. Oktober 2019)

* Hinzugefügte `s._ppvFoldsSeen` und `s._ppvFoldsAvailable` Lösungen

### v3.01 (13. August 2018)

* Es wurde ein Problem bei Seiten behoben, die mehrere AppMeasurement-Objekte auf einer Seite haben

### v3.0 (13. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße)
* Plug-in erstellt jetzt Variablen, die Adobe Analytics-Variablen anstelle von Rückgabewerten zugewiesen werden sollen
