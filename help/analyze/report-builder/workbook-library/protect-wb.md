---
description: Erfahren Sie, wie Sie alle Anforderungen in einer Arbeitsmappe vor dem Hinzufügen und Bearbeiten von Anforderungen schützen können, indem Sie die Arbeitsmappe sperren.
title: Arbeitsmappen sperren und entsperren
uuid: ef5c276c-5f74-4741-b6fa-4c79eda29f62
feature: Report Builder
role: User, Admin
exl-id: b5a83532-9fa7-4f1f-b744-e5d74781fffb
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 77%

---

# Arbeitsmappen sperren und entsperren

Sie können alle Anforderungen in einer Arbeitsmappe davor schützen, dass Anforderungen hinzugefügt und bearbeitet werden, indem Sie die Arbeitsmappe sperren. Dies ermöglicht eine Offline-Bearbeitung der Arbeitsmappen, indem alle Berichtsanforderungen angehalten werden – für eine effizientere Bearbeitung.

Wenn Sie als Analyst eine Arbeitsmappe sperren, können Sie Ihre Arbeitsmappenanforderungen davor schützen, dass sie von anderen Benutzern in Ihrer Organisation bearbeitet werden. Gleichzeitig können diese Benutzer die Anforderungen in der Arbeitsmappe noch bearbeiten.

Um eine Arbeitsmappe vor Änderungen zu schützen, klicken Sie auf der Report Builder-Symbolleiste auf **[!UICONTROL Gesperrt]** ( ![](assets/locked_icon.png)).

Um die Sperrung für eine Arbeitsmappe aufzuheben, klicken Sie auf **[!UICONTROL Entsperrt]** ( ![](assets/unlocked_icon.png)).

Sie können eine Arbeitsmappe entsperren, wenn Sie über eine der folgenden Berechtigungen verfügen:

* Sie sind ein Administrator oder
* Sie sind die Person, die die Arbeitsmappe ursprünglich gesperrt hat. In diesem Fall müssen Sie kein Administrator sein.

>[!NOTE]
>
>Sie können einer geschützten Arbeitsmappe keine Anforderung hinzufügen, außer Sie sind berechtigt, die Arbeitsmappe zu entsperren.

Wenn eine Arbeitsmappe für die Bearbeitung von Anforderungen gesperrt ist, gilt Folgendes:

* Benutzer können keine Anforderungen erstellen und hinzufügen.
* Benutzer können über den Anforderungs-Assistenten keine Anforderungen bearbeiten.
* Benutzer können über die Funktion „Mehrere Anforderungen bearbeiten“ keine Anforderungen bearbeiten.
* Benutzer können keine Anforderungen ausschneiden, kopieren oder einfügen. Jedoch können sie zum Ausschneiden/Kopieren/Einfügen das native Excel-Kontextmenü verwenden, um den Inhalt der Anforderung(en) auszuschneiden/zu kopieren/einzufügen.
* Benutzer können Anforderungen entweder individuell oder als Mitglied einer Gruppe aktualisieren.
* Wenn bei der Anforderung Eingabewerte aus Zellen verwendet werden (Datumsbereich, Segment, Filter) können Benutzer diese Werte in den Zellen ändern und so die Anforderungen indirekt bearbeiten, indem sie sie aktualisieren.

Wenn Sie versuchen, eine geschützte Arbeitsmappe über das Kontextmenü zu bearbeiten, oder **[!UICONTROL Anforderungs-Manager]** oder **[!UICONTROL Mehrere Anforderungen bearbeiten]** kann es sein, dass Sie dies tun dürfen oder nicht:

* Wenn Sie nicht berechtigt sind, eine Anforderung zu entsperren, wird Ihnen eine Meldung angezeigt, in der Sie darauf hingewiesen werden, dass Sie nicht über die Rechte zum Entsperren und Bearbeiten der Arbeitsmappe verfügen.

  ![Screenshot mit der Fehlermeldung, wenn Sie nicht über die Berechtigung zum Entsperren einer Anforderung verfügen.](assets/locked_workbook_error.png)

## Workflow {#section_260D05FF632B41DB97DB43E2ADBE2E75}

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
