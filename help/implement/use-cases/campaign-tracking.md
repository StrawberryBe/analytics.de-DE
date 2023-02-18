---
title: Kampagnen-Tracking-Workflow
description: Verwenden Sie Adobe Analytics, um Ihre Marketing-Maßnahmen zu verfolgen.
feature: Implementation Basics
exl-id: 9f7920e0-471c-46bc-9314-7b0a7c93fdce
source-git-commit: c118d42667c4a1af55929834b87d148a5973bed9
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Kampagnen-Tracking-Workflow

Wenn Ihr Unternehmen die Leistung und die Clickthrough-Rate der Marketing-Maßnahmen verfolgen möchte, können Sie den folgenden Prozess verwenden. Jeder dieser Schritte enthält die folgenden Abschnitte, die weitere Details enthalten.

1. [Richten Sie einen Tracking-Code-Generierungsprozess ein.](#establish-a-tracking-code-generation-process)
1. [Fügen Sie den gewünschten Trackingcode zur E-Mail hinzu](#add-the-desired-tracking-code-to-the-email)
1. [Einrichten oder Anpassen Ihrer Adobe Analytics-Implementierung, um Trackingcode-Daten einzuschließen](#include-campaign-variables-in-your-implementation)
1. [Berichte in Analysis Workspace anzeigen](#view-the-reports-in-analysis-workspace)

[Adobe Campaign](https://business.adobe.com/products/campaign/adobe-campaign.html) kann dabei helfen, diese Schritte zu vereinfachen, um Ihre Marketing-Maßnahmen optimal zu nutzen. Wenden Sie sich für weitere Informationen an Ihren Adobe-Vertriebsmitarbeiter.

## Richten Sie einen Tracking-Code-Generierungsprozess ein.

Jede Organisation benötigt unterschiedliche Trackingcodes. Einige Organisationen benötigen unter Umständen nur minimale Trackingcodes, die manuell erstellt wurden. Andere Unternehmen möchten möglicherweise mehr Kontrolle über das Tracking und verfügen über mehrere Systeme zum Erstellen der gewünschten Trackingcodes. Wenn Ihr Unternehmen zusätzlich zu Adobe Analytics Google Analytics verwendet, verfügt Ihr Unternehmen möglicherweise bereits über eine `utm` eingerichtetes Trackingcode-Modell.

Unabhängig davon, wie Sie Trackingcodes erstellen oder generieren, ist es für Ihr Unternehmen viel einfacher, Trackingcodes für Berichte zu gruppieren, wenn ein konsistentes System vorhanden ist. Mit konsistent strukturierten Trackingcodes können Sie [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md) damit Sie Einblicke in die kategorische Leistung erhalten.

## Fügen Sie den gewünschten Trackingcode zu einer URL hinzu

Sobald Sie über den gewünschten Trackingcode-Wert verfügen, können Sie ihn zu allen Links hinzufügen, die Sie online posten, z. B. Werbung, soziale Medien oder E-Mail. Das Hinzufügen dieser Trackingcodes erfolgt normalerweise in der Abfragezeichenfolge eines Links. Welchen Abfragezeichenfolgenparameter Sie verwenden, hängt von den Tracking-Anforderungen Ihres Unternehmens ab. ein allgemeiner Abfragezeichenfolgenparameter ist `cid` (kurz für Kampagnen-ID). Einige Unternehmen, die auch Google Analytics verwenden, verfügen möglicherweise bereits über mehrere Kampagnen-Abfragezeichenfolgenparameter wie `utm_source`, `utm_medium`und andere.

Das Hinzufügen von Abfragezeichenfolgen zu einem Link in einer E-Mail würde in etwa wie folgt aussehen:

```text
https://example.com?cid=EM989027
```

## Kampagnenvariablen in Ihre Implementierung einbeziehen

Adobe Analytics verfügt über eine dedizierte [Trackingcode](/help/components/dimensions/tracking-code.md) -Dimension, mit der Sie verschiedene Marketing-Maßnahmen in Ihrer Organisation messen können. Verschiedene Organisationen haben jedoch möglicherweise unterschiedliche Tracking-Anforderungen. Es ist wichtig, auf die [Lösungsdesigndokument](../prepare/solution-design.md) , um die richtigen Werte in den richtigen Variablen konsistent zu verfolgen.

Wenn Ihr Unternehmen noch kein Kampagnen-Tracking eingerichtet hat, können Sie Ihre Implementierung so anpassen, dass [`campaign`](/help/implement/vars/page-vars/campaign.md) -Variable. Siehe [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) -Methode verwenden, um zu erfahren, wie Sie Abfragezeichenfolgenparameterwerte erfassen können, die für die Implementierung Ihres Unternehmens spezifisch sind.

Wenn Ihr Unternehmen `utm` Abfragezeichenfolgen können Sie zwischen folgenden Optionen wählen:

* Alle senden `utm` Abfragezeichenfolgen in die Dimension &quot;Trackingcode&quot;als verkettete Werte. Sie können dann [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md) um zusätzliche Dimensionen zu erstellen, die sich jeweils auf die `utm` Parameter. Diese Methode weist eine komplexere Lernkurve auf, verwendet jedoch keine zusätzlichen eVars.
* Senden Sie jeden `utm` Abfragezeichenfolge in eine separate [eVar](/help/components/dimensions/evar.md). Diese Methode ist einfacher zu implementieren, erfordert jedoch die Verwendung zusätzlicher eVars.

## Berichte in Analysis Workspace anzeigen

Nachdem Sie Ihre Implementierung zur Erfassung von Trackingcode-Daten ordnungsgemäß eingerichtet haben, können Sie Berichte in Analysis Workspace anzeigen.

1. Melden Sie sich bei der [Adobe Experience Cloud](https://experience.adobe.com) und wählen Sie [!UICONTROL Adobe Analytics].
1. Erstellen Sie eine [Workspace-Projekt](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).
1. Ziehen Sie in der Liste der Komponenten auf der linken Seite die [Trackingcode](/help/components/dimensions/tracking-code.md) in die Arbeitsfläche.
1. Ziehen Sie die gewünschte Metrik, z. B. [Besuche](/help/components/metrics/visits.md) oder [Bestellungen](/help/components/metrics/orders.md) rechts neben der Arbeitsfläche.

![Kampagnen-Tracking-Bericht](../assets/campaign-tracking-report.png)
