---
description: Seitenanalysen in Echtzeit (Livemodus) ermöglichen Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.
title: Seitenanalysen in Echtzeit (Livemodus)
topic: Activity map
uuid: a3faa9bd-73d8-48b3-be2b-f818ed7456fb
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Seitenanalysen in Echtzeit (Livemodus)

Seitenanalysen in Echtzeit (Livemodus) ermöglichen Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.

Activity Map zeigt jetzt Analysedaten in Inkrementen von 1 bis 15 Minuten an, um die Beliebtheit von Links basierend auf Micro-Trends für ausgewählte Seiten zu überwachen. Es ist besonders wichtig für publizierende Unternehmen, das steigende oder sinkende Interesse an Beiträgen zu verfolgen, darauf zu reagieren und den Datenverkehr in Echtzeit zu überwachen.

Als Eigentümer des Inhalts einer Site gehört es zu Ihren Aufgaben, zu erkennen, wann Inhalt höhergestuft oder entfernt werden muss, um den Besuchern laufend interessanten Inhalt zu bieten. Echtzeit-Daten sind das A und O, um diese Aufgabe erfüllen zu können. Wenn Sie den aktuellen Trend für Links und Inhalt kennen, können Sie schnell und gezielt reagieren, um Leser und Kunden weiterhin an Ihre Marke zu binden.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

## Datenlatenz als Folge der A4T-Konfiguration {#section_806CE36354FC4C539A0DED9266A5C704}

Nach Aktivierung der A4T-Integration in Adobe Target ist in Adobe Analytics eine zusätzliche Latenz von 5 bis 10 Minuten festzustellen. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus Analytics und Target für den gleichen Treffer, sodass Sie Tests nach Seite und Site-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in sämtlichen Services und Tools von Adobe Analytics wider, einschließlich Live-Stream und Echtzeit-Berichterstattung, und gilt für folgende Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/) beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.
