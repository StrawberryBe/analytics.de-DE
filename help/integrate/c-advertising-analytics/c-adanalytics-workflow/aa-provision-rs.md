---
description: Konfigurieren Sie eine Report Suite, die Experience Cloud zugeordnet ist, für die Verwendung in Advertising Analytics.
title: Report Suite für Advertising Analytics aktivieren
uuid: 934f0e02-b5d7-4eca-93d8-92f95bd7014a
translation-type: ht
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: ht
source-wordcount: '283'
ht-degree: 100%

---


# Report Suite für Advertising Analytics aktivieren

Um die Advertising Analytics-Suchdaten in Analytics anzuzeigen, müssen Sie jede der Experience Cloud zugeordnete Report Suite für das Advertising Analytics-Reporting konfigurieren.

1. [Ordnen Sie Ihre Report Suite einer Organisation zu.](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html)
1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die Ihrer Experience Cloud-Organisation zugeordnet ist.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**.

   ![Berichterstellung](assets/aa_reporting.png)

   >[!IMPORTANT]
   >
   >„AMO-ID“ bezieht sich auf die Adobe Advertising Cloud-Variable, in die die Suchdaten eingefügt werden sollen.

1. Legen Sie die Variablenzuordnung und die Gültigkeitsdauer für die AMO-ID-Variable fest. Konversionsvariablen (eVars) ermöglichen es Adobe Analytics, Erfolgsereignisse spezifischen Variablenwerten zuzuordnen. Manchmal weisen Variablen mehrere Werte auf, bevor sich ein Erfolgsereignis einstellt. In diesen Fällen wird durch die Zuordnung festgelegt, auf welchen Variablenwert das Ereignis zurückgeführt wird.

   | Einstellung | Definition |
   |--- |--- |
   | Ausgangswert (Erster) | Das Ereignis wird vollständig dem ersten angezeigten Wert zugeordnet, unabhängig davon, welche Werte die Variable in Folge annimmt. |
   | Zuletzt verwendet (Letzter) | Das Erfolgsereignis wird vollständig dem letzten angezeigten Wert zugeordnet, unabhängig davon, welche Variablen zuvor vorhanden waren. |
   | Läuft ab nach | Hier wird ein Zeitraum bzw. ein Ereignis angegeben, nachdem der eVar-Wert abläuft (ihm also keine Erfolgsereignisse mehr zugeordnet werden).  Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ zugeschrieben. |

1. Klicken Sie auf **[!UICONTROL Advertising Analytics-Reporting aktivieren]** (beim ersten Mal) oder **[!UICONTROL Advertising Analytics-Reporting aktualisieren]** (bei darauffolgenden Malen). Ihre Report Suite kann jetzt Advertising Analytics-Suchdaten empfangen. Sie sind nun bereit, [Werbekonten zu erstellen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md).

