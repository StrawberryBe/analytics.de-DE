---
description: Mit dem Virtual Report Suite Manager können Administratoren Virtual Report Suites bearbeiten, hinzufügen, taggen, löschen, umbenennen, genehmigen, kopieren, exportieren und filtern. Er ist für Nicht-Admin-Benutzer nicht sichtbar.
keywords: Virtual Report Suite
title: Virtual Report Suites verwalten
topic: Reports and analytics
uuid: ce683c01-2d7d-4f2a-98db-946f68eda99b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Virtual Report Suites verwalten

Mit dem Virtual Report Suite Manager können Administratoren Virtual Report Suites bearbeiten, hinzufügen, taggen, löschen, umbenennen, genehmigen, kopieren, exportieren und filtern. Er ist für Nicht-Admin-Benutzer nicht sichtbar.

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]**

![](assets/vrs-manage.png)

>[!NOTE] Im Virtual Report Suite Manager sehen Sie nur Ihre eigenen Virtual Report Suites. You have to click **[!UICONTROL Show All]** to see everyone else&#39;s.

| Aufgabe | Beschreibung |
|--- |--- |
| Fügen Sie | Wechselt zum Virtual Report Suite Builder, in dem Sie neue Virtual Report Suites erstellen können. |
| Tag | Alle Benutzer können Tags für Segmente erstellen und eines oder mehrere Tags auf ein Segment anwenden. Sie können Tags jedoch nur für die Segmente anzeigen, deren Inhaber Sie sind. Welche Arten von Tags sollten Sie erstellen? Hier einige Vorschläge für nützliche Tags:<ul><li>Tags, die auf Teamnamen basieren, z. B. Social Marketing, Mobile Marketing</li><li>Projekt-Tags (Analyse-Tags), z. B. Entrypage-Analyse</li><li>Kategorien-Tags: Männer; Geografie</li><li>Workflow-Tags: Kuratiert für (eine bestimmte Geschäftseinheit); Genehmigt</li></ul> |
| Löschen | Wenn Sie eine Virtual Report Suite löschen, arbeiten terminierte Berichte und Dashboards, auf die diese Virtual Report Suite angewendet ist, normal weiter. Der Bericht oder das Dashboard verwendet die gelöschte Virtual Report Suite so lange weiter, bis Sie den terminierten Bericht erneut speichern.  Terminierte Berichte werden nicht aktualisiert, wenn Sie eine Virtual Report Suite mit demselben Namen bearbeiten.<br>Beispiel: Angenommen, Sie haben zwei Virtual Report Suites mit demselben Namen und unterschiedlichen übergeordneten Report Suites:<br>Sie haben ein Lesezeichen, das auf die Virtual Report Suite für die Report Suite „mainprod“verweist. Dann löschen Sie die Virtual Report Suite, weil es sich um ein Duplikat handelt. Das Lesezeichen wird weiterhin ausgeführt und bezieht sich auf die Definition der gelöschten VRS. Wenn Sie die Definition für die verbleibende VRS ändern, ändert sich die auf das Lesezeichen angewendete VRS nicht. Es verwendet die alte Definition. Um dies zu beheben, aktualisieren Sie das Lesezeichen, um auf die neue Definition zu verweisen. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht eine VRS verwendet, können Sie den Namen der VRS ändern, damit deutlich wird, ob das Lesezeichen die VRS verwendet. |
| Umbenennen | Überall, wo die Virtual Report Suite angezeigt wird, wie in der Report Suite-Auswahl, wird der neue Name angezeigt. |
| Genehmigen/Nicht genehmigen | Genehmigen Sie Virtual Report Suites, um sie &quot;offiziell&quot;oder &quot;kanonisch&quot;zu machen. Sie können den Prozess rückgängig machen, indem Sie die Genehmigung aufheben. |
| Kopieren | Erstellt eine eindeutige Kopie mit einer eigenen neuen Report Suite-ID, jedoch mit demselben Namen und derselben Definition. |
| In CSV exportieren | Exportiert die Definition der Virtual Report Suite in eine CSV-Datei. |
| Filter | Filtern Sie nach Tags, übergeordneter Report Suite, Inhabern und anderen Filtern (Alle anzeigen, Meine, Favoriten und Genehmigt). |
