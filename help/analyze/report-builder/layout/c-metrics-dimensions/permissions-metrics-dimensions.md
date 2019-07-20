---
description: Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
seo-description: Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
seo-title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
solution: Analytics
title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
topic: ReportBuilder
uuid: b 561407 d-c 4 fa -4 f 1 e -8 b 16-5 ca 46 fcbf 36 f
translation-type: tm+mt
source-git-commit: d75c58caf1220031fa36483a0ad50ea6f7be7c39

---


# Benutzerzugriffsberechtigungen für Dimensionen und Metriken

Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.

Als Benutzer ohne Administratorrechte haben Sie möglicherweise bereits Arbeitsmappen mit Anforderungen erstellt, die auf Dimensionen und Metriken verweisen, auf die Sie keinen Zugriff haben. Diese Berechtigungen kommen nun zur Geltung.

Wenn Sie zum Beispiel eine Anforderung aktualisieren, die Dimensionen oder Metriken enthält, auf die Sie keinen Zugriff haben, erhalten Sie eine Fehlermeldung wegen eingeschränkter Berechtigung:

![](assets/arb_restrc_perm.png)

Befolgen Sie diese Anweisungen für **jede** ReportBuilder-Arbeitsmappe, die Sie pflegen:

1. Öffnen Sie die Arbeitsmappe.
1. Aktualisieren Sie alle Anforderungen.
1. Wenn ein Fehler wegen Benutzerzugriffsberechtigungen angezeigt wird, klicken Sie auf **[!UICONTROL CSV-Datei öffnen], um Zugriff auf die Liste der Fehler wegen eingeschränkter Berechtigungen zu erhalten.**
1. Erstellen Sie eine Datei mit dem Namen „AllRestrictedPermissionErrors.xlsx“ und kopieren Sie die Liste mit den Fehlern wegen eingeschränkter Berechtigungen aus der CSV-Datei und fügen Sie sie in diese Datei ein.
1. Schließen Sie die ReportBuilder-Arbeitsmappe.

Wenn Sie alle Arbeitsmappen verarbeitet haben, sollten Sie über eine umfassende Liste mit Fehlern wegen eingeschränkter Berechtigungen in „AllRestrictedPermissionErrors.xlsx“ verfügen. Senden Sie diese Liste an Ihren für den Benutzerzugriff zuständigen Adobe Analytics-Administrator und bitten Sie darum, Ihnen Zugriff auf die Metriken und Dimensionen zu gewähren.
