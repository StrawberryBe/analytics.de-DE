---
description: In der Experience Cloud gibt es verschiedene Variablentypen. Props und eVars, die beiden am häufigsten verwendeten Typen, ermöglichen es Ihrer Organisation, benutzerdefinierte Dimensionen auf Ihrer Website darzustellen. Mit vordefinierten Standardberichten wäre das nicht möglich.
keywords: Analytics-Implementierung; prop; evar; props vs. evars; Benennungskonvention; Traffic-Variablen; persistence; Erfolgsereignis; Pfade
seo-description: In der Experience Cloud gibt es verschiedene Variablentypen. Props und eVars, die beiden am häufigsten verwendeten Typen, ermöglichen es Ihrer Organisation, benutzerdefinierte Dimensionen auf Ihrer Website darzustellen. Mit vordefinierten Standardberichten wäre das nicht möglich.
seo-title: Props und eVars im Vergleich
solution: Analytics
title: Props und eVars im Vergleich
topic: Entwickler und Implementierung
uuid: 0 f 02760 f-ff 69-481 c-a 817-799 f 02 dafe 8 e
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Props und eVars im Vergleich

In der Experience Cloud gibt es verschiedene Variablentypen. Props und eVars, die beiden am häufigsten verwendeten Typen, ermöglichen es Ihrer Organisation, benutzerdefinierte Dimensionen auf Ihrer Website darzustellen. Mit vordefinierten Standardberichten wäre das nicht möglich.

Wenn Sie sich mit der Zuweisung von Variablen beschäftigen, müssen Sie wissen, wie sich die Funktionen von Props und eVars unterscheiden. Wenn Ihre Organisation mit diesen Unterschieden vertraut ist, kann sie die optimale Verwendung dieser Variablen festlegen. 

**Props und eVars**

Props und eVars unterscheiden sich hauptsächlich in Folgendem:

* **Namenskonvention**: Props sind Traffic-Variablen. Das bedeutet, dass mit ihnen die Popularität verschiedener Dimensionen Ihrer Website gemeldet wird. eVars sind Konversionsvariablen. Mit ihnen wird bestimmt, welche Dimensionen der Website am meisten zu Erfolgsereignissen beitragen.
* **Persistenz**: Props bleiben nach der Bildanforderung, zu der sie ausgelöst wurden, nicht erhalten. Sie können keinen anderen Variablen zugeordnet werden, die sich nicht in derselben Bildanforderung befinden. eVars sind hingegen persistent. Der ursprünglich ausgelöste Wert wird mit einer Backend-Variablen beibehalten, sodass er später Erfolgsereignissen zugeordnet werden kann. 
* **Erfolgsereignisse**: Erfolgsereignisse, auch Konversionsereignisse genannt, sind Metriken, mit denen gemessen wird, wie häufig ein Besucher ein Ziel erreicht. Es kann sich um ein beliebiges Ereignis handeln, wie beispielsweise einen Einkauf auf der Website oder das Abonnement eines Newsletters. eVars dienen dazu, Konversionsereignisse zu melden, mit denen Sie erkennen, welche Werte am besten dazu beitragen, dass die Besucher zu den von Ihnen gewünschten Zielen gelangen. Traffic-Variablen bieten diese Funktionen nicht. Sie können Beitragsmetriken jedoch anzeigen, wenn Sie die Report Suite richtig konfigurieren.
* **Pfadsetzung**: Props können die Pfadsetzung verwenden. Dadurch kann Ihre Organisation den speziellen Pfad erkennen, dem ein Benutzer im Kontext der angezeigten Variable gefolgt ist. Ein Adobe-Support-Mitarbeiter kann diese Funktion bei Bedarf aktivieren. Bei eVars werden Pfade nicht berücksichtigt.
* **Potenziell verfügbare Metriken**: Welche Metriken bei Props und eVars verfügbar sind, hängt weitgehend von den Einstellungen und der Datenplattform/Version der Variablen ab. Die folgende Liste veranschaulicht, was aktiviert werden kann (nicht, was standardmäßig aktiviert ist). Wenn Sie eine bestimmte Metrik nicht finden, die Sie für Ihre Berichte wünschen, bitten Sie einen der unterstützen Benutzer, sich an den Kundendienst zu wenden.

