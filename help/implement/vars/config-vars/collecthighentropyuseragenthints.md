---
title: collectHighEntropyUserAgentHints
description: Verwenden Sie die Variable „collectHighEntropyUserAgentHints“, um zu bestimmen, ob Adobe Hinweise mit hoher Entropie von Chromium-Browsern (z. B. Google Chrome und Microsoft Edge) anfordern soll.
exl-id: 97cfa0f9-b35d-4c73-822f-adf30d0b7efc
feature: Variables
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 100%

---

# collectHighEntropyUserAgentHints

Client-Hinweise mit hoher Entropie werden von Adobe Analytics verwendet, um die Geräte- und Browser-Identifizierung zu verbessern. Diese Option ist ab Version 2.23.0 von AppMeasurement.js verfügbar. Weitere Informationen zu Client-Hinweisen finden Sie in [diesem Überblick und diesen häufig gestellten Fragen](/help/technotes/client-hints.md) sowie im [Google-Blog](https://web.dev/user-agent-client-hints/).

## Erfassen von Hinweisen mit hoher Entropie über das Web SDK 

Client-Hinweise mit hoher Entropie sind Teil der Web SDK-Kontextkategorien. Weitere Informationen finden Sie unter [Konfigurieren von Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de).

## Erfassen von Hinweisen mit hoher Entropie über die Adobe Analytics-Erweiterung

**[!UICONTROL Benutzeragenten-Hinweise mit hoher Entropie erfassen]** ist ein Kontrollkästchen unter dem Akkordeon „Allgemein“ bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/#/@adobepm/data-collection?lang=de) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte [!UICONTROL Tag-Eigenschaft].
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], um das Kontrollkästchen [!UICONTROL Benutzeragenten-Hinweise mit hoher Entropie erfassen] anzuzeigen. Es ist standardmäßig deaktiviert.

## collectHighEntropyUserAgentHints in AppMeasurement

Die Variable `s.collectHighEntropyUserAgentHints` bestimmt, ob AppMeasurement Hinweise mit hoher Entropie von Chromium-Browsern (z. B. Google Chrome und Microsoft Edge) anfordern soll. Diese Hinweise werden von Adobe Analytics verwendet, um die Geräte- und Browser-Identifizierung zu verbessern.

Wenn sie auf `true` festgelegt ist, werden alle Hinweise mit hoher Entropie vom Browser angefordert.

```js
s.collectHighEntropyUserAgentHints = true;
```
