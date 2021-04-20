---
description: Feldbeschreibungen für den Manager für geplante Aufgaben.
title: Manager für geplante Aufgaben
uuid: dec259f0-2a04-4c94-abbc-5008cf2f1cb8
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 97%

---


# Manager für geplante Aufgaben

Im Manager für geplante Aufgaben können Sie eine Liste mit den vorhandenen terminierten Berichten, ihren Empfängern, Zeitplandetails und Dateiformaten sehen. Sie können außerdem geplante Arbeitsmappen, deren Ausführung fehlgeschlagen ist, reaktivieren.

| Feld | Beschreibung |
| --- | --- |
| Registerkarte **Terminierte Berichte** |  |
| Berichtsname | Dies ist der Name des terminierten Berichts. |
| E-Mail/FTP | Die E-Mail- oder FTP-Adresse des Empfängers. **Hinweis:** Wenn E-Mail ausgewählt ist, werden Berichte, die größer als 1 MB sind, automatisch als ZIP-Datei an die E-Mail angehängt. Dank dieser Funktion bleibt die Größe des Anhangs gering und Anhänge werden nicht deaktiviert. |
| Veröffentlichungsoptionen | Diese Spalte enthält Power BI, wenn eine der [Power BI-Veröffentlichungsoptionen](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/publish-powerbi/power-bi.html) ausgewählt ist. |
| Zeitplan | Der Typ der geplanten Bereitstellung. |
| Dateiformat | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
| Reaktivieren | Wenn eine geplante Arbeitsmappe nicht ausgeführt werden kann, unternimmt Report Builder in jeweils 15 Minuten Abstand zwei weitere Ausführungsversuche. Nach drei fehlgeschlagenen Versuchen deaktiviert Report Builder den Plan und zeigt die Schaltfläche Reaktivieren an. Wenn Sie eine Arbeitsmappe reaktivieren, wird die geplante Bereitstellung ab dem Zeitpunkt wiederaufgenommen, an dem die Deaktivierung erfolgte.  Wenn eine geplante Arbeitsmappe beispielsweise vor 14 Tagen deaktiviert wurde und Sie sie heute reaktivieren, wird sie für jeden fehlenden Tag, also 14-mal ausgeliefert. Wenn die Arbeitsmappe für die fehlenden Tage nicht ausgeliefert werden soll, können Sie die geplante Arbeitsmappe löschen und eine neue geplante Arbeitsmappe unter Verwendung derselben Planungsparameter erstellen.   Hinweis: Sie sollten eine Arbeitsmappe erst reaktivieren, wenn Sie die Ursache der Deaktivierung durch das System kennen. Eine Möglichkeit der Fehlerbehebung besteht darin, die deaktivierte Arbeitsmappe herunterzuladen und sie auf der Clientseite aktualisieren. Wenn keine Fehlermeldung erfolgt, sollte die Arbeitsmappe reaktiviert werden können. |
| Zuletzt gesendet | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| Registerkarte **Empfänger** |  |
| E-Mail-Adresse des Empfängers | Die E-Mail-Adresse des Berichtempfängers. |
| Berichte | Die Berichte, die an die einzelnen Empfänger gesendet wurden. |
| Registerkarte **Berichte – Verlauf** |  |
| Dateiname | Dies ist der Name des terminierten Berichts. |
| Datum | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| Status | Der Status gibt an, ob der Bericht gesendet oder nicht gesendet wurde. |
| E-Mail/FTP | Die E-Mail- oder FTP-Adresse für den Empfänger des Berichts. |
| Dateiformat | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |

