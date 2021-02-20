---
description: Virtual Report Suites und Multisuite-Tagging bieten unterschiedliche Vorteile. Erfahren Sie, welche die beste Lösung für Ihr Unternehmen ist.
keywords: Virtual Report Suite, VRS
title: Virtual Report Suites und Multisuite-Tagging
topic: Adobe Analytics
uuid: f17d3659-a5b1-4807-a01d-a1b422009a64
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '1739'
ht-degree: 99%

---


# Virtual Report Suites und Multisuite-Tagging

Mit Virtual Report Suites werden Daten einer Report Suite angezeigt, die in Ihren digitalen Properties erfasst werden, aber über ein dauerhaft zugewiesenes Segment verfügen.

In vielen Fällen können Sie Virtual Report Suites verwenden, um Multi-Suite-Tagging zu ersetzen. Durch den Wechsel zu Virtual Report Suites kann die Notwendigkeit [sekundärer Server-Aufrufe](/help/admin/c-server-call-usage/overage-overview.md) effektiv beseitigt werden. Ihre Organisation verfügt beispielsweise über 6 verschiedene Websites, von denen jede Daten an ihre eigene Report Suite sowie eine kombinierte globale Report Suite sendet. Jede Site erhält einen sekundären Server-Aufruf, einen an die Report Suite der jeweiligen Marken und einen zweiten an die globale Report Suite. Stattdessen können Sie Daten von allen Sites ausschließlich an die globale Report Suite senden und dann mehrere Virtual Report Suites verwenden, um die Marken voneinander zu trennen.

Wenn Sie Multi-Suite-Tagging durch eine globale Report Suite und Virtual Report Suites ersetzen, können Sie Ihre Adobe Analytics-Implementierung vereinfachen und die Anzahl der Server-Aufrufe reduzieren. Dies wird als Best Practice empfohlen. Es gibt jedoch einige wichtige Einschränkungen für Virtual Report Suites. Die folgenden Richtlinien sollen Ihnen bei der Entscheidung helfen, ob auf einer globalen Report Suite erstellte Virtual Report Suites der richtige Ansatz für Sie sind.

## Richtlinien

Wenn Sie sich nicht sicher sind, ob die beschriebenen Anwendungsfälle auf Sie und Ihr Unternehmen zutreffen, wenden Sie sich an andere Administratoren von Adobe Analytics oder an Ihren Adobe-Kundenbetreuer. Sie können Ihnen dabei helfen, Ihre Geschäftsanforderungen zu beurteilen, und eine Empfehlung abgeben.

Berücksichtigen Sie bei der Entscheidung, ob Sie Multi-Suite-Tagging oder Virtual Report Suites verwenden sollten, folgende Aspekte:

### Veröffentlichen von Segmenten in der Adobe Experience Cloud

Für Virtual Report Suites wird die Freigabe von Segmenten in Adobe Experience Cloud derzeit nicht unterstützt. Benutzer, die ein Segment für die Experience Cloud freigeben möchten, müssen Zugriff auf die Quell-Report Suite haben.

Segmente aus einer Virtual Report Suite können noch nicht für die Personalisierung und das Targeting in Adobe Experience Cloud veröffentlicht werden. Alle Benutzer, die Segmente veröffentlichen, benötigen zu diesem Zweck Zugriff auf die Quell-Report Suite. Nehmen wir an, Sie möchten, dass Ihre Benutzer ausschließlich Zugriff auf Virtual Report Suites in ihrer geografischen Region haben. Sie möchten aber, dass sie auch Segmente aus Adobe Analytics erstellen und für das Targeting mit Adobe Target in Adobe Experience Cloud freigeben können. In diesem Fall empfiehlt Adobe die Verwendung von Multi-Suite-Tagging. Wenn es Sie nicht stört, dass Benutzer Zugriff auf die globale Report Suite haben, oder keine Segmente veröffentlichen müssen, um sie in anderen Lösungen zu verwenden, können Virtual Report Suites verwendet werden.

### Echtzeitdaten und aktuelle Daten

Virtual Report Suites unterstützen keine Echtzeitberichte, weil die Daten segmentiert sind. Die Funktion „Aktuelle Daten“ wird in Virtual Report Suites nicht unterstützt, da sie keine Segmentierung unterstützt. Beide Funktionen sind spezifisch für Reports &amp; Analytics.

[Echtzeitberichte](/help/admin/admin/realtime/t-realtime-admin.md) und [Aktuelle Daten](/help/technotes/latency.md) stehen in Virtual Report Suites nicht zur Verfügung. Dies betrifft Benutzer, die innerhalb von Sekunden oder Minuten nach der Datenerfassung auf Trends in Reports &amp; Analytics reagieren. Dazu könnten beispielsweise Bearbeiter in einem Newsroom gehören, die die Schlagzeilen basierend auf dem Inhaltskonsum in Echtzeit anpassen. Erwägen Sie die Verwendung von Multi-Suite-Tagging, wenn Sie über erhebliche Echtzeitdaten verfügen, die für einzelne Report Suites spezifisch sind. Echtzeitdaten und aktuelle Daten können weiterhin in der globalen Report Suite verwendet werden.

### Individuelle Einschränkungen

Wenn Sie über eine globale Report Suite verfügen, die eine große Anzahl von Sites zusammenfasst, begegnet Ihnen unter Umständen regelmäßig der Zeileneintrag [geringer Traffic](/help/technotes/low-traffic.md). Wenn Sie Multi-Suite-Tagging verwenden, betrifft dieses Problem nur die globale Report Suite (einzelne Report Suites haben selten geringen Traffic). Wenn Sie Virtual Report Suites verwenden, werden individuelle Einschränkungen freigegeben, sodass einzelne Report Suites auch geringen Traffic anzeigen. Erwägen Sie die Verwendung von Multi-Suite-Tagging, wenn Sie vermeiden möchten, dass Daten mit geringem Traffic zusammengefasst werden.

Beispiel: Eine große Medienorganisation verfügt über 100 Webeigenschaften. Jede Eigenschaft veröffentlicht monatlich einige tausend News-Artikel, zusätzlich zum Hosting aller Artikel aus den Vormonaten. Diese Organisation verwendet eine globale Report Suite, bei der eVar1 „Artikelname“ lautet. In diesem Bericht werden monatlich etwa 4 Millionen individuelle Artikelnamen aus den verschiedenen Eigenschaften zusammengeführt. Bei Verwendung einer Virtual Report Suite werden die 500.000 Top-Werte, die den Großteil des Traffics ausmachen, in Virtual Report Suites einbezogen. Die verbleibenden 3,5 Millionen werden als „geringer Traffic“ klassifiziert. Wenn Multi-Suite-Tagging verwendet wird, hat jede einzelne Report Suite ihre eigenen 500.000 Top-Werte. Die individuellen Einschränkungen der globalen Report Suite sind bei Multi-Suite-Tagging und Virtual Report Suites gleich.

Die Adobe-Kundenunterstützung kann die individuellen Wertgrenzen für eine kleine Anzahl von Dimensionen erhöhen, wodurch dieses Problem vollständig beseitigt werden kann. Weitere Informationen erhalten Sie bei Ihrer Kundenbetreuung und Kundenunterstützung.

### Freigegebene Metriken über Report Suites hinweg

Virtual Report Suites verfügen nicht über eigene Dimensionen und Metriken, sondern übernehmen sie von der Quell-Report Suite. Die globale Report Suite muss alle Dimensionen und Metriken für alle Websites erfassen. Report Suites verfügen derzeit über maximal 250 eVars und 1000 benutzerspezifische Ereignisse.

