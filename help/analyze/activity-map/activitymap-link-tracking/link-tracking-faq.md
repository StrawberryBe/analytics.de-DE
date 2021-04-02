---
description: Häufig gestellte Fragen zum Linktracking in Activity Map.
title: Linktracking – Häufig gestellte Fragen
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: f9d9c7dbaf5fde5bd51c929d927d4cd3f61cb63b
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 65%

---


# Linktracking – Häufig gestellte Fragen

Häufig gestellte Fragen zum Linktracking in Activity Map.

>[!CAUTION]
>
>Beim Aktivieren von Activity Map-Tracking **erfassen Sie möglicherweise persönlich identifizierbare Informationen (PII)**. Diese Daten können alleine oder in Verbindung mit anderen Informationen dazu verwendet werden, eine Einzelperson zu identifizieren, zu kontaktieren oder zu lokalisieren oder eine Einzelperson im Kontext zu identifizieren.

Im Folgenden finden Sie einige Fälle, in denen PII-Daten möglicherweise mit dem Activity Map-Tracking gesammelt werden:

* `Mailto`-Links. Ein Mailto-Link ist ein HTML-Linktyp, der den standardmäßigen E-Mail-Client auf dem Computer für das Senden einer E-Mail aktiviert.
* `User ID`-Links, die in der Kopf-/Fußzeile einer Website angezeigt werden, nachdem sich der Benutzer angemeldet hat.
* Für Kreditinstitute wird möglicherweise die Kontonummer als ein Link angezeigt. Wenn darauf geklickt wird, wird der Linktext erfasst.
* Auf Websites für das Gesundheitswesen werden PII-Daten ebenfalls als Links angezeigt. Durch Klicken auf diese Links wird der Linktext erfasst. Dadurch werden die PII-Daten gesammelt.

