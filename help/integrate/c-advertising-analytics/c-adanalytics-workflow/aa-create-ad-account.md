---
seo-title: Einrichten eines Anzeigenkontos
title: Einrichten eines Anzeigenkontos
uuid: 4 e 37 caa 3-e 4 a 5-43 ad -97 c 0-12 db 62 ad 5283
translation-type: tm+mt
source-git-commit: 463e28e9d710cc41e4ab4ace5e3861b8ae8fbdcc

---


# Einrichten eines Anzeigenkontos

Adobe Analytics-Administratoren können neue Werbekonten erstellen und mehrere Konten verschiedenen Report Suites zuordnen (1:1, 1:n, n:n).

Administratoren können auch [Nicht-Administratoren Zugriff gewähren](../../../integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369), damit sie Werbekonten einrichten können.

![](assets/aa_accounts.png)

1. In Adobe Analytics, navigate to **[!UICONTROL Admin]** &gt; **[!UICONTROL Advertising Accounts]**.
1. (Nur bei erster Verwendung) Akzeptieren Sie die Bedingungen der Endnutzer-Lizenzvereinbarung.
1. Klicken Sie auf **[!UICONTROL + Hinzufügen]**.
1. Das Dialogfeld [!UICONTROL Neues Suchmaschinenkonto] wird angezeigt:

   ![](assets/aa_new_se_account.png)

1. Legen Sie die **[!UICONTROL Suchmaschineneinstellungen]gemäß folgenden Richtlinien fest:**

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
      <td colname="col2"> <p>Sie haben zwei Optionen: Google adwords und Microsoft Bing Ads. </p> <p>Hinweis: Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar.  </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kontoname </p> </td> 
      <td colname="col2"> <p>Sie können einen beliebigen Kontonamen festlegen. Dieser Name wird später in der Benutzeroberfläche angezeigt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>OAuth-Token </p> </td> 
      <td colname="col2"> <p>Hinweis: Bei OAuth handelt es sich um einen offenen Zugriffsstandard, der häufig eingesetzt wird, um Websites oder Anwendungen Zugang zu Informationen auf anderen Websites zu bieten, ohne hierzu Passwörter preiszugeben. </p> <p>Hinweis: Hierbei werden Sie an eine Drittanbieter-URL (efrontier.com) umgeleitet. Adobe nutzt efrontier, um den OAuth-Authentifizierungsprozess für alle drei Suchmaschinen zu verarbeiten. </p> <p>Hinweis: Wenn Sie Internet Explorer 11 (oder niedriger) verwenden, können Sie für keine der drei Suchmaschinen das OAuth-Token abrufen. Verwenden Sie stattdessen einen anderen Webbrowser. </p> <p>Wenn Sie auf <span class="uicontrol">Token abrufen</span> klicken, wird der OAuth2-Authentifizierungsprozess gestartet. Sie werden daraufhin aufgefordert, sich mit Ihren Anmeldedaten bei Ihrem Google- oder Bing-Suchkonto anzumelden. Je nach ausgewählter Suchmaschine unterscheidet sich der Prozess leicht: </p> 
        <ul id="ul_FC9B5612F6554495B04C357CB0AB72EB"> 
        <li id="li_CD54231BFF134F83B3B5B14B34A0E1D2">Google AdWords: Geben Sie die Google-Konto-ID an. </li> 
        <li id="li_89B9D54BAA914E5DB2959B193489582E">Microsoft Bing: Geben Sie die Bing-Konto-ID und die Bing-Kunden-ID an. </li> 
        </ul> <p>Weitere Informationen finden Sie unter <a href="../../../integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md#concept_F7F67448F3B44342967E0419E96F384D" format="dita" scope="local"> Finden Sie Ihre Konto-ID</a>, um weitere Informationen zu diesen IDs zu erhalten. </p> <p>Sobald Sie sich erfolgreich angemeldet haben, wird das Feld oauth Token angezeigt. 
        <systemoutput>
          Abgerufen
        </systemoutput>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Geben Sie im Abschnitt **[!UICONTROL Tracking]Informationen dazu ein, wie die Suchmaschine von Ihrer Adobe Analytics-Implementierung verfolgt wird.** Dieser Schritt ist erforderlich, um die Adobe Analytics-Daten ordnungsgemäß durch die Suchmaschinendaten zu ergänzen.
