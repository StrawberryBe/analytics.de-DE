---
description: Sie können alle Anforderungen in einer Arbeitsmappe vor dem Hinzufügen und Bearbeiten von Anforderungen schützen, indem Sie die Arbeitsmappe sperren. Dies ermöglicht die Offline-Bearbeitung von Arbeitsmappen durch Anhalten aller Berichtsanforderungen für eine effizientere Bearbeitung.
title: Arbeitsmappen sperren/entsperren
topic: Report builder
uuid: ef5c276c-5f74-4741-b6fa-4c79eda29f62
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Arbeitsmappen sperren/entsperren

Sie können alle Anforderungen in einer Arbeitsmappe vor dem Hinzufügen und Bearbeiten von Anforderungen schützen, indem Sie die Arbeitsmappe sperren. Dies ermöglicht die Offline-Bearbeitung von Arbeitsmappen durch Anhalten aller Berichtsanforderungen für eine effizientere Bearbeitung.

Durch das Sperren einer Arbeitsmappe als Analyst können Sie Ihre Arbeitsmappenanforderungen vor Manipulationen durch andere Benutzer in Ihrer Organisation schützen. Gleichzeitig können diese Benutzer die Anforderungen in der Arbeitsmappe aktualisieren.

To protect a workbook against editing, click **[!UICONTROL Locked]** on the Report Builder toolbar ( ![](assets/locked_icon.png)

).

To unprotect a workbook, click **[!UICONTROL Unlocked]** ( ![](assets/unlocked_icon.png)

).

Sie können eine Arbeitsmappe entsperren, wenn Sie über eine der folgenden Berechtigungen verfügen:

* Sie sind Administrator oder
* Sie sind die Person, die die Arbeitsmappe ursprünglich gesperrt hat. In diesem Fall müssen Sie kein Administrator sein.

>[!NOTE] Sie können einer geschützten Arbeitsmappe keine Anforderung hinzufügen, außer Sie sind berechtigt, die Arbeitsmappe zu entsperren.

Wenn eine Arbeitsmappe gegen die Bearbeitung einer Anforderung gesperrt ist,

* Benutzer können keine Anforderungen erstellen/hinzufügen.
* Benutzer können Anforderungen nicht über den Anforderungs-Assistenten bearbeiten.
* Benutzer können Anforderungen nicht über die Funktion Mehrere Anforderungen bearbeiten bearbeiten bearbeiten.
* Benutzer können keine Anforderungen ausschneiden, kopieren oder einfügen. Benutzer können jedoch weiterhin das native Excel-Kontextmenü zum Ausschneiden/Kopieren/Einfügen verwenden, um den Inhalt der Anforderung(en) zu kopieren/einzufügen.
* Benutzer können Anforderungen entweder einzeln oder als Teil einer Gruppe aktualisieren.
* Wenn die Anforderung Eingabewerte aus Zellen (Datumsbereich, Segment, Filter) verwendet, können die Benutzer diese Werte in den Zellen ändern und die Anforderungen indirekt bearbeiten, indem sie sie aktualisieren.

Wenn Sie versuchen, eine geschützte Arbeitsmappe zu bearbeiten (über das Kontextmenü oder **[!UICONTROL Request Manager]** oder **[!UICONTROL Edit Multiple Requests]**), ist dies möglicherweise nicht möglich:

* Wenn Sie nicht berechtigt sind, die Anforderung(en) zu entsperren, wird diese Aufforderung angezeigt:

   ![](assets/locked_workbook_error.png)

* Wenn Sie über die erforderlichen Berechtigungen verfügen, wird keine Eingabeaufforderung angezeigt und Sie können die Anforderung bearbeiten.

## Arbeitsablauf {#section_260D05FF632B41DB97DB43E2ADBE2E75}

Nehmen wir an, dass Arbeitsmappe A über eine Anforderung verfügt, die gesperrt ist und von Benutzer A erstellt wurde.

**Beispiel 1: Benutzer A mit Administratorrechten (Benutzer A)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Arbeitsmappe A ist gesperrt, sodass auf der Symbolleiste die Schaltfläche „Anforderung erstellen“ deaktiviert ist. Auch andere Schaltflächen sind aufgrund der Sperre deaktiviert.
1. Wenn der Benutzer versucht, eine der deaktivierten Schaltflächen zu verwenden, wird eine Meldung angezeigt, dass die Arbeitsmappe derzeit gesperrt ist.
1. Der Benutzer kann die Arbeitsmappe entsperren, wodurch eine vollständige Bearbeitungsfunktion aktiviert wird.
1. Nach dem Entsperren bleibt die Arbeitsmappe entsperrt, bis sie explizit erneut gesperrt wird.

**Beispiel 2: Benutzer ohne Administratorrechte (Benutzer B)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Benutzer können die Anforderung nicht hinzufügen/bearbeiten.
1. Der Benutzer kann die Arbeitsmappe nicht entsperren.

