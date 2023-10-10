---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Abbrechen von Berichtsanforderungen im Reporting Activity Manager
feature: Admin Tools
source-git-commit: 4da5da34518c3fb7350799c185faed789ef5a22b
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 7%

---

# Abbrechen von Berichtsanforderungen im Reporting Activity Manager

{{release-limited-testing}}

Die [!UICONTROL Reporting Activity Manager] ermöglicht es Administratoren, Berichtsanforderungen schnell zu diagnostizieren und abzubrechen, um Probleme mit der Berichtskapazität während Spitzenzeiten der Berichterstellung zu beheben.

Beachten Sie beim Abbrechen von Berichtsanforderungen Folgendes:

* Sie können bestimmte Anforderungen abbrechen, alle Anforderungen eines bestimmten Benutzers abbrechen oder alle Anforderungen im Zusammenhang mit einem bestimmten Projekt abbrechen.

* Wenn Sie Anforderungen abbrechen, können Sie auch nachfolgende Anforderungen für einen bestimmten Zeitraum einschränken.

* Sie können eine Anforderung nicht abbrechen, wenn die Variable [!UICONTROL **Benutzer**] -Spalte einer Anforderung wird als [!UICONTROL **Nicht erkannt**]. In diesem Fall bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben.

Weitere Informationen zum Reporting Activity Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Übersicht über die Berichterstellung in Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Bestimmte Anforderungen abbrechen

Sie können einzelne Anforderungen abbrechen, die eine große Menge an Berichtskapazität beanspruchen.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Anforderungen**] und wählen Sie dann eine oder mehrere Anforderungen aus.

   <!-- add screenshot -->

1. Auswählen [!UICONTROL **Anforderungen abbrechen**].

   Die [!UICONTROL **Abbrechen _x_ Berichtsanforderungen**] angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) Um zukünftige Anforderungen für einen bestimmten Zeitraum zu beschränken, aktivieren Sie die Option [!UICONTROL **Einschränken nachfolgender Anforderungen**] und wählen Sie dann aus den folgenden Optionen aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Benutzerin bzw. Benutzer und Projekt**] | Benutzer, die mit den ausgewählten Anforderungen verknüpft sind, sind vorübergehend von der Ausführung von Berichtsanfragen für die verknüpften Projekte ausgeschlossen. |
   | [!UICONTROL **Benutzer**] | Benutzende, die mit den ausgewählten Anträgen verknüpft sind, können vorübergehend keine weiteren Reporting-Anfragen stellen. |
   | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von allen Reporting-Anfragen ausgeschlossen. |
   | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!-- double-check this --><p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

   {style="table-layout:auto"}

1. Auswählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Abbrechen von Anforderungen durch den Benutzer

Sie können alle Anforderungen abbrechen, die mit einem oder mehreren Benutzern verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Benutzer**] und wählen Sie einen oder mehrere Benutzer aus.

   <!-- add screenshot -->

1. Auswählen [!UICONTROL **Anforderungen abbrechen**].

   Die [!UICONTROL **Abbrechen _x_ Berichtsanforderungen von x Benutzern**] angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) Um zukünftige Anforderungen für einen bestimmten Zeitraum zu beschränken, aktivieren Sie die Option [!UICONTROL **Einschränken nachfolgender Anforderungen**] und wählen Sie dann aus den folgenden Optionen aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Benutzerin bzw. Benutzer und Projekt**] | Ausgewählte Benutzer sind vorübergehend daran gehindert, Reporting-Anfragen für die zugehörigen Projekte zu stellen. |
   | [!UICONTROL **Benutzer**] | Ausgewählte Benutzer können vorübergehend keine Reporting-Anfragen stellen. |
   | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Benutzern verknüpft sind, sind auf Berichterstellungsanforderungen eines beliebigen Benutzers beschränkt. |
   | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

   {style="table-layout:auto"}

1. Auswählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Anforderungen nach Projekt abbrechen

Sie können alle Anforderungen abbrechen, die mit einem oder mehreren Projekten verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Projekte**] und wählen Sie ein oder mehrere Projekte aus.

   <!-- add screenshot -->

1. Auswählen [!UICONTROL **Anforderungen abbrechen**].

   Die [!UICONTROL **Abbrechen _x_ Berichtsanforderungen aus x Projekten**] angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) Um zukünftige Anforderungen für einen bestimmten Zeitraum zu beschränken, aktivieren Sie die Option [!UICONTROL **Einschränken nachfolgender Anforderungen**] und wählen Sie dann aus den folgenden Optionen aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Benutzerin bzw. Benutzer und Projekt**] | Ausgewählte Projekte sind vorübergehend auf Berichterstellungsanfragen der zugehörigen Benutzer beschränkt. |
   | [!UICONTROL **Benutzer**] | Benutzer, die mit den ausgewählten Projekten verknüpft sind, können keine Berichterstellungsanfragen stellen. |
   | [!UICONTROL **Projekt**] | Ausgewählte Projekte sind vorübergehend von jeglichen Berichtsanfragen eines Benutzers ausgeschlossen. |
   | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

   {style="table-layout:auto"}

1. Auswählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Erlebnis beim Zugriff auf einen abgebrochenen Bericht

In Analysis Workspace sehen Benutzer die folgende Meldung, wenn sie versuchen, auf einen Bericht zuzugreifen, der von einem Administrator abgebrochen wurde:

![cancel-user-notice](/help/admin/admin/assets/cancel-user-facing.png)