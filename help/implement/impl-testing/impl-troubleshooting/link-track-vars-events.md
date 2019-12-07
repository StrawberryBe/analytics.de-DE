---
description: Für eine erfolgreiche Implementierung der Linktracking ist es unbedingt erforderlich, dass man weiß, wie die Variablen „s.linkTrackVars“ und „s.linkTrackEvents“ funktionieren. Hiermit können benutzerspezifische Variablenwerte bei Benutzeraktionen weitergegeben werden.
keywords: Analytics Implementation
title: Verwendung von „s.linkTrackVars“ und „s.linkTrackEvents“
topic: Developer and implementation
uuid: f6b7019b-987b-4b7d-a446-80205f7cc36c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verwendung von „s.linkTrackVars“ und „s.linkTrackEvents“

Für eine erfolgreiche Implementierung der Linktracking ist es unbedingt erforderlich, dass man weiß, wie die Variablen „s.linkTrackVars“ und „s.linkTrackEvents“ funktionieren. Hiermit können benutzerspezifische Variablenwerte bei Benutzeraktionen weitergegeben werden.

Beim Implementieren von benutzerspezifischem Linktracking und Festlegen [!UICONTROL benutzerspezifischer] Variablen und *`events`* müssen Sie darauf achten, dass die Variable [!UICONTROL s.linkTrackVars] eine kommagetrennte Liste aller Variablen enthält, die weitergegeben werden sollen (inklusive der Variable *`events`*). Vergewissern Sie sich, dass [!UICONTROL s.linkTrackEvents] eine kommagetrennte Liste aller Ereignisse enthält, die weitergegeben werden sollen.

Durch das Setzen von [!UICONTROL s.linkTrackVars] und [!UICONTROL s.linkTrackEvents] werden diese Variablen bzw. Ereignisse nicht tatsächlich festgelegt, sondern nur der [!DNL Analytics]-Code darauf vorbereitet, dies durchzuführen. Sie müssen die Variablen noch manuell festlegen, wie im folgenden Beispiel gezeigt:

```js
<script language="javascript"> 
function customLinks () { 
 var s=s_gi('myreportsuite'); 
 s.linkTrackVars="prop1,eVar7,products,events"; 
 s.linkTrackEvents="event5,event9"; 
 s.prop1="Link Click"; 
 s.eVar7="my_page.html"; 
 s.events="event5"; 
 s.tl(true,'o','Custom Link Click'); 
} 
</script> 
<a href="my_page.html" onclick="customLinks();">My Page</a> 
```

Beachten Sie, dass in der Variablen [!UICONTROL s.linkTrackVars] auch „events“ aufgeführt ist. Die einzelnen Ereignisse, die übergegeben werden, stehen in der Variablen [!UICONTROL s.linkTrackEvents] und später in der Funktion auch in [!UICONTROL s.events]. Alle übergebenen Variablen werden in [!UICONTROL s.linkTrackVars] aufgeführt, bevor sie später in der Funktion aufgefüllt werden. Außerdem wurde „event9“ zwar in [!UICONTROL s.linkTrackEvents], nicht jedoch in [!UICONTROL s.events] eingesetzt. Dieses Ereignis wird nicht aufgezeichnet. Dies wäre jedoch der Fall gewesen, wenn der Benutzer s.events="event5,event9" festgelegt hätte.

Die automatischer Dateidownloads und [!UICONTROL Exitlinktracking] funktionieren auf eine unterschiedliche Weise. Die Variablen [!UICONTROL s.linkTrackVars] und [!UICONTROL s.linkTrackEvents] sind in der Datei [!DNL s_code.js] vorhanden und jeweils auf „none“ eingestellt. Diese Variablen bleiben in der Datei [!DNL s_code.js] für gewöhnlich auf „none“ belassen, damit bei der automatischen Linktracking (anders als bei der [!UICONTROL benutzerspezifischen Linktracking]) die in der globalen JavaScript-Datei festgelegten [!UICONTROL s.linkTrackVars]- und [!UICONTROL s.linkTrackEvents]-Werte verwendet werden. Die vorhandenen Werte dieser Variablen werden, sobald ein Dateidownload oder ein [!UICONTROL Exitlink] aufgezeichnet wird, übergegeben.

Betrachten Sie das Beispiel, bei dem s.channel="Home" ist, wenn die Seite geladen wird, während laut der Datei [!DNL s_code.js] s.linkTrackVars="channel" sein soll. Wenn ein Benutzer klickt, um eine Datei herunterzuladen, gibt die automatische Dateidownload-Verfolgung Daten an [!DNL Analytics] weiter, in denen [!UICONTROL s.channel] den Wert hat, der beim Laden der Seite festgelegt wurde. „Home“ wird ein zweites Mal übergeben, was dazu führt, dass die Anzahl der Seitenansichten für diesen Wert im Bericht [!UICONTROL Sitebereiche] zu hoch angegeben wird.

Adobe empfiehlt ausdrücklich, die Variablen [!UICONTROL s.linkTrackVars] und [!UICONTROL s.linkTrackEvents] in der globalen JavaScript-Datei auf „none“ gesetzt zu belassen und sie (falls erforderlich) beim Implementieren von [!UICONTROL benutzerspezifischer Linktracking] explizit festzulegen.
