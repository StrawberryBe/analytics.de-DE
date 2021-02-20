---
description: Seitenanalysen in Echtzeit (Livemodus) ermöglichen es Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.
title: Seitenanalysen in Echtzeit (Livemodus)
topic: Activity map
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 72%

---


# Seitenanalyse in Echtzeit (Livemodus)

Seitenanalysen in Echtzeit (Livemodus) ermöglichen es Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.

Activity Map zeigt jetzt Analysedaten in Inkrementen von 1 bis 15 Minuten an, um die Linkpopularität basierend auf Mikrotrends für ausgewählte Seiten zu überwachen. Es ist besonders wichtig für publizierende Unternehmen, das steigende oder sinkende Interesse an Beiträgen zu verfolgen, darauf zu reagieren und den Datenverkehr in Echtzeit zu überwachen.

Als Eigentümer des Inhalts einer Site gehört es zu Ihren Aufgaben, zu erkennen, wann Inhalt höhergestuft oder entfernt werden muss, um den Besuchern laufend interessanten Inhalt zu bieten. Echtzeit-Daten sind das A und O, um diese Aufgabe erfüllen zu können. Wenn Sie den aktuellen Trend für Links und Inhalt kennen, können Sie schnell und gezielt reagieren, um Leser und Kunden weiterhin an Ihre Marke zu binden.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

Wenn Sie prüfen möchten, welches Element im Livemodus am häufigsten angeklickt wird:

1. Wählen Sie den Zeitraum in der Trendlinie **[!UICONTROL Livemodus]** der Symbolleiste aus, die Sie analysieren möchten.
1. Klicken Sie auf das Augensymbol in der Symbolleiste, um auf die Tabelle &quot;Linkbericht&quot;zuzugreifen.
1. Ordnen Sie die Tabelle über den Link an.

## Datenlatenz als Folge der A4T-Konfiguration

Nachdem die [A4T-Integration](https://docs.adobe.com/content/help/de-DE/target/using/integrate/a4t/a4t.html) in Adobe Target aktiviert ist, wird eine zusätzliche Latenz von 5-10 Minuten in Adobe Analytics auftreten. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus Analytics und Target für den gleichen Treffer, sodass Sie Tests nach Seite und Site-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in sämtlichen Services und Tools von Adobe Analytics wider, einschließlich Live-Stream und Echtzeit-Berichterstattung, und gilt für folgende Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des [Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.

Weitere Informationen [hier](/help/analyze/activity-map/activitymap-standard-live.md).