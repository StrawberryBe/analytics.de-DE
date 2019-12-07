---
description: Misst die Bildlaufaktivität eines Besuchers, um festzustellen, wie viel Prozent einer Seite der Benutzer ansieht, bevor er auf eine andere Seite wechselt. Mit diesem Plug-in können Sie ermitteln, wie viel des Inhalts die Benutzer durchschnittlich ansehen, sodass Sie die Seitenlänge und das Seitenlayout entsprechend dem Benutzerverhalten anpassen können.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getPercentPageViewed
topic: Developer and implementation
uuid: 1751dcdb-699f-4bd1-8bcb-5e62fa24896a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getPercentPageViewed

Das Plug-in getPercentPageViewed misst die Bildlaufaktivität eines Besuchers, um zu sehen, wie viel von einer Seite der Besucher angezeigt hat, bevor er zu einer anderen Seite wechselt.

>[!NOTE]
>Sie müssen das getPercentPageViewed-Plugin nicht verwenden, wenn Ihre Webseiten klein sind und Sie nicht messen müssen, wie weit Besucher nach unten blättern. Wenn Sie die Bildlaufaktivität nur auf Ausstiegsseiten messen möchten, können Sie dieses Plug-in nicht verwenden.

## Voraussetzungen

Sie müssen über AppMeasurement und das Hilfedokument handlePPVevents verfügen, um das Plug-in getPercentPageViewed auszuführen.

## Implementierung

Um dieses Plug-in zu implementieren, kopieren Sie den Code und fügen Sie ihn an einer beliebigen Stelle im Abschnitt **[!UICONTROL Plugins]** der [!DNL AppMeasurement]-Datei ein.

>[!NOTE]
>Das Hinzufügen der fett markierten Kommentare/Versionsnummern des Codes zur AppMeasurement-Datei hilft Adobe Consulting bei der Fehlerbehebung potenzieller Implementierungsprobleme.

Sie können die Funktion `getPercentPageViewed` nach Bedarf innerhalb der Funktion doPlugins ausführen (siehe Beispielaufrufe unten).

## Zu übergebende Argumente in

| Argument | Definition |
|---|---|
| pid (optional, Zeichenfolge) | Eine Seitenkennung, die mit den Prozentwerten korreliert, die von den Plug-in-Messungen bereitgestellt werden. Standardmäßig wird die Analytics-Variable „pageName“ verwendet oder die URL, wenn die Variable „pageName“ nicht festgelegt wird |
| ch (optional, Boolescher Wert) | Der empfohlene/Standardwert für dieses Argument ist „true“. Setzen Sie diesen Wert auf „false“, wenn Sie nicht möchten, dass dieses Plug-in Änderungen berücksichtigt, die aufgrund von SPA-Code, dynamischem HTML usw. an der Größe einer Seite nach dem erstmaligen Laden vorgenommen wurden. |

## Rückgabe

Das getPercentPageViewed-Plug-in gibt nichts aus. Stattdessen werden die folgenden Variablen innerhalb des Objekts „AppMeasurement“ eingestellt:

* `s._ppvPreviousPage`: Der Name der vorherigen angezeigten Seite (da endgültige Messungen erst verfügbar sind, wenn eine neue Seite geladen wurde)
* `s._ppvHighestPercentViewed`: Der höchste Prozentsatz der vorherigen Seite, die der Besucher angezeigt hat (im Höhenbereich). Mit anderen Worten, der am weitesten entfernte Punkt, zu dem der Besucher auf der vorherigen Seite gescrollt hat.
* `s._ppvInitialPercentViewed`: Der Prozentsatz der vorherigen Seite, der beim ersten Laden der vorherigen Seite sichtbar war.
* `s._ppvHighestPixelSeen`: Die höchste Anzahl der insgesamt angesehenen Pixel (in der Höhe), während der Besucher einen Bildlauf auf der vorherigen Seite ausgeführt hat.

## Cookies

Das getPercentPageViewed-Plug-in erstellt ein Cookie mit dem Namen `s_ppv`, das von Seite zu Seite weitergegeben wird. Der Inhalt des Cookies enthält die Werte, die in die vier oben beschriebenen Variablen eingefügt wurden und am Ende der Sitzung ablaufen.

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
* Bestimmt, ob s.pageName festgelegt ist und wenn ja, wird die Funktion getPercentPageViewed vom Code ausgeführt.
* Wenn die Funktion `getPercentPageViewed` ausgeführt wird, erstellt sie die Variablen, die im Abschnitt „Ausgaben“ oben beschrieben sind.
* Wenn die Variablen „Ausgaben“ erfolgreich eingestellt wurden:

   * Der Code setzt s.prop1 gleich dem Wert von `s._ppvPreviousPag`e (d. h. dem vorherigen Wert von `s.pageName` oder der vorherigen Seite).
   * Der Code setzt s.prop2 auch gleich dem höchsten angezeigten Prozentsatz der vorherigen Seite und dem anfänglichen Prozentsatz der vorherigen Seite.

>[!NOTE]
>Wenn beim ersten Laden eine ganze Seite sichtbar ist, entsprechen sowohl die Dimensionen „Höchster Prozentsatz“ als auch „Anfänglicher Prozentsatz“ dem Wert 100. Wenn jedoch beim ersten Laden eine ganze Seite nicht sichtbar ist, der Besucher jedoch nie nach unten scrollt, bevor er zur nächsten Seite wechselt, sind sowohl die Dimensionen „Höchster Prozentsatz“ als auch „Anfänglicher Prozentsatz“ gleich demselben Wert.

**Beispielaufruf 2**

Angenommen, s.prop5 wurde so eingestellt, dass anstelle des gesamten Seitennamens ein aggregierter „Seitentyp“ erfasst wird.

Der folgende Code bestimmt, ob s.prop5 eingestellt wurde, und speichert in diesem Fall seinen Wert als „vorherige Seite“, um ihn mit den Dimensionen „Höchster angezeigter Prozentsatz“ und „Anfänglicher Prozentsatz“ zu korrelieren. Der Wert wird weiterhin in der `s._ppvPreviousPage`-Variable gespeichert, kann jedoch so behandelt werden, als wäre er der vorherige Seitentyp und nicht der vorherige Seitenname.

```
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}  
```

## S-Objektaustausch

Ändern Sie bei der Instanziierung des AppMeasurement-Hauptbibliotheksobjekts mit einem anderen Namen als „s“ den folgenden Teil des Plug-in-Codes von:

`s.getPercentPageViewed=function(pid,ch)`

wie folgt:

`[objectname].getPercentPageViewed=function(pid,ch)`

## Bereitzustellender Code

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
