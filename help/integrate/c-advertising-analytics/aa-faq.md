---
description: Häufig gestellte Fragen zu Advertising Analytics.
title: Häufig gestellte Fragen zu Werbeanalysen
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: c947de8eaa4e4dc3a0c10989ef6ae450cebc1f3e
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 36%

---

# Häufig gestellte Fragen

## Zugriff/Berechtigungen {#access}

+++ Muss ich Adobe Advertising Cloud- oder Adobe Advertising Cloud-Kunde (AMO) sein, um auf diese Funktion zugreifen zu können?

Nein, diese Funktion ist für Nicht-Advertising Cloud- und Nicht-AMO-Kunden verfügbar. </p> <p>AMO-Kunden können die bestehende Analytics-AMO-Integration nutzen, jedoch nicht Advertising Analytics verwenden.

+++

+++ Welche Adobe Analytics-SKUs berechtigen zur Verwendung von Advertising Analytics?

Advertising Analytics ist für Adobe Analytics verfügbar

* [Auswählen](https://www.adobe.com/de/data-analytics-cloud/analytics/select.html)

* [Prime](https://www.adobe.com/de/data-analytics-cloud/analytics/prime.html)

* [Ultimate](https://www.adobe.com/de/data-analytics-cloud/analytics/ultimate.html)

+++

+++ Muss ich für die Nutzung von Advertising Analytics extra bezahlen?

Nein, außerhalb der richtigen SKU-Bereitstellung verursacht Advertising Analytics keine zusätzlichen Kosten.

+++

+++ Zählt Advertising Analytics die Nutzung meiner Server-Aufrufe?

Nein, Advertising Analytics verwendet einen speziellen Datenquellentyp, der keine Serveraufrufkosten verursacht.

+++

+++ Wenn ich bereits Advertising Cloud/AMO verwende, kann ich dann weiterhin die Advertising Analytics-Funktion verwenden?

Jedes kompatible Suchmaschinenkonto wird an Advertising Analytics übergeben und als schreibgeschützt angezeigt. Sämtliche Bearbeitungen oder Aktualisierungen müssen in Advertising Cloud/AMO vorgenommen werden.

+++

+++ Ich besitze die richtige SKU, aber ich kann nicht auf Advertising Analytics zugreifen. Warum ist das so?

Advertising Analytics ist nur für Adobe Analytics-Administratoren verfügbar. Administratoren können jedoch Nicht-Administratoren Zugriff gewähren. Wenden Sie sich also an Ihren Administrator, um Zugriffsrechte zu erhalten.

+++

## Verwenden von Advertising Analytics {#using}

+++ Welche Suchmaschinenkonten sind in Advertising Analytics enthalten?

Zu den Suchmaschinenkonten gehören Google AdWords und Microsoft Bing.

+++

+++ Wo greife ich auf Advertising Analytics zu?

Navigieren Sie nach der Anmeldung bei Adobe Analytics zum [!UICONTROL Admin]. Wählen Sie anschließend [!UICONTROL Advertising Analytics] , um Suchmaschinenkonten hinzuzufügen.

+++

+++ Wie werden die Daten erfasst und an Analytics übergeben?

Advertising Analytics verwendet eine Reihe benutzerdefinierter APIs, um Daten von Suchmaschinen über Adobe Advertising Cloud an Analytics zu übergeben.

+++

+++ Welche Suchdaten erhalte ich bei dieser Integration?

Sie werden

* Impressions
* Klicks
* Kosten
* Qualitätsbewertung
* Durchschnittliche Position direkt aus den Suchmaschinen sowie
* AMO-ID-Instanzen (klicken Sie auf Instanzen).

+++

+++ Kann ich meine Advertising Analytics-Daten nach anderen Analytics-Daten (Metriken/Dimensionen) aufschlüsseln?

Nein, die Rohdaten der Suche werden als unabhängiger Datensatz angezeigt. Es gibt jedoch eine Instanzenversion der Klickdaten, die nach anderen Analytics-Daten aufgeschlüsselt werden kann.

+++ Wie werden die verschiedenen Statusindikatoren für meine Konten definiert (Ausstehend, Aktiv, Ausgesetzt usw.)? Jede dieser Statusindikatoren identifiziert die Lebenszyklusphase jedes Suchmaschinenkontos.

* [!UICONTROL Ausstehend]
* [!UICONTROL Angehalten] bedeutet, dass das Konto zuvor eingerichtet wurde, aber inaktiv ist.
* [!UICONTROL Aktiv] bedeutet, dass das Konto vollständig eingerichtet wurde und Suchdaten abruft.

+++

+++ Ich versuche, meine Advertising Analytics-Konten einer bestimmten Report Suite zuzuordnen, aber sie ist nicht im Report Suite-Modal verfügbar. Warum?

Bevor Sie einem Advertising Analytics-Konto eine Report Suite zuweisen können, muss die gewünschte Report Suite [für Advertising Analytics Reporting bereitgestellt](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md)
Dies erfolgt über eine separate Admin-Seite, auf die Sie zugreifen können: Admin > Report Suites > [Report Suite auswählen] > Einstellungen bearbeiten > Advertising Analytics-Konfiguration.

+++

+++ Ist es möglich, einem Advertising Analytics-Konto eine Virtual Report Suite zuzuweisen?

Virtual Report Suites erfassen keine Daten, sodass Sie ein Advertising Analytics-Konto nicht direkt einer Virtual Report Suite zuordnen können. Sie können das Advertising Analytics-Konto jedoch der übergeordneten Report Suite der Virtual Report Suite zuordnen, in der die Daten angezeigt werden sollen. Die Suchmaschinenmetriken (Klicks/Kosten/Impressionen) werden möglicherweise nicht in der Virtual Report Suite angezeigt, es sei denn, Sie fügen eine &quot;oder&quot;-Bedingung in Ihre Segmentlogik auf der Grundlage der AMO-ID (oder ihrer Classification) ein. Beispiel: Durch das Hinzufügen von „alle Treffer, bei denen eine AMO-ID existiert“ werden die Suchmaschinenmetriken in das Segment aufgenommen.

+++

+++ Können Advertising Analytics-Metriken in der <b>Marketingkanäle</b> Bericht?

Nein, sie sind nicht im Marketingkanalbericht enthalten.

+++

+++ F: Wann werden die Suchdaten in Analytics abgerufen?

A: Die Suchdaten werden um ca. 6:00 Uhr in der Zeitzone Ihres Analytics-Rechenzentrums von den Suchmaschinen abgerufen. Zu diesem Zeitpunkt werden die AMO-Daten erfasst und in die Report Suite eingefügt. Diese Daten werden dann im Rahmen ihrer Einfügung in Analytics in die Report Suite-Zeitzonen umgewandelt.

+++

+++ Was kann <b>vor dem Klick erfasst</b>? Werden Impressionen, Kosten, durchschnittliche Position usw. auch ohne Klick erfasst? </p> </td>

Die AMO-ID erfasst die Suchmaschinenmetriken: Impressionen, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung. Sind keine Klicks aber Impressionen vorhanden, werden die Daten zu Impression/Position/Qualität dennoch an Analytics gesendet. In der Regel entstehen keine Kosten, wenn keine Klicks vorhanden sind.

+++

+++ Auf welcher Ebene werden diese Daten erfasst? <b>Besucher? Treffer?</b>

Die Suchmaschinenmetriken werden auf Trefferebene erfasst und mit der AMO-ID (und ihren Klassifizierungen) verbunden. Dabei handelt es sich um Daten der Zusammenfassungsebene, die nicht mit Besuchen/Besuchern verbunden sind. Daher können die Suchmaschinen-Metriken nur in Segmenten verwendet werden, die sich im Umfang der Trefferebene befinden und die auf der AMO-ID (oder zugehörigen Klassifizierungen) basieren.

Die AMO-ID wird auch auf der Landingpage im Treffer für die betreffende Seite (über die die Verbindung zum Besuch/Besucher hergestellt wird) erfasst. Sie bleibt in der absteigenden Hierarchie bestehen, um für andere Analytics-Metriken berücksichtigt zu werden (bis sie abläuft oder durch eine neue AMO-ID überschrieben wird). Sie ist wie jede andere eVar vollständig in den Datensatz integriert.

+++

+++ Erfassen Sie nur google.com oder <b>Länderversionen</b> (z. B. google.co.uk, google.it, google.fr oder google.de)?

Die Anzeigenplattform-Classification erfasst die folgenden Werte: &quot;Google Adwords&quot;und &quot;Bing Ads&quot;. Als gängige Best Practice sollte der Ländercode bei der Benennung der Kampagnen eingefügt werden. Anschließend können Sie detaillierter filtern oder eine Segmentierung vornehmen (Beispiel: Wenn alle Kampagnen mit „ländercode_“ beginnen, würden Sie durch die Erstellung eines Segments, in dem die Kampagnen (AMO-ID) mit „UK_“ beginnen, nur Daten für Großbritannien erhalten).

+++

+++ Die Metrik &quot;AMO-Kosten&quot;sind die Kosten, die für jeden Suchbegriff/jede Anzeige gezahlt werden, wie von der Suchmaschine angegeben. Handelt es sich hierbei um Netto- oder Bruttokosten?

&quot;AMO-Kosten&quot;sind nur die Kosten, die den Suchmaschinen gezahlt werden. Sie enthalten keinerlei Gebühren für Agenturen oder Suchoptimierungs-/Verwaltungsplattformen.

+++

+++ Gibt es Pläne, andere Werbekanäle wie <b>Anzeige</b> oder <b>Social</b>?

Nein, wir haben derzeit keine Pläne für diese anderen Kanäle auf dem Fahrplan.

+++


## Automatisches Tracking im Vergleich zu manuellem Tracking {#section_7437C4698A6D482EB7ED94A948390119}

+++ Beim Einrichten meines Werbekontos wird darauf hingewiesen, dass<b> Automatisches Tracking</b> kann zu unbeabsichtigten Folgen führen. Welche Art von Folgen sind hier gemeint?

Der automatische Modus versucht, URL-Parameter im richtigen Format an das Ende der Tracking-Vorlagen/Ziel-URLs anzuhängen. <b>Es liegt jedoch in Ihrer Verantwortung sicherzustellen, dass die hinzugefügten URL-Parameter ordnungsgemäß auf der endgültigen Landingpage beibehalten werden. Der Auto-Modus kann Keywords in die Landing-URL einfügen, die möglicherweise Sonderzeichen enthalten, die Ihr Webserver nicht unterstützt.

+++

+++ Wenn ich das manuelle oder automatische Tracking anfangs eingerichtet habe, kann ich später in den anderen Tracking-Modus wechseln? Was sind die Auswirkungen?

Ja, Sie können die Tracking-Modi wechseln. Sie müssen jedoch die alte Tracking-Logik entfernen, bevor Sie den Wechsel vornehmen. Dies kann zu Ausfallzeiten beim Tracking am Tag des Wechsels führen (insbesondere beim Wechsel vom manuellen zum automatischen Tracking). Daher empfehlen wir, nur dann zu wechseln, wenn dies unbedingt erforderlich ist.

* Wechsel von Manuell zu Automatisch: Entfernen Sie die manuellen Ergänzungen der Tracking-Vorlagen, schalten Sie dann in der Advertising Analytics-Benutzeroberfläche den Umschalter von Manuell zu Automatisch um und speichern Sie die Einstellung. Beachten Sie, dass es mehrere Stunden dauern kann, bis das System die automatischen Trackingcodes ausfüllt.

* Wechseln von Automatisch zu Manuell: Aktualisieren Sie den Umschalter in der Advertising Analytics-Setup-Benutzeroberfläche von manuell auf automatisch und stellen Sie dann die manuellen Trackingcodes so schnell wie möglich bereit. Wenn Sie während der Bereitstellung der manuellen Trackingcodes die automatischen Trackingcodes in den Tracking-Vorlagen der Suchmaschine sehen, entfernen Sie sie.

+++
