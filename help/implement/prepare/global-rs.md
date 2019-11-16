---
title: Globale Report Suites in Adobe Analytics
description: Machen Sie sich mit den Vorteilen und Anforderungen einer globalen Report Suite vertraut.
translation-type: tm+mt
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# Überlegungen zur globalen Report Suite

Bei einer globalen Report Suite handelt es sich um eine Report Suite, die Daten aus allen Domänen und Apps sammelt, deren Inhaber Ihre Organisation ist. Diese Datenerfassungstechnik erfordert die Vorbereitung und kann eine Koordinierung zwischen Teams in Ihrem Unternehmen erfordern.

## Vorteile

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite.

* **** Aggregierte Daten: Globale Report Suites ermöglichen es Ihnen, KPIs und Erfolgsereignisse über Ihre eigenen Sites hinweg anzuzeigen. Mithilfe von Segmentierung und Virtual Report Suites können Site-spezifische Daten angezeigt werden.
* **** Unterstützung für geräteübergreifende Analytics: Für CDA ist eine Report Suite erforderlich, die Daten von mehreren Orten wie Ihrer Website und Ihrer mobilen App erfasst. Separate Geräte können Daten zusammenfügen, wenn sie korrekt implementiert sind. Weitere Informationen finden Sie unter [Geräteübergreifende Analyse](../../components/cda/cda-home.md) im Komponenten-Benutzerhandbuch.
* **** Es ist nicht mehr als eine Report Suite erforderlich: Alle Daten können in einer einzigen Report Suite gesammelt werden. Daher ist es weniger wahrscheinlich, dass ein Entwickler fälschlicherweise Daten an die falsche Report Suite sendet.
* **** Keine Datenaggregation erforderlich: Datenaggregationen sind eine relativ zeitgemäße Funktion, mit der individuelle Report Suite-Daten täglich aggregiert werden. Datenaggregationen deduplizieren keine Besuchs- oder Besucherdaten, was zu überhöhten Zahlen führen kann. Weitere Informationen finden Sie unter [Datenaggregationen](../../admin/c-manage-report-suites/rollup-report-suite.md) im Admin-Benutzerhandbuch.

> [!NOTE] Die Koordination einer globalen Report Suite-Implementierung ist ein großes Projekt. Adobe empfiehlt, mit einem Berater zusammenzuarbeiten, um Komplikationen und auftretende Probleme zu reduzieren.

## Starten einer neuen Implementierung mit einer globalen Report Suite

Verwenden Sie die folgenden allgemeinen Richtlinien, um die Implementierung einer globalen Report Suite zu verstehen.

1. Erstellen Sie die globale Report Suite in Adobe Analytics. Weitere Informationen finden Sie unter Report Suite[ ](../../admin/admin-console/create-report-suite.md)erstellen im Administratorbenutzerhandbuch.
2. Arbeiten Sie mit Teams in Ihrem Unternehmen zusammen, die für jede Domäne zuständig sind. Viele Teams verfügen über Berichterstattungsanforderungen, die sich auf ihren Geschäftsbereich beziehen.
3. Zeichnen Sie alle diese Anforderungen in einem [Lösungsdesigndokument](solution-design.md)auf und fassen Sie sie zusammen. Wenn Teams ähnliche Anforderungen für eine Dimension haben, können sie dieselbe benutzerdefinierte Variable verwenden. Wenn z. B. sowohl Site A als auch Site B eine Breadcrumb-Dimension erfordern, können Implementierungen für beide Sites diese Daten über eVar1 senden.
   > [!IMPORTANT] Achten Sie darauf, dass jede beliebige benutzerdefinierte Variable domänenübergreifend auf ähnliche Weise verwendet wird. Verwenden Sie nicht dieselbe eVar oder dasselbe Ereignis für verschiedene Zwecke auf Ihren Websites.
4. Stellen Sie sicher, dass jede Domäne über eine Datenschicht verfügt, um die Datenerfassung zu vereinfachen. Daten können weiterhin ohne Datenschicht erfasst werden, aber die Zuverlässigkeit und Langlebigkeit Ihrer Implementierung nimmt ab, insbesondere wenn Ihre Site neu gestaltet wird.
5. Verwenden Sie Adobe Experience Platform Launch, um Analytics zu implementieren. Verschiedene Sites erfordern wahrscheinlich unterschiedliche Datenelemente. Verwenden Sie für jede Domäne spezifische Regeln, um sicherzustellen, dass jedes Datenelement korrekt ausgefüllt wird, und weisen Sie diese Datenelemente dann ihren jeweiligen eVars und Ereignissen zu. Siehe [Startübersicht](https://docs.adobe.com/content/help/en/launch/using/overview.html) im Benutzerhandbuch für Adobe Experience Platform Launch.

## Ändern einer vorhandenen Implementierung mit einer globalen Report Suite

Der Prozess der Umstellung einer vorhandenen Implementierung auf eine einzige globale Report Suite auf mehrere Sites erfordert mehr Zeit und Koordination zwischen Teams in Ihrem Unternehmen.

1. Bestimmen Sie, ob Sie eine Ihrer vorhandenen Report Suites verwenden möchten, oder beginnen Sie mit einer neuen Report Suite. Wenn Sie die Verwendung vorhandener Variablen in Ihrer Implementierung ändern möchten, wird empfohlen, mit einer neuen Report Suite zu beginnen.
2. Legen Sie ein Überschneidungsdatum fest, ab dem Sie zu einer globalen Report Suite wechseln möchten. Die beste Zeit, um eine Kürzung vorzunehmen, liegt zwischen zwei wichtigen Berichtszeiträumen, wie einem Geschäftsquartal oder einem Geschäftsjahr.
3. Gehen Sie wie oben beschrieben vor (erstellen Sie eine Report Suite, erfassen Sie Berichterstattungsanforderungen in einem Lösungsdesigndokument und richten Sie auf jeder Site eine Datenschicht ein). Validieren Sie bei der Implementierung von Launch Ihre Implementierung mit einer Entwicklungsversion Ihrer Website.
4. Sobald Sie bestätigt haben, dass Ihre Implementierung an dev arbeitet, veröffentlichen Sie Ihre Implementierung am Schnittdatum.

## Verwandte Seiten

[Wechsel von Multi-Suite-Tagging zu einer globalen Report Suite und Virtual Report Suites](../../components/vrs/vrs-considerations.md)Vergleich von Datenaggregationen und globalen Report Suites[](../../admin/c-manage-report-suites/rollup-report-suite.md)