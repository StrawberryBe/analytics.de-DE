---
description: Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.
title: Arbeitsmappen sperren/entsperren
uuid: ef5c276c-5f74-4741-b6fa-4c79eda29f62
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 99%

---


# Arbeitsmappen sperren/entsperren

Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.

Wenn Sie als Analyst eine Arbeitsmappe sperren, können Sie Ihre Arbeitsmappenanforderungen davor schützen, dass sie von anderen Benutzern in Ihrer Organisation bearbeitet werden. Gleichzeitig können diese Benutzer die Anforderungen in der Arbeitsmappe noch bearbeiten.

Um eine Arbeitsmappe vor Änderungen zu schützen, klicken Sie auf der Report Builder-Symbolleiste auf **[!UICONTROL Gesperrt]** ( ![](assets/locked_icon.png)

).

Um die Sperrung für eine Arbeitsmappe aufzuheben, klicken Sie auf **[!UICONTROL Entsperrt]** ( ![](assets/unlocked_icon.png)

).

Sie können eine Arbeitsmappe entsperren, wenn Sie über eine der folgenden Berechtigungen verfügen:

* Sie sind ein Administrator oder
* Sie sind die Person, die die Arbeitsmappe ursprünglich gesperrt hat. In diesem Fall müssen Sie kein Administrator sein.

>[!NOTE]
>
>Sie können einer geschützten Arbeitsmappe keine Anforderung hinzufügen, außer Sie sind berechtigt, die Arbeitsmappe zu entsperren.

Wenn eine Arbeitsmappe für die Bearbeitung von Anforderungen gesperrt ist, gilt Folgendes:

* Benutzer können keine Anforderungen erstellen/hinzufügen.
* Benutzer können über den Anforderungs-Assistenten keine Anforderungen bearbeiten.
* Benutzer können über die Funktion „Mehrere Anforderungen bearbeiten“ keine Anforderungen bearbeiten.
* Benutzer können keine Anforderungen ausschneiden, kopieren oder einfügen. Jedoch können sie zum Ausschneiden/Kopieren/Einfügen das native Excel-Kontextmenü verwenden, um den Inhalt der Anforderung(en) auszuschneiden/zu kopieren/einzufügen.
* Benutzer können Anforderungen entweder individuell oder als Mitglied einer Gruppe aktualisieren.
* Wenn bei der Anforderung Eingabewerte aus Zellen verwendet werden (Datumsbereich, Segment, Filter) können Benutzer diese Werte in den Zellen ändern und so die Anforderungen indirekt bearbeiten, indem sie sie aktualisieren.

Wenn Sie eine geschützte Arbeitsmappe bearbeiten möchten (über das Kontextmenü oder den **[!UICONTROL Anforderungs-Manager]** oder über **[!UICONTROL Mehrere Anforderungen bearbeiten]**), sind Sie dazu möglicherweise nicht berechtigt:

* Wenn Sie nicht berechtigt sind, die Anforderung(en) zu entsperren, wird die folgende Meldung angezeigt:

   ![](assets/locked_workbook_error.png)

* Wenn Sie über die erforderlichen Berechtigungen verfügen, wird keine Meldung angezeigt und Sie können die Anforderung bearbeiten.

## Arbeitsablauf {#section_260D05FF632B41DB97DB43E2ADBE2E75}

Nehmen wir an, dass Arbeitsmappe A über eine Anforderung verfügt, die gesperrt ist und von Benutzer A erstellt wurde.

**Beispiel 1: Benutzer A mit Administratorrechten (Benutzer A)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Arbeitsmappe A ist gesperrt, sodass auf der Symbolleiste die Schaltfläche „Anforderung erstellen“ deaktiviert ist. Auch andere Schaltflächen sind aufgrund der Sperre deaktiviert.
1. Wenn der Benutzer versucht, eine der deaktivierten Schaltflächen zu verwenden, wird eine Nachricht angezeigt, dass die Arbeitsmappe derzeit gesperrt ist.
1. Der Benutzer kann die Arbeitsmappe entsperren, sodass alle Bearbeitungsfunktionen aktiviert werden.
1. Nach dem Entsperren bleibt die Arbeitsmappe entsperrt, bis sie explizit erneut gesperrt wird.

**Beispiel 2: Benutzer ohne Administratorrechte (Benutzer B)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Der Benutzer kann die Anforderung nicht hinzufügen/bearbeiten.
1. Der Benutzer kann die Arbeitsmappe nicht entsperren.

