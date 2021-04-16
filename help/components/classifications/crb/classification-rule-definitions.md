---
description: Definitionen der Elemente auf den Seiten im Classification Rule Builder.
subtopic: Classifications
title: Klassifizierungsregeln – Definitionen
feature: Admin Tools
uuid: 77af8669-6e11-435c-9cc3-b03eb627c855
exl-id: 514501d1-7e1b-45da-b8fe-c68331e59dab
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 100%

---

# Klassifizierungsregeln – Definitionen

Definitionen der Elemente auf den Seiten im Classification Rule Builder.

## Seite „Regeln“ {#section_4A5BF384EEEE4994B6DC888339833529}

Auf dieser Seite werden die Regeln in einem Regelsatz angezeigt.

![](assets/classification_rules_page.png)

**Definitionen**

<table id="table_2B3A8BB7BDE14836ACA6A1D444B011CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Report Suites und Variablen auswählen </p> </td> 
   <td colname="col2"> <p><b>Report Suite</b> </p> <p>Die Report Suites, auf die der Regelsatz angewendet wird. </p> <p><b>Variable</b> </p> <p>Beim Erstellen eines Classification-Regelsatzes können Sie nur eine einzelne Variable anwenden. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden. </p> <p>Hinweis: Sie können nur die Variablen verwenden, auf die Sie in Ihren Report Suites Zugriff haben. Variablen werden erst im Bereich <span class="wintitle">Neuer Regelsatz</span> angezeigt, nachdem mindestens eine Classification für diese Variable definiert wurde. </p> <p> Sie können Classifications für eine Variable unter <span class="uicontrol">Admin</span> &gt; <span class="uicontrol">Report Suites</span> &gt; <span class="uicontrol">Traffic</span> &gt; <span class="uicontrol">Traffic-Classifications</span> (oder <span class="uicontrol">Konversion</span> &gt; <span class="uicontrol">Konversion-Classifications</span>) erstellen. Wählen Sie dann die Variable aus und klicken Sie auf <span class="uicontrol">Classification hinzufügen</span>. </p> <p>Weitere Informationen finden Sie in der Admin-Hilfe unter <a href="https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/traffic-variables/traffic-classifications.html"  >Traffic-Classifications</a> und <a href="https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/conversion-variables/conversion-classifications.html"  >Konversion-Classifications</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Aktivieren</span> </p> </td> 
   <td colname="col2"> <p>Validiert und aktiviert eine Regel. Aktive Regeln werden täglich verarbeitet, wobei die zu untersuchenden Classification-Daten in der Regel einen Monat zurückgehen. Die Regeln suchen automatisch nach neuen Werten und laden die Classifications hoch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Deaktivieren</span> </p> </td> 
   <td colname="col2"> <p>Deaktiviert die Regeln, so dass Sie sie bearbeiten und testen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suites und Variablen konfigurieren </p> </td> 
   <td colname="col2"> <p>Zeigt die Seite <span class="wintitle">Verfügbare Report Suites</span> an, auf der Sie verfügbare Report Suites auswählen können, die für alle Regelsätze verwendet werden sollen. (Diese Seite wird auch angezeigt, wenn Sie den <span class="wintitle">Classification Rule Builder</span> zum ersten Mal ausführen.) </p> <p>Mit dieser Funktion soll die Ladezeit für Report Suites reduziert werden, falls Hunderte Report Suites verfügbar sind. </p> <p>Die hier gewählten Report Suites werden auf Regelebene verfügbar gemacht, wenn Sie auf <span class="uicontrol">Suites hinzufügen</span> klicken, während Sie eine Regel erstellen. </p> <p>Hinweis: Eine Report Suite steht <span class="term"> nur</span>zur Verfügung, wenn in den Report Suites mindestens eine Classification für die Variable in den <span class="wintitle"> Admin Tools</span> definiert ist. <p>(Eine Erläuterung zu dieser Voraussetzung finden Sie unter <span class="term">Variable</span> unter <a href="/help/components/classifications/crb/classification-rule-set.md"  >Klassifizierungsregelsätze</a>.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln überschreiben alle vorhandenen Werte </p> </td> 
   <td colname="col2"> <p> (Standardeinstellung) Vorhandene Classification-Schlüssel werden immer überschrieben, einschließlich Classifications, die über das Importtool (SAINT) hochgeladen wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln überschreiben nur nicht festgelegte Werte. </p> </td> 
   <td colname="col2"> <p>Es werden nur leere (nicht festgelegte) Zellen ausgefüllt. Vorhandene Classifications werden nicht geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lookback-Fenster </p> </td> 
   <td colname="col2"> <p>Wenn Sie Regeln aktivieren und validieren, können Sie angeben, ob die Regeln vorhandene Classifications für die betroffenen Schlüssel überschreiben sollen. (Hiervon sind ausschließlich klassifizierte Schlüssel betroffen, die vorher im angegebenen Zeitraum an <span class="keyword">Adobe Analytics</span> übergeben wurden.) </p> <p>Wenn Sie kein <span class="term">Lookback-Fenster</span> festlegen, betrachten die Regeln rückblickend einen Zeitraum von etwa einem Monat (hängt vom aktuellen Tag des Monats ab). Vorhandene Classifications werden nicht überschrieben, sofern Sie diese Option nicht aktivieren. </p> <p><b>Entwicklungszentrum</b>: Partner können im <span class="wintitle">Entwicklungszentrum</span> Classification-Regeln erstellen. Diese Regeln werden angewandt, wenn der Kunde eine Integration aktiviert. Mit der Option <span class="wintitle">„Seit“ überschreiben</span> im <span class="uicontrol">Entwicklungszentrum</span> kann der Partner angeben, ob der Kunde den Überschreibungswert festlegen kann, wenn er eine Integration aktiviert oder bearbeitet. </p> <p>Weitere Informationen zur Verarbeitung von Regeln finden Sie unter <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  >Verarbeitung der Regeln</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Regel hinzufügen </a> </td> 
   <td colname="col2"> <p>Hier können Sie Regeln zum Regelsatz hinzufügen. </p> <p>Hinweis: Wenn für einen Wert zwei oder mehr Übereinstimmungen in einem Regelsatz vorliegen, wird dieser Wert anhand der jeweils letzten Regel klassifiziert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Entwurf</span> </td> 
   <td colname="col2"> Hier legen Sie eine Regel fest, die sich im Entwurfsmodus befindet. Im Entwurfsmodus können Sie eine Regel vor dem Ausführen testen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Duplizieren</span> </td> 
   <td colname="col2"> Dupliziert (kopiert) einen Regelsatz, so dass Sie diesen Regelsatz auf eine andere Variable anwenden können (oder auch auf dieselbe Variable in einer anderen Report Suite). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Testregelsatz </a> </p> </td> 
   <td colname="col2"> <p>Hier testen Sie die Validität eines Regelsatzes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Übereinstimmende Bedingung</span> </td> 
   <td colname="col2"> Bestimmt die Bedingungen für die Regel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classification-Aktion</span> </td> 
   <td colname="col2"> <p>Bestimmt die Aktion, die ausgeführt werden soll, wenn die übereinstimmende Bedingung eintritt. </p> <p>Wenn Sie beispielsweise $2 für den Kampagnennamen festlegen, wird entsprechend die zweite Position in einem Trackingcode als Kampagnenname verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> #</span> </td> 
   <td colname="col2"> <p>Die Nummer der Regel. </p> <p>Siehe <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Verarbeitung der Regeln</a> für weitere Informationen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Regeltyp auswählen</span> </td> 
   <td colname="col2"> <p>Jeder Regelsatz gilt für eine bestimmte Variable. Folgende Auswahlen sind gültig: </p> 
    <ul id="ul_6A8E06BB4AF2402B99C215823CB3D59D"> 
     <li id="li_5C702D4F460841D38A59621A5161A3BC">Beginnt mit </li> 
     <li id="li_8052A741D9F34A2FBC136C181600193E">Endet mit </li> 
     <li id="li_D0FA6EA4F09644FFBC9E6BC568BE80AC">Enthält </li> 
     <li id="li_48675FE5253942ED887C6A72D1DCEF54"> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Regulärer Ausdruck </a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Übereinstimmungskriterien eingeben</span> </td> 
   <td colname="col2"> Das Textmuster, nach dem in einem Schlüssel gesucht werden soll. Diese Kriterien können beispielsweise aus Begriffen, Zeichen oder regulären Ausdrücken bestehen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classification auswählen</span> </td> 
   <td colname="col2"> Die Classification-Spalte, die festgelegt werden soll, wenn die Übereinstimmungskriterien erfüllt sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Hierzu</span> </td> 
   <td colname="col2"> Der Wert, der für die ausgewählte Classification-Spalte festgelegt werden soll, wenn die Übereinstimmungskriterien erfüllt sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filter </td> 
   <td colname="col2"> Hier können Sie nach Regeln suchen. </td> 
  </tr> 
 </tbody> 
</table>

## Seite Regulärer Ausdruck {#section_C932A5469E774841B2229965A154163C}

Auf der Seite [!UICONTROL Regulärer Ausdruck] können Sie reguläre Ausdrücke bearbeiten.

![](assets/regex_tracking_code.png)

**Definitionen**

| Element | Beschreibung |
|---|---|
| Beispielschlüssel | Die zu verwendende Testzeichenfolge. So können Sie beispielsweise eine Classification anhand bestimmter Zeichen in einem Trackingcode erstellen. Sie können bestimmte Zeichen, Wörter oder Zeichenmuster abgleichen. |
| Übereinstimmungsgruppen | Zeigt, wie der reguläre Ausdruck den Zeichen der Kampagnen-ID entspricht, so dass Sie eine Position in der Kampagnen-ID klassifizieren können. |
| Übereinstimmungsergebnis | Zeigt die Teile einer Zeichenfolge an, die mit dem regulären Ausdruck übereinstimmt. |

Siehe [Reguläre Ausdrücke in Classification-Regeln](/help/components/classifications/crb/classification-quickstart-rules.md).

## Seite „Tests“ {#section_EC926F97901C4E65901413F9683AA70A}

Auf dieser Seite können Sie die Regeln in einem Regelsatz testen.

**Definitionen**

| Element | Beschreibung |
|---|---|
| Test ausführen | Beim Testen des Regelsatzes verwenden Sie Schlüssel aus dem Bericht, und es wird ermittelt, wie sich der Regelsatz auf diese Schlüssel auswirkt. |
| Filter | Filtert die Werte im Bereich [!UICONTROL Ergebnisse]. |
