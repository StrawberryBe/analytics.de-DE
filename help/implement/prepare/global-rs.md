---
title: Globale Report Suites in Adobe Analytics
description: Machen Sie sich mit den Vorteilen und Anforderungen einer globalen Report Suite vertraut.
exl-id: fa949b1e-80bd-41cf-a294-c840503b568f
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '878'
ht-degree: 100%

---

# Überlegungen zur globalen Report Suite

Bei einer globalen Report Suite handelt es sich um eine Report Suite, die Daten aus allen Domänen und Apps sammelt, deren Inhaber Ihre Organisation ist. Diese Datenerfassungstechnik erfordert Vorbereitung und unter Umständen eine Koordinierung zwischen Teams in Ihrer Organisation.

## Vorteile

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite.

* **Aggregierte Daten:** Globale Report Suites ermöglichen es Ihnen, KPIs und Erfolgsereignisse über Ihre eigenen Sites hinweg anzuzeigen. Mithilfe von Segmentierung und Virtual Report Suites können Site-spezifische Daten angezeigt werden.
* **Unterstützung für Cross-Device Analytics:** Cross-Device Analytics erfordert eine Report Suite, die Daten von mehreren Stellen sammelt, z. B. von Ihrer Website und Ihrer Mobile App. Separate Geräte können bei korrekter Implementierung Daten zuordnen. Weitere Informationen finden Sie unter [Cross-Device Analytics](../../components/cda/overview.md) im Benutzerhandbuch zu den Komponenten.
* **Nicht mehr als eine Report Suite erforderlich:** Alle Daten können in einer einzigen Report Suite gesammelt werden. So ist es weniger wahrscheinlich, dass ein Entwickler fälschlicherweise Daten an die falsche Report Suite sendet.
* **Keine Datenaggregation erforderlich:** Datenaggregationen sind eine ziemlich veraltete Funktion, mit der individuelle Report Suite-Daten täglich aggregiert werden. Datenaggregationen deduplizieren keine Besuchs- oder Besucherdaten, was zu verfälschten Zahlen führen kann. Weitere Informationen finden Sie unter [Datenaggregationen](../../admin/c-manage-report-suites/rollup-report-suite.md) im Admin-Benutzerhandbuch.
* **Zeit sparen:** Workspace-Projekte, Klassifizierungen, Segmente und berechnete Metriken sind mit derselben globalen Report Suite verknüpft. Administratoren verbringen weniger Zeit mit der Verwaltung dieser Komponenten und der Datenverwaltung.
* **Präzisere markenübergreifende Attribution:** Wenn ein Besuch auf einer Site beginnt und der Besucher dann auf eine andere Ihrer eigenen Sites klickt, bevor ein Erfolgsereignis ausgelöst wird, wird die Attribution genau erfasst. Beispiel: Ein Besucher klickt auf einen Paid Search-Link und landet auf Site A. Anschließend klickt er auf einen Link zu Site B und tätigt dort einen Kauf. Eine globale Report Suite ordnet die erworbenen Produkte korrekt der Paid Search zu.
* **Vereinfachte Implementierung:** Da alle Marken/Sites Daten an dieselbe Report Suite senden, sind Ihre Implementierungen auf jeder Site aufeinander abgestimmt. Diese erzwungene Verwaltung stellt sicher, dass eine bestimmte Dimension oder Metrik in derselben eVar oder demselben Ereignis gespeichert wird. Administratoren, Tester, Tag-Management-Inhaber und Analysten profitieren von dieser Vereinfachung.

>[!NOTE]
>
>Die Koordination einer globalen Report Suite-Implementierung ist ein großes Projekt. Adobe empfiehlt, mit einem Berater zusammenzuarbeiten, um Komplikationen und auftretende Probleme zu reduzieren.

## Starten einer neuen Implementierung mit einer globalen Report Suite

Befolgen Sie die folgenden allgemeinen Richtlinien, um die Implementierung einer globalen Report Suite zu verstehen.

1. Erstellen Sie die globale Report Suite in Adobe Analytics. Weitere Informationen finden Sie unter [Erstellen einer Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) im Admin-Benutzerhandbuch.
1. Arbeiten Sie mit Teams in Ihrer Organisation zusammen, die für die jeweilige Domäne zuständig sind. Viele Teams verfügen über Reporting-Anforderungen, die sich auf ihren Geschäftsbereich beziehen.
1. Erfassen und aggregieren Sie alle diese Anforderungen in einem [Lösungsdesigndokument](solution-design.md). Wenn Teams ähnliche Anforderungen an eine Dimension haben, können sie dieselbe benutzerdefinierte Variable verwenden. Wenn beispielsweise sowohl Site A als auch Site B eine Breadcrumb-Dimension erfordern, können Implementierungen für beide Sites diese Daten über eVar1 senden.

   >[!IMPORTANT]
   >
   >Achten Sie darauf, dass jede benutzerdefinierte Variable domänenübergreifend gleich verwendet wird. Verwenden Sie nicht dieselbe eVar oder dasselbe Ereignis zu verschiedenen Zwecken auf Ihren Sites.
1. Stellen Sie sicher, dass jede Domäne über eine Datenschicht verfügt, um die Datenerfassung zu vereinfachen. Daten können weiterhin ohne Datenschicht erfasst werden, doch die Zuverlässigkeit und Langlebigkeit Ihrer Implementierung nimmt dann ab, insbesondere wenn Ihre Site neu gestaltet wird.
1. Verwenden Sie Adobe Experience Platform Launch, um Analytics zu implementieren. Verschiedene Sites erfordern wahrscheinlich unterschiedliche Datenelemente. Verwenden Sie für jede Domäne spezifische Regeln, um sicherzustellen, dass jedes Datenelement korrekt ausgefüllt wird, und weisen Sie diese Datenelemente dann ihren jeweiligen eVars und Ereignissen zu. Siehe [Launch-Übersicht](https://docs.adobe.com/content/help/de-DE/launch/using/overview.html) im Benutzerhandbuch zu Adobe Experience Platform Launch.
1. Schließen Sie den [Adobe Experience Cloud ID-Dienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) ein und verwenden Sie die Funktion [appendVisitorIDsTo](https://docs.adobe.com/content/help/de-DE/id-service/using/id-service-api/methods/appendvisitorid.html). Diese Funktion führt Besucherdaten zusammen, wenn Benutzer von einer Domäne auf eine andere klicken.

## Ändern einer bestehenden Implementierung mit einer globalen Report Suite

Der Prozess der Umstellung einer vorhandenen Implementierung über mehrere Sites hinweg auf eine einzige globale Report Suite erfordert mehr Zeit und Koordination zwischen Teams in Ihrer Organisation.

1. Bestimmen Sie, ob Sie eine Ihrer vorhandenen Report Suites oder eine neue Report Suite verwenden möchten. Wenn Sie die Verwendungszwecke vorhandener Variablen in Ihrer Implementierung ändern möchten, wird empfohlen, mit einer neuen Report Suite zu beginnen.
2. Legen Sie ein Umstellungsdatum fest, an dem Sie zu einer globalen Report Suite wechseln möchten. Der beste Zeitpunkt für eine Umstellung ist zwischen zwei wichtigen Reporting-Zeiträumen oder in Kombination mit größeren Änderungen an Ihrer Site. Beispiele sind der Beginn eines Geschäftsquartals oder -jahres, während einer Site-Aktualisierung oder beim Wechsel zu einem neuen Tag-Management-System.
3. Gehen Sie wie oben beschrieben vor (erstellen Sie eine Report Suite, erfassen Sie Reporting-Anforderungen in einem Lösungsdesigndokument und richten Sie auf jeder Site eine Datenschicht ein). Validieren Sie bei der Implementierung von Launch Ihre Implementierung mit einer Entwicklungsversion Ihrer Website.
4. Sobald Sie sich vergewissert haben, dass Ihre Implementierung in der Entwicklung funktioniert, veröffentlichen Sie Ihre Launch-Implementierung am Umstellungsdatum.

## Weiterführende Seiten

[Umstellung von Multi-Suite-Tagging zu einer globalen Report Suite und Virtual Report Suites](../../components/vrs/vrs-considerations.md)
[Vergleich von Datenaggregationen und globalen Report Suites](../../admin/c-manage-report-suites/rollup-report-suite.md)
