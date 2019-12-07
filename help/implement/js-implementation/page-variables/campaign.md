---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---



# Kampagne

In der Variablen sind die Marketing-Kampagnen angegeben, über die Besucher zu Ihrer Site gelangen. Der Wert wird normalerweise einem Abfragezeichenfolgen-Parameter entnommen.
https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/page-variables/browserheight.html

<!-- 

campaign.xml

 -->

**Parameter**

<table id="table_A35175678B6C4D3D86287199AFBE6803"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>255 Byte </p> </td> 
   <td> <p>v0 </p> </td> 
   <td> <p>„Konversion“ &gt; „Kampagnen“ &gt; „Trackingcode“ </p> </td> 
   <td> <p>"" </p> </td> 
  </tr> 
 </tbody> 
</table>

Jedem Element in einer Marketing-Kampagne muss ein eindeutiger Trackingcode zugeordnet sein. So hat z. B. ein Keyword aus einer kostenpflichtigen Suchmaschinenkampagne den Trackingcode „112233“. Wenn ein Besucher auf das Keyword mit dem Trackingcode „112233“ klickt und auf die zugehörige Website gelangt, wird der Trackingcode in der *`campaign`*-Variablen vermerkt.

Es gibt zwei Möglichkeiten zum Auffüllen der Variable *`campaign`*:

* Das Plug-in [!UICONTROL getQueryParam] aus der JavaScript-Datei ruft einen Abfragezeichenfolgen-Parameter aus der URL ab. Weitere Informationen zum Plug-in [!UICONTROL getQueryParam] finden Sie in [Plug-ins für Implementierungen](/help/implement/js-implementation/plugins/impl-plugins.md).

* Weisen Sie der Variable *`campaign`* im HTML-Code auf der Webseite einen Wert zu.

Bei beiden Methoden zum Füllen der Variable *`campaign`* kann der Traffic der Zurück-Schaltfläche die tatsächliche Anzahl der Clickthroughs eines Kampagnenelements erhöhen.

Beispiel: Ein Besucher gelangt auf Ihre Website, indem er auf einen Keyword aus einer kostenpflichtigen Suchmaschinenkampagne klickt. Wenn der Besucher auf Ihre Landingpage gelangt, enthält die URL einen Abfragezeichenfolgen-Parameter, der den Trackingcode für den Keyword angibt. Anschließend klickt der Besucher auf einen Link zu einer anderen Seite, kehrt dann jedoch wieder auf Ihre Landingpage zurück, indem er auf die Schaltfläche „Zurück“ klickt. Wenn der Besucher zum zweiten Mal auf Ihre Landingpage gelangt, gibt die URL mit dem Abfragezeichenfolgen-Parameter erneut diesen Trackingcode an. Auch dieser zweite Clickthrough wird registriert und führt dann dazu, dass die Clickthrough-Rate fälschlicherweise zu hoch vermerkt wird.

Um diesen Effekt zu vermeiden, empfiehlt Adobe, mithilfe des Plug-ins [!UICONTROL getValOnce] zu erzwingen, dass jeder Kampagnen-Clickthrough nur einmal pro Sitzung gezählt wird. Weitere Informationen zum Plug-in [!UICONTROL getValOnce] finden Sie unter [Plug-ins für Implementierungen](/help/implement/js-implementation/plugins/impl-plugins.md).

**Syntax und mögliche Werte** {#section_91A141841A6D4711A1EE08A6145A301D}

```js
s.campaign="112233"
```

Für die Variable *`campaign`* gelten die gleichen Einschränkungen wie für alle anderen Variablen. Adobe empfiehlt, sich bei Werten für diese Variable auf standardmäßige ASCII-Zeichen zu beschränken.

**Groß-/Kleinschreibung** {#section_112A9A0F886148B6BEF9A7C94BE0A36F}

Bei eVars wird zwischen Groß- und Kleinschreibung unterschieden, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Beispiel: Wenn eVar1 bei der ersten Instanz den Wert „Angemeldet“ enthält, in den darauf folgenden Instanzen jedoch „angemeldet“ heißt, wird in Berichten immer „Angemeldet“ als Wert von eVar angezeigt.

**Beispiele** {#section_705A25D05F6848E29C78320247AECB5F}

```js
s.campaign="112233"
```

```js
s.campaign=s.getQueryParam('cid');
```

**Konfigurationseinstellungen** {#section_4083F281968443169EAF8C0E8529D7BC}

Jeder Kampagnenwert bleibt für einen Benutzer aktiv, und in ihm werden bis zum Ablauf der Variablen alle Aktivitäten und Erfolgsereignisse des zugehörigen Benutzers vermerkt. Den Ablaufzeitpunkt der Kampagnenvariablen können Sie in der Admin Console ändern.

**Probleme, Fragen und Tipps** {#section_94B5C4BF9DE84BA3A16F9E9E9D197F0C}

* Um zu verhindern, dass die Clickthrough-Rate unnötig hochgezählt wird, verwenden Sie das Plug-in [!UICONTROL getValOnce], damit die Clickthrough-Raten für eine Kampagne nur einmal pro Sitzung gezählt werden. Weitere Informationen zum Plug-in [!UICONTROL getValOnce] finden Sie in [Plug-ins für Implementierungen](/help/implement/js-implementation/plugins/impl-plugins.md).

* Weitere Informationen über das Verfolgen von Marketing-Kampagnen und gekauften Keywords finden Sie in [Kampagnen](https://marketing.adobe.com/resources/help/en_US/reference/campaign.html).
* Mit dem [!DNL DigitalPulse Debugger] können Sie ermitteln, wie hoch der tatsächliche Wert von Kampagnen ist („v0“ im Debugger). Wenn „v0“ im Debugger nicht angezeigt wird, bedeutet dies, dass für diese Seite keine Kampagnendaten vermerkt wurden.
