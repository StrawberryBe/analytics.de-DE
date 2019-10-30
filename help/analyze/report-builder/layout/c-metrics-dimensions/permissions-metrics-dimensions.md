---
description: Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
seo-description: Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
seo-title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
solution: Analytics
title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
topic: ReportBuilder
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

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
1. Erstellen Sie die Datei "AllRestrictedPermissionErrors.xlsx"und kopieren Sie die Liste der Fehler mit eingeschränkter Berechtigung aus der CSV-Datei in diese Datei.
1. Schließen Sie die ReportBuilder-Arbeitsmappe.

Nachdem Sie alle Arbeitsmappen verarbeitet haben, sollten Sie eine umfassende Liste mit Fehlern wegen eingeschränkter Berechtigung in "AllRestrictedPermissionErrors.xlsx"haben. Senden Sie diese Liste an Ihren für den Benutzerzugriff zuständigen Adobe Analytics-Administrator und bitten Sie darum, Ihnen Zugriff auf die Metriken und Dimensionen zu gewähren.
