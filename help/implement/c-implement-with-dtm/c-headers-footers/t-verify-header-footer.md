---
description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
keywords: Analytics-Implementierung; Implementierungsmethode; dynamisches Tag-Management; dtm; code; page code; header code; Fußzeilencode; Einbettungscode; verify code; verify header code; Überprüfen des Fußzeilencodes; embed Registerkarte; embed
seo-description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
seo-title: Kopf- und Fußzeilencode überprüfen
solution: Analytics
title: Kopf- und Fußzeilencode überprüfen
topic: Entwickler und Implementierung
uuid: d 395 a 417-0 c 61-41 a 6-a 124-d 2 f 400 f 4626 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kopf- und Fußzeilencode überprüfen

Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.

1. Öffnen Sie Ihre Website im Browser.
1. Open the [!UICONTROL Developer Console] by right-clicking and choosing **[!UICONTROL Inspect Element]** &gt; **[!UICONTROL Console]**.
1. Press **[!UICONTROL Enter]**.

   If the code was properly installed, you will see *`true`* display in the console.

   Wenn der Code nicht korrekt installiert wurde, wird der Verweisfehler angezeigt:

   `_satellite is not defined`

   Wenn dieser Fehler angezeigt wird, müssen Sie sicherstellen, dass:

* You have included the full header code on every page of the site in the [!DNL HEAD] section, as close to the [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">]-Tag. 
* Keine unerwarteten Zeichen im Codeabschnitt angezeigt werden (die beispielsweise beim Kopieren und Einfügen aus einem formatierten Dokument entstanden sein können).

