---
description: Seitenanalysen in Echtzeit (Livemodus) ermöglichen es Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.
title: Seitenanalysen in Echtzeit (Livemodus)
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: 29ccd89e-d82b-41d4-a940-addc6656b5ec
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 67%

---

# Seitenanalysen in Echtzeit (Livemodus)

Seitenanalysen in Echtzeit (Livemodus) ermöglichen es Ihnen, Ergebnisse mit genauen Details in Echtzeit zu erhalten.

Activity Map zeigt jetzt Analysedaten in 1-15-minütigen Schritten an, um die Beliebtheit von Links basierend auf Mikrotrends für ausgewählte Seiten zu überwachen. Es ist besonders wichtig für publizierende Unternehmen, das steigende oder sinkende Interesse an Beiträgen zu verfolgen, darauf zu reagieren und den Datenverkehr in Echtzeit zu überwachen.

Als Eigentümer des Inhalts einer Site gehört es zu Ihren Aufgaben, zu erkennen, wann Inhalt höhergestuft oder entfernt werden muss, um den Besuchern laufend interessanten Inhalt zu bieten. Echtzeit-Daten sind das A und O, um diese Aufgabe erfüllen zu können. Wenn Sie den aktuellen Trend für Links und Inhalt kennen, können Sie schnell und gezielt reagieren, um Leser und Kunden weiterhin an Ihre Marke zu binden.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

Wenn Sie überprüfen möchten, welches Element am häufigsten im Livemodus angeklickt wird:

1. Wählen Sie den Zeitraum in der Trendlinie **[!UICONTROL Livemodus]** der Symbolleiste aus, die Sie analysieren möchten.
1. Klicken Sie in der Symbolleiste auf das Symbol &quot;Auge&quot;, um auf die Tabelle &quot;Link-Bericht&quot;zuzugreifen.
1. Sortieren Sie die Tabelle nach dem Link.

## Datenlatenz als Folge der A4T-Konfiguration

Nachdem die [A4T-Integration](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) in Adobe Target aktiviert wurde, kommt es in Adobe Analytics zu einer zusätzlichen Latenz von 5 bis 10 Minuten. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus Analytics und Target für den gleichen Treffer, sodass Sie Tests nach Seite und Site-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in sämtlichen Services und Tools von Adobe Analytics wider, einschließlich Live-Stream und Echtzeit-Berichterstattung, und gilt für folgende Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.

Weitere Infos [hier](/help/analyze/activity-map/activitymap-standard-live.md).
