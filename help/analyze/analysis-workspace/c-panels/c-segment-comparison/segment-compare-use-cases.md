---
description: Segment-IQ (Segmentvergleich) ist eine der meistgenutzten Funktionen in Analysis Workspace. Kunden finden damit immer wieder neue, innovative Möglichkeiten für Einblicke. Hier ist eine kleine Auswahl erfolgreicher Anwendungsfälle.
keywords: Segment-IQ
seo-description: Segment-IQ (Segmentvergleich) ist eine der meistgenutzten Funktionen in Analysis Workspace. Kunden finden damit immer wieder neue, innovative Möglichkeiten für Einblicke. Hier ist eine kleine Auswahl erfolgreicher Anwendungsfälle.
seo-title: Verwendungsfälle für Segmente in Segment
title: Verwendungsfälle für Segmente in Segment
uuid: 2 a 98 b 96 b -5529-4 c 7 f-a 787-27920603 d 5 b 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verwendungsfälle für Segmente in Segment

Segment-IQ (Segmentvergleich) ist eine der meistgenutzten Funktionen in Analysis Workspace. Kunden finden damit immer wieder neue, innovative Möglichkeiten für Einblicke. Hier ist eine kleine Auswahl erfolgreicher Anwendungsfälle.

## Use case 1: compare mobile vs desktop implementations {#section_B3A5983E58D0470895C030EA527C4966}

**„Wir haben zwei Seiten hinsichtlich der Treffer verglichen und schnell einige Abweichungen beim Tagging festgestellt. So konnten wir Datenprobleme vor der Produktveröffentlichung vermeiden.“**

**Szenario**: Ein Produkt-Manager, der für eine mobile Website und eine Desktop-Website zuständig ist, sollte sicherstellen, dass die Tags auf beiden Websites einheitlich waren. Um sich zu vergewissern, dass er nichts Wichtiges übersehen hatte, verglich er mit Segment-IQ die Treffer von der mobilen Website mit denen von der Desktop-Website. Er bemerkte, dass er vergessen hatte, das Checkout-Ereignis auf der mobilen Website zu taggen und konnte vor der Veröffentlichung der Website die richtigen Tags platzieren. So konnte der Produktmanager vermeiden, dass die mobile Website keine Konversionen aufzeichnete, was zu einer Datenkatastrophe geführt hätte.

**So richten Sie diesen Vergleich ein:**

<table id="table_B5FA23CB34DE4331A8BD65ED4B351038"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Segment 1 </th> 
   <th colname="col3" class="entry"> Segment 2 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verwenden/erstellen Sie ein Segment auf Trefferebene, in dem </p> <p> </p> <p> 
     <ul id="ul_1F5D5136620E449D93A771CD2576A18A"> 
      <li id="li_CB32DD1033DA4E5CA3B9AD41030800E6">„Mobilgerätetyp“ „Mobiltelefon“ oder „Tablet“ lautet </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Verwenden/erstellen Sie ein Segment auf Trefferebene, in dem </p> <p> </p> <p> 
     <ul id="ul_79CC51C4C9494275B3F37B6D2AB0505E"> 
      <li id="li_83BE21AD1FB34195BAFF3F15421DBB3D">„Mobilgerätetyp“ nicht „Mobiltelefon“ oder „Tablet“ lautet </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Use case 2: compare customers who use a certain feature to those who don't {#section_878B08FDD70A45E186C1F28EBA296636}

**„Wir stellten fest, dass Kunden, die unseren Produktvergleich nutzten, mit 10 % höherer Wahrscheinlichkeit konvertierten. Wir platzierten diese Funktion am Anfang der Seite. Dadurch stieg die Anzahl der Bestellungen um 4 %!“**

**Szenario** Das Optimierungsteam eines Online-Shops wollte die Nutzer besser verstehen, die eine kürzlich veröffentlichte Produktvergleichsfunktion nutzten. Sie erstellten ein Segment mit Besuchern, die diese Funktion genutzt hatten, und konnten so mit Segment-IQ diese Nutzer mit allen anderen Besuchern der Website vergleichen. Segment-IQ fand schnell einige wichtige Unterschiede, darunter die Tatsache, dass diese Nutzer mit 10 % höherer Wahrscheinlichkeit ein Produkt kauften. Das Optimierungsteam entschied sich, versuchsweise die Produktvergleichsfunktion auffälliger am Anfang der Seite zu platzieren.

**So richten Sie diesen Vergleich ein:**

| Segment 1 | Segment 2 |
|--- |--- |
| Verwenden/erstellen Sie ein Segment auf Besucherebene mit Besuchern, die mit der Preisvergleichsfunktion interagiert haben. | Verwenden Sie das automatisch erzeugte Segment Alle anderen, das alle Besucher enthält, die nicht in Segment 1 enthalten sind. |

## Use case 3: compare news site visitors to other site section visitors {#section_0EAFC90C450244058B161200AC9901B8}

**„Wir haben festgestellt, dass sich Besucher unseres News-Abschnitts mit doppelter Wahrscheinlichkeit Videoanzeigen ansehen. Deshalb haben wir in diesem Abschnitt mehr Videooptionen hinzugefügt. Dadurch sind die angesehenen Videoanzeigen um 7 % gestiegen!“**

**Szenario:** Ein großer Medienverlag suchte nach Möglichkeiten, die Interaktion mit Inhalten durch Besucher des News-Bereichs zu verbessern. Um die News-Zielgruppe besser zu verstehen, erstellte das Unternehmen ein Segment mit Besuchern, die den News-Bereich der Website besucht hatten. Segment-IQ analysierte jede Metrik und Dimension und fand sofort heraus, dass diese Nutzer sich mit doppelter Wahrscheinlichkeit wie Besucher anderer Website-Bereiche Videoanzeigen ansahen. Das Video-Team erstellte in der Seitenleiste des News-Bereichs einen Abschnitt mit empfohlenen Videos und erzielte eine Steigerung der angesehenen Videoanzeigen um 7 %. So konnten im Vergleich mit anderen möglichen Maßnahmen mit wenig Aufwand schnelle, messbare Ergebnisse erzielt werden.

**So richten Sie diesen Vergleich ein:**

| Segment 1 | Segment 2 |
|--- |--- |
| Verwenden/erstellen Sie ein Segment auf Besucherebene mit Besuchern des News-Bereichs. | Verwenden Sie das automatisch erzeugte Segment Alle anderen, das alle Besucher enthält, die nicht in Segment 1 enthalten sind. |

## Use case 4: compare visitors from paid search to everyone else {#section_73912670409349CAB131FE9D8B4FB11C}

**„Wir konnten bei Besuchern, die unsere Seite über Suchmaschinen erreicht hatten, mit dreimal höherer Wahrscheinlichkeit einen Up-Sell erzielen als bei allen anderen. Wir steigerten daher unsere Ausgaben für bestimmte Schlüsselwörter und erzielten eine Steigerung der Up-Sells um 56 %.“**

**Szenario:** Ein großes B2B-Unternehmen hatte die Absicht, den Traffic besser zu verstehen, der durch bezahlte Suchbegriffe auf die Website gelangte. Es hatte durch bezahlte Suchbegriffe nicht viele Konversionen direkt erzielt, und der Marketingleiter dachte darüber nach, das Budget dafür zu senken. Das Marketingteam erstellte ein Segment mit Besuchern, die die Website über einen bezahlten Suchbegriff erreicht hatten, und verglich sie mit Segment-IQ mit allen anderen Besuchern. Das Ergebnis war, dass diese Besucher zwar weniger wahrscheinlich direkt konvertierten, aber mit dreimal höherer Wahrscheinlichkeit ein Up-Sell für eine zuvor gekaufte Dienstleistung erzielt werden konnte. Das Marketingteam konzentrierte sein Budget auf Suchbegriffe im Zusammenhang mit Up-Selling und erzielte eine Steigerung der Up-Sells für Dienstleistungen um 56 %.

**So richten Sie diesen Vergleich ein:**

| Segment 1 | Segment 2 |
|--- |--- |
| Verwenden/erstellen Sie ein Segment auf Besucherebene für Besucher, die die Website durch eine kostenlose Suche oder eine SEM-Kampagne erreicht haben. | Verwenden Sie das automatisch erzeugte Segment Alle anderen, das alle Besucher enthält, die nicht in Segment 1 enthalten sind. |

## Use case 5: compare Fitbit purchasers to everyone else {#section_9142B8A270764545B0A516AA309F1785}

**„Wir haben festgestellt, dass Käufer von Fitbits mit sechsmal höherer Wahrscheinlichkeit die Nachricht „Nicht vorrätig“ erhielten. Deshalb haben wir schnell mehr Fitbits bestellt und konnten die Nachfrage decken!“**

**Szenario:** Ein großer Online-Händler wollte daran interessiert sein, wie einer der heimarischen Urlaubsprodukte - "Fitbit -" verkauft und die ersten Kunden einzigartig waren. Das Marketingteam konnte einfach auf den Zeileneintrag „Fitbit“ im Produktbericht rechtsklicken und im Handumdrehen eine Segment-IQ-Analyse durchführen. Das Team fand heraus, dass Nutzer, die Fitbits kauften, mit sechsmal höherer Wahrscheinlichkeit die Nachricht „Nicht vorrätig“ erhielten als alle anderen Kunden. Nach weiteren Analysen konnte das Marketingteam diese Besucher an seine Ladengeschäfte verweisen, während es darauf wartete, dass die Einkaufsabteilung weitere Fitbits bestellte. So konnte das Unternehmen weitere Bestandslücken vermeiden und die Weihnachtsnachfrage besser decken.

**So richten Sie diesen Vergleich ein:**

<table id="table_9018BEB4C2DE429FA773B250CB5C3E58"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Segment 1 </th> 
   <th colname="col3" class="entry"> Segment 2 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verwenden/erstellen Sie ein Segment auf Besucherebene, in dem </p> <p> 
     <ul id="ul_52E8ED6F4F7241D5ABE4EE7EA1E556D8"> 
      <li id="li_33750601AB2A43728834B29AF86D5CCF">„Bestellungen“ größer oder gleich 1 ist UND </li> 
      <li id="li_4E09D1286DAE4BABA49E4834E73BDC28">die Marke „Fitbit“ lautet </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Verwenden Sie das automatisch erzeugte Segment <span class="wintitle">Alle anderen</span>, das alle Besucher enthält, die nicht in Segment 1 enthalten sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

