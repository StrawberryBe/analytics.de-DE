---
description: Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. Vergewissern Sie sich, dass Sie sich zuerst mit den Beschriftungen und deren Definitionen vertraut machen.
title: Report Suite-Daten beschriften
uuid: a694851c-8933-496e-9118-113cc38cba8a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Report Suite-Daten beschriften

Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. Vergewissern Sie sich, dass Sie sich zuerst mit den Beschriftungen und deren Definitionen vertraut machen.

>[!NOTE] Beachten Sie, dass die Beschriftung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Eine erneute Implementierung Ihrer mobilen Apps oder Websites kann die Art und Weise ändern, wie vorhandene Variablen verwendet werden. Dies kann auch Aktualisierungen der Beschriftungen erforderlich machen.

## Report Suite-Beschriftungen zuweisen oder bearbeiten {#section_39F829F35A274EACA532E2F6FF392996}

**Beispiel**: Sie als Datenverantwortlicher planen die Erfassung von E-Mail-Adressen und Cookie-IDs von Datensubjekten, um ihre Datenschutzanfragen zu verarbeiten. Diese Cookie-IDs werden in einer Report Suite in Adobe Analytics gespeichert. Um eine Beschriftung für E-Mail-Adressen und Cookie-IDs zu erstellen, müssen Sie das Adobe Cloud Platform-DULE-Framework (Data Usage Labeling &amp; Enforcement) in Analytics verwenden.

1. Navigieren Sie in Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]** > **[!UICONTROL (select report suite)]**![](assets/privacy_rs_settings.png)

1. Wählen Sie die Variablengruppe aus, die Sie beschriften möchten.

   ![](assets/variables.png)

   * **Standardabmessungen** (Standardabmessungen in Adobe Analytics)
   * **Standardmetriken** (Adobe Analytics-Standardmetriken)
   * **Konversionsereignisse** (benutzerspezifische Erfolgsereignisse)
   * **Merchandising-Konversionsdimensionen** (Merchandising-eVars)
   * **Konversionsdimensionen** (nicht Merchandising-eVars)
   * **Benutzerdefinierte Traffic-Dimensionen** (Props)
   * **Lösungsdimensionen und Ereignis** (Dimensionen/Ereignis im Zusammenhang mit Lösungen wie Mobil, Video, Aktivität Map usw. und Integrationen mit Lösungen wie Adobe Campaign, Adobe Experience Manager, Advertising Cloud usw.)
   * **Datenverarbeitungs-Dimensionen** (Variablen, die nicht direkt im Reporting über die Adobe Analytics-UI verfügbar sind, die Ihnen jedoch über Daten-Feeds und/Data Warehouse-Anfragen zur Verfügung stehen)

1. (Optional) Klicken Sie auf das Informationssymbol (i) neben den einzelnen Variablen, um die häufigsten Werte der letzten 90 Tage besser nachvollziehen zu können. (Diese Funktion steht nicht für Datenverarbeitungsdimensionen zur Verfügung, da sie in der Benutzeroberfläche von Analytics nicht verfügbar sind.)

   ![](assets/info.png)

1. Select one or more variables by clicking their checkbox, then select the **[!UICONTROL Edit]** icon (to the right) to edit one or more variable(s).

   ![](assets/edit.png)

1. Das Dialogfeld **Identitätsdatenbeschriftungen** wird automatisch geöffnet. Diese Beschriftungen klassifizieren Daten, die von sich aus oder in Kombination mit anderen Daten zur Identifizierung oder Aktivierung des direkten Kontakts mit einer Person verwendet werden können. Weitere Informationen zu diesen Optionen finden Sie unter [Beschriftungen für Identitätsdaten (DULE).](/help/admin/c-data-governance/gdpr-labels.md#identity-data-labels)

   >[!NOTE]
   >
   >Das DULE-Framework (Data Usage Labeling &amp; Enforcement) wurde entwickelt, um über Lösungen, Services und Plattformen hinweg eine einheitliche Methode zur Erfassung, Kommunikation und Verwendung von Metadaten zu Daten in der Adobe Experience Cloud bereitzustellen. Über die Metadaten können Datenverantwortliche angeben, bei welchen Daten es sich um personenbezogene Informationen handelt, welche Daten vertraulich sind und welche vertraglichen Beschränkungen für die Daten gelten.

   ![](assets/identity_labels.png)

1. Öffnen Sie den Bereich **Vertrauliche Daten**, um Beschriftungen für vertrauliche Daten festzulegen, mit deren Hilfe die geografischen Daten kategorisiert werden. Weitere Informationen zu diesen Optionen finden Sie unter [Beschriftungen für vertrauliche Daten (DULE).](/help/admin/c-data-governance/gdpr-labels.md#sensitive-data-labels)

   ![](assets/sensitive_data.png)

1. Öffnen Sie den Bereich „Datenschutzdaten“, um **Data Governance**-Beschriftungen festzulegen. In diesem Bereich können Sie Adobe anweisen, wie die einzelnen Variablen für Datenschutz-Zugriffs- und -Löschanfragen verarbeitet werden, und Sie können definieren, welche Variablen überprüft werden sollen, um die Datensubjekt-IDs für diese Anfragen zu finden. Weitere Informationen zu diesen Optionen finden Sie unter [Beschriftungen für Data Governance (Datenschutz).](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels)

   ![](assets/privacy_labels.png)

1. Click **[!UICONTROL Apply]** once you have completed all labeling.

## Beschriftungen zu Report Suite(s) kopieren {#section_7C6FDAFF049F4126B84F6261F72668EE}

Wenn Sie DULE-/Datenschutzeinstellungen auf mehr als eine Report Suite anwenden möchten, führen Sie folgende Schritte aus:

1. Wählen Sie die Variablengruppe aus (Standarddimensionen, Konversionsdimensionen usw.), enthält die zu kopierende Variable. Beachten Sie, dass Sie die Beschriftungen nur für eine Gruppe von Variablen gleichzeitig kopieren können.
1. Wählen Sie einige oder alle Variablen in dieser Gruppe aus.
1. Klicken Sie **[!UICONTROL Copy Labels to Report Suite(s)]** oben rechts im Dialogfeld &quot;Datenverwaltung&quot;.

   ![](assets/apply_as_template.png)

1. Either check **[!UICONTROL Select All]** to copy labels for the selected variables to all report suites or select the individual report suites that you want to copy the labels to.

   >[!IMPORTANT]
   >
   >Denken Sie daran, dass alle ausgewählten Report Suites Ihrer Experience Cloud-Organisation zugeordnet sein müssen.

   Wenn Sie die Beschriftungen für eine Variable oder Variablengruppe in eine andere Report Suite kopieren, wird die Kopie an der entsprechenden Stelle in der Ziel-Report Suite abgelegt. Bei Standarddimensionen, Standardmetriken, Lösungsdimensionen und Ereignissen und Datenverarbeitungsdimensionen werden die Beschriftungen in die Variable mit dem **gleichen Namen** in der Ziel-Report Suite kopiert.

   Bei Konversionsvariablen (eVars), Merchandising-Konversionsdimensionen und benutzerspezifischen Traffic-Dimensionen (Props) wird die Kopie jedoch unter der Variable mit **derselben Nummer** in der Ziel-Report Suite erstellt. eVar12 wird beispielsweise zu eVar12 in allen Ziel-Report Suites kopiert. Die Namen dieser Variablen werden bei der Bestimmung des Ziels der Kopie ignoriert. Wenn die entsprechende Variable in der Ziel-Report Suite nicht aktiviert ist, schlägt die Kopie für diese Variable fehl.

   Beim Kopieren der Beschriftungen für Klassifizierungen, die für eine Variable definiert sind, werden die Beschriftungen in eine Klassifizierung für die entsprechende Variable in der Ziel-Report Suite kopiert (z. B. eVar7 zu eVar7), deren Name identisch mit der kopierten Klassifizierung ist. Andernfalls schlägt die Kopie der Beschriftungen dieser Classification fehl.

   Nach dem Anwenden eines Beschriftungssatzes wird eine Statusmeldung angezeigt. Die Statusmeldung enthält die Namen aller Zielvariablen oder Classifications und deren Report Suites, für die die Kopie fehlgeschlagen ist.

   >[!IMPORTANT]
   >
   >Sie sollten immer die Ziel-Report Suites überprüfen, um sicherzustellen, dass die Beschriftungen korrekt kopiert wurden. Dies ist insbesondere für Variablen mit ID- oder DEL-Beschriftungen wichtig.

1. Klicken Sie auf **[!UICONTROL Apply]**.

