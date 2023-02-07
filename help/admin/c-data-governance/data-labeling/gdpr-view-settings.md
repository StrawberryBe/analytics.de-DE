---
description: Das Dialogfeld Datenschutzbezeichnungen für Data Governance bietet einen Überblick über die Datenschutzbezeichnungen und Namespaces einer Report Suite. Sie können die Einstellungen von hier aus auch in eine CSV-Datei exportieren.
title: Datenschutzbezeichnungen für Data Governance anzeigen/verwalten
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: f135138de15f3fc788e637128daeb064d0d453af
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 41%

---

# Datenschutzbezeichnungen für Data Governance anzeigen/verwalten

Die **[!UICONTROL Datenschutzbezeichnungen für Data Governance]** bietet einen Überblick über die Datenschutzbezeichnungen und Namespaces einer Report Suite. Sie können die Einstellungen von hier aus auch in eine CSV-Datei exportieren.

## Datenschutzbezeichnungen anzeigen {#view-privacy}

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Data Governance]**.

   >[!NOTE]
   >
   >Wenn dieser Menüpunkt nicht angezeigt wird, müssen Sie sich zu einem [Produktprofil in Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html?lang=de) hinzufügen lassen, das über die entsprechenden Berechtigungen für diese Funktion verfügt.

1. Wählen Sie oben rechts eine Report Suite aus, deren Datenschutzbezeichnungen Sie anzeigen oder verwalten möchten.

   ![](assets/privacy_labeling.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Name der Komponente]** | Diese Spalte listet alle Komponenten (Dimensionen, Metriken) auf, die Teil dieser Report Suite sind. |
| **[!UICONTROL Identität]** | Die Beschriftungen für Identitätsdaten („I“) werden verwendet, um Daten zu kategorisieren, über die eine bestimmte Person identifiziert oder kontaktiert werden kann. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#identity-data-labels) |
| **[!UICONTROL Sensitivität]** | Die Beschriftungen für vertrauliche Daten („S“) werden verwendet, um vertrauliche Daten, wie z. B. geografische Daten, zu kategorisieren. In Zukunft werden zusätzliche Datenbeschriftungen eingeführt, um andere Arten vertraulicher Informationen zu identifizieren. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#sensitive-data-labels) |
| **[!UICONTROL DSGVO-Zugriff]** | Über Data Governance-Beschriftungen können Benutzer Daten klassifizieren, die datenschutzbezogene Überlegungen und vertragliche Bedingungen zur Einhaltung von Verordnungen und Unternehmensrichtlinien enthalten. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#data-privacy-access-labels) |
| **[!UICONTROL DSGVO-Löschung]** | Eine Löschbeschriftung ist nur für Felder erforderlich, die einen Wert enthalten, der die Zuordnung eines Treffers zur betroffenen Person ermöglicht (d. h. die Identifizierung der betroffenen Person ermöglichen würde). [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#data-privacy-delete-labels) |
| **[!UICONTROL Namespace]** | Wenn Sie eine Variable als ID-DEVICE oder ID-PERSON beschriften, werden Sie zum Bereitstellen eines Namespace aufgefordert. Sie können entweder einen zuvor definierten Namespace verwenden oder einen neuen definieren. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#section_F0A47AF8DA384A26BD56032D0ABFD2D7) |
| **[!UICONTROL Kategorie]** | Bezieht den Komponententyp, z. B. Standardkomponente, Konversionsvariable usw. |

{style=&quot;table-layout:auto&quot;}

## Kopieren von Datenschutzbezeichnungen in eine Report Suite  {#copy-to-rs}

Wenn Sie dieselben Datenschutzeinstellungen auf mehr als eine Report Suite anwenden möchten, führen Sie die folgenden Schritte aus:

1. Wählen Sie die Variable aus, die Sie kopieren möchten. Beachten Sie, dass Sie die Beschriftungen nur für jeweils eine Variable kopieren können.
1. Klicken **[!UICONTROL In Report Suite(s) kopieren]** unten im Dialogfeld &quot;Data Governance&quot;.

   ![In die Report Suite kopieren](assets/copy_to_reportsuite.png)

1. Der sich ergebende Bildschirm zeigt den Variablennamen, die aktuell angewendeten Beschriftungen, die Sie kopieren möchten, die Report Suites und deren IDs sowie die Übereinstimmung der Einstellungen in den Ziel-Report Suites.

   ![Kopieren der Beschriftung in die Report Suite](assets/copy_to_rs.png)

   >[!IMPORTANT]
   >
   >Beachten Sie, dass alle ausgewählten Report Suites Ihrer Experience Cloud-Organisation zugeordnet sein müssen.

   Wenn Sie die Beschriftungen für eine Variable oder Variablengruppe in eine andere Report Suite kopieren, wird die Kopie an der entsprechenden Stelle in der Ziel-Report Suite abgelegt. Bei Standardkomponenten, Listenvariablen und Erfolgsereignissen werden die Beschriftungen mit der Variablen **gleicher Name** in der Ziel-Report Suite.

   Bei Konversionsvariablen (eVars) und Traffic-Dimensionen (props) wird die Kopie jedoch mit der Variablen **gleiche Zahl** in der Ziel-Report Suite. eVar12 wird beispielsweise zu eVar12 in allen Ziel-Report Suites kopiert. Die Namen dieser Variablen werden bei der Bestimmung des Ziels der Kopie ignoriert. Wenn die entsprechende Variable in der Ziel-Report Suite nicht aktiviert ist, schlägt die Kopie für diese Variable fehl.

   Beim Kopieren der Beschriftungen für Klassifizierungen, die für eine Variable definiert sind, werden die Beschriftungen in eine Klassifizierung für die entsprechende Variable in der Ziel-Report Suite kopiert (z. B. eVar7 zu eVar7), deren Name identisch mit der kopierten Klassifizierung ist. Andernfalls schlägt die Kopie für die Beschriftungen der betreffenden Classification fehl.

1. Aktivieren Sie das Kontrollkästchen neben einer oder mehreren Report Suites, bei denen die Einstellungen übereinstimmen.
1. Klicken Sie auf **[!UICONTROL Anwenden]**.

   Nachdem eine Beschriftung angewendet wurde, wird eine Statusmeldung angezeigt. Die Statusmeldung enthält die Namen der Zielvariablen oder Klassifizierungen und die zugehörigen Report Suites, für die die Kopie fehlgeschlagen ist.

   >[!IMPORTANT]
   >
   >Sie sollten immer die Ziel-Report Suites überprüfen, um sicherzustellen, dass die Beschriftungen korrekt kopiert wurden. Dies ist insbesondere für Variablen mit ID- oder DEL-Beschriftungen wichtig.

## Exportieren in eine CSV-Datei {#export-csv}

Sie können eine CSV-Datei herunterladen, die alle aktuellen Beschriftungsdefinitionen für alle Variablen für die ausgewählten Report Suites enthält. Es wird empfohlen, dass Ihre Rechtsabteilung die Beschriftungseinstellungen überprüft. Diese Überprüfung wird mithilfe dieser Option vereinfacht. Statt die Überprüfung durchführen zu müssen, während Sie bei der Data-Governance-Benutzeroberfläche angemeldet sind, können Sie einfach die CSV-Datei weitergeben.

1. Klicken **[!UICONTROL CSV exportieren]** oben rechts und dieses Dialogfeld wird angezeigt:

   ![](assets/export_csv.png)

1. Wählen Sie eine oder mehrere Report Suites aus, für die Sie alle Data Governance-Einstellungen exportieren möchten.

## Bearbeiten von Datenschutzbezeichnungen {#edit}

Siehe [Zuweisen oder Bearbeiten von Datenschutzbezeichnungen für Report Suites](/help/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md).
