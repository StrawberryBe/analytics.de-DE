---
description: Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.
solution: Experience Cloud
title: Häufig gestellte Fragen
uuid: 9dfc8f19-f9b2-4c2e-bff9-3d91cfe01bca
translation-type: ht
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16
workflow-type: ht
source-wordcount: '1098'
ht-degree: 100%

---


# Häufig gestellte Fragen

Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.

## FAQs zu rechtlichen Fragen {#section_B51CFC961C0B45A2BE5F4A4404620764}

<table id="table_22037CCB516C4231BF5820004FBB351A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>F: Woher weiß ich, ob sich in meinen Analytics-Daten persönlich identifizierbare Informationen (PII) befinden? Wenn ja, wie verhalte ich mich?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_71E0ECD5981D4B65BCDA065BE07A43AA"> 
     <li id="li_F8FF61A4D7B54BA39DAA6F28DB51D749">Wenn sich in einer prop oder eVar E-Mail-Adressen, Adressen usw. befinden, könnten Sie die Daten bei der Erfassung mit einem Hash behandeln. </li> 
     <li id="li_57A8B4C7BB784FFCBC1DC363B35D9FF7">Wenn in Ihrem Land IP-Adressen als persönlich identifizierbare Informationen gelten, <a href="https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/exclude-ip.html"  >aktivieren Sie die IP-Verschleierung </a>. </li> 
     <li id="li_C7AA02B831AE47A59E783623126A7789">Sprechen Sie mit Ihrem Analytics-Administrator, um zu ermitteln, was Sie erfassen. </li> 
     <li id="li_F6AAE868141E486AB8CAB291BD8EDB71">Sprechen Sie mit Ihrer Rechtsabteilung, um zu erfahren, welche Angaben als persönliche identifizierbare Informationen eingestuft werden. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>F: Woher weiß ich, ob meine Berichtssuiten Personalisierung auf der Site bzw. Targeting auf der Site oder außerhalb der Site vornehmen?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_F0984CEF80DB4B589716BC55549E32B8"> 
     <li id="li_9BC3819784A9408F846D60FF0F20AAF9">Dies bezieht sich nicht auf das Senden von Adobe Analytics-Daten an Adobe Audience Manager. </li> 
     <li id="li_050A1BF9978E436895B5C7E33A82527D">Fragen Sie sich selbst: Möchten Sie ein von Analytics freigegebenes Segment mit einer MCA-Dimension wieder für Experience Cloud freigeben? </li> 
     <li id="li_C52D969681B94F4AAA18FDEB21EC5B49">Exportieren Sie (z. B. über Datenfeeds) in ein Business Intelligence-System (BI), das für diese Zwecke verwendet wird? </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## AAM-spezifische FAQs  {#section_6BDF746BA6464359A6A89A64EB025D12}

