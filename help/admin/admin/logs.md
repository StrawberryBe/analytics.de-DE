---
description: Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen.
title: Protokolle
feature: Admin Tools
exl-id: 43f79e2a-2cb9-47eb-982a-54714c9cbafc
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 67%

---

# Protokolle

Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Protokolle]**

## Admin-Protokoll {#section_8ADE8A7204A8401C968ABC20AECA381D}

Das Admin-Protokoll enthält alle Änderungen, die von Administratoren in den Admin-Tools vorgenommen wurden. Das Protokoll bietet ein Gateway zu benutzerdefinierten Berichten aus jedem der drei Protokolle. Sie können nach Ereignissen suchen, die Ihre Kriterien in einem bestimmten Datumsbereich erfüllen.

## Nutzungs- und Zugriffsprotokoll  {#section_6FBAF92D9EA244809C45A78A2F0A7232}

Das [!UICONTROL Nutzungs- und Zugriffsprotokoll] ermöglicht es Ihnen, die Berichtsnutzung auf Benutzerkontenebene auszuwerten. Beispielsweise können Sie damit Aktionen wie Öffnen, Erstellen, Aktualisieren, Aufheben der Freigabe und Löschen in Analysis Workspace verfolgen. Das bietet einen besseren Überblick darüber, wer Workspace wie häufig nutzt.

| Element | Beschreibung |
|---|---|
| Datumsbereich | Geben Sie einen Filter für den Datumsbereich an. Sie können ein Datum manuell im Format JJJJ-MM-TT eingeben oder auf das Kalendersymbol klicken und ein Datum auswählen. |
| Anmelden | Filtern Sie das Protokoll nach dem Benutzernamen. |
| IP | Filtern Sie das Protokoll nach der IP-Adresse. |
| Report Suite | Filtern Sie das Protokoll nach einer bestimmten Report Suite-ID. |
| Ereignistyp | Filtern Sie das Protokoll nach Ereignistyp. Wählen Sie einen Ereignistyp aus der Dropdownliste aus. Siehe die vollständige Liste der Ereignistypen unten. |
| Ereignis- | Filtern Sie das Protokoll nach einzelnen oder mehreren Wörtern aus der Ereignisbeschreibung. |
| Bericht herunterladen | Exportiert den Inhalt des [!UICONTROL Nutzungs- und Zugriffsprotokolls] in eine durch Tabulatoren getrennte Datei. |

### Ereignistypen

| Ereignistyp | Beschreibung |
| --- | --- |
| Keine Kategorie | Kann ein beliebiger Ereignistyp sein. |
| Anmeldung fehlgeschlagen | Der Benutzeranmeldungsprozess ist fehlgeschlagen. |
| Anmeldung erfolgreich | Benutzer hat sich erfolgreich angemeldet. |
| Admin-Aktion | Es kam zu einer Administratoraktion, z. B. zum Bearbeiten einer Report Suite, zum Ändern der Unternehmenseinstellungen, zum Erstellen eines Benutzers usw. |
| Änderung der Sicherheitseinstellung | Eine Sicherheitseinstellung wurde geändert. |
| Bericht angezeigt | Ein Reports &amp; Analytics-Bericht wurde angezeigt. |
| Bericht heruntergeladen | Ein Reports &amp; Analytics-Bericht wurde heruntergeladen. |
| Warnhinweis gesendet | Es wurde ein Warnhinweis gesendet. |
| Benutzeraktion | Die Benutzerinformationen wurden bearbeitet. |
| Tool angezeigt | Ein Tool wurde angezeigt. |
| Omniture-Aktion | Eine Aktion wurde von Adobe ausgeführt. |
| Kennwortwiederherstellung | Ein Passwort wurde wiederhergestellt. |
| BookMarks | Ein Lesezeichen wurde verwaltet. |
| Dashboards | Ein Dashboard wurde verwaltet. |
| Warnhinweise | Ein Warnhinweis wurde verwaltet. |
| Kalenderereignisse | Ein Kalenderereignis wurde verwaltet. |
| Zielgruppen | Eine Zielgruppe wurde verwaltet. |
| Berichtseinstellungen | Eine Berichtseinstellung wurde verwaltet. |
| Terminierte Berichte | Ein terminierter Bericht wurde verwaltet. |
| Nach IP ausschließen | Die IP-Einstellung wurde geändert. |
| Seiten benennen | Nicht mehr verwendet |
| Klassifizierungen | Eine Classification wurde verwaltet. |
| Datenquellen | Eine Datenquelle wurde verwaltet. |
| Workspace-Projekt | Ein Workspace-Projekt wurde angezeigt oder bearbeitet. |
| Segment | Ein Segment wurde erstellt/bearbeitet. |
| Berechnete Metrik | Eine berechnete Metrik wurde erstellt/bearbeitet. |
| Datumsbereich | Ein Datumsbereich wurde erstellt/bearbeitet. |
| Virtual Report Suite | Eine Virtual Report Suite wurde erstellt/bearbeitet. |
| Beitragsanalyse | Ein Beitragsanalyseauftrag wurde ausgeführt. |
| API-Methode | Es wurde ein API-Aufruf durchgeführt. |


## Report Suite-Änderungsprotokoll  {#section_3864966639414BBEA871F4D0352F56B6}

Das Report Suite-Änderungsprotokoll enthält alle Änderungen, die außerhalb von Admin an Ihren Report Suites vorgenommen wurden.

Unter anderem kann mit den folgenden Tools eine Report Suite außerhalb der [!UICONTROL Admin Tools] geändert werden:

* Classifications-Uploads über einen Webbrowser (Classifications-Uploads über FTP werden im Änderungsprotokoll nicht berücksichtigt)
* Änderungen, die in früheren Versionen vorgenommen wurden.
* Von einem Kundenbetreuer oder durch den Kundendienst mit internen Werkzeugen vorgenommene Änderungen

| Element | Beschreibung |
|---|---|
| Datumsbereich | Geben Sie einen Filter für den Datumsbereich an. Sie können ein Datum manuell im Format JJJJ-MM-TT eingeben oder auf das Kalendersymbol klicken und ein Datum auswählen. |
| Firma | Filtern Sie das Protokoll nach dem Firmennamen. |
| Anmelden | Filtern Sie das Protokoll nach dem Benutzernamen. |
| IP | Filtern Sie das Protokoll nach der IP-Adresse. |
| Ereignis- | Filtern Sie das Protokoll nach einzelnen oder mehreren Wörtern aus der Ereignisbeschreibung. |
| Bericht herunterladen | Exportiert den Inhalt des [!UICONTROL Nutzungs- und Zugriffsprotokolls] in eine durch Tabulatoren getrennte Datei. |
