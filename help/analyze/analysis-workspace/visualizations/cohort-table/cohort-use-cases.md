---
description: Anwendungsfälle für die Kohortenanalyse.
keywords: Analysis Workspace
title: Anwendungsfälle für die Kohortenanalyse
topic: Reports and analytics
uuid: 5ec46f84-5702-4bc1-a796-874a3abe87c9
translation-type: tm+mt
source-git-commit: 79849c574909543d74e2935e493008927700585d
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 74%

---


# [!UICONTROL Anwendungsfälle] der Kohorte

Use case examples for [!UICONTROL Cohort Analysis].

## Anwendungsfall: App-Nutzung {#section_ADEC6EE79F1846319B2E0D9544CC5E40}

Angenommen Sie möchten herausfinden, wie Benutzer, die Ihre Anwendung installieren, im Laufe der Zeit damit interagieren. Installieren sie die Anwendung, benutzen sie aber nie? Benutzen sie die Anwendung eine Zeit lang und hören dann auf? Oder bleiben Sie die ganze Zeit dabei?

You can create a six-month [!UICONTROL Cohort Analysis]:

**Granularität**: Monatlich, von Januar 2015 bis Juni 2015

**Aufnahmemetrik**: Anwendungsinstallationen

**Rückkehrmetrik**: Sitzungen oder Starts

Besucher zählen in den nachfolgenden Monaten erst dann als  *`engaged`*, wenn eine Sitzung stattgefunden hat oder wenn sie die App gestartet haben. [!UICONTROL Die Analyse] der Kohorte zeigt Ihnen dann Nutzungsmuster an, die *`App Install`* immer am 0. Monat auftreten. Vielleicht stellen Sie fest, dass die Verwendung im zweiten Monat zurückgeht, unabhängig vom Zeitpunkt der Installation der Anwendung durch die Benutzer. (Für diejenigen, die die Anwendung im Januar 2015 installiert haben, ist der zweite Monat der März 2015. Für diejenigen, die die Anwendung im Februar 2015 installiert haben, ist der zweite Monat der April 2015 usw.) Diese Analyse bietet Ihnen die Möglichkeit, im zweiten Monat nach der Installation der Anwendung an alle Benutzer eine E-Mail oder eine Push-Nachricht zu senden, um sie daran zu erinnern, die Anwendung zu verwenden.

## Anwendungsfall: Abonnement {#section_FDECB16766CF415BB84AE46BA491FB5F}

Sie arbeiten bei Adobe.com und bieten ein kostenloses Creative Cloud-Abonnement an. Das Ziel besteht darin, dass die Benutzer ein Upgrade von der kostenlosen Version auf das 30-tägige Probe-Abo oder letztlich auf die zahlungspflichtige Version durchführen.

**Granularität**: Monatlich

**Aufnahmemetrik**: Download-Link

**Rückkehrmetrik**: Kauf der zahlungspflichtigen Creative Cloud

Using this [!UICONTROL Cohort Analysis], you could see, for example, that anywhere between 8% and 10% of free Creative Cloud users upgrade in the first month after installation, regardless of when they installed. 12–15 % führen im zweiten Monat der Verwendung ein Upgrade durch. Danach lassen die Upgrades merklich nach: 4–5 % im dritten Monat, 3–4 % im vierten Monat und 1–2 % im fünften Monat.

Da deutlich wird, dass Sie im dritten Monat keine potenziellen Kunden verlieren sollten, richten Sie eine E-Mail-Kampagne ein, die in der Mitte des dritten Monats an eine Stichprobe der Benutzer herausgeht und Benutzern, die noch kein Upgrade durchgeführt haben, einen Gutschein über 50 $ anbietet.

Einige Monate später erstellen Sie erneut einen Kohortenanalysebericht. Für Kohorten, die nach dem Start der Kampagne gebildet wurden, ist die Konversion zu zahlungspflichtigen Creative Cloud-Abonnements von 4–5 % auf 13–14 % gestiegen, was pro Kohorte für mehrere hunderttausend Dollar steht, für alle monatlichen Kohorten, die ab diesem Punkt den dritten Monat erreichen.

## Anwendungsfall für komplexe Kohortensegmente

Eine große Hotelkette zielt auf mehrere Kundengruppen für Promotionen ab und verfolgt sie auf Grundlage der Leistung nach. Um die besten Gruppen von Benutzerkohorten für die Zielgruppe zu identifizieren, sollen sehr spezifische Kohortengruppen gebildet werden. Using the augmented [!UICONTROL Inclusion] and [!UICONTROL Return] Criteria within [!UICONTROL Cohort] Tables, they are able to define just the right cohort groupings with multiple metrics and segments to identify underperforming customers groups in order to target them with promotions and deals to increase bookings.

## Anwendungsfall zur Annahme der App-Version

Bei einem großen Versicherungsunternehmen wird ein großer Teil der Kundeninteraktion über die Nutzung der mobilen Anwendung gefördert. Da jedoch immer wieder neue Funktionen zur App hinzugefügt werden, ist es wichtig, dass die Kunden eine Aktualisierung auf die neueste App-Version durchführen. They can analyze and compare all of their app versions side-by-side using [!UICONTROL Custom Dimension] Cohort to see which customers on which app version to target. Darüber hinaus können sowohl die Bindung als auch die Abwanderung verfolgt werden, um festzustellen, ob bestimmte App-Versionen Kunden davon abhalten, die App im Laufe der Zeit zu nutzen. Durch mobiles Messaging kann eine erneute Interaktion mit solchen Benutzern stattfinden, damit diese eine Aktualisierung auf die neueste Version durchführen, um die Vorteile der neuesten Funktionen nutzen zu können.

## Anwendungsfall zur Kampagnentreue

Ein internationales Medienunternehmen verwendet Zielgruppen-Kampagnen, um Benutzer auf die verschiedenen Plattformen zu leiten und so die Interaktion zu fördern. Die Werbeausgaben pro Plattform basieren auf der Kundeninteraktion und -bindung, daher sind erfolgreiche Kampagnen entscheidend für den Erfolg des Unternehmens. They use our new [!UICONTROL Custom Dimension] Cohort feature in [!UICONTROL Cohort] Tables to compare various campaigns side-by-side to identify which campaigns are most effective at acquiring and retaining users to increase engagement. Sie können dann herausfinden, welche Aspekte eine Kampagne erfolgreich machen, und sie auf andere Kampagnen anwenden, um die Interaktion über ihre verschiedenen Plattformen hinweg zu steigern.

## Anwendungsfall für Produktstart

Ein großer Kleidungseinzelhändler verfügt über viele spezifische Kundensegmente, durch die große Teile des Unternehmensumsatzes gefördert werden. Für jedes Segment werden spezifische Produkte unter Berücksichtigung des jeweiligen Segments entwickelt und hergestellt. Mit jedem Produkt-Launch soll identifiziert werden, wie das neue Produkt im Laufe der Zeit den Verkauf in verschiedenen Kohorten gefördert hat. Using the new [!UICONTROL Latency Table] setting in [!UICONTROL Cohort Analysis], they are able to analyze a given customer segment&#39;s pre-launch and post-launch behavior and revenue. Anhand dieser Informationen kann festgestellt werden, durch welche Produkte neue Umsätze generiert werden und welche bei den Kunden weniger beliebt sind.

## Anwendungsfall für individuelle Treue – die meisten treuen Benutzer  Anwendungsfall

Bei einer großen Fluggesellschaft hängt der Erfolg und Umsatz zu einem großen Teil von wiederkehrenden und treuen Kunden ab. In vielen Fällen machen treue Reisende den Großteil des Umsatzes aus und die Bindung dieser Kunden ist entscheidend für den langfristigen Erfolg. Oft kann es sich schwierig gestalten herauszufinden, welche die treuesten und beständigsten Kunden sind. However, using the new [!UICONTROL Rolling Calculation] setting in [!UICONTROL Cohort Analysis], they were able to analyze loyal customer segments and find out which travelers were repeat purchasers month-over-month. So konnten diese Reisenden dann mit Vorteilen und Vergünstigungen für ihre Treue belohnt werden. Darüber hinaus konnte durch die Umstellung des Kohortentyps von Bindung auf Abwanderung auch Monat für Monat festgestellt werden, welche Reisenden nicht erneut Kunden waren, um diese Segmente mit Promotionen anzusprechen, die Interaktion mit diesen Kunden so wieder herzustellen und sicherzustellen, dass sie auch in Zukunft treue Kunden bleiben.
