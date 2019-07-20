---
description: Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.
keywords: Analytics-Implementierung
seo-description: Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.
seo-title: Benutzerspezifische Besucher-ID
solution: Analytics
title: Benutzerspezifische Besucher-ID
topic: Entwickler und Implementierung
uuid: 49881 e 27-0418-4 ecf-a 922-dcc 3 db 923 f 40
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Benutzerspezifische Besucher-ID

Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.

Eine benutzerspezifische Besucher-ID kann auf Sites verwendet werden, bei denen Sie Besucher auf eindeutige Weise identifizieren können. So wird z. B. möglicherweise eine ID generiert, wenn sich ein Benutzer mit einem Benutzernamen und einem Passwort bei einer Website anmeldet.

Wenn Sie die [!UICONTROL Besucher-IDs] Ihrer Benutzer ableiten und verwalten können, stehen die folgenden Methoden zum Festlegen der ID zur Verfügung:

| Methode | Beschreibung |
|---|---|
| [Variable „s.visitorID“](/help/implement/js-implementation/c-variables/page-variables.md) | Wenn JavaScript im Browser verwendet wird oder Sie eine andere AppMeasurement-Bibliothek verwenden, können Sie die Besucher-ID in einer Datenerfassungsvariablen festlegen. |
| Abfragezeichenfolgen-Parameter in der Bildanforderung | Bei dieser Option können Sie die [!UICONTROL Besucher-ID] über den Abfragezeichenfolgen-Parameter [!UICONTROL vid] in einer fest programmierten Bildanforderung an Adobe übergeben. |
| Dateneinfüge-API | On devices using wireless protocols that don't accept JavaScript, you can send an XML post containing the `<visitorid/>` XML element to Adobe collection servers from your servers. |
| Umschreiben der URL und VISTA | Einige Implementierungsarchitekturen bieten Unterstützung für das Umschreiben von URLs an, damit der Sitzungsstatus auch dann aufrechterhalten werden kann, wenn das Setzen eines Cookies nicht möglich ist. In solchen Fällen kann Adobe Engineering Services eine [!DNL VISTA]-Regel implementieren, die nach dem Sitzungswert in der URL der Seite sucht und diesen dann formatiert und in die [!UICONTROL visid]-Werte einsetzt. |
>[!CAUTION]
>**Benutzerspezifische Besucher-IDs müssen ausreichend granularer/eindeutig** sein: Eine ungültige Implementierung von benutzerdefinierten Besucher-IDs kann zu falschen Daten und mangelhaften Berichterstattungsleistungen führen. Wenn die benutzerspezifische Besucher-ID nicht eindeutig oder granular genug ist oder falsch auf einen allgemeinen Standardwert wie die Zeichenfolge "NULL" oder" 0" gesetzt ist, werden die Treffer von vielen verschiedenen Besuchern von Adobe Analytics als Einzelbesucher erkannt. Dies führt zu falschen Daten, wenn Besucherzählungen zu niedrig sind und Segmente für diesen Besucher nicht richtig funktionieren. Eine nicht ausreichend detaillierte benutzerspezifische Besucher-ID verhindert außerdem, dass die Daten ordnungsgemäß über die Knoten im Analytics-Berichtscluster verteilt werden. In diesem Fall wird ein Knoten überlastet und die Berichtanforderungen können nicht zeitnah verarbeitet werden. Alle Berichte für die Report Suite schlagen fehl. <br>Schlecht implementierte Besucher-IDs wirken sich möglicherweise nicht unmittelbar auf die Berichterstellungsleistung aus, da Analytics häufig mehrere Monate lang nicht ausgeglichene Daten verarbeiten kann; Im Laufe der Zeit kann ein schlecht implementierter Besucher-ID-Wert jedoch problematisch werden, damit Analytics die Verarbeitung für betroffene Report Suites deaktivieren kann.</br><br>Implementoren sollten die Richtlinie befolgen, dass ein einzelner benutzerspezifischer Besucher-ID-Wert niemals mehr als 1% des Traffic der Report Suite gutgeschrieben werden sollte. Although the 1% guideline is sufficient for most report suites, the actual limit that might cause reporting performance to be impacted may be lower than 1% for very large report suites.</br>
