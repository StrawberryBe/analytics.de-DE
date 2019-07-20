---
description: Beispiele für Anwendungsfälle für die Kohortenanalyse.
keywords: Analysis Workspace
seo-description: Beispiele für Anwendungsfälle für die Kohortenanalyse.
seo-title: Anwendungsfälle für Kohortenanalyse
solution: Analytics
title: Anwendungsfälle für Kohortenanalyse
topic: Reports and Analytics
uuid: 5 ec 46 f 84-5702-4 bc 1-a 796-874 a 3 abe 87 c 9
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Anwendungsfälle für Kohortenanalyse

Beispiele für Anwendungsfälle für die Kohortenanalyse.

## App engagement use case {#section_ADEC6EE79F1846319B2E0D9544CC5E40}

Angenommen Sie möchten herausfinden, wie Benutzer, die Ihre Anwendung installieren, im Laufe der Zeit damit interagieren. Installieren sie die Anwendung, benutzen sie aber nie? Benutzen sie die Anwendung eine Zeit lang und hören dann auf? Oder bleiben Sie die ganze Zeit dabei?

Sie können eine Kohortenanalyse über sechs Monate erstellen

**Granularität**: Monatlich, von Januar 2015 bis Juni 2015.

**Aufnahmemetrik**: Anwendungsinstallationen

**Rückkehrmetrik**: Sitzungen oder Starts

Besucher zählen in den nachfolgenden Monaten erst dann als *`engaged`*, wenn eine Sitzung stattgefunden hat oder wenn sie die Anwendung gestartet haben. Cohort analysis would then show you patterns in usage where *`App Install`* always occurs on Month 0. Vielleicht stellen Sie fest, dass die Verwendung im zweiten Monat zurückgeht, unabhängig vom Zeitpunkt der Installation der Anwendung durch die Benutzer. (Für diejenigen, die die Anwendung im Januar 2015 installiert haben, ist der zweite Monat der März 2015. Für diejenigen, die die Anwendung im Februar 2015 installiert haben, ist der zweite Monat der April 2015 usw.) Diese Analyse bietet Ihnen die Möglichkeit, im zweiten Monat nach der Installation der Anwendung an alle Benutzer eine E-Mail oder eine Push-Nachricht zu senden, um sie daran zu erinnern, die Anwendung zu verwenden.

## Subscription use case {#section_FDECB16766CF415BB84AE46BA491FB5F}

Sie arbeiten bei Adobe.com und bieten ein kostenloses Creative Cloud-Abonnement an. Das Ziel besteht darin, dass die Benutzer ein Upgrade von der kostenlosen Version auf das 30-tägige Probe-Abo oder letztlich auf die zahlungspflichtige Version durchführen.

**Granularität**: Monatlich

**Aufnahmemetrik**: Download-Link

**Rückkehrmetrik**: Kauf der zahlungspflichtigen Creative Cloud

Mithilfe dieser Kohortenanalyse könnten Sie z. B. sehen, dass zwischen 8 % und 10 % der Benutzer der kostenlosen Creative Cloud-Version im ersten Monat nach der Installation ein Upgrade durchführen, unabhängig vom Zeitpunkt der Installation. 12–15 % führen im zweiten Monat der Verwendung ein Upgrade durch. Danach lassen die Upgrades merklich nach: 4–5 % im dritten Monat, 3–4 % im vierten Monat und 1–2 % im fünften Monat.

Da deutlich wird, dass Sie im dritten Monat keine potenziellen Kunden verlieren sollten, richten Sie eine E-Mail-Kampagne ein, die in der Mitte des dritten Monats an eine Stichprobe der Benutzer herausgeht und Benutzern, die noch kein Upgrade durchgeführt haben, einen Gutschein über 50 $ anbietet.

Einige Monate später erstellen Sie erneut einen Kohortenanalysebericht. Für Kohorten, die nach dem Start der Kampagne gebildet wurden, ist die Konversion zu zahlungspflichtigen Creative Cloud-Abonnements von 4–5 % auf 13–14 % gestiegen, was pro Kohorte für mehrere hunderttausend Dollar steht, für alle monatlichen Kohorten, die ab diesem Punkt den dritten Monat erreichen.

## Komplexe Kohorte-Segmente verwenden Groß- und Kleinschreibung

