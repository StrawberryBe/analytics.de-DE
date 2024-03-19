---
title: Kampagnen-Tracking-Workflow
description: Verwenden Sie Adobe Analytics, um Ihre Marketing-Maßnahmen nachzuverfolgen.
feature: Implementation Basics
exl-id: 9f7920e0-471c-46bc-9314-7b0a7c93fdce
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: ht
source-wordcount: '576'
ht-degree: 100%

---

# Kampagnen-Tracking-Workflow

Wenn Ihr Unternehmen die Performance und die Clickthrough-Rate der Marketing-Maßnahmen nachverfolgen möchte, können Sie den folgenden Prozess anwenden. Jeder dieser Schritte enthält die folgenden Abschnitte mit weiteren Details.

1. [Einrichten eines Prozesses für die Trackingcode-Generierung](#establish-a-tracking-code-generation-process)
1. [Hinzufügen des gewünschten Trackingcodes zur E-Mail](#add-the-desired-tracking-code-to-the-email)
1. [Einrichten oder Anpassen Ihrer Adobe Analytics-Implementierung zum Einschließen von Trackingcode-Daten](#include-campaign-variables-in-your-implementation)
1. [Anzeigen von Berichten in Analysis Workspace](#view-the-reports-in-analysis-workspace)

[Adobe Campaign](https://business.adobe.com/products/campaign/adobe-campaign.html) kann zur Vereinfachung dieser Schritte beitragen, damit Sie Ihre Marketing-Maßnahmen optimal nutzen können. Wenden Sie sich an Ihren Adobe-Vertriebskontakt, um weitere Informationen zu erhalten.

## Einrichten eines Prozesses für die Trackingcode-Generierung

Jedes Unternehmen benötigt unterschiedliche Trackingcodes. Die Anforderungen einiger Unternehmen sind unter Umständen minimal, sodass manuell erstellte Trackingcodes mehr als ausreichend sind. Andere Unternehmen wünschen sich möglicherweise mehr Kontrolle über das Tracking und verfügen über mehrere Systeme zum Erstellen der gewünschten Trackingcodes. Wenn Ihr Unternehmen neben Adobe Analytics auch Google Analytics verwendet, steht möglicherweise bereits ein eingerichtetes `utm`-Trackingcode-Modell zur Verfügung.

Unabhängig davon, wie Sie Trackingcodes erstellen oder generieren, ist es für Ihr Unternehmen viel einfacher, Trackingcodes für Berichte zu gruppieren, wenn ein konsistentes System vorhanden ist. Mit konsistent strukturierten Trackingcodes können Sie [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md) erstellen, um Erkenntnisse zur Kategorien-Performance zu erhalten.

## Hinzufügen des gewünschten Trackingcodes zu einer URL

Sobald Sie über den gewünschten Trackingcode-Wert verfügen, können Sie ihn zu allen Links hinzufügen, die Sie online posten, z. B. Werbung, Social Media oder E-Mail. Das Hinzufügen dieser Trackingcodes erfolgt normalerweise in der Abfragezeichenfolge eines Links. Welchen Abfragezeichenfolge-Parameter Sie verwenden, hängt von den Tracking-Anforderungen Ihres Unternehmens ab. Ein gängiger Abfragezeichenfolge-Parameter ist `cid` (kurz für Kampagnen-ID). Einige Unternehmen, die ebenfalls Google Analytics verwenden, verfügen möglicherweise bereits über mehrere Kampagnen-Abfragezeichenfolge-Parameter wie `utm_source`, `utm_medium` und andere.

Das Hinzufügen von Abfragezeichenfolgen zu einem Link in einer E-Mail würde in etwa wie folgt aussehen:

```text
https://example.com?cid=EM989027
```

## Einbeziehen von Kampagnenvariablen in Ihre Implementierung

Adobe Analytics verfügt über eine dedizierte [Trackingcode](/help/components/dimensions/tracking-code.md)-Dimension, mit der Sie verschiedene Marketing-Maßnahmen in Ihrem Unternehmen messen können. Verschiedene Unternehmen haben jedoch möglicherweise unterschiedliche Tracking-Anforderungen. Es ist wichtig, das [Lösungs-Design-Dokument](../prepare/solution-design.md) Ihres Unternehmens zu berücksichtigen, um konsistent die richtigen Werte in den richtigen Variablen zu verfolgen.

Wenn Ihr Unternehmen noch kein Kampagnen-Tracking eingerichtet hat, können Sie Ihre Implementierung so anpassen, dass die Variable [`campaign`](/help/implement/vars/page-vars/campaign.md) festgelegt wird. Sehen Sie sich die [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md)-Methode an, um zu erfahren, wie Sie Abfragezeichenfolge-Parameterwerte erfassen können, die für die Implementierung Ihres Unternehmens spezifisch sind.

Wenn Ihr Unternehmen `utm`-Abfragezeichenfolgen erfasst, können Sie zwischen folgenden Optionen wählen:

* Senden Sie alle `utm`-Abfragezeichenfolgen als verkettete Werte in die Trackingcode-Dimension. Anschließend können Sie mit [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md) zusätzliche Dimensionen erstellen, die sich jeweils auf jeden `utm`-Parameter fokussieren. Diese Methode weist eine komplexere Lernkurve auf, verwendet jedoch keine zusätzlichen eVars.
* Senden Sie jede `utm`-Abfragezeichenfolge in eine separate [eVar](/help/components/dimensions/evar.md). Diese Methode lässt sich insgesamt einfacher implementieren, erfordert jedoch die Verwendung zusätzlicher eVars.

## Anzeigen von Berichten in Analysis Workspace

Nachdem Sie Ihre Implementierung zur Erfassung von Trackingcode-Daten ordnungsgemäß eingerichtet haben, können Sie Berichte in Analysis Workspace anzeigen.

1. Melden Sie sich bei [Adobe Experience Cloud](https://experience.adobe.com) an und wählen Sie [!UICONTROL Adobe Analytics] aus.
1. Erstellen Sie ein [Workspace-Projekt](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).
1. Ziehen Sie in der Liste der Komponenten auf der linken Seite die [Trackingcode](/help/components/dimensions/tracking-code.md)-Dimension in die Arbeitsfläche.
1. Ziehen Sie die gewünschte Metrik, beispielsweise [Besuche](/help/components/metrics/visits.md) oder [Bestellungen](/help/components/metrics/orders.md), rechts neben die Arbeitsfläche.

![Kampagnen-Tracking-Bericht](../assets/campaign-tracking-report.png)
