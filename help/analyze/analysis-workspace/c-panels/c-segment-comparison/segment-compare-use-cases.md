---
title: Anwendungsfälle für Segmentvergleiche
description: Erfahren Sie, wie Sie mithilfe des Segmentvergleichsfelds Einblicke in die Marketing-Strategie gewinnen können.
keywords: Segment IQ
feature: Panels
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 99%

---


# Anwendungsfälle für Segment IQ

Der Bereich für den Segmentvergleich ist eine häufig verwendete Funktion in Analysis Workspace. Kunden entdecken häufig neue Wege, damit Einblicke zu gewinnen. Im Folgenden werden einige erfolgreiche Anwendungsfälle aufgeführt.

## Anwendungsfall 1: Vergleich zwischen Mobile- und Desktop-Implementierung

> *„Wir haben zwei Seiten hinsichtlich der Hits verglichen und schnell einige Abweichungen beim Tagging festgestellt. So konnten wir Datenprobleme vor der Produktveröffentlichung vermeiden.“*

Ein Produkt-Manager, der für eine mobile Website und eine Desktop-Website zuständig ist, sollte sicherstellen, dass die Tags auf beiden Websites einheitlich waren. Um sicherzustellen, dass er nichts Wichtiges versäumt hatte, nutzte er das Fenster für den Segmentvergleich, um Hits von der mobilen Site mit Hits zu vergleichen, die von der Desktop-Site stammten. Er bemerkte, dass es auf der mobilen Website keine Checkout-Ereignisse gab, und implementierte die korrekten Tags vor der Veröffentlichung der mobilen Site. So konnte der Produkt-Manager vermeiden, dass die mobile Website keine Konversionen aufzeichnete, was zu einer Datenkatastrophe geführt hätte.

| Segment 1 | Segment 2 |
|--- |--- |
| Hit-Container, bei dem Mobilgerätetyp gleich Mobiltelefon oder Tablet ist | Alle anderen |

## Anwendungsfall 2: Vergleich zwischen Kunden, die eine bestimmte Funktion nutzen, und solchen, die sie nicht nutzen

> *„Wir stellten fest, dass Kunden, die unseren Produktvergleich nutzten, mit 10 % höherer Wahrscheinlichkeit konvertierten. Wir platzierten diese Funktion am Anfang der Seite. Dadurch stieg die Anzahl der Bestellungen um 4 %!“*

Das Optimierungs-Team einer Einzelhandels-Website wollte die Nutzer besser verstehen, die eine kürzlich veröffentlichte Produktvergleichsfunktion nutzten. Sie nutzten das Bedienfeld für den Segmentvergleich, um Benutzer, die die Produktvergleichsfunktion verwendeten, mit allen anderen auf der Site zu vergleichen. Sie fanden schnell einige wichtige Unterschiede, darunter die Tatsache, dass diese Nutzer mit 10 % höherer Wahrscheinlichkeit ein Produkt kauften. Das Optimierungs-Team entschied sich, versuchsweise die Produktvergleichsfunktion auffälliger am Anfang der Seite zu platzieren.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, in dem ein benutzerdefiniertes Ereignis (Preisvergleichswerkzeug) vorhanden ist | Alle anderen |

## Anwendungsfall 3: Vergleich zwischen Besuchern der News-Website und Besuchern anderer Website-Abschnitte

> *„Wir haben festgestellt, dass sich Besucher unseres News-Abschnitts mit doppelter Wahrscheinlichkeit Videoanzeigen ansehen. Deshalb haben wir in diesem Abschnitt mehr Videooptionen hinzugefügt. Dadurch sind die angesehenen Videoanzeigen um 7 % gestiegen!“*

Ein großer Medienverlag suchte nach Möglichkeiten, die Interaktion mit Inhalten durch Besucher seines News-Bereichs zu verbessern. Er erstellte ein Segment von Besuchern, die die News-Site besucht hatten, um die News-Zielgruppe besser zu verstehen. Sofort wurde festgestellt, dass diese Benutzer mit doppelt so hoher Wahrscheinlichkeit Videoanzeigen ansehen wie Besucher anderer Website-Bereiche. Das Video-Team erstellte in der Seitenleiste des News-Bereichs einen Abschnitt mit empfohlenen Videos und erzielte eine Steigerung der angesehenen Videoanzeigen um 7 %.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, bei dem der Website-Bereich „News“ entspricht | Alle anderen |

## Anwendungsfall 4: Vergleich zwischen Besuchern aus Paid Search und allen anderen

> *„Wir konnten bei Besuchern, die unsere Seite über Suchmaschinen erreicht hatten, mit dreimal höherer Wahrscheinlichkeit einen Upsell erzielen als bei allen anderen. Wir steigerten daher unsere Ausgaben für bestimmte Schlüsselwörter und erzielten eine Steigerung der Upsells um 56 %.“*

Ein großes B2B-Unternehmen wollte den Traffic besser verstehen, der durch Paid-Search-Suchbegriffe seine Website erreichte. Es hatte durch Paid Search nicht viele Konversionen direkt erzielt, und der Marketing-Leiter dachte darüber nach, das Budget dafür zu senken. Das Marketing-Team erstellte ein Segment mit Besuchern, die die Website über Paid Search erreicht hatten, und verglich sie mit dem Segmentvergleich mit allen anderen Besuchern. Das Ergebnis war, dass diese Besucher zwar weniger wahrscheinlich direkt konvertierten, aber mit dreimal höherer Wahrscheinlichkeit einen Upsell für eine zuvor gekaufte Dienstleistung erzielt werden konnte. Das Marketing-Team konzentrierte sein Budget auf Suchbegriffe im Zusammenhang mit Upselling und erzielte eine Steigerung der Upsells für Dienstleistungen um 56 %.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, bei dem der Typ der verweisenden Stelle „Paid Search“ ist | Alle anderen |

## Anwendungsfall 5: Vergleich zwischen Käufern von Fitbit und allen anderen

> *„Wir haben festgestellt, dass Käufer von Fitbits mit sechsmal höherer Wahrscheinlichkeit die Nachricht „Nicht vorrätig“ erhielten. Deshalb haben wir schnell mehr Fitbits bestellt und konnten die Nachfrage decken!“*

**Szenario:** Ein großes Online-Einzelhandelsunternehmen hatte die Absicht, herauszufinden, wie sich Fitbit – einer der beliebtesten Weihnachtsartikel – verkaufte und was Fitbit-Käufer von anderen Kunden unterschied. Das Marketingteam konnte einfach auf den Zeileneintrag „Fitbit“ im Produktbericht rechtsklicken und im Handumdrehen eine Segment-IQ-Analyse durchführen. Das Team fand heraus, dass Nutzer, die Fitbits kauften, mit sechsmal höherer Wahrscheinlichkeit die Nachricht „Nicht vorrätig“ erhielten als alle anderen Kunden. Nach weiteren Analysen konnte das Marketingteam diese Besucher an seine Ladengeschäfte verweisen, während es darauf wartete, dass die Einkaufsabteilung weitere Fitbits bestellte. So konnte das Unternehmen weitere Bestandslücken vermeiden und die Weihnachtsnachfrage besser decken.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, in dem Bestellungen vorhanden sind und benutzerdefinierte Dimension „Marke“ gleich „FitBit“ | Alle anderen |
