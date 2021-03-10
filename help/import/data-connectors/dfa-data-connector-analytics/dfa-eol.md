---
title: DFA-Integration - Informationen zum Ende des Lebenszyklus
description: Warum ist der DFA Data Connector mit der Adobe beendet und welche Alternativen gibt es?
translation-type: tm+mt
source-git-commit: 6669f678c1327b6af4a5b67c8033a9b7d8c9dbcf
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 1%

---


# DFA-Integration - Informationen zum Ende des Lebenszyklus

Adobe kündigte vor kurzem [ihre Pläne für den End-of-Life Data Connector](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/data-connectors-eol.html) an, einen alten Werkzeugsatz zur Integration von Drittanbieterdaten (z. B. ESP, VOC usw.) mit Adobe Analytics.

## Warum gehen Data Connectors in das Ende der Lebensdauer?

Die unterstützte Plattform für die Partnerintegration ist [Adobe Exchange](https://exchange.adobe.com/experiencecloud), die die Integration von Adobe Digital Experience-Anwendungen, die Integration von Drittanbietern CXM und die Unterstützung der verschiedenen Datenanforderungen von Kunden und Partnern bis weit in die Zukunft erleichtern soll. Viele Partner, die ihre Integrationen mithilfe von Data Connectors erstellt haben, haben diese Integrationen bereits zu Adobe Exchange migriert, und weitere Partner planen dies.

## Warum wird die DFA-Integration in das Ende des Lebenszyklus integriert?

In [Januar 2020 gab Google bekannt, dass es bis 2022 Drittanbieter-Cookies in Chrome auslaufen lassen wird. ](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html) Dies entspricht den Branchenstandards, die Apple und Mozilla für ihre Safari- bzw. Firefox-Browser festgelegt haben. Die DFA-Integration beruht in hohem Maße auf Drittanbieter-Cookies und wird daher mit der Entfernung von Drittanbieter-Cookies in den drei wichtigsten Internetbrowsern ineffektiv und überholt sein. Google [hat diese Haltung im März 2021](https://blog.google/products/ads-commerce/a-more-privacy-first-web) durch die Ankündigung verstärkt, dass keine alternative Lösung veröffentlicht wird.

Leider Google — im Besitz der DFA-Integration — Es ist unwahrscheinlich, dass es auf der Adobe Exchange-Plattform replizieren. Daher gehen wir weiter unter der Annahme, dass die bestehende Integration nach dem Offline-Betrieb von Data Connectors nicht mehr funktioniert und keinen produktiven Ersatz mehr hat.

Ein wichtiger und zusätzlicher Faktor ist die &quot;Ansicht-through&quot;-Funktion der DFA-Integration. Dadurch kann Adobe Analytics Fälle nachverfolgen, in denen ein Benutzer eine Anzeige sah, nicht klickte, aber später die Website besuchte. &quot;Durchklickraten&quot;basieren auf Drittanbieter-Cookies, die im Laufe des Jahres 2021 schrittweise eingestellt werden. Das ist eine marktweite Frage, nicht nur eine Frage der Adobe. Derzeit gibt es keine Alternativen zur Replizierung dieser Daten.

## Welche Alternativen gibt es für Sie?

Für Kunden, die an der Integration von Display-Anzeigendaten (ohne &quot;Ansicht-through&quot;) in Adobe Analytics interessiert sind, stehen derzeit die folgenden Optionen zur Verfügung:

* Adobe Advertising Cloud DSP-Kunden können [eine produktive Integration mit Adobe Analytics](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/introduction-to-the-analytics-for-advertising-cloud-dsp-integration.html?lang=en#integrations) nutzen, um Display-Anzeigendaten von Google auf Adobe Analytics festzulegen. Diese Integration ist unsere beste Alternative und wäre unsere Empfehlung an die Kunden. Die Ad Cloud-DSP ermöglicht es Kunden, über alle Kanal der Werbung, einschließlich gebührenpflichtiger Suche, Anzeige, Video und andere, miteinander verbundene Erlebnisse bereitzustellen. [Weitere Informationen](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/introduction/dsp-about.html?lang=en#introduction). Die DSP der Ad Cloud wird jedoch auch durch den Verlust von Drittanbieter-Cookies beeinträchtigt.
* Adobe Experience Platform und [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=en), die Funktionen zur Integration von Display-Anzeigen in andere Datenquellen bereitstellen. Kunden können ihre Anzeigedaten von ihrem gebührenpflichtigen Suchanbieter herunterladen und in die Experience Platform hochladen. Anschließend bringen sie die Daten direkt in CJA ein, um sie zusammen mit ihren anderen Datensätzen zu analysieren.
* Adobe Consulting (Engineering Architects) kann eine benutzerdefinierte Lösung zum Erfassen von Anzeigenmetriken in Adobe Analytics entwickeln. Diese Lösung befindet sich noch in der Entwicklung und alle Kunden, die an der Beta-Teilnahme interessiert sind, sind herzlich willkommen. Weitere Details zu Funktionen, Verfügbarkeit und Kosten werden bereitgestellt, sobald sie verfügbar sind.
* Sie können Ihre eigene Display-Anzeigenintegration verwalten, indem Sie die Data Sources-Funktionalität sowie Classifications in Adobe Analytics verwenden. Importieren Sie Ihre gebührenpflichtigen Such- und Anzeigedaten manuell mit Data Sources and Classifications [wie hier beschrieben. ](https://experienceleague.adobe.com/docs/analytics/import/use-cases/paid-search-metrics.html?lang=en#use-cases) (Hinweis: Dieses Dokument bezieht sich auf die gebührenpflichtige Suche, aber der Verwendungsfall und das Konzept sind identisch und können auf die Anzeige angewendet werden).

Für weitere Fragen oder Support wenden Sie sich bitte an den [Adobe Kundendienst](https://helpx.adobe.com/de/contact/enterprise-support.ec.html).