---
description: Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.
seo-description: Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.
seo-title: Sperren/entsperren Sie Arbeitsmappen
solution: Analytics
title: Sperren/entsperren Sie Arbeitsmappen
topic: ReportBuilder
uuid: ef 5 c 276 c -5 f 74-4741-b 6 fa -4 c 79 eda 29 f 62
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sperren/entsperren Sie Arbeitsmappen

Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.

Wenn Sie als Analyst eine Arbeitsmappe sperren, können Sie Ihre Arbeitsmappenanforderungen davor schützen, dass sie von anderen Benutzern in Ihrer Organisation bearbeitet werden. Gleichzeitig können diese Benutzer die Anforderungen in der Arbeitsmappe noch bearbeiten.

Um eine Arbeitsmappe vor Änderungen zu schützen, klicken Sie auf der ReportBuilder-Symbolleiste auf **[!UICONTROL Gesperrt (]**![](assets/locked_icon.png)

).

Um die Sperrung für eine Arbeitsmappe aufzuheben, klicken Sie auf **[!UICONTROL Entsperrt]** ( ![](assets/unlocked_icon.png)

).

Sie können eine Arbeitsmappe entsperren, wenn Sie über eine der folgenden Berechtigungen verfügen:

* Sie sind ein Administrator oder
* Sie sind die Person, die die Arbeitsmappe ursprünglich gesperrt hat. In diesem Fall müssen Sie kein Administrator sein.

>[!NOTE]
>
>Sie können einer geschützten Arbeitsmappe nur eine Anforderung hinzufügen, wenn Sie über die Berechtigung zum Entsperren der Arbeitsmappe verfügen.

Wenn eine Arbeitsmappe für die Bearbeitung von Anforderungen gesperrt ist, gilt Folgendes:

* Benutzer können keine Anforderungen erstellen/hinzufügen.
* Benutzer können über den Anforderungs-Assistenten keine Anforderungen bearbeiten.
* Benutzer können über die Funktion „Mehrere Anforderungen bearbeiten“ keine Anforderungen bearbeiten.
* Benutzer können keine Anforderungen ausschneiden, kopieren oder einfügen. Jedoch können sie zum Ausschneiden/Kopieren/Einfügen das native Excel-Kontextmenü verwenden, um den Inhalt der Anforderung(en) auszuschneiden/zu kopieren/einzufügen.
* Benutzer können Anforderungen entweder individuell oder als Mitglied einer Gruppe aktualisieren.
* Wenn bei der Anforderung Eingabewerte aus Zellen verwendet werden (Datumsbereich, Segment, Filter) können Benutzer diese Werte in den Zellen ändern und so die Anforderungen indirekt bearbeiten, indem sie sie aktualisieren.

If you try to edit a protected workbook (through the context menu, or **[!UICONTROL Request Manager]**, or **[!UICONTROL Edit Multiple Requests]**), you may or may not be allowed to do so:

* Wenn Sie nicht berechtigt sind, die Anforderung(en) zu entsperren, wird die folgende Meldung angezeigt:

   ![](assets/locked_workbook_error.png)

* Wenn Sie über die erforderlichen Berechtigungen verfügen, wird keine Meldung angezeigt und Sie können die Anforderung bearbeiten.

## Arbeitsablauf {#section_260D05FF632B41DB97DB43E2ADBE2E75}

Es wird angenommen, dass Arbeitsmappe A über eine Anforderung verfügt, die gesperrt ist und von Benutzer A erstellt wurde.

**Beispiel 1: Admin-Benutzer (oder Benutzer A)**

1. Der Benutzer meldet sich bei ReportBuilder an und öffnet Arbeitsmappe 
1. Arbeitsmappe A ist derzeit gesperrt, sodass auf der Symbolleiste die Schaltfläche „Anforderung erstellen“ deaktiviert ist. Auch andere Schaltflächen sind aufgrund der Sperre deaktiviert.
1. Wenn der Benutzer versucht, eine der deaktivierten Schaltflächen zu verwenden, wird eine Nachricht angezeigt, dass die Arbeitsmappe derzeit gesperrt ist.
1. Der Benutzer kann die Arbeitsmappe entsperren, sodass alle Bearbeitungsfunktionen aktiviert werden.
1. Nach dem Entsperren bleibt die Arbeitsmappe entsperrt, bis sie explizit erneut gesperrt wird.

**Beispiel 2: Benutzer ohne Administratorrechte (Benutzer B)**

1. Der Benutzer meldet sich bei ReportBuilder an und öffnet Arbeitsmappe 
1. Der Benutzer kann die Anforderung nicht hinzufügen/bearbeiten.
1. Der Benutzer kann die Arbeitsmappe nicht entsperren.