<table id="table_0951EAC617344156BAE43000CCD838AF">
 <tbody>
  <tr>
   <td colname="col1"> <b>F: Wann ist Linktracking aktiv?</b> </td>
   <td colname="col2"> A: Sobald ein Benutzer auf eine Seite klickt, identifiziert Activity Map den Link und die Region. </td>
  </tr>
  <tr>
   <td colname="col1"> <b>F: Was wird standardmäßig verfolgt?</b> </td>
   <td colname="col2"> A: Wenn auf ein Element geklickt wird, durchläuft es mehrere Prüfungen, um zu bestimmen, ob es von AppMeasurement als Link behandelt wird. Die Prüfungen sind:
    <ul id="ul_81B9A5A7F8534E71AEF68F2199A154F0">
     <li id="li_49F6DDD9DC124AE5846EC5B7D7BEA20E">Ist dies ein <code>&lt;A&gt;</code>- oder <code>&lt;AREA&gt;</code>-Tag mit einer <code>"href"</code>-Eigenschaft? </li>
     <li id="li_77828D24D54343E5B9A1FF7345221781">Gibt es ein <code>"onclick"</code>-Attribut, das eine <code>s_objectID</code>-Variable festlegt? </li>
     <li id="li_D4B0AEEEA58A4F82A1BCBD3971A60D02">Ist dies ein <code>&lt;INPUT&gt;</code>-Tag oder eine <code>&lt;SUBMIT&gt;</code>-Schaltfläche mit einem Wert oder einem untergeordneten Text? </li>
     <li id="li_F7ABE88308E1413E9B9C2224DEC91BAB">Ist dies ein <code>&lt;INPUT&gt;</code>-Tag mit dem Typ <code>&lt;IMAGE&gt;</code> und einer <code>"src"</code>-Eigenschaft? </li>
     <li id="li_F34A0C986E8040109A1DDF88C26E56D5">Ist dies ein <code>&lt;BUTTON&gt;</code>? </li>
    </ul>
    Wenn die Antwort auf eine der vorangehenden Fragen <b>Ja</b> ist, wird dieses Element als Link verwendet und verfolgt. <br/>
     <br/>
    Wichtig: Schaltflächen-Tags mit dem Attribut  <code>type="button"</code> werden von AppMeasurement nicht als Links betrachtet. Entfernen Sie <code>type="button"</code> in den Schaltflächen-Tags und fügen Sie stattdessen <code>role="button"</code> oder <code>submit="button"</code> hinzu. <br/>
     <br/>
    Wichtig: Ein Anker-Tags mit einem  <code>"href"</code> Namen, mit dem Beginn  <code>"#"</code> arbeiten, wird von AppMeasurement als interner Speicherort der Zielgruppe und nicht als Link betrachtet (da Sie die Seite nicht verlassen). Standardmäßig verfolgt Activity Map diese internen Zielorte nicht. Es werden nur Links verfolgt, die den Benutzer zu einer neuen Seite führen. </td> 
  </tr>
  <tr>
   <td colname="col1"> <b>F: Wie verfolgt Activity Map andere visuelle HTML-Elemente?</b> </td>
   <td colname="col2">
    <ol id="ol_DA3AED165CFF44B08DFB386D4DEE26C5">
     <li id="li_E3E3F498F37B4FADAFDA39CCAE41511F"> <b>Über die<code>s.tl()</code> Funktion</b>  <br/>
       <br/>
      Wenn der Klick über einen  <code>s.tl()</code> Aufruf erfolgte, erhält Activity Map auch dieses Klick-Ereignis und ermittelt, ob eine  <code>linkName</code> Zeichenfolgenvariable gefunden wurde. Bei der Ausführung von <code>s.tl()</code> wird <code>linkName</code> als Activity Map-Link-ID festgelegt. Das Element, auf das geklickt wurde, das den <code>s.tl()</code>-Aufruf ausgelöst hat, wird zur Bestimmung der Region verwendet. <br/>
       <br/>
      Beispiel:  <br/>
       <br/>
      <code>&lt;img&nbsp;onclick="s.tl(true,'o','abc')"&nbsp;src="someimageurl.png"/&gt;</code><br/>
       
     </li>
     <li id="li_A93725B810FE408BA5E6B267CF8CEAE5"> <b>Über  <code>s_objectID</code> </b> <br/>
       <br/>
      variableExample:  <br/>
       <br/>
      <code>&lt;img&nbsp;onclick="s_objectID='abc';"&nbsp;src="someimageurl.png"/&gt;</code><br/>
      <code>&lt;a&nbsp;href="some-url.html"&nbsp;onclick="s_objectID='abc';"&nbsp;&gt;</code><br/>
      <code>&nbsp;&nbsp;Link&nbsp;Text&nbsp;Here</code><br/>
      <code>&lt;/a&gt;</code> <br/>
       <br/>
      Wichtig: Beachten Sie, dass ein nachfolgender Semikolon (<code>;</code>) bei der Verwendung  <code>s_objectID</code> in Activity Map erforderlich ist.
     </li>
    </ol>
   </td>
  </tr>
  <tr>
   <td colname="col1"> <b>F: Können Sie einige Beispiele für Links nennen, die verfolgt werden?</b> </td>
   <td colname="col2">
    <ol id="ol_697E5CE0B84D4A309DD80670697A02BA">
     <li id="li_2C511EFD10F14F438B1F3A1BAB4B45E0">
      <code>&lt;a&nbsp;href="/home"&gt;Home&lt;/a&gt;</code>
     </li>
     <li id="li_76F3DB36ED734132A2386871E6EB4929">
      <code>&lt;input&nbsp;type="submit"&nbsp;value="Submit"/&gt;</code>
     </li>
     <li id="li_10CF9EDA224645169E7CDF74956DB98B">
      <code>&lt;input&nbsp;type="image"&nbsp;src="submit-button.png"/&gt;</code>
     </li>
     <li id="li_9FA171D7F49547E798DE21869F73A402">
      <code>&lt;p&nbsp;onclick="var&nbsp;s_objectID='custom&nbsp;link&nbsp;id';"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/p&gt;</code>
     </li>
     <li id="li_C5D77589006E4514AA6F3AEB509A0BAF">
      <code>&lt;div&nbsp;onclick="s.tl(true,'o','custom&nbsp;link&nbsp;id')"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/div&gt;</code>
     </li>
    </ol>
   </td>
  </tr>
  <tr>
   <td colname="col1"> <b>F: Können Sie einige Beispiele für Links nennen, die NICHT verfolgt werden?</b> </td>
   <td colname="col2">
    <ol id="ol_CDFDB572F76B4F68A64B66A6B0237547">
     <li id="li_99372060646B43EF94C13A9C682CE693">Grund: Anker-Tag hat keine gültige <code>"href"</code> <br/>
       <br/>
      <code>&lt;a&nbsp;name="innerAnchor"&gt;Section&nbsp;header&lt;/a&gt;</code><br/>
       
     </li>
     <li id="li_736A5F7DC2D74B4DA1CECEE3AD10EB19">Grund: Weder <code>s_ObjectID</code> noch <code>s.tl()</code> sind vorhanden <br/>
       <br/>
      <code>&lt;p&nbsp;onclick="showPanel('market&nbsp;rates')"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/p&gt;</code><br/>
       
     </li>
     <li id="li_45F9ED97140F47F99F8C167BC1DC546F">Grund: Weder <code>s_ObjectID</code> noch <code>s.tl()</code> sind vorhanden <br/>
       <br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="A"/&gt;</code><br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="B"/&gt;</code><br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="C"/&gt;</code><br/>
       
     </li>
     <li id="li_9EBFCC58F3A94F30BA62156F14B15D55">Grund: <code>"src"</code>-Eigenschaft fehlt ein Formular <code>input</code> Element <br/>
       <br/>
      <code>&lt;input&nbsp;type="image"/&gt;</code><br/>
       
     </li>
    </ol>
   </td>
  </tr>
 </tbody>
</table>