<table id="table_15B44592161240BDA79F3B020EA9CC9D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>F: Wie erstelle ich ein Analytics-Ziel in Audience Manager?</b> </p> </td> 
   <td colname="col2"> Siehe <a href="https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html"  >Konfigurieren des Analytics-Ziels in AAM</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Wie lange dauert es nach dem Erstellen und Speichern eines Analytics-Ziels, bis Daten in meinen ausgewählten Report Suites angezeigt werden?</b> </p> </td> 
   <td colname="col2"> <p>Es kann einige Stunden dauern, Ihre Report Suites mit neuen Daten zu füllen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Ich habe ein neues Analytics-Ziel erstellt, aber es wird mir nicht im Bereich „Zielzuweisungen“ meiner verfügbaren Segmente angezeigt. Wo wurde dieses Ziel abgelegt oder wie kann ich es finden?</b> </p> </td> 
   <td colname="col2"> <p>Ein Analytics-Ziel wird aus dem Bereich „Zielzuweisungen“ eines Segments entfernt, wenn Sie die Option <span class="uicontrol">Alle aktuellen und zukünftigen Segmente automatisch zuweisen</span> in <span class="uicontrol">Segmentzuweisungen</span> auswählen. </p> <p><img placement="break" align="left"  src="assets/auto-mapping.png" id="image_670ED5A306784FCBA8A0B336AC1F0FC6" width="300px" /> </p> <p>Um das zu vermeiden, wählen Sie statt der automatischen Option <span class="uicontrol">Segmente manuell zuweisen</span> aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>F: Erhalte ich damit alle Informationen von AAM in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Nein, nur Daten, die sich auf Personen beziehen, die während oder nach der Aktivierung von Audience Manager-Zielgruppen und während oder nach der Qualifizierung des Segments auf Ihre Site kommen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>F: Erhalte ich damit eine vollständige adressierbare Zielgruppe pro Segment?</b> </p> </td> 
   <td colname="col2"> <p>Nicht ganz. Sie erfahren die Anzahl der Besucher in diesem Segment, die während oder nach der Qualifizierung des Segments auf Ihre Site kamen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>F: Inwiefern unterscheidet sich dies vom herkömmlichen Cookie-Ziel Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Die Qualifizierung für Segmente und die Rückgabe erfolgen in Echtzeit – bei demselben Treffer. </p> <p>Die Anzeigenamen werden automatisch angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Was ist, wenn einige meiner Report Suites persönliche Daten enthalten und andere nicht?</b> </p> </td> 
   <td colname="col2"> <p>Tipp: Erstellen Sie zwei Ziele – Fügen Sie die Report Suites mit persönlichen Daten zu einem Ziel hinzu und die Report Suites ohne persönliche Daten zum anderen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Analytics-spezifische FAQs  {#section_67BFB1B1E48D4113A38B075C020931BA}

<table id="table_19AEAE0A3575423CB4F5F164DB5626D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>F: Wird diese Integration in Analytics als Dimension oder als Segment dargestellt?</b> </p> </td> 
   <td colname="col2"> <p>Als Dimensionen: Zielgruppen-ID und Zielgruppenname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Wo kann ich diese Dimensionen in Analytics verwenden?</b> </p> </td> 
   <td colname="col2"> <p>Fast überall; sie werden wie jede andere in Analytics erfasste Dimension behandelt. Es gibt eine Ausnahme: Daten können zurzeit nicht in Data Workbench verwendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Warum kommen keine Daten in Analytics durch?</b> </p> </td> 
   <td colname="col2"> <p>Wahrscheinlich gibt es bei Ihnen einen Konflikt bei den AAM-Datenschutzbestimmungen zwischen der Datenquelle und dem Ziel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Warum fehlen einige meiner Segmente in Analytics, obwohl ich ausgewählt habe, dass alle Segmente gesendet werden sollen?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_B8938FD08C6F4F2387EDADDEF8089319"> 
     <li id="li_50A9BDF612304062913370F16BC882EF">Unter Umständen stehen Ihre AAM-Datenexportbestimmungen für das Ziel und die Datenquellen der Segmente in Konflikt, wodurch einige Segmente nicht gesendet werden können. </li> 
     <li id="li_AF5D6F883D6F4D3192E0BF23CF12ADEA">Wenn Sie Eigenschaften mit Drittpartei-Daten in Ihren Segmenten verwenden, können diese Segmente nicht an ein Ziel (einen Satz von Report Suites) weitergeleitet werden, das persönliche Daten enthält. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Warum wird in meinem Analytics-Bericht „Zielgruppenlimit erreicht“ angezeigt? (Hinweis: Dies wird auch als Zielgruppe-ID = -1 und als „::max_audiences_exceeded::“ in Data Warehouse dargestellt)</b> </p> </td> 
   <td colname="col2"> <p>Standardmäßig sendet die Audience Analytics-Integration für AAM alle Segmente pro Treffer an Analytics, für die sich ein Besucher qualifiziert. Wenn ein Besucher bei einem einzigen Treffer mehr als 150 AAM-Segmenten angehört, werden die <b>150 aktuellsten qualifizierten Segmente</b> an Analytics gesendet und der Rest der Liste wird nicht gesendet. </p> <p>Es wird ein zusätzliches Warnsignal an Analytics gesendet, das anzeigt, dass die Segmentliste gekürzt wurde. Dieses Warnsignal wird in der Dimension „Zielgruppendimension“ als „Zielgruppenlimit erreicht“ und in der Dimension „Zielgruppen-ID“ als „-1“ dargestellt. </p> <p>Es ist zwar unwahrscheinlich, dass sich ein Besucher bei einem bestimmten Treffer für mehr als 150 Segmente qualifiziert, aber es kann in seltenen Fällen vorkommen. Wenn Ihnen in Ihrer Berichterstellung die Meldung „Zielgruppenlimit erreicht“ angezeigt wird, haben Sie zwei Optionen: </p> 
    <ul id="ul_8E290B2E32DC49738F6FD00CB0CE2BBB"> 
     <li id="li_12F498981EA949B5BCBD40ECC954C339"><b>Option 1</b>: Lassen Sie die Integration weiterhin im Out-of-the-Box-Zustand arbeiten und die 150 Segmente eines bestimmten Benutzers senden, für die dieser sich zuletzt qualifiziert hat. </li> 
     <li id="li_CA4D5747AA4A4452929097807B604959"><b>Option 2</b>: Wählen Sie in AAM die 150 Segmente für die Integration aus, die am bedeutsamsten für Ihr Unternehmen sind. Daraufhin überprüft AAM Besucher nur auf diese 150 Segmente. Der Nachteil dieser Vorgehensweise ist, dass Sie bei allen Besuchern nur noch diese 150 Segmente erhalten. Dahingegen liefert die Vorgehensweise in Option 1 dadurch, dass die Integration pro Treffer Segmente sendet, eine unbegrenzte Anzahl an Segmenten. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Werden bei dieser Integration zusätzliche Server-Aufrufe für Analytics berechnet?</b> </p> </td> 
   <td colname="col2"> <p>Nein. AAM-Zielgruppen sind serverseitig Teil des Analytics-Treffers. Dabei fallen keine zusätzlichen Server-Aufrufe für Analytics an (primär oder sekundär). </p> </td> 
  </tr> 
 </tbody> 
</table>

## FAQs zur serverseitigen Weiterleitung  {#section_ADDE84ABCA0D4906B6235E92D185E0C6}

<table id="table_B7067B70FF85498896801F58D716202F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>F: Wenn ich eine veraltete serverseitige Weiterleitung implementiert habe, muss ich die serverseitige Weiterleitung von Report Suites dann ebenfalls in Analytics Admin aktivieren?</b> </p> </td> 
   <td colname="col2"> <p>Ja. In der AAM-Zieleinrichtung sehen Sie nur Report Suites, bei denen die serverseitige Weiterleitung aktiviert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Warum kann ich bestimmte Report Suites nicht in Analytics Admin aktivieren?</b> </p> </td> 
   <td colname="col2"> <p>Es können nur Suites aktiviert werden, die Ihrer Experience Cloud-Org zugeordnet sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere häufig gestellte Fragen zu diesem Thema finden Sie unter [FAQs zur serverseitigen Weiterleitung](/help/admin/admin/c-server-side-forwarding/ssf-faq.md).

## Allgemeine FAQs {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

<table id="table_1F7C0C785F9C472286A96F8C25E8440B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>F: Warum unterscheiden sich die Besucherzahlen für Segmente in Audience Manager und Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Siehe  <a href="/help/integrate/c-audience-analytics/visitor-count-reconciliation.md"  > Unterschiede in der Besucherzahl </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Was ist der Unterschied zwischen „Zielgruppen“ in AAM und „Segmenten“ in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Siehe  <a href="/help/integrate/c-audience-analytics/aam-analytics-segments.md"  > Segmente in Analytics und Audience Manager – Grundlagen </a>. </p> <p>AAM-Zielgruppen werden als „Dimensions“-Komponenten an Analytics gesendet und dort verwendet. Sie werden beispielsweise nicht als Segmente im Segmentaufbau angezeigt, sondern als Dimensionen, mit denen Sie Segmente erstellen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Was ist der Unterschied zwischen Kundenattributen und von AAM integrierten Kundendaten?</b> </p> </td> 
   <td colname="col2"> <p>Kundenattribute sind nicht zeitbasiert; sie gelten rückwirkend und zukünftig. Von AAM integrierte Daten sind zeitbasiert und gelten nur zukünftig. Außerdem stellen Kundenattribute eine Nachschlagetabelle für Experience Cloud-Besucher-IDs dar, während die AAM-Integration Daten umfasst, die einem Besucher bei jedem Treffer zugeordnet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Wie steht es mit veralteten Ansätzen für dieses Problem, beispielsweise der alten Beta-Version oder der Nutzung von Plugin-Cookie-Zielen?</b> </p> </td> 
   <td colname="col2"> <p>Wir empfehlen Ihnen, die neue Integration zu implementieren und alte Ziele zu entfernen. </p> </td> 
  </tr> 
 </tbody> 
</table>

