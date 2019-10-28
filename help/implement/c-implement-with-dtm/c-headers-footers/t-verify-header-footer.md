---
description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
keywords: Analytics-Implementierung;Implementierungsmethode;Dynamic Tag Management;DTM;Code;Seiten-Code;Kopfzeilencode;Fußzeilencode:Einbettungscode;Code überprüfen;Kopfzeilencode überprüfen;Fußzeilencode überprüfen;Registerkarte „Einbettung“;einbetten
seo-description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
seo-title: Kopf- und Fußzeilencode überprüfen
solution: Analytics
title: Kopf- und Fußzeilencode überprüfen
topic: Entwickler und Implementierung
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kopf- und Fußzeilencode überprüfen

Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.

1. Öffnen Sie Ihre Website im Browser.
1. Öffnen Sie die [!UICONTROL Entwickler-Konsole], indem Sie mit der rechten Maustaste klicken und **[!UICONTROL Element prüfen]** &gt; **[!UICONTROL Konsole]** auswählen.
1. Drücken Sie die **[!UICONTROL Eingabetaste]**.

   Wenn der Code ordnungsgemäß installiert wurde, wird *`true`* in der Konsole angezeigt.

   Wenn der Code nicht korrekt installiert wurde, wird der Verweisfehler angezeigt:

   `_satellite is not defined`

   Wenn dieser Fehler angezeigt wird, müssen Sie sicherstellen, dass:

* Sie auf jeder einzelnen Seite der Website den vollständigen Kopfzeilencode im [!DNL HEAD]-Bereich so nah wie möglich am [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">]-Tag platziert haben.
* Keine unerwarteten Zeichen im Codeabschnitt angezeigt werden (die beispielsweise beim Kopieren und Einfügen aus einem formatierten Dokument entstanden sein können).

