---
description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
keywords: Analytics-Implementierung;Implementierungsmethode;Dynamic Tag Management;DTM;Code;Seiten-Code;Kopfzeilencode;Fußzeilencode:Einbettungscode;Code überprüfen;Kopfzeilencode überprüfen;Fußzeilencode überprüfen;Registerkarte „Einbettung“;einbetten
title: Kopf- und Fußzeilencode überprüfen
topic-fix: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
exl-id: bed44ba7-8e0e-49e2-bedc-fb1ba66e5b18
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 100%

---

# Kopf- und Fußzeilencode überprüfen

Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.

1. Öffnen Sie Ihre Website im Browser.
1. Öffnen Sie die [!UICONTROL Entwickler-Konsole] indem Sie mit der rechten Maustaste klicken und **[!UICONTROL Element prüfen]** > **[!UICONTROL Konsole]** auswählen.
1. Drücken Sie die **[!UICONTROL Eingabetaste]**.

   Wenn der Code ordnungsgemäß installiert wurde, wird *`true`* in der Konsole angezeigt.

   Wenn der Code nicht korrekt installiert wurde, wird der Verweisfehler angezeigt:

   `_satellite is not defined`

   Wenn dieser Fehler angezeigt wird, müssen Sie sicherstellen, dass:

* Sie auf jeder einzelnen Seite der Website den vollständigen Kopfzeilencode im [!DNL HEAD]-Bereich so nah wie möglich am `<head>` -Tag platziert haben.
* Keine unerwarteten Zeichen im Codeabschnitt angezeigt werden (die beispielsweise beim Kopieren und Einfügen aus einem formatierten Dokument entstanden sein können).
