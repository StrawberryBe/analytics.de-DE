---
description: Virtual Report Suites und Multi-Suite-Tagging bieten unterschiedliche Vorteile. Erfahren Sie, welche die beste Lösung für Ihr Unternehmen ist.
keywords: Virtual Report Suite,VRS
solution: Analytics
title: Überlegungen zu Virtual Report Suites und Multi-Suite-Tagging
topic: Adobe Analytics
uuid: f17d3659-a5b1-4807-a01d-a1b422009a64
translation-type: tm+mt
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# Überlegungen zu Virtual Report Suites und Multi-Suite-Tagging

Mit Virtual Report Suites werden Daten einer Report Suite angezeigt, die in Ihren digitalen Properties erfasst werden, aber über ein dauerhaft zugewiesenes Segment verfügen.

In vielen Fällen können Sie Virtual Report Suites verwenden, um Multi-Suite-Tagging zu ersetzen. Durch den Wechsel zu Virtual Report Suites kann die Notwendigkeit für [sekundäre Serveraufrufe](/help/admin/c-server-call-usage/overage-overview.md)effektiv beseitigt werden. Ihre Organisation verfügt beispielsweise über 6 verschiedene Websites, von denen jede Daten an ihre eigene Report Suite sowie eine kombinierte globale Report Suite sendet. Jede Site erhält einen sekundären Server-Aufruf. eine zur Report Suite der einzelnen Marken und eine Sekunde zur globalen Report Suite. Stattdessen können Sie Daten von allen Sites ausschließlich an die globale Report Suite senden und dann mehrere Virtual Report Suites verwenden, um jede Marke zu trennen.

Wenn Sie Multi-Suite-Tagging durch eine globale Report Suite und VRS ersetzen, können Sie Ihre Adobe Analytics-Implementierung vereinfachen und den Verbrauch von Server-Aufrufen reduzieren. Dies wird als Best Practice empfohlen. Es gibt jedoch einige wichtige Einschränkungen der fVRS. Die folgenden Richtlinien sollen Ihnen bei der Entscheidung helfen, ob auf einer globalen Report Suite erstellte Virtual Report Suites der richtige Ansatz für Sie sind.

## Richtlinien

Wenn Sie sich nicht sicher sind, ob die beschriebenen Anwendungsfälle für Sie und Ihr Unternehmen gelten, wenden Sie sich an Ihre anderen Adobe Analytics-Administratoren oder Ihren Adobe-Kundenbetreuer. Diese können Ihnen dabei helfen, Ihre Geschäftsanforderungen zu beurteilen, und eine Empfehlung abgeben.

Berücksichtigen Sie bei der Entscheidung, ob Sie Multi-Suite-Tagging oder Virtual Report Suites verwenden sollten, folgende Aspekte:

### Veröffentlichen von Segmenten in der Adobe Experience Cloud

Für Virtual Report Suites wird die Freigabe von Segmenten in Adobe Experience Cloud derzeit nicht unterstützt. Benutzer, die ein Segment für die Experience Cloud freigeben möchten, müssen Zugriff auf die Quell-Report Suite haben.

Segmente können noch nicht aus einer Virtual Report Suite zur Personalisierung und zum Targeting in Adobe Experience Cloud veröffentlicht werden. Alle Benutzer, die Segmente veröffentlichen, benötigen zu diesem Zweck Zugriff auf die Quell-Report Suite. Sie möchten beispielsweise, dass Benutzer nur Zugriff auf Daten für ihre geografischen Regionen haben, Sie möchten jedoch, dass sie Segmente aus Adobe Analytics in Adobe Experience Cloud für das Targeting in Adobe Target erstellen und freigeben können. In diesem Fall empfiehlt Adobe die Verwendung von Multi-Suite-Tagging. Wenn es Sie nicht stört, dass Benutzer Zugriff auf die globale Report Suite haben, oder Sie keine Segmente veröffentlichen müssen, um sie in anderen Lösungen zu verwenden, können Virtual Report Suites verwendet werden.

