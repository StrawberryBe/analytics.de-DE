---
description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
title: Interne URL-Filter
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 2beb4cd38fc8b48e2b34468a4570f7168aeacb78
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 30%

---


# Interne URL-Filter

Mit internen URL-Filtern können Sie die Referrer identifizieren, die Sie als intern für Ihre Site betrachten. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.

Ein Referrer oder eine verweisende Seite ist normalerweise die Seite, von der aus Besucher Ihre Website aufgerufen haben. Um Datenverzerrungen zu vermeiden, können Sie interne Seiten als Referrer herausfiltern. Berichte schließen gefilterte Referrer aus   der Dimension [Referrers](/help/components/dimensions/referrer.md), der Dimension [Referrerdomänen](/help/components/dimensions/referring-domain.md) und anderen Traffic-Quellendimensionen aus.

## Vorhandene interne URL-Filter anzeigen

>[!NOTE]
>
>Einige Report Suites verfügen über einen internen URL-Filter für einen Punkt (.) standardmäßig konfiguriert. Wenn dieser Filter vorhanden ist, wird der gesamte Traffic als intern klassifiziert. Berichte der verweisenden Stelle funktionieren erst mit dem Punkt (.) -Filter entfernt.

So überprüfen Sie, welche internen URL-Filter für eine Report Suite konfiguriert sind: <!-- I don't see the period in my instance? Is the following information valid? "To avoid this, remove the rule listing a period (.) as a filter, and add your own site. The reason why a period is the default internal URL filter is to allow data to be collected in the Pages report. If hits do not match internal URL filters, all pages come up as Other. A period is always somewhere in the URL, which guarantees the Pages report is populated.")-->

1. Auswählen **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** , um auf den Report Suite Manager zuzugreifen.

1. Wählen Sie die Report Suite aus, in der Sie prüfen möchten, welche internen URL-Filter konfiguriert sind, und wählen Sie dann **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**.

   Alle vorhandenen Filter werden im [!UICONTROL **Aktuelle Filter**] Abschnitt.

## Internen URL-Filter zu einer Report Suite hinzufügen

1. Auswählen **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** , um auf den Report Suite Manager zuzugreifen.

1. Wählen Sie die Report Suite aus, der Sie einen internen URL-Filter hinzufügen möchten, und wählen Sie dann **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**.

1. Geben Sie im Abschnitt Filter hinzufügen im bereitgestellten Feld die URL der Seite ein, die Sie filtern möchten, und wählen Sie dann [!UICONTROL **Hinzufügen**].

   Die von Ihnen hinzugefügte URL ist jetzt im [!UICONTROL **Aktuelle Filter**] Abschnitt.
