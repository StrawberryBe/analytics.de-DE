---
description: Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.
keywords: Analytics Implementation
title: Benutzerspezifische Besucher-ID
topic: Developer and implementation
uuid: 49881e27-0418-4ecf-a092-dcc3db923f40
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Benutzerspezifische Besucher-ID

Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.

Eine benutzerspezifische Besucher-ID kann auf Sites verwendet werden, bei denen Sie Besucher auf eindeutige Weise identifizieren können. So wird z. B. möglicherweise eine ID generiert, wenn sich ein Benutzer mit einem Benutzernamen und einem Passwort bei einer Website anmeldet.

Wenn Sie die [!UICONTROL Besucher-IDs] Ihrer Benutzer ableiten und verwalten können, stehen die folgenden Methoden zum Festlegen der ID zur Verfügung:

| Methode | Beschreibung |
|---|---|
| [Variable „s.visitorID“](/help/implement/js-implementation/page-variables/page-variables.md) | Wenn JavaScript im Browser verwendet wird oder Sie eine andere AppMeasurement-Bibliothek verwenden, können Sie die Besucher-ID in einer Datenerfassungsvariablen festlegen. |
| Abfragezeichenfolgen-Parameter in der Bildanforderung | Bei dieser Option können Sie die [!UICONTROL Besucher-ID] über den Abfragezeichenfolgen-Parameter [!UICONTROL vid] in einer fest programmierten Bildanforderung an Adobe übergeben. |
| Dateneinfüge-API | Bei Geräten mit Wireless-Protokollen, die kein JavaScript akzeptieren, können Sie einen XML-Post mit dem XML-Element `<visitorid/>` von Ihren Servern an Adobe-Erfassungsserver senden. |
| Umschreiben der URL und VISTA | Einige Implementierungsarchitekturen bieten Unterstützung für das Umschreiben von URLs an, damit der Sitzungsstatus auch dann aufrechterhalten werden kann, wenn das Setzen eines Cookies nicht möglich ist. In solchen Fällen kann Adobe Engineering Services eine [!DNL VISTA]-Regel implementieren, die nach dem Sitzungswert in der URL der Seite sucht und diesen dann formatiert und in die [!UICONTROL visid]-Werte einsetzt. |
>[!CAUTION]
>**Benutzerspezifische Besucher-IDs müssen ausreichend granular/eindeutig sein**: Eine ungültige Implementierung benutzerspezifischer Besucher-IDs kann zu falschen Daten und schlechter Berichterstellung führen. Wenn die benutzerdefinierte Besucher-ID nicht eindeutig oder granular genug ist oder falsch auf einen allgemeinen Standardwert wie die Zeichenfolge "NULL"oder "0"eingestellt ist, werden die Treffer vieler verschiedener Besucher von Adobe Analytics als einzelner Besucher angesehen. Dies führt zu falschen Daten, da die Besucherzahlen zu niedrig sind und Segmente für diesen Besucher nicht richtig funktionieren. Eine nicht ausreichend granulare benutzerdefinierte Besucher-ID verhindert auch, dass die Daten ordnungsgemäß über Knoten im Analytics-Berichtscluster verteilt werden. In diesem Fall wird ein Knoten überlastet und kann Berichtsanforderungen nicht zeitnah verarbeiten. Schließlich schlägt die Berichterstellung für die Report Suite fehl. <br>Schlecht implementierte benutzerdefinierte Besucher-IDs wirken sich möglicherweise nicht sofort auf die Berichterstellungsleistung aus, da Analytics häufig unausgeglichene Daten aus mehreren Monaten verarbeiten kann. Im Laufe der Zeit kann ein schlecht implementierter benutzerdefinierter Besucher-ID-Wert jedoch so problematisch werden, dass Analytics die Verarbeitung für betroffene Report Suites deaktivieren muss.</br><br>Implementierer sollten die Richtlinie befolgen, wonach einem einzelnen benutzerdefinierten Besucher-ID-Wert nie mehr als 1 % des Traffics Ihrer Report Suite gutgeschrieben werden sollte. Obwohl die Leitlinie von 1 % für die meisten Report Suites ausreicht, kann die tatsächliche Grenze, die die Berichtleistung beeinträchtigen könnte, bei sehr großen Report Suites unter 1 % liegen.</br>
