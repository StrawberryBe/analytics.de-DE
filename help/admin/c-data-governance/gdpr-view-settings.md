---
description: Über das Data-Governance-Dialogfeld in den Admin Tools können Sie einsehen, welche Report Suites für Data Governance konfiguriert wurden, ob sie einer Experience Cloud-Organisation zugeordnet wurden und ob für die entsprechende Report Suite eine Richtlinie zur Datenaufbewahrung vorhanden ist.
title: Data-Governance-Einstellungen von Report Suites anzeigen/verwalten
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 538d5bcea449ecb868ff9ebcce4ca742f91b4a87
workflow-type: ht
source-wordcount: '517'
ht-degree: 100%

---

# Data-Governance-Einstellungen von Report Suites anzeigen/verwalten

Über das Data-Governance-Dialogfeld in den Admin Tools können Sie einsehen, welche Report Suites für Data Governance konfiguriert wurden, ob sie einer Experience Cloud-Organisation zugeordnet wurden und ob für die entsprechende Report Suite eine Richtlinie zur Datenaufbewahrung vorhanden ist.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Öffnen Sie **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]**.

>[!NOTE]
>
>Wenn dieser Menüpunkt nicht angezeigt wird, müssen Sie sich zu einem [Produktprofil in Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html?lang=de) hinzufügen lassen, das über die entsprechenden Berechtigungen für diese Funktion verfügt.

1. So zeigen Sie alle Report Suites an, die zu Ihrem angemeldeten Unternehmen gehören:

   ![](assets/privacy_setup_an.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Report Suites]** | Die erste Zeile enthält den Anzeigenamen der Report Suite. Die zweite Zeile enthält den internen Namen der Report Suite. Wenn Sie Beschriftungen für eine Report Suite festlegen dürfen, befindet sich in der ersten Zeile ein Link, auf den Sie klicken können und über den Sie zur Beschriftungsseite gelangen. |
| **[!UICONTROL Organisationszuordnung]** | <ul><li>Zugeordnet: Diese Report Suite wurde bereits derselben Experience Cloud-Organisation wie das Analytics-Anmeldeunternehmen zugeordnet, bei dem Sie angemeldet sind. Es können nur Report Suites mit dieser Einstellung beschriftet werden.</li><li>Einer anderen Organisation zugeordnet: Diese Report Suite wurde bereits einer anderen Experience Cloud-Organisation zugeordnet.</li></ul> |
| **[!UICONTROL Richtlinie zur Datenaufbewahrung]** | Für die Datenschutzimplementierung in Analytics müssen Sie eine Richtlinie zur Datenaufbewahrung erstellen. Diese Einstellung zeigt:<ul><li>ob eine Richtlinie zur Datenaufbewahrung für die entsprechende Report Suite vorhanden ist und</li><li>wie lange die Daten von Adobe aufbewahrt werden, bis sie gelöscht werden. Standardmäßig beträgt der Aufbewahrungszeitraum 25 Monate.</li></ul>**Hinweis:** Adobe Analytics kann Sie nicht bei der Verarbeitung von Anfragen an die Datenschutz-API unterstützen, also bei der Verarbeitung von Zugriffs- oder Löschungsanfragen, die Sie von Ihren Endnutzer/innen erhalten, wenn keine Datenspeicherungsfrist festgelegt wurde. Wenden Sie sich an Ihren Customer Success Manager, um den Zeitraum der Datenaufbewahrung festzulegen. |
| **[!UICONTROL Gruppen]** | Die Gruppierungsfunktionalität ist derzeit nicht implementiert. |
| Linke Sidebar | Klicken Sie auf das Trichtersymbol, um die Sidebar zu öffnen oder zu schließen. Im Abschnitt [!UICONTROL Organisationszuordnung] wird die Anzahl der Report Suites angezeigt, die in jede der beschriebenen Kategorien fallen. Im Abschnitt [!UICONTROL Datenspeicherungsrichtlinie] wird jede einzelne Datenspeicherungsrichtlinie angezeigt, die derzeit für Ihre Organisation gilt, sowie die Anzahl der Report Suites, denen diese Speicherrichtlinie zugewiesen wurde. |
| **[!UICONTROL In CSV exportieren]** | Wenn Sie das Kontrollkästchen neben einer oder mehreren Report Suites aktivieren, wird die Option „In CSV exportieren“ angezeigt. Mithilfe dieser Option können Sie eine CSV-Datei mit allen aktuellen Beschriftungsdefinitionen für sämtliche Variablen aller ausgewählten Report Suites herunterladen. Es wird empfohlen, dass Ihre Rechtsabteilung die Beschriftungseinstellungen überprüft. Diese Überprüfung wird mithilfe dieser Option vereinfacht. Statt die Überprüfung durchführen zu müssen, während Sie bei der Data-Governance-Benutzeroberfläche angemeldet sind, können Sie einfach die CSV-Datei weitergeben. |
