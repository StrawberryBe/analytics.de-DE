---
description: Misst die Bildlaufaktivität eines Besuchers, um festzustellen, wie viel Prozent einer Seite der Benutzer ansieht, bevor er auf eine andere Seite wechselt. Mit diesem Plug-in können Sie ermitteln, wie viel des Inhalts die Benutzer durchschnittlich ansehen, sodass Sie die Seitenlänge und das Seitenlayout entsprechend dem Benutzerverhalten anpassen können.
keywords: Analytics-Implementierung
seo-description: Misst die Bildlaufaktivität eines Besuchers, um festzustellen, wie viel Prozent einer Seite der Benutzer ansieht, bevor er auf eine andere Seite wechselt. Mit diesem Plug-in können Sie ermitteln, wie viel des Inhalts die Benutzer durchschnittlich ansehen, sodass Sie die Seitenlänge und das Seitenlayout entsprechend dem Benutzerverhalten anpassen können.
seo-title: getPercentPageViewed
solution: Analytics
subtopic: Plug-ins
title: getPercentPageViewed
topic: Entwickler und Implementierung
uuid: 1751 dcdb -699 f -4 bd 1-8 bcb -5 e 62 fa 24896 a
translation-type: tm+mt
source-git-commit: f9912a0da5930be965e4d249f3d2c1891cfd6ed6

---


# getPercentPageViewed

Das getpercentpageviewed-Plugin misst die Bildlaufaktivität eines Besuchers, um zu sehen, wie viel einer Seite der Besucher aufgerufen hat, bevor er zu einer anderen Seite wechselt.

>[!NOTE]
>Sie müssen das Plugin getpercentpageviewed nicht verwenden, wenn Ihre Webseiten in der Höhe kleiner sind und nicht gemessen werden muss, wie weit Besucher nach unten blättern. Wenn Sie die Bildlaufaktivität nur auf Ausstiegsseiten messen möchten, können Sie dieses Plug-in nicht verwenden.

## Voraussetzungen

Sie müssen über appmeasurement und das helleppvevents Helper-Plugin verfügen, um das Plugin getpercentpageviewed auszuführen.

## Implementierung

To implement this plugin, copy and paste the code to anywhere within the **[!UICONTROL Plugins]** section of the [!DNL AppMeasurement] file.

>[!NOTE]
>Die fett hervorgehobene Kommentare/Versionsnummer des Codes zur appmeasurement-Datei hilft Adobe Consulting bei der Fehlerbehebung potenzieller Implementierungsprobleme.

You can run the `getPercentPageViewed` function as needed within the doPlugins function (see example calls below.)

## Zu übergebende Argumente

| Argument | Definition |
|---|---|
| pid (optional, Zeichenfolge) | Eine Seitenkennung, die mit den von den Plugin-Messungen bereitgestellten Prozentwerten korreliert wird. Standardmäßig wird die Variable "Analytics pagename" oder die URL verwendet, wenn die Variable" pagename" nicht eingestellt ist. |
| ch (optional, Boolescher Wert) | " True" ist der empfohlene/standardwert für dieses Argument. Setzen Sie dieses Plug-plugin auf "false" , wenn Sie nach dem ersten Laden aufgrund von SPA-Code, dynamischem HTML usw. nach dem ersten Laden keine Änderungen an der Größe einer Seite berücksichtigen möchten. |

## Rückgabe

Das getpercentpageviewed-Plugin gibt nichts zurück. Stattdessen werden die folgenden Variablen innerhalb des Objekts „AppMeasurement“ eingestellt:

* `s._ppvPreviousPage`: Der Name der vorherigen angezeigten Seite (da die endgültigen Messungen erst verfügbar sind, wenn eine neue Seite geladen wird).
* `s._ppvHighestPercentViewed`: Der höchste Prozentsatz der vorherigen Seite, die der Besucher angezeigt hat (Höhe: weich). Das heißt, der weiteste Punkt, den der Besucher auf der vorherigen Seite heruntergefahren hat.
* `s._ppvInitialPercentViewed`: Der Prozentsatz der vorherigen Seite, die beim ersten Laden der vorherigen Seite angezeigt wurde.
* `s._ppvHighestPixelSeen`: Die höchste Anzahl der insgesamt angezeigten Pixel (Höhe), als der Besucher die vorherige Seite durchlief.

## Cookies