Für verschiedene Sites gelten unterschiedliche Implementierungsanforderungen. Einige Dimensionen und Ereignisse können zwischen zwei Sites freigegeben werden. Beispielsweise kann bei einer E-Mail-Registrierung dasselbe Ereignis auf mehreren Websites verwendet werden, wodurch dasselbe benutzerspezifische Ereignis ausgelöst wird. Andere Dimensionen können spezifisch für eine Site sein. Beispielsweise kann nur über eine Ihrer Sites vom Benutzer das Profilbild geändert werden. Dieses benutzerspezifische Ereignis wird nur auf der Website implementiert, die es unterstützt.

Stellen Sie sicher, dass die Anzahl der individuellen Dimensionen und Metriken in eine einzige globale Report Suite passt. Wenn Sie feststellen, dass zu viele individuelle Dimensionen oder Metriken vorhanden sind, überprüfen Sie jede Dimension in jeder Implementierung. Es gibt wahrscheinlich Überlagerungen und Dimensionen, die für den Geschäftserfolg nicht entscheidend sind. Erwägen Sie auch die Verwendung von [Klassifizierungen](/help/components/classifications/c-classifications.md). Sie können zum Beispiel die Classification „Produktname“ auf der Grundlage der „Produkt“-Dimension erstellen, anstatt „Produktname“ in eVar5 zu erfassen. Klassifizierungen in einer Quell-Report Suite stehen automatisch allen abhängigen Virtual Report Suites zur Verfügung.

>[!TIP]
>
>Mit der Einführung der [Kuratierung](/help/analyze/analysis-workspace/curate-share/curate.md) können Sie den Namen einer bestimmten Dimension oder Metrik für jede einzelne Virtual Report Suite ändern.

### Segmentierungsnuancen

Eine Virtual Report Suite ist im Grunde genommen ein Segment, das auf eine Report Suite angewendet wird. Besuchs- und besucherbasierte Dimensionen können zu nicht intuitiven Berichtsergebnissen führen.

Sie haben beispielsweise zwei Websites, A und B, die beide Daten an eine globale Report Suite senden. Einige Besucher wechseln unweigerlich von Site A zu Site B, und diese Bewegung von der einen zur anderen Site ist im Pathing der globalen Report Suite sichtbar. Wenn Sie Virtual Report Suites für die Sites A und B erstellen, wird bei einem Besuch, der auf Site A begonnen und auf Site B geendet hat, keine Entrypage in VRS B angezeigt. Die Entrypage für diesen Besuch hat auf Site A begonnen, die aus der Virtual Report Suite segmentiert ist.

### Währungsumrechnung

Virtual Report Suites können nur die Währung der Report Suite anzeigen, auf der sie basieren. Adobe Analytics ermöglicht zwar die Konvertierung der Währung bei der Erstellung von Berichten. Der Wechselkurs ist jedoch der des aktuellen Tages (auch wenn es sich um historische Daten handelt).

Wenn Ihre Organisation ihre Analyse in einer einheitlichen Währung durchführt, ist dies kein Problem. Wenn Sie jedoch einen erheblichen geschäftlichen Bedarf an verschiedenen regionalen Teams haben, die den Umsatz in ihrer eigenen Landeswährung anzeigen müssen, sollten Sie die Verwendung von Multi-Suite-Tagging in Betracht ziehen.

### Datenfeeds

Daten-Feeds können keine Virtual Report Suites verwenden. Sie können jedoch einen Daten-Feed von einer globalen Report Suite empfangen und dann trennen.

Mit Daten-Feeds erhalten Sie einen täglichen oder stündlichen Export aller Adobe Analytics-Daten auf individueller Treffer-Ebene. Daten-Feeds können nicht vorab segmentiert werden, bevor sie Ihnen bereitgestellt werden. Daher können Sie nur einen Daten-Feed für Ihre globale Report Suite erhalten. Wenn Ihr Unternehmen individuelle Daten-Feeds auf Basis einer Marke, Eigenschaft, Region oder anderen granularen Ebene dringend benötigt, sollten Sie Multi-Suite-Tagging in Erwägung ziehen.

