---
title: getPercentPageViewed
description: Rufen Sie den Prozentsatz der Seite ab, die der Besucher aufgerufen hat.
translation-type: ht
source-git-commit: 69c1daa9dbf3bbf39072cc7104f2dd32fb95eb79
workflow-type: ht
source-wordcount: '781'
ht-degree: 100%

---


# Adobe-Plug-in: getPercentPageViewed

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getPercentPageViewed`-Plug-in misst die Bildlaufaktivität eines Besuchers, um festzustellen, wie viel Prozent einer Seite der Benutzer ansieht, bevor er auf eine andere Seite wechselt. Dieses Plug-in ist nicht erforderlich, wenn Ihre Seiten eine geringe Höhe haben oder die Bildlaufaktivität nicht gemessen werden soll.

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
/* Adobe Consulting Plugin: getPercentPageViewed v4.0 w/handlePPVevents helper function (Requires p_fo plug-in) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange="undefined"===typeof ch||!0==ch?!0:!1;if("undefined"=== typeof s.linkType||"o"!==s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()), s.p_fo("s_gppvLoad") &&window.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1)),s._ppvPreviousPage=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:"",s._ppvFoldsSeen=a[4]?a[4]:"",s._ppvFoldsAvailable=a[5]?a[5]:""};

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v4.0 Plugin) */
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,g=s_c_il.length;c<g;c++)if(s_c_il[c]&& (s_c_il[c].getPercentPageViewed||s_c_il[c].getPreviousPageActivity)){var s=s_c_il[c];break}if(s&&s.ppvID){var f=Math.max (Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight, document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),h= window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight;c=(window.pageYOffset|| window.document.documentElement.scrollTop||window.document.body.scrollTop)+h;g=Math.min(Math.round(c/f*100),100);var k=Math.floor(c/h);h=Math.floor(f/h);var d="";if(!s.c_r("s_tp")||s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID) ||1==s.ppvChange&&s.c_r("s_tp")&&f!=s.c_r("s_tp")){(s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID+"1"))&&s.c_w("s_ips",c);if(s.c_r("s_tp")&&s.unescape(s.c_r("s_ppv").split(",")[0])===s.ppvID){s.c_r("s_tp");d=s.c_r("s_ppv");var e=-1< d.indexOf(",")?d.split(","):[];d=e[0]?e[0]:"";e=e[3]?e[3]:"";var l=s.c_r("s_ips");d=d+","+Math.round(e/f*100)+","+Math.round(l/ f*100)+","+e+","+k}s.c_w("s_tp",f)}else d=s.c_r("s_ppv");var b=d&&-1<d.indexOf(",")?d.split(",",6):[];f=0<b.length?b[0]: escape(s.ppvID);e=1<b.length?parseInt(b[1]):g;l=2<b.length?parseInt(b[2]):g;var m=3<b.length?parseInt(b[3]):c,n=4<b.length? parseInt(b[4]):k;b=5<b.length?parseInt(b[5]):h;0<g&&(d=f+","+(g>e?g:e)+","+l+","+(c>m?c:m)+","+(k>n?k:n)+","+(h>b?h:b)); s.c_w("s_ppv",d)}}};

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
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

### v4.0 (7. Oktober 2019)

* `s._ppvFoldsSeen`- und `s._ppvFoldsAvailable`-Lösungen hinzugefügt

### v3.01 (13. August 2018)

* Es wurde ein Problem bei Seiten behoben, die mehrere AppMeasurement-Objekte auf einer Seite haben

### v3.0 (13. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe)
* Das Plug-in erstellt jetzt Variablen, die Adobe Analytics-Variablen anstelle von Rückgabewerten zugewiesen werden