Legen Sie die **[!UICONTROL Tracking-Einstellungen]gemäß folgenden Richtlinien fest:**

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
            <li id="li_6F3A6D6259C0420CB7E6FD2C26A1B6E0">Der Parameter „s_kwcid“ und der Wert „s_kwcid“ werden den Kontotracking-Vorlagen oder Landingpage-URLs in dem hinzugefügten Konto hinzugefügt. Die Einfügung erfolgt am Ende der URL. Daher können zusätzliche Maßnahmen von Ihrer Seite erforderlich sein, wenn Ihr Webserver ein bestimmtes „key=value“-Paar am Ende der URL ODER ein Update zur Unterstützung eines neuen „key=value“-Paares in der URL erfordert. </li> 
            <li id="li_A04D4AA31A934392808639E46C86573F">Darüber hinaus können Keywords als Teil des Wertes „s_kwcid“ in die Landingpage-URL eingefügt werden. Wenn sie Sonderzeichen oder Symbole enthalten, überprüfen Sie daher bitte, ob Ihr Webserver diese Zeichen unterstützen kann. (Ein häufig verwendetes Sonderzeichen ist beispielsweise „+“, das in „Broad Match Modified“-Keywords verwendet wird.) </li> 
          </ul> </p> </li> 
        <li id="li_EAA7A7CA1E584854A7EC1E43E13B63FE"><span class="uicontrol"> Manuell</span>: Hierüber können Sie verwalten, wie Tracking-Parameter zu den Tracking-Vorlagen/Ziel-URLs der Suchmaschine hinzugefügt werden. <a href="../../../integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md#concept_87B28BA9E7F84BA5972F69E6F3482A33" format="dita" scope="local"> Weitere Informationen finden Sie in den Beispielen für manuelles Tracking für die einzelnen Suchmaschinen</a>. </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Wählen Sie im Abschnitt **[!UICONTROL Zuordnung]aus, welche Report Suite(s) mit diesem Suchmaschinenkonto verknüpft werden soll(en).** Sie müssen mindestens eine Report Suite angeben, bevor Sie das Werbekonto speichern können. Sie können mehrere Konten verschiedenen Report Suites zuordnen (1:1, 1:n, n:n). Beachten Sie, dass die Daten, die AMO aus der Suchmaschine abruft, einfach in die zugeordnete Report Suite kopiert werden. Die Daten werden also nicht aufgeteilt.

   >[!IMPORTANT]
   >
   >Only report suites that have been [mapped to an Experience Cloud organization](https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html) will be available for selection. If you do not see your report suite listed, refer to [Troubleshoot Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md).

   Legen Sie die **[!UICONTROL Zuordnungseinstellungen]gemäß folgenden Richtlinien fest:**

   <table id="table_AF876DC40F97403882C0AA528BD204FF"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Einstellung </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Report-Suite-Zuordnung </p> </td> 
      <td colname="col2"> <p>Die Report-Suite-Zuordnung bestimmt die Report Suite, die mit diesem Suchmaschinenkonto verknüpft werden soll. Anders ausgedrückt: Sie bestimmt, an welche Report Suite(s) die Daten der Suchmaschine gesendet werden. </p> <p>Wenn Ihre Report Suite nicht aufgeführt ist, können Sie sie mit diesem Tool <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html" format="html" scope="external">einer Experience Cloud-Organisation zuordnen</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Nachdem Sie auf „Speichern“ geklickt haben, wird ein Haftungsausschluss mit einer Reihe von Hinweisen angezeigt. Sie werden dazu aufgefordert zu bestätigen, dass Sie die Vereinbarung gelesen und verstanden haben. Aktivieren Sie das Kontrollkästchen und klicken Sie auf **[!UICONTROL OK]**.

   Nun wird die [Verwaltungsoberfläche](../../../integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md#concept_531B99165A4E47B4B8849376B532AFDB) für Werbekonten angezeigt, in der das neu erstellte Konto aufgeführt sein sollte.

>[!NOTE]
>
>Sie sollten mindestens 24 Stunden warten, bis die Suchmaschinendaten Ihre Analytics-Berichte auffüllen.

