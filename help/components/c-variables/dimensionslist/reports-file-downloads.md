---
description: „Dateidownloads“ zeigt Ihnen, wie oft Besucher Dateien von Ihrer Site herunterladen. Beispiele für Dateidownloads sind Dateien aus Textverarbeitungsprogrammen, Tabellen, Audiodateien, Filmdateien, Benutzerhandbücher und Ähnliches. Dazu gehören sowohl Dateien, die direkt im Browser gespeichert und geöffnet werden, als auch Dateien, die auf dem Computer des Benutzers gespeichert werden. Der Bericht zeigt den Namen der heruntergeladenen Datei sowie die vollständige URL, die für den Zugriff auf die Datei benötigt wird.
seo-description: „Dateidownloads“ zeigt Ihnen, wie oft Besucher Dateien von Ihrer Site herunterladen. Beispiele für Dateidownloads sind Dateien aus Textverarbeitungsprogrammen, Tabellen, Audiodateien, Filmdateien, Benutzerhandbücher und Ähnliches. Dazu gehören sowohl Dateien, die direkt im Browser gespeichert und geöffnet werden, als auch Dateien, die auf dem Computer des Benutzers gespeichert werden. Der Bericht zeigt den Namen der heruntergeladenen Datei sowie die vollständige URL, die für den Zugriff auf die Datei benötigt wird.
seo-title: Dateiladungen
solution: Analytics
title: Dateiladungen
topic: Berichte
uuid: 897fc221-aa30-4eac-aca6-bccb76adaf71
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Dateiladungen

„Dateidownloads“ zeigt Ihnen, wie oft Besucher Dateien von Ihrer Site herunterladen. Beispiele für Dateidownloads sind Dateien aus Textverarbeitungsprogrammen, Tabellen, Audiodateien, Filmdateien, Benutzerhandbücher und Ähnliches. Dazu gehören sowohl Dateien, die direkt im Browser gespeichert und geöffnet werden, als auch Dateien, die auf dem Computer des Benutzers gespeichert werden. Der Bericht zeigt den Namen der heruntergeladenen Datei sowie die vollständige URL, die für den Zugriff auf die Datei benötigt wird.

**Navigation**

**[!UICONTROL Berichte]** &gt; **[!UICONTROL Site-Inhalt]** &gt; **[!UICONTROL Links]** &gt; **[!UICONTROL Dateidownloads]**

Wenn sich dieser Bericht nicht an der üblichen Stelle befindet, wenden Sie sich an einen Administrator. Möglicherweise wurde die Standardmenüstruktur den Anforderungen Ihrer Organisation entsprechend geändert.

Verwenden Sie diesen Bericht, um:

* die Dateien zu bestimmen, die am häufigsten von Ihrer Site heruntergeladen werden.
* zu erkennen, ob bestimmte Dateien zu bestimmten Zeiten häufiger heruntergeladen werden.
* zu bestätigen, dass das jeweilige Dokument in allen Formaten angegeben ist.

   So können Sie z. B. im Begriff sein, Ihre Benutzerhandbücher in 12 Sprachen übersetzen zu lassen, um sie auf Ihrer Website anzubieten. Mit dem Dateidownloadbericht wissen Sie, wie oft die einzelnen Versionen des Benutzerhandbuchs heruntergeladen wurden und sind so in der Lage, den Wert zukünftiger Übersetzungen in alle 12 Sprachen zu erwägen.

**Fehlerbehebung**

Marketing-Berichte erfassen Informationen zu Dateien, die von Seiten Ihrer Website heruntergeladen wurden, sofern diese Seiten JavaScript-Code enthalten. Bestimmte Variablen müssen jedoch vorhanden und ordnungsgemäß eingerichtet sein, damit Informationen zum Dateidownload berichtet werden können. Falls dieser Bericht keine Daten oder nicht die erwarteten Werte anzeigt, führen Sie zum Überprüfen Ihrer Implementierung die folgenden Schritte aus.

1. Suchen Sie auf Ihrer Site die globale JavaScript-Datei. Die Datei trägt häufig den Namen [!DNL s_code.js]„, “, kann jedoch umbenannt worden sein. Wenn sie umbenannt wurde, können Sie die JavaScript-Dateien auf Ihrer Site nach dem Wert durchsuchen, der Teil des JavaScript-Codes *`s.account`* ist.

1. Suchen Sie in der Datei die Variable [„s.trackDownloadLinks“](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_trackdownllinks.html). Stellen Sie sicher, dass die Variable auf *„True“* festgelegt ist.

1. Suchen Sie die Variable [„s.linkDownloadFileTypes“](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkdownfiletypes.html). Stellen Sie sicher, dass alle gewünschten Dateierweiterungen in der Liste enthalten sind. If necessary, add missing extensions like [!DNL .zip], [!DNL .pdf], and so on.)

Wenn diese Variablen anscheinend richtig konfiguriert sind, der [!UICONTROL Download-Bericht] jedoch trotzdem keine Daten empfängt, sollte sich ein unterstützter Benutzer Ihrer Organisation an den Kundendienst wenden.