### Echtzeit- und aktuelle Daten

Virtual Report Suites unterstützen keine Echtzeitberichte, weil die Daten segmentiert sind. Aktuelle Daten werden auch in Virtual Report Suites nicht unterstützt, da keine Segmentierung unterstützt wird. Beide Funktionen sind spezifisch für Reports &amp; Analysen.

[Echtzeitberichte](/help/admin/admin/realtime/t-realtime-admin.md) und [aktuelle Daten](/help/technotes/latency.md) stehen in Virtual Report Suites nicht zur Verfügung. Dies betrifft Benutzer, die innerhalb von Sekunden oder Minuten nach der Datenerfassung auf Trends in Reports &amp; Analysen reagieren. Dazu könnten beispielsweise Redakteure in einem Newsroom gehören, die die Schlagzeilen basierend auf dem Inhaltskonsum in Echtzeit anpassen. Erwägen Sie die Verwendung von Multi-Suite-Tagging, wenn Sie über erhebliche Echtzeitdaten verfügen, die für einzelne Report Suites spezifisch sind. Echtzeit- und aktuelle Daten können weiterhin in der globalen Report Suite verwendet werden.

### Eindeutige Beschränkungen

Wenn Sie über eine globale Report Suite verfügen, die eine große Anzahl von Sites zusammenfasst, können Sie häufig auf den Zeileneintrag [mit niedrigem Traffic](/help/technotes/low-traffic.md) zugreifen. Wenn Sie Multi-Suite-Tagging verwenden, ist dies nur ein Problem für die globale Report Suite (einzelne Report Suites sehen weniger Traffic). Wenn Sie Virtual Report Suites verwenden, werden eindeutige Beschränkungen freigegeben, sodass einzelne Report Suites auch wenig Traffic anzeigen. Erwägen Sie die Verwendung von Multi-Suite-Tagging, wenn Sie vermeiden möchten, dass Daten in wenig Traffic aufgezeichnet werden.

So verfügt beispielsweise eine große Medienorganisation über 100 Webeigenschaften. Jede Eigenschaft veröffentlicht monatlich einige tausend News-Artikel, zusätzlich zum Hosten aller Artikel aus den Vormonaten. Diese Organisation verwendet eine globale Report Suite, bei der eVar1 "Artikelname"lautet. In diesem Bericht werden monatlich etwa 4 Millionen eindeutige Artikelnamen aus den verschiedenen Eigenschaften zusammengeführt. Bei Verwendung einer Virtual Report Suite werden die 500.000 höchsten Werte, die den Großteil des Datenverkehrs ausmachen, in Virtual Report Suites eingeschlossen. Die verbleibenden 3,5 Millionen sind unter geringer Verkehrsdichte zu verzeichnen. Wenn Multi-Suite-Tagging verwendet wird, kann jede einzelne Report Suite ihre eigenen Top-500-k-Werte sehen. Die eindeutigen Einschränkungen der globalen Report Suite sind zwischen Multi-Suite-Tagging und Virtual Report Suites gleich.

Der Adobe-Kundendienst kann die individuellen Wertgrenzen für eine kleine Anzahl von Dimensionen erhöhen, wodurch dieses Problem vollständig beseitigt werden kann. Weitere Informationen erhalten Sie bei Ihrer Kundenbetreuung und Kundenunterstützung.

### Freigegebene Variablen in Report Suites

Virtual Report Suites haben keine eigenen Dimensionen und Metriken; sie übernehmen sie von ihrer Quell-Report Suite. Die globale Report Suite muss alle Dimensionen und Metriken für alle Websites erfassen. Report Suites verfügen derzeit über maximal 250 eVars und 1000 benutzerspezifische Ereignisse.

Für verschiedene Sites gelten unterschiedliche Implementierungsanforderungen. Einige Dimensionen und Ereignisse können zwischen zwei Sites freigegeben werden. Beispielsweise kann bei einer E-Mail-Registrierung dasselbe Ereignis auf mehreren Websites verwendet werden, wodurch dasselbe benutzerdefinierte Ereignis ausgelöst wird. Andere Dimensionen können spezifisch für eine Site sein. Beispielsweise kann nur eine Ihrer Sites vom Benutzer das Profilbild ändern. Dieses benutzerspezifische Ereignis wird nur auf der Website implementiert, die es unterstützt.

Stellen Sie sicher, dass die Anzahl der individuellen Dimensionen und Metriken in eine einzige globale Report Suite passt. Wenn Sie feststellen, dass zu viele eindeutige Dimensionen oder Metriken vorhanden sind, überprüfen Sie jede Dimension in jeder Implementierung. Es gibt wahrscheinlich Überschneidungen und Dimensionen, die für den Geschäftserfolg nicht entscheidend sind. Erwägen Sie auch die Verwendung von [Klassifizierungen](/help/components/c-classifications2/c-classifications.md) . Sie können zum Beispiel die Klassifizierung „Produktname“ auf der Grundlage der „Produkt“-Dimension erstellen, anstatt „Produktname“ in eVar5 zu erfassen. Classifications in einer Quell-Report Suite stehen automatisch allen abhängigen Virtual Report Suites zur Verfügung.

> [!TIP] Mit der Einführung der [Kuration](/help/analyze/analysis-workspace/curate-share/curate-projects-vrs.md)können Sie den Namen einer bestimmten Dimension oder Metrik auf VRS-Basis ändern.

### Segmentierungsnuancen

Eine Virtual Report Suite auf einer grundlegenden Ebene ist einfach ein Segment, das auf eine Report Suite angewendet wird. Besuchs- und besucherbasierte Dimensionen können zu intuitiven Berichtsergebnissen führen.

Sie haben beispielsweise zwei Websites, A und B, die beide Daten in eine globale Report Suite senden. Einige Besucher wechseln unweigerlich von Site A zu Site B, und diese Bewegung von einem zum anderen ist in der Pfade der globalen Report Suite sichtbar. Wenn Sie Virtual Report Suites für die Sites A und B erstellen, wird bei einem Besuch, der auf Website A begann und auf Website B endete, keine Einstiegsseite in VRS B angezeigt. Die Einstiegsseite für diesen Besuch begann auf Site A, die aus der Virtual Report Suite segmentiert ist.

### Währungsumrechnung

Virtual Report Suites basieren nicht auf einer anderen Währung als die Report Suite, auf der sie basieren. In Adobe Analytics können Sie bei der Ausführung von Berichten Währungen konvertieren. Der Wechselkurs basiert jedoch auf dem aktuellen Tag (auch für historische Daten).

Wenn Ihre Organisation ihre Analyse in einer einheitlichen Währung durchführt, ist dies kein Problem. Wenn Sie jedoch einen erheblichen geschäftlichen Bedarf für verschiedene regionale Teams haben, die Umsätze in ihrer eigenen Landeswährung anzeigen müssen, sollten Sie Multi-Suite-Tagging in Betracht ziehen.

### Datenfeeds

Data Feeds können keine Virtual Report Suites verwenden. Sie können jedoch einen Datenfeed von einer globalen Report Suite empfangen und dann trennen.

Mit Data Feeds können Sie jeden Tag oder stündlich alle Ihre Adobe Analytics-Daten auf einer Trefferebene exportieren. Datenfeeds können nicht vorab segmentiert werden, bevor sie Ihnen bereitgestellt werden. Daher können Sie nur einen Datenfeed für Ihre globale Report Suite erhalten. Wenn Ihr Unternehmen individuelle Datenfeeds auf einer Marke, einer Eigenschaft, einer Region oder einer anderen granularen Ebene dringend benötigt, sollten Sie Multi-Suite-Tagging in Erwägung ziehen.

