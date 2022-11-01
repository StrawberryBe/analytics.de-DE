---
title: Datenschicht erstellen
description: Erfahren Sie, was eine Datenschicht in Ihrer Analytics-Implementierung ist und wie sie zur Zuordnung von Variablen in Adobe Analytics verwendet werden kann.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
source-git-commit: 571192e27972f2bc15912481f9a578427e1c1cfb
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 60%

---

# Datenschicht erstellen

Eine Datenschicht ist ein Framework von JavaScript-Objekten auf Ihrer Site, die die in Ihrer Analytics-Implementierung verwendeten Variablenwerte enthalten. Dies ermöglicht eine bessere Kontrolle und einfachere Wartung beim Zuweisen von Werten zu Analytics-Variablen.

## Voraussetzungen

[Erstellen Sie ein Lösungsdesigndokument](solution-design.md): Für Ihr Unternehmen ist es wichtig, die Tracking-Anforderungen abzustimmen. Stellen Sie sicher, dass Sie ein Lösungs-Design-Dokument vorbereitet haben, bevor Sie sich an die Entwicklungs-Teams in Ihrer Organisation wenden.

## Workflow

Die Implementierung von Adobe Analytics mit einer Datenschicht folgt normalerweise diesen Schritten:

1. **Arbeiten Sie mit Ihrem Website-Entwicklungs-Team zusammen, um eine Datenschicht zu implementieren**: Ihr Website-Entwicklungs-Team ist in erster Linie dafür verantwortlich, dass das Datenschichtobjekt mit den richtigen Werten gefüllt wird. Gehen Sie diese Seite mit Ihrem Website-Entwicklungs-Team durch, um sicherzustellen, dass die Erwartungen zwischen den Teams abgestimmt sind.

   >[!NOTE]
   >
   >Das Befolgen der von Adobe empfohlenen Datenschichtspezifikationen ist optional. Wenn Sie bereits über eine Datenschicht verfügen oder sich anderweitig gegen die Adobe-Spezifikationen entscheiden, stellen Sie sicher, dass Ihre Organisation sich an den zu befolgenden Spezifikationen orientiert.

1. **Validieren Sie Ihre Datenschicht mithilfe einer Browser-Konsole**: Sobald eine Datenschicht erstellt ist, können Sie mit der Entwicklerkonsole eines beliebigen Browsers überprüfen, ob sie funktioniert. Sie können die Entwicklerkonsole in den meisten Browsern mit der Taste `F12` öffnen. Ein Beispiel für einen Variablenwert wäre `adobeDataLayer.page.title`.
1. **Verwenden der Adobe Experience Platform-Datenerfassung zum Zuordnen von Datenschichtobjekten zu Datenelementen**: Dieser Schritt variiert je nach Implementierungsmethode Ihres Unternehmens:
   * **Bei Verwendung des Web SDK**: Ordnen Sie die gewünschten Datenschichtobjekte den gewünschten XDM-Feldern in Adobe Experience Platform Edge zu. Siehe [Analytics-Variablenzuordnung](../aep-edge/variable-mapping.md) , um die gewünschte Datenschichtzuordnung zu bestimmen.
   * **Bei Verwendung der Analytics-Erweiterung**: Erstellen Sie Datenelemente unter Tags in der Adobe Experience Platform-Datenerfassung und weisen Sie sie den gewünschten Datenschichtobjekten zu. Weisen Sie dann innerhalb der Analytics-Erweiterung jedes Datenelement der entsprechenden Analytics-Variablen zu.

## Spezifikationen

Adobe empfiehlt die Verwendung der [Adobe Client-Datenschicht](https://github.com/adobe/adobe-client-data-layer/wiki) für neue oder umstrukturierte Implementierungen.

Ihr Unternehmen kann andere Datenschichtspezifikationen verwenden, z. B. die [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf), oder eine andere benutzerdefinierte Spezifikation vollständig. Am wichtigsten ist es, eine konsistente Datenschicht zu schaffen, die den Anforderungen Ihres Unternehmens entspricht.

Datenschichten sind erweiterbar. Wenn Sie unternehmensspezifische Anforderungen haben, können Sie Objekte in Ihre Datenschicht aufnehmen, um diese Anforderungen zu erfüllen.

## Festlegen von Datenschichtwerten

Datenschichten werden normalerweise Server-seitig generiert und verweisen auf dieselben Objekte, die zum Erstellen des Website-Inhalts verwendet wurden. Richten Sie die Datenschicht der Website anhand der im [Lösungsdesigndokument](solution-design.md) Ihres Unternehmens festgelegten Tracking-Anforderungen ein.

## Nächste Schritte

[Ordnen Sie Datenschichtobjekte Datenelementen zu](../launch/layer-to-elements.md): Verwenden Sie die Datenschicht Ihrer Site in Adobe Experience Platform.