Eine große Hotelkette zielt auf mehrere Kundengruppen für Promotionen ab und verfolgt sie auf Grundlage der Leistung nach. Um die besten Gruppen von Benutzerkohorten für die Zielgruppe zu identifizieren, sollen sehr spezifische Kohortengruppen gebildet werden. Mithilfe der erweiterten Aufnahme- und Rückkehrkriterien innerhalb der Kohortentabellen können genau die richtigen Kohortengruppierungen mit mehreren Kennzahlen und Segmenten definiert werden, um leistungsschwache Kundengruppen zu identifizieren und diese mit Promotionen und Angeboten zur Steigerung der Buchungen anzusprechen.

## Verwendungsfall für Anwendungsversion App

Bei einem großen Versicherungsunternehmen wird ein großer Teil der Kundeninteraktion über die Nutzung der mobilen Anwendung gefördert. Da jedoch immer wieder neue Funktionen zur App hinzugefügt werden, ist es wichtig, dass die Kunden eine Aktualisierung auf die neueste App-Version durchführen. Sie können alle App-Versionen mithilfe der angepassten Dimensionskohorte gegeneinander analysieren und miteinander vergleichen, um zu sehen, auf welche Kunden mit welcher App-Version abgezielt werden sollte. Darüber hinaus können sowohl die Bindung als auch die Abwanderung verfolgt werden, um festzustellen, ob bestimmte App-Versionen Kunden davon abhalten, die App im Laufe der Zeit zu nutzen. Durch mobiles Messaging kann eine erneute Interaktion mit solchen Benutzern stattfinden, damit diese eine Aktualisierung auf die neueste Version durchführen, um die Vorteile der neuesten Funktionen nutzen zu können.

## Verwendungsfall für Kampagnenstickiness

Ein internationales Medienunternehmen verwendet Zielgruppen-Kampagnen, um Benutzer auf die verschiedenen Plattformen zu leiten und so die Interaktion zu fördern. Die Werbeausgaben pro Plattform basieren auf der Kundeninteraktion und -bindung, daher sind erfolgreiche Kampagnen entscheidend für den Erfolg des Unternehmens. Unsere neue Funktion der angepassten Dimensionskohorte in Kohortentabellen wird verwendet, um verschiedene Kampagnen nebeneinander zu vergleichen und herauszufinden, welche Kampagnen am effektivsten sind, um Benutzer zu gewinnen und zu binden und so die Interaktion zu fördern. Anschließend kann festgestellt werden, welche Aspekte zum Erfolg einer Kampagne beitragen. Diese Erkenntnisse können dann auf andere Kampagnen angewendet werden, um die Interaktion auf den verschiedenen Plattformen zu fördern..

## Verwendungsfall des Produkts

Ein großer Kleidungseinzelhändler verfügt über viele spezifische Kundensegmente, durch die große Teile des Unternehmensumsatzes gefördert werden. Für jedes Segment werden spezifische Produkte unter Berücksichtigung des jeweiligen Segments entwickelt und hergestellt. Mit jedem Produkt-Launch soll identifiziert werden, wie das neue Produkt im Laufe der Zeit den Verkauf in verschiedenen Kohorten gefördert hat. Mit der neuen Einstellung der Latenztabelle in Kohortentabellen können das Verhalten und der Umsatz eines bestimmten Kundensegments vor und nach der Markteinführung analysiert werden. Anhand dieser Informationen kann festgestellt werden, durch welche Produkte neue Umsätze generiert werden und welche bei den Kunden weniger beliebt sind.

## Individuelle Treue – die meisten treuen Benutzer Anwendungsfall

Bei einer großen Fluggesellschaft hängt der Erfolg und Umsatz zu einem großen Teil von wiederkehrenden und treuen Kunden ab. In vielen Fällen machen treue Reisende den Großteil des Umsatzes aus und die Bindung dieser Kunden ist entscheidend für den langfristigen Erfolg. Oft kann es sich schwierig gestalten herauszufinden, welche die treuesten und beständigsten Kunden sind. Mit der neuen Einstellung der rollierenden Berechnung in den Kohortentabellen konnten jedoch Segmente treuer Kunden analysiert und Monat für Monat bestimmt werden, welche Reisenden erneut Kunden waren. So konnten diese Reisenden dann mit Vorteilen und Vergünstigungen für ihre Treue belohnt werden. Darüber hinaus konnte durch die Umstellung des Kohortentyps von Bindung auf Abwanderung auch Monat für Monat festgestellt werden, welche Reisenden nicht erneut Kunden waren, um diese Segmente mit Promotionen anzusprechen, die Interaktion mit diesen Kunden so wieder herzustellen und sicherzustellen, dass sie auch in Zukunft treue Kunden bleiben.