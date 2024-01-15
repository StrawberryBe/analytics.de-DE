---
description: Das Dialogfeld „Datenschutzkennzeichnungen für Data Governance“ bietet einen Überblick über die Datenschutzkennzeichnungen und Namespaces einer Report Suite. Sie können die Einstellungen von hier aus auch in eine CSV-Datei exportieren.
title: Anzeigen/Verwalten von Datenschutzkennzeichnungen für Data Governance
feature: Data Governance
role: Admin
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 94%

---

# Anzeigen/Verwalten von Datenschutzkennzeichnungen für Data Governance

Das Dialogfeld **[!UICONTROL Datenschutzkennzeichnungen für Data Governance]** bietet einen Überblick über die Datenschutzkennzeichnungen und Namespaces einer Report Suite. Sie können die Einstellungen von hier aus auch in eine CSV-Datei exportieren.

## Anzeigen von Datenschutzkennzeichnungen {#view-privacy}

1. Melden Sie sich bei Adobe Experience Cloud an.
2. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Data Governance]**.

   >[!NOTE]
   >
   >Wenn dieses Menüelement nicht angezeigt wird, müssen Sie zu einem [Produktprofil in der Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html?lang=de) über Berechtigungen für diese Funktion verfügen oder Zugriff auf eine Report Suite innerhalb der Admin Console erhalten haben.

3. Wählen Sie oben rechts eine Report Suite aus, deren Datenschutzkennzeichnungen Sie anzeigen oder verwalten möchten.

   ![](assets/privacy_labeling.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Name der Komponente]** | In dieser Spalte werden alle Komponenten (Dimensionen, Metriken) aufgelistet, die Teil dieser Report Suite sind. |
| **[!UICONTROL Identität]** | Die Kennzeichnung für Identitätsdaten („I“) wird verwendet, um Daten zu kategorisieren, über die eine bestimmte Person identifiziert oder kontaktiert werden kann. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-identity-labels) |
| **[!UICONTROL Vertraulichkeit]** | Diese Kennzeichnung („S“) wird verwendet, um vertrauliche Daten, wie z. B. geografische Daten, zu kategorisieren. In Zukunft werden zusätzliche Datenkennzeichnungen verfügbar sein, um andere Arten vertraulicher Informationen zu kennzeichnen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#sensitive-data-labels) |
| **[!UICONTROL DSGVO-Zugriff]** | Mit Data-Governance-Kennzeichnungen können Benutzende Daten klassifizieren, die datenschutzbezogene Informationen und vertragliche Bedingungen zur Einhaltung von Verordnungen und Unternehmensrichtlinien enthalten. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-access-labels) |
| **[!UICONTROL DSGVO-Löschung]** | Eine Löschkennzeichnung ist nur für Felder mit einem Wert erforderlich, der die Zuordnung eines Treffers zur betroffenen Person zulässt (d. h. der die Identifizierung der betroffenen Person ermöglicht). [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-delete-labels) |
| **[!UICONTROL Namespace]** | Wenn Sie eine Variable als ID-DEVICE oder ID-PERSON beschriften, werden Sie zum Bereitstellen eines Namespace aufgefordert. Sie können entweder einen zuvor definierten Namespace verwenden oder einen neuen definieren. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#provide-namespace) |
| **[!UICONTROL Kategorie]** | Bezieht sich auf den Komponententyp, z. B. Standardkomponente, Konversionsvariable usw. |

{style="table-layout:auto"}

## Kopieren von Datenschutzkennzeichnungen in eine Report Suite  {#copy-to-rs}

Wenn Sie dieselben Datenschutzeinstellungen auf mehr als eine Report Suite anwenden möchten, führen Sie folgende Schritte aus:

1. Wählen Sie die Variable aus, die Sie kopieren möchten. Beachten Sie, dass Sie jeweils nur die Kennzeichnungen für eine Variable kopieren können.
1. Klicken Sie im Dialogfenster „Data Governance“ unten auf **[!UICONTROL In Report Suite(s) kopieren]**.

   ![In die Report Suite kopieren](assets/copy_to_reportsuite.png)

1. Der folgende Bildschirm enthält den Variablennamen, die aktuell angewendeten Kennzeichnungen, die Sie kopieren möchten, die Report Suites und deren IDs sowie Informationen darüber, ob die Einstellungen in den Ziel-Report-Suites passend sind.

   ![Kopieren von Kennzeichnungen in die Report Suite](assets/copy_to_rs.png)

   >[!IMPORTANT]
   >
   >Denken Sie daran, dass alle ausgewählten Report Suites Ihrer Experience Cloud-Organisation zugeordnet sein müssen.

   Wenn Sie die Kennzeichnungen für eine Variable oder Variablengruppe in eine andere Report Suite kopieren, wird die Kopie an der entsprechenden Stelle in der Ziel-Report Suite abgelegt. Bei Standardkomponenten, Listenvariablen und Erfolgsereignissen werden die Kennzeichnungen in die **gleichnamige Variable** in der Ziel-Report-Suite kopiert.

   Bei Konversionsvariablen (eVars) und Traffic-Dimensionen (Props) wird die Kopie jedoch unter der Variablen mit **derselben Nummer** in der zielseitigen Report Suite erstellt. eVar12 wird beispielsweise zu eVar12 in allen Ziel-Report Suites kopiert. Die Namen dieser Variablen werden bei der Bestimmung des Ziels der Kopie ignoriert. Wenn die entsprechende Variable in der Ziel-Report Suite nicht aktiviert ist, schlägt die Kopie für diese Variable fehl.

   Beim Kopieren der Beschriftungen für Klassifizierungen, die für eine Variable definiert sind, werden die Beschriftungen in eine Klassifizierung für die entsprechende Variable in der Ziel-Report Suite kopiert (z. B. eVar7 zu eVar7), deren Name identisch mit der kopierten Klassifizierung ist. Andernfalls schlägt die Kopie der Kennzeichnung der betreffenden Klassifizierung fehl.

1. Aktivieren Sie das Kontrollkästchen neben einer oder mehreren Report Suites mit passenden Einstellungen.
1. Klicken Sie auf **[!UICONTROL Anwenden]**.

   Nach dem Anwenden einer Kennzeichnung wird eine Statusmeldung angezeigt. Die Statusmeldung enthält die Namen der Zielvariablen oder Klassifizierungen und die zugehörigen Report Suites, für die die Kopie fehlgeschlagen ist.

   >[!IMPORTANT]
   >
   >Sie sollten immer die zielseitigen Report Suites überprüfen, um sicherzustellen, dass die Kennzeichnungen korrekt kopiert wurden. Dies ist insbesondere für Variablen mit ID- oder DEL-Kennzeichnungen wichtig.

## Exportieren in eine CSV-Datei {#export-csv}

Sie können eine CSV-Datei herunterladen, die alle aktuellen Kennzeichnungsdefinitionen für alle Variablen der ausgewählten Report Suite(s) enthält. Es wird empfohlen, dass Ihre Rechtsabteilung Ihre Kennzeichnungen überprüft, und diese Option erleichtert diese Überprüfung. Auf diese Weise müssen die Prüfenden zur Überprüfung nicht in der Data-Governance-Benutzeroberfläche angemeldet sein. Stattdessen können Sie ihnen einfach die CSV-Datei zusenden.

1. Klicken Sie oben rechts auf **[!UICONTROL CSV exportieren]**. Daraufhin wird dieses Dialogfeld angezeigt:

   ![](assets/export_csv.png)

1. Wählen Sie eine oder mehrere Report Suites aus, deren Data-Governance-Einstellungen exportiert werden sollen.

## Bearbeiten von Datenschutzkennzeichnungen {#edit}

Siehe [Zuweisen oder Bearbeiten von Report-Suite-Datenschutzkennzeichnungen](/help/admin/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md).
