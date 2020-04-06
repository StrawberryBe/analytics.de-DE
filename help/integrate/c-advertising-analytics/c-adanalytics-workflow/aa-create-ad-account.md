---
title: Werbekonto einrichten
uuid: 4e37caa3-e4a5-43ad-97c0-12db62ad5283
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Werbekonto einrichten

Adobe Analytics-Administratoren können neue Werbekonten erstellen und mehrere Konten mehreren Report Suites zuordnen (1:1, 1:Many, Many:Many).

Administratoren können auch [Nichtadministratoren Zugriff auf Werbekonten zur Einrichtung von Werbekonten gewähren](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) .

![](assets/aa_accounts.png)

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Advertising Accounts]**.
1. (Nur Erstverwendung) Akzeptieren Sie die Bedingungen der Endbenutzer-Lizenzvereinbarung.
1. Klicken Sie auf **[!UICONTROL + Add]**.
1. Das [!UICONTROL New Search Engine Account] Dialogfeld wird angezeigt:

   ![](assets/aa_new_se_account.png)

1. Füllen Sie die **[!UICONTROL Search Engine Settings]** folgenden Richtlinien aus:

   <table id="table_B3BE66B7D4C54766B8FFD2C6DCD657AF"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Einstellung </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Typ </p> </td> 
      <td colname="col2"> <p>Sie haben zwei Möglichkeiten: Google AdWords und Microsoft Bing. </p> <p>Hinweis: Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar.  </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kontoname </p> </td> 
      <td colname="col2"> <p>Sie können diesen Kontonamen auf einen beliebigen Namen einstellen, der Ihnen passt. Dies ist der Anzeigename des Kontos, der in der Benutzeroberfläche angezeigt wird. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>OAuth-Token </p> </td> 
      <td colname="col2"> <p>Hinweis: Bei OAuth handelt es sich um einen offenen Zugriffsstandard, der häufig eingesetzt wird, um Websites oder Anwendungen Zugang zu Informationen auf anderen Websites zu bieten, ohne hierzu Passwörter preiszugeben. </p> <p>Hinweis: Hierbei werden Sie an eine Drittanbieter-URL (efrontier.com) umgeleitet. Adobe nutzt efrontier, um den OAuth-Authentifizierungsprozess für alle drei Suchmaschinen zu verarbeiten. </p> <p>Hinweis: Wenn Sie Internet Explorer 11 (oder niedriger) verwenden, können Sie für keine der drei Suchmaschinen das OAuth-Token abrufen. Verwenden Sie stattdessen andere Webbrowser. </p> <p>Durch Klicken auf<span class="uicontrol"> Token</span> abrufen wird der OAuth2-Authentifizierungsprozess gestartet. Das bedeutet, dass Sie mit Ihren Anmeldeinformationen bei Ihrem Google/Bing-Suchkonto angemeldet werden müssen. Je nachdem, welche Suchmaschine Sie ausgewählt haben, unterscheidet sich der Prozess geringfügig: </p> 
        <ul id="ul_FC9B5612F6554495B04C357CB0AB72EB"> 
        <li id="li_CD54231BFF134F83B3B5B14B34A0E1D2">Google Adwords: Geben Sie die Google-Konto-ID ein. </li> 
        <li id="li_89B9D54BAA914E5DB2959B193489582E">Microsoft Bing: Geben Sie die Bing-Konto-ID und die Bing-Kunden-ID ein. </li> 
        </ul> <p>Refer to <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md"  > Locate your Account ID</a> for information on these IDs. </p> <p>Sobald Sie sich erfolgreich angemeldet haben, wird im OAuth-Token-Feld 
        <systemoutput>
          „Abgerufen“ angezeigt
        </systemoutput>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Geben Sie im Abschnitt **[!UICONTROL Tracking]** Informationen dazu ein, wie die Suchmaschine von Ihrer Adobe Analytics-Implementierung verfolgt wird. Dieser Schritt ist erforderlich, um die Adobe Analytics-Daten ordnungsgemäß durch die Suchmaschinendaten zu ergänzen.
Füllen Sie die **[!UICONTROL Tracking Settings]** folgenden Richtlinien aus:

   <table id="table_1AB4E31456E84ABF8209B02058259C4D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Einstellung </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Typ </p> </td> 
      <td colname="col2"> 
        <ul id="ul_1C5A0502A4984E57A08417A91CCD6FFE"> 
        <li id="li_5736E38286FF494ABDDC6E85281D7F2A"> <span class="uicontrol"> Auto</span>: Hier entscheidet die Advertising Cloud-Engine, wie die Tracking-Parameter an die Tracking-Vorlagen/Ziel-URLs der Suchmaschine angehängt werden. Dies ist der einfachste Ansatz, der jedoch möglicherweise nicht zum besten integrierten Datensatz führt. <p>Wichtig: Wenn Sie ein Suchmaschinenkonto im „Auto-Modus“ konfigurieren möchten, sind Sie für die folgenden Aktionen verantwortlich: 
          <ul id="ul_4FF9D1E3CC4E452BA339E0A725D29FEE"> 
            <li id="li_6F3A6D6259C0420CB7E6FD2C26A1B6E0">Der Parameter und der Wert "s_kwcid"werden den Kontoverfolgungsvorlagen oder Landingpages-URLs im hinzugefügten Konto hinzugefügt. Dies wird am Ende der URL eingefügt. Daher kann es erforderlich sein, dass Sie zusätzliche Aktionen durchführen, wenn Ihr Webserver ein bestimmtes Schlüssel/Wert-Paar am Ende der URL oder ein Update benötigt, um ein neues Schlüssel/Wert-Paar in der URL zu unterstützen. </li> 
            <li id="li_A04D4AA31A934392808639E46C86573F">Darüber hinaus können Suchbegriffe als Teil des Werts "s_kwcid"in die Einstiegs-URL eingefügt werden. Wenn sie also Sonderzeichen oder Symbole enthalten, bestätigen Sie bitte, dass Ihr Webserver diese Zeichen unterstützen kann (ein Beispiel für häufig vorkommende Sonderzeichen ist "+", das in Suchbegriffen mit "Weit gefasst" verwendet wird). </li> 
          </ul> </p> </li> 
        <li id="li_EAA7A7CA1E584854A7EC1E43E13B63FE"><span class="uicontrol"> Manuell</span>: Hierüber können Sie verwalten, wie Tracking-Parameter zu den Tracking-Vorlagen/Ziel-URLs der Suchmaschine hinzugefügt werden. <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md"  > Weitere Informationen finden Sie in den Beispielen für manuelles Tracking für die einzelnen Suchmaschinen</a>. </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Wählen Sie im **[!UICONTROL Mapping]** Abschnitt die Report Suites aus, die mit diesem Suchmaschinenkonto verknüpft werden sollen. Sie müssen mindestens eine Report Suite angeben, bevor Sie das Advertising-Konto speichern können. Sie können mehreren Report Suites mehrere Konten zuordnen (1:1, 1:Many, Many:Many). Beachten Sie, dass die Daten, die AMO von der Suchmaschine abruft, einfach in eine zugeordnete Report Suite kopiert werden, sodass keine Daten geteilt werden.

   >[!IMPORTANT]
   >
   >Nur Report Suites, die [einer Experience Cloud-Organisation zugeordnet sind](https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html), stehen zur Auswahl zur Verfügung. Wenn Ihre Report Suite nicht aufgeführt ist, suchen Sie im Abschnitt [Problembehebung in Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md) nach weiteren Informationen.

   Für die **[!UICONTROL Mapping Settings]** folgenden Leitlinien:

   <table id="table_AF876DC40F97403882C0AA528BD204FF"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Einstellung </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Report Suite  Zuordnen </p> </td> 
      <td colname="col2"> <p>Die Zuordnung der Report Suite bestimmt die Report Suite, die mit diesem Suchmaschinenkonto verknüpft wird. Mit anderen Worten, es bestimmt, in welche Report Suite/n die Suchmaschinendaten gesendet werden. </p> <p>Wenn Ihre Report Suite nicht aufgeführt ist, können Sie sie mit diesem Tool <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html"  >einer Experience Cloud-Organisation zuordnen</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klicken Sie auf **[!UICONTROL Save]**.
1. Nach dem Speichern zeigt ein Haftungsausschluss eine Liste von Einschränkungen an. Sie werden gebeten zu bestätigen, dass Sie diese Vereinbarung gelesen haben und verstehen. Click the checkbox, then click **[!UICONTROL OK]**.

   Sie werden jetzt zur Benutzeroberfläche [Verwaltung](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md)der Advertising Accounts weitergeleitet, in der Ihr neu erstelltes Konto aufgeführt werden sollte.

>[!NOTE] Es dauert in der Regel mindestens 24 Stunden, bis Suchmaschinendaten in Ihren Analytics-Berichten angezeigt werden.