<table id="table_FB963F60857A4AD79562324FB6F4B6A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Metrik </p> </th> 
   <th colname="col2" class="entry"> <p>Props </p> <p>(Traffic-Variablen) </p> </th> 
   <th colname="col3" class="entry"> <p>eVars </p> <p>(Konversionsvariablen) </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Durchschnittliche Klicktiefe </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_165C1BF1574247CEA9190ADCABF79D69" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durchschnittliche Besuchszeit </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_9F0F396E11B442959EC3E5D4D508496D" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Absprungrate </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_A268EAF747EA45F8A6A93A1B66667A06" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_09D486144CEA4293A505DCA3F90B82EC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Absprünge </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_471A02B78FD842BB97ED3FF4A5908B03" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_D2F11B5687484D9EBF6D1DEB3F303A20" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berechnete Metriken  </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_7FAB1CF2ACC44D9198C648D3FC9E52D9" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_8BCC2EE92CC04778809D1BD48D2623D7" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerspezifische Konversionsereignisse </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_D75C764B83AE4491A7E68C459FED1300" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Einstiege </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_E9A1FCDFCB924D75ABFAEBD5570D4EE0" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_F5E57974B5A64F3FA3A145428420EB23" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ausstiege </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_BE343F94EAD74D54B6ABC80E8A76A9BD" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_3183B2BB62C24B048EDED3295F2BEC85" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Instanzen </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_8733F5AC189E43DAA8D1847416EA68C8" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_B10AB2898F3D4EBA947FADB27B118143" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitenansichten </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_8BD2B23FBDA64A648BED40A2993F7C1C" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_CBDFD74340FA4973847033C1F956F0AC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beitragsmetriken </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_E63F978830FB46809E62654F37C4C182" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_6AB756A4598F4452887D29AD4971985A" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Einkaufsmetriken </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_8F8AB7CD02764245BA73CA1E6B69BAE1" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Neuladungen </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_FBE0C84E01004937B7B408198A33A9E7" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Einkaufswagen-Metriken </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_123993465D734EABB311730ED03263F6" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Einzelzugriff </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_038C6991E3F341B18E7A355D17C88895" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gesamtbesuchszeit </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_090587D29F1649319033D5A15B34B138" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_841DF09FD32A44B1B1B876F4E0CE29AC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unique Visitors </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_38556E6A43B04E2E8A01855452D30A83" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_F5D4BDE1AA9C4C58A6402418390EEC52" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Besuche </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_017BB279C5824028870360A5D4D27556" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_2832E346D220429DA643B908EC10260D" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

* **Aufschlüsselung**: Props verwenden Korrelationen, mit denen Seitenansichten für andere Traffic-Variablen angezeigt werden, die in derselben Bildanforderung ausgelöst werden. eVars verwenden Subrelationen, die eine Aufschlüsselung anderer Konversionsvariablen in Bezug auf Erfolgsereignisse bereitstellen.

## Vorteile von Eigenschaften oder eVars {#section_B384031AB8674065BA5187B0A3A3DAB9}

Mit der Veröffentlichung von Version 15 wurden die Unterschiede zwischen Eigenschaften und eVars deutlich verringert. Vor Kurzem wurden die eVars aktualisiert, sodass sie nun über Funktionen wie Besuche/Unique Visitor sowie Pfadverfolgungsmetriken verfügen und bei deren Verarbeitung eine minimale Belastung verursachen.

Die Eigenschaften verfügen über einige Vorteile im Vergleich zu eVars. Einige davon können umgangen werden:

* Eigenschaftsdaten werden bei der Berichterstellung sofort gesammelt und verfügbar gemacht. Bei eVars kann es bis zu 30 Minuten dauern, bis die Daten in der Report Suite angezeigt werden.
* Für alle Eigenschaften können flussdiagrammähnliche Berichte aktiviert werden, bei denen der Pfad ersichtlich wird, den Benutzer genommen haben. These pathing flow reports are available for both Props and eVars in [!UICONTROL Ad Hoc Analysis].
* Eigenschaften können auf mehreren Ebenen zusammenspielen, während eVars nur einmal untergeordnet verknüpft werden können. Diese Einschränkung kann durch die Verwendung einer Segmentierung umgangen werden, bei der identische Daten als Bezüge bereitgestellt werden.
* Beitragsmetriken ermöglichen die Anzeige der Eigenschaftswerte, die auf dem Weg zu einem Erfolgsereignis eine Rolle spielten.

eVars hingegen haben einige Vorteile gegenüber den Beschränkungen der Eigenschaften:

* eVars können Erfolgsereignisse als Metriken verwenden. Bei Eigenschaften ist das nicht möglich.
* Der Ablaufzeitpunkt von eVars kann vom Benutzer festgelegt werden, wobei auch ein Ablaufzeitpunkt für jeden Treffer eingeschlossen ist (keinerlei langlebige Werte). Eigenschaften bestehen in keinem Fall fort.

Pfadmetriken wie Gesamtbesuchszeit, Aufrufe und Schließvorgänge waren ursprünglich nicht für eVars verfügbar. Durch kürzlich erfolgte Aktualisierungen jedoch wurden diese Metriken für eVars verfügbar gemacht, was deren Wert steigerte.

## Welche Option soll ich verwenden? {#section_022D016A4EEB45179A15BFF044A261A4}

**Eigenschaften:** Wenn Sie sich hauptsächlich um die Wartezeit sorgen und ausschließlich Traffic (und keine Erfolgsereignisse) messen möchten, sollten Sie Eigenschaften verwenden.

**eVars:** Wenn Sie hauptsächlich Daten aufschlüsseln und Beziehungen erkennen möchten, sollten Sie eVars verwenden.

>[!TIP]
>
>Wenn Sie nicht möchten, dass eine evar beibehalten wird, können Sie den Ablauf auf "Treffer" ändern, damit keine Daten über den Treffer hinaus aufbewahrt werden.