### Data Connectors mit Partnerkonten

Bestimmte Adobe-Partner-Integrationen in Adobe Analytics sind auf ein Partnerkonto pro Report Suite beschränkt. Einige Organisationen benötigen möglicherweise mehrere Partnerkonten für dieselbe Integration.

Beispielsweise ist pro Report Suite nur ein Google DCM zulässig. Viele Unternehmen verfügen über mehrere DCM-Konten, mit denen verschiedene Marken, Geschäftseinheiten und Regionen ihre Anzeigen getrennt voneinander verwalten können. Integrationen können nicht in Virtual Report Suites eingerichtet werden. Wenn Sie über abhängige Data Connectors mit mehreren Konten verfügen, sollten Sie Multi-Suite-Tagging in Erwägung ziehen.

### Zusammenfassungsdatenquellen

Mit „Zusammenfassungsdatenquellen“ können Sie aggregierte Metriken auf Report Suite-Ebene in Adobe Analytics importieren. Da Uploads von „Zusammenfassungsdatenquellen“ aggregierte Metriken enthalten, können sie nicht segmentiert werden. Da VRS mit Segmentierung arbeitet, sind nicht alle Daten, die mit Zusammenfassungsdatenquellen importiert wurden, in Virtual Report Suites verfügbar. Zusammenfassungsdatenquellen sind nur in der Quell-Report Suite sichtbar.

>[!TIP]
>
>Datenquellen mit vollständiger Verarbeitung unterstützen die Segmentierung und können in Virtual Report Suites verwendet werden.

## Schritte, die bei der Verwendung von Virtual Report Suites zu befolgen sind

Wenn Sie sich dafür entscheiden, sekundäre Server-Aufrufe zugunsten von Virtual Report Suites zu entfernen:

1. Erstellen Sie Virtual Report Suites so, dass deren Daten denen in Ihren untergeordneten Report Suites entsprechen. Segmentieren Sie eine benutzerdefinierte Dimension, die Ihre Sites voneinander unterscheidet.
   * Wenn Sie von einer vorhandenen Multi-Suite-Tagging-Implementierung migrieren, vergleichen Sie die Segmente der Virtual Report Suite mit Ihren vorhandenen untergeordneten Report Suites. Sie sollten sicherstellen, dass die Daten vergleichbar sind, bevor Sie Benutzer in die Virtual Report Suite verschieben.
   * Es empfiehlt sich, die [Segmentstapelung](/help/components/segmentation/segmentation-workflow/seg-build.md) als Best Practice zu verwenden, sodass Sie ein Segment an einem Ort bearbeiten und es auf alle abhängigen Virtual Report Suites anwenden können.
   * Verwenden Sie Treffercontainer, wenn Virtual Report Suites sich gegenseitig ausschließen sollen.
2. Nachdem Sie bestätigt haben, dass die Virtual Report Suites korrekt eingerichtet sind, entfernen Sie die sekundären Report Suite-IDs aus Ihrer Implementierung. So entfernen Sie sekundäre Report Suites:
   * Klicken Sie in Adobe Experience Platform Launch auf das „x“ neben den Report Suites, die Sie nicht mehr verwenden möchten.
   * Suchen Sie in DTM die Eigenschaft und das Analytics-Tool. Entfernen Sie in den Feldern „Produktionskonto-ID“ und „Testkonto-ID“ alle IDs der Report Suite, die Sie nicht mehr verwenden möchten.
   * Suchen Sie in veralteten JavaScript-Implementierungen die `s.account`-Variable und entfernen Sie alle Report Suite-IDs, die Sie nicht mehr verwenden möchten.
   * Behalten Sie in jedem Fall nur die IDs der globalen/übergeordneten Report Suites bei, die Daten Ihrer Sites und Apps erfassen.
   * Navigieren Sie zu „Admin“ > „Report Suites“ und blenden Sie alle nicht mehr verwendeten sekundären Report Suites aus.