### Data Connectors mit Partnerkonten

Bestimmte Adobe-Partner-Integrationen in Adobe Analytics sind auf ein Partnerkonto pro Report Suite beschränkt. Einige Unternehmen benötigen möglicherweise mehrere Partnerkonten für dieselbe Integration.

Beispielsweise ist pro Report Suite nur ein Google DCM zulässig. Viele Unternehmen verfügen über mehrere DCM-Konten, mit denen verschiedene Marken, Geschäftseinheiten und Regionen ihre Anzeigen getrennt voneinander verwalten können. Integrationen können nicht in Virtual Report Suites eingerichtet werden. Wenn Sie über abhängige Data Connectors mit mehreren Konten verfügen, sollten Sie Multi-Suite-Tagging in Erwägung ziehen.

### Zusammenfassungsdatenquellen

Mithilfe von Zusammenfassungsdatenquellen können Sie aggregierte Metriken auf Report Suite-Ebene in Adobe Analytics importieren. Da Zusammenfassende Datenquellen-Uploads aggregierte Metriken enthalten, können sie nicht segmentiert werden. Da VRS mit der Segmentierung arbeitet, sind nicht alle Daten, die mit zusammenfassenden Datenquellen importiert wurden, in Virtual Report Suites verfügbar. Zusammenfassungsdatenquellen sind nur in der Quell-Report Suite sichtbar.

> [!TIP] Datenquellen mit vollständiger Verarbeitung unterstützen die Segmentierung und können in Virtual Report Suites verwendet werden.

## Schritte, die bei der Verwendung von Virtual Report Suites zu befolgen sind

Wenn Sie sich dafür entscheiden, sekundäre Serveraufrufe zugunsten von Virtual Report Suites zu entfernen:

1. Erstellen Sie Virtual Report Suites, die den Daten in Ihren untergeordneten Report Suites entsprechen. Segmentieren Sie eine benutzerdefinierte Dimension, die Ihre Sites voneinander unterscheidet.
   * Wenn Sie von einer vorhandenen Multi-Suite-Implementierung mit Tags migrieren, vergleichen Sie die Segmente der Virtual Report Suite mit Ihren vorhandenen untergeordneten Report Suites. Sie sollten sicherstellen, dass die Daten vergleichbar sind, bevor Sie Benutzer zur Virtual Report Suite verschieben.
   * Es empfiehlt sich, die [Segmentstapelung](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md) zu verwenden, damit Sie ein Segment an einer Position bearbeiten können und es für alle abhängigen Virtual Report Suites gelten kann.
   * Verwenden Sie Trefferbehälter, wenn Virtual Report Suites sich gegenseitig ausschließen sollen.
2. Nachdem Sie bestätigt haben, dass die Virtual Report Suites korrekt eingerichtet sind, entfernen Sie die sekundären Report Suite-IDs aus Ihrer Implementierung. So entfernen Sie sekundäre Report Suites:
   * Klicken Sie im Adobe Experience Platform Launch auf das X neben den Report Suites, die Sie nicht mehr verwenden möchten.
   * Suchen Sie in DTM die Eigenschaft und das Analytics-Tool. Entfernen Sie in den Feldern "Produktions-Konto-ID"und "Staging-Konto-ID"alle Report Suite-IDs, die Sie nicht mehr verwenden möchten.
   * Suchen Sie in älteren JavaScript-Implementierungen die `s.account` Variable und entfernen Sie alle Report Suite-IDs, die Sie nicht mehr verwenden möchten.
   * Lassen Sie in allen Fällen nur die globale/übergeordnete Report Suite-ID, um Daten für Ihre Sites und Apps zu erfassen.
   * Navigieren Sie zu Admin &gt; Report Suites und blenden Sie alle nicht mehr verwendeten sekundären Report Suites aus.