The getPercentPageViewed plugin creates a cookie, called `s_ppv`, that is passed from page to page. Der Inhalt des Cookies enthält die Werte, die in den vier oben beschriebenen Variablen eingegeben wurden und am Ende der Sitzung ablaufen.

## Beispielaufrufe

**Beispielaufruf 1**

```
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + "initialPercentViewed="s._ppvInitialPercentViewed;
}  
```

Das obige Codebeispiel:
* Bestimmt, ob s. pagename festgelegt ist, und falls ja, wird der Code die getpercentpageviewed-Funktion ausgeführt.
* When the `getPercentPageViewed` function runs, it creates the variables described in the "Returns" section above.
* Wenn die Variablen "Gibt" erfolgreich festgelegt wurden:

   * The code sets s.prop1 equal to the value of `s._ppvPreviousPag`e (i.e. the previous value of `s.pageName`, or the previous page.)
   * Der Code legt s. prop 2 gleich dem höchsten Prozentsatz der vorherigen Seite und dem anfänglichen Prozentsatz der vorherigen Seite fest.

>[!NOTE]
>Wenn beim ersten Laden eine ganze Seite sichtbar ist, entsprechen die Dimensionen "Höchste Prozentwerte" und" Anfänglich angezeigte Prozentwerte" 100. Wenn eine ganze Seite beim ersten Laden nicht sichtbar ist, der Besucher jedoch nie die Seite nach unten blättert, bevor sie zur nächsten Seite wechselt, dann wäre sowohl der höchste angezeigte Prozentsatz als auch die Dimensionen anfänglich angezeigte Prozentwerte gleich dem gleichen Wert.

**Beispielaufruf 2**

Angenommen, s. prop 5 wurde zur Erfassung eines aggregierten Seitentyps anstelle des gesamten Seitennamens eingestellt.

Der folgende Code bestimmt, ob s. prop 5 eingestellt wurde, und speichert, falls ja, seinen Wert als "vorherige Seite" , um mit dem höchsten Prozentsatz und den Dimensionen für die anfängliche Prozentanzeige korreliert zu werden. The value is still stored in the `s._ppvPreviousPage` variable but can be treated as if it were the previous page type instead of the previous page name.

```
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}  
```

## S-Objektersetzung

Ändern Sie beim Instanziieren des Haupt-appmeasurement-Bibliotheksobjekts mit einem anderen Namen als "s" den folgenden Teil des Plugin-Codes:

`s.getPercentPageViewed=function(pid,ch)`

dazu:

`[objectname].getPercentPageViewed=function(pid,ch)`

## Bereitzustellende Code

Plug-in-Abschnitt: Fügen Sie in der Datei `s_code.js` den folgenden Code im Abschnitt PLUGINS SECTION hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```
/******************************************* BEGIN CODE TO DEPLOY *******************************************/ 
/* Adobe Consulting Plugin: getPercentPageViewed v3.01 w/handlePPVevents helper function (Requires AppMeasurement and p_fo plugin) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); 
pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange=ch?ch:!0;if("undefined"===typeof s.linkType||"o"!==
s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()),s.p_fo("s_gppvLoad")&&window
.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1),window.addEventListener("resize",s.handlePPVevents,!1)),s._ppvPreviousPage
=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:""}; 

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v3.01 Plugin) */ 
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,d=s_c_il.length;c<d;c++)if(s_c_il[c]&&s_c_il[c].getPercentPageViewed){var a=s_c_il[c];break}if(a&&a.ppvID){var f=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.
body.clientHeight,document.documentElement.clientHeight));c=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight);d=Math.min(Math.round
(c/f*100),100);var e="";!a.c_r("s_tp")||a.unescape(a.c_r("s_ppv").split(",")[0])!==a.ppvID||1==a.ppvChange&&
a.c_r("s_tp")&&f!= a.c_r("s_tp")?(a.c_w("s_tp",f),a.c_w("s_ppv","")):e=a.c_r("s_ppv");var b=e&&-1<e.indexOf(",")?e.split(",",4):[];f=0<b.length?b[0]:escape(a.ppvID);var g=1<b.length?parseInt(b[1]):d,h=2<b.length?parseInt(b[2]):d;b=3<b.length?parseInt(b[3]):c;0<d&&(e=f+","+(d>g?d:g)+","+h+","+(c>b?c:b));a.c_w("s_ppv",e)}}}; 

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 (Requires AppMeasurement) */ 
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0}; 
/******************************************** END CODE TO DEPLOY ********************************************/
```
