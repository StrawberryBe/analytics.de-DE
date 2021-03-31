---
description: Häufig gestellte Fragen zum Linktracking in Activity Map.
title: Linktracking – Häufig gestellte Fragen
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 99%

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
   <td colname="col1"> <b>F: Wann ist Linktracking aktiv?</b> <p> </p> </td> 
   <td colname="col2"> A: Sobald ein Benutzer auf eine Seite klickt, identifiziert Activity Map den Link und die Region. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>F: Was wird standardmäßig verfolgt?</b> <p> </p> </td> 
   <td colname="col2"> A: Wenn auf ein Element geklickt wird, durchläuft es mehrere Prüfungen, um zu bestimmen, ob es von AppMeasurement als Link behandelt wird. Die Prüfungen sind: 
    <ul id="ul_81B9A5A7F8534E71AEF68F2199A154F0"> 
     <li id="li_49F6DDD9DC124AE5846EC5B7D7BEA20E">Handelt es sich um ein Tag des Typs &lt;A&gt; oder &lt;AREA&gt; mit einer HREF-Eigenschaft? </li> 
     <li id="li_77828D24D54343E5B9A1FF7345221781">Ist ein onclick-Attribut vorhanden, das eine s_objectID-Variable festlegt? </li> 
     <li id="li_D4B0AEEEA58A4F82A1BCBD3971A60D02">Gibt es ein INPUT-Tag oder eine SUBMIT-Schaltfläche mit einem Wert oder einem untergeordneten Text? </li> 
     <li id="li_F7ABE88308E1413E9B9C2224DEC91BAB">Ist dies ein INPUT-Tag mit dem Typ IMAGE und einer src-Eigenschaft? </li> 
     <li id="li_F34A0C986E8040109A1DDF88C26E56D5">Ist das eine &lt;Schaltfläche&gt;? </li> 
    </ul> <p>Wenn die Antwort auf eine der vorangehenden Fragen <b>Ja</b> ist, wird dieses Element als Link verwendet und verfolgt. </p> <p>Wichtig: Schaltflächen-Tags mit dem Attribut type="button" werden von AppMeasurement nicht als Links erachtet. Entfernen Sie ggf. "type='button'" für Schaltflächen-Tags und fügen Sie stattdessen role="button" oder submit="button" hinzu. </p> <p>Wichtig: Ein Anker-Tag mit einem href, das mit „#“ beginnt, wird von AppMeasurement als interner Zielort erachtet, nicht als Link (da Sie die Seite nicht verlassen). Standardmäßig verfolgt Activity Map diese internen Zielorte nicht. Es werden nur Links verfolgt, die den Benutzer zu einer neuen Seite führen.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>F: Wie verfolgt Activity Map andere visuelle HTML-Elemente?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_DA3AED165CFF44B08DFB386D4DEE26C5"> 
     <li id="li_E3E3F498F37B4FADAFDA39CCAE41511F"> <b>Über die<code> s.tl() </code> Funktion</b> <p>Wenn der Klick über einen s.tl-Aufruf erfolgte, erhält Activity Map außerdem dieses Klickereignis und bestimmt, ob die Zeichenfolgenvariable linkName gefunden wurde. Während der Ausführung von s.tl wird dieser linkName als Activity Map-Link-ID festgelegt. Das Element, auf das geklickt wurde und von dem der s.tl()-Aufruf stammt, wird zur Bestimmung der Region verwendet. Beispiel: </p> <p> 
       <code>
         &lt;img&amp;nbsp;onclick="s.tl(true,'o','abc')"&amp;nbsp;src="someimageurl.png"/&gt; 
       </code> </p> </li> 
     <li id="li_A93725B810FE408BA5E6B267CF8CEAE5"> <b>Über die<code> s_objectID </code> Variable</b> <p>Beispiel: </p> <p> 
       <code>
         &lt;img&nbsp;onclick="s_objectID='abc';"&nbsp;src="someimageurl.png"/&gt; &lt;a&nbsp;href="some-url.html"&nbsp;onclick="s_objectID='abc';"&nbsp;&gt;Link&nbsp;Text&nbsp;Here&lt;/a&gt;
       </code> </p> <p>Wichtig: Bei Verwendung von s_objectID in Activity Map muss ein Semikolon (;) folgen. </p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>F: Können Sie einige Beispiele für Links nennen, die verfolgt werden?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_697E5CE0B84D4A309DD80670697A02BA"> 
     <li id="li_2C511EFD10F14F438B1F3A1BAB4B45E0"> 
      <code>
        &lt;a&amp;nbsp;href="/home"&gt;Home&lt;/a&gt; 
      </code> </li> 
     <li id="li_76F3DB36ED734132A2386871E6EB4929"> 
      <code>
        &lt;input&amp;nbsp;type="submit"&amp;nbsp;value="Submit"/&gt; 
      </code> </li> 
     <li id="li_10CF9EDA224645169E7CDF74956DB98B"> 
      <code>
        &lt;input&amp;nbsp;type="image"&amp;nbsp;src="submit-button.png"/&gt; 
      </code> </li> 
     <li id="li_9FA171D7F49547E798DE21869F73A402"> 
      <code>
        &lt;p&nbsp;onclick="var&nbsp;s_objectID='custom&nbsp;link&nbsp;id';"&gt; &nbsp;&nbsp;&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;&lt;span&nbsp; class="subtitle"&gt;1.45USD&lt;/span&gt; &lt;/p&gt;
      </code> </li> 
     <li id="li_C5D77589006E4514AA6F3AEB509A0BAF"> 
      <code>
        &lt;div&nbsp;onclick="s.tl(true,'o','custom&nbsp;link&nbsp;id')"&gt; &nbsp;&nbsp;&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;&lt;span&nbsp; class="subtitle"&gt;1.45USD&lt;/span&gt; &lt;/div&gt;
      </code> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>F: Können Sie einige Beispiele für Links nennen, die NICHT verfolgt werden?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_CDFDB572F76B4F68A64B66A6B0237547"> 
     <li id="li_99372060646B43EF94C13A9C682CE693">Grund: Anker-Tag hat keine gültige href 
       
      <code>
        &lt;a&amp;nbsp;name="innerAnchor"&gt;Section&amp;nbsp;header&lt;/a&gt; 
      </code> </li> 
     <li id="li_736A5F7DC2D74B4DA1CECEE3AD10EB19">Grund: Weder <code> s_ObjectID </code> noch <code> s.tl() </code> sind vorhanden 
      <code>
        &lt;p&nbsp;onclick="showPanel('market&nbsp;rates')"&gt; &nbsp;&nbsp;&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;&lt;span&nbsp; class="subtitle"&gt;1.45USD&lt;/span&gt; &lt;/p&gt;
      </code> </li> 
     <li id="li_45F9ED97140F47F99F8C167BC1DC546F">Grund: Weder <code> s_ObjectID </code> noch <code> s.tl() </code> sind vorhanden 
      <code>
        &lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="A"/&gt; &lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="B"/&gt; &lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="C"/&gt;
      </code> </li> 
     <li id="li_9EBFCC58F3A94F30BA62156F14B15D55">Grund: src-Eigenschaft fehlt ein Formular-Eingabeelement 
      <code>
        &lt;input&amp;nbsp;type="image"/&gt; 
      </code> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
