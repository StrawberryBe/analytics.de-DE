---
description: Adobe Report Builder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
feature: Report Builder
role: User, Admin
exl-id: 53cfdcf4-31c3-40ab-aca4-8f0f9be6fe13
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 82%

---

# Benutzerzugriffsberechtigungen für Dimensionen und Metriken

Adobe Report Builder bietet Berechtigungseinstellungen, die denen in den Analytics Admin Tools ähneln.

Als Benutzer ohne Administratorrechte haben Sie möglicherweise bereits Arbeitsmappen mit Anforderungen erstellt, die auf Dimensionen und Metriken verweisen, auf die Sie keinen Zugriff haben. Diese Berechtigungen kommen nun zur Geltung.

Wenn Sie zum Beispiel eine Anforderung aktualisieren, die Dimensionen oder Metriken enthält, auf die Sie keinen Zugriff haben, erhalten Sie eine Fehlermeldung wegen eingeschränkter Berechtigung. Die Fehlermeldung weist darauf hin, dass für Ihr Benutzerkonto aufgrund von Administratorberechtigungen keine Anfrage verfügbar ist.

![Screenshot mit der Fehlermeldung &quot;Fehler wegen eingeschränkter Berechtigung&quot;.](assets/arb_restrc_perm.png)

Befolgen Sie diese Anweisungen für **jede** Report Builder-Arbeitsmappe, die Sie pflegen:

1. Öffnen Sie die Arbeitsmappe.
1. Aktualisieren Sie alle Anforderungen.
1. Wenn ein Fehler wegen Benutzerzugriffsberechtigungen angezeigt wird, klicken Sie auf **[!UICONTROL CSV-Datei öffnen]**, um Zugriff auf die Liste der Fehler wegen eingeschränkter Berechtigungen zu erhalten.
1. Erstellen Sie eine Datei mit dem Namen „AllRestrictedPermissionErrors.xlsx“ und kopieren Sie die Liste mit den Fehlern wegen eingeschränkter Berechtigungen aus der CSV-Datei und fügen Sie sie in diese Datei ein.
1. Schließen Sie die Report Builder-Arbeitsmappe.

Wenn Sie alle Arbeitsmappen verarbeitet haben, sollten Sie über eine umfassende Liste mit Fehlern wegen eingeschränkter Berechtigungen in „AllRestrictedPermissionErrors.xlsx“ verfügen. Senden Sie diese Liste an Ihren für den Benutzerzugriff zuständigen Adobe Analytics-Administrator und ersuchen Sie um Zugriff auf die Metriken und Dimensionen.
