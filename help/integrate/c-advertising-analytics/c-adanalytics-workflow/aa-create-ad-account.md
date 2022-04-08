---
title: Einrichten eines Werbekontos in Advertising Analytics
description: Ermöglicht die Erstellung neuer Werbekonten und die Zuordnung mehrerer Konten zu mehreren Report Suites.
feature: Advertising Analytics
exl-id: f593c714-e85f-4000-85b2-6294cad81e25
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: ht
source-wordcount: '819'
ht-degree: 100%

---

# Werbekonto einrichten

Adobe Analytics-Administratoren können neue Werbekonten erstellen und mehrere Konten verschiedenen Report Suites zuordnen (1:1, 1:n, n:n).

Administratoren können auch [Nicht-Administratoren Zugriff gewähren](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369), damit sie Werbekonten einrichten können.

![](assets/aa_accounts.png)

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Werbekonten]**.
1. (Nur bei erster Verwendung) Akzeptieren Sie die Bedingungen der Endnutzer-Lizenzvereinbarung.
1. Klicken Sie auf **[!UICONTROL + Hinzufügen]**.
1. Das Dialogfeld [!UICONTROL Neues Suchmaschinenkonto] wird angezeigt:

   ![](assets/aa_new_se_account.png)

1. Legen Sie die **[!UICONTROL Suchmaschineneinstellungen]** gemäß folgenden Richtlinien fest:

   | Einstellung | Beschreibung |
   | --- | --- |
   | Typ | Sie haben zwei Optionen: Google AdWords und Microsoft Bing Ads.  Hinweis: Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar. |
   | Kontoname | Sie können einen beliebigen Kontonamen festlegen. Dieser Name wird später in der Benutzeroberfläche angezeigt. |
   | OAuth-Token | **Hinweis:** Bei OAuth handelt es sich um einen offenen Zugriffsstandard, der häufig eingesetzt wird, um Websites oder Anwendungen Zugang zu Informationen auf anderen Websites zu bieten, ohne hierzu Passwörter preiszugeben. Dabei werden Sie an eine Drittanbieter-URL (efrontier.com) umgeleitet. Adobe nutzt efrontier, um den OAuth-Authentifizierungsprozess für alle drei Suchmaschinen zu verarbeiten. Wenn Sie Internet Explorer 11 (oder niedriger) verwenden, können Sie für keine der drei Suchmaschinen das OAuth-Token abrufen. Verwenden Sie stattdessen einen anderen Webbrowser.<p>Wenn Sie auf **[!UICONTROL Token abrufen]** klicken, wird der OAuth2-Authentifizierungsprozess gestartet. Sie werden daraufhin aufgefordert, sich mit Ihren Anmeldedaten bei Ihrem Google- oder Bing-Suchkonto anzumelden. Je nach ausgewählter Suchmaschine ist der Prozess leicht unterschiedlich: <ul><li>Google AdWords: Geben Sie die Google-Konto-ID an</li><li>Microsoft Bing: Geben Sie die Bing-Konto-ID und die Bing-Kunden-ID an.</li></ul>Weitere Informationen finden Sie unter Informationen zu diesen IDs finden Sie unter [Finden Ihrer Konto-ID](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md). Nachdem Sie sich erfolgreich angemeldet haben, wird im Feld **[!UICONTROL OAuth-Token]** **[!UICONTROL Abgerufen]** angezeigt. |

1. Geben Sie im Abschnitt **[!UICONTROL Tracking]** Informationen dazu ein, wie die Suchmaschine von Ihrer Adobe Analytics-Implementierung verfolgt wird. Dieser Schritt ist erforderlich, um die Adobe Analytics-Daten ordnungsgemäß mit den Suchmaschinendaten zu ergänzen.
Legen Sie die **[!UICONTROL Tracking-Einstellungen]** gemäß folgenden Richtlinien fest:

   | Einstellung | Beschreibung |
   | --- | --- |
   | Typ | <ul><li>**Auto**: Hier entscheidet die Advertising Cloud-Engine, wie die Tracking-Parameter an die Tracking-Vorlagen/Ziel-URLs der Suchmaschine angehängt werden. Dies ist der einfachste Ansatz, der jedoch möglicherweise nicht zum besten integrierten Datensatz führt.<br>**Wichtig:** Um ein Suchmaschinenkonto im Auto-Modus zu konfigurieren, müssen Sie die folgenden Aktionen ausführen:<br>- Der Parameter „s_kwcid“ und der Wert werden den Konto-Tracking-Vorlagen oder Landingpages-URLs im hinzugefügten Konto hinzugefügt. Die Einfügung erfolgt am Ende der URL. Daher können zusätzliche Maßnahmen von Ihrer Seite erforderlich sein, wenn Ihr Webserver ein bestimmtes „key=value“-Paar am Ende der URL ODER ein Update zur Unterstützung eines neuen „key=value“-Paares in der URL erfordert. **Hinweis:** Erfahren Sie mehr darüber, ob Sie diesen Parameter zu Ihrer [Richtlinie zur Inhaltssicherheit](https://experienceleague.adobe.com/docs/id-service/using/reference/csp.html?lang=de) hinzufügen sollten.<br>- Darüber hinaus können Keywords als Teil des Wertes „s_kwcid“ in die Landingpage-URL eingefügt werden. Wenn sie Sonderzeichen oder Symbole enthalten, überprüfen Sie daher, ob Ihr Webserver diese Zeichen unterstützen kann. (Ein häufig verwendetes Sonderzeichen ist beispielsweise „+“, das in „Broad Match Modified“-Keywords verwendet wird.)</li><li>**Manuell**: Hierüber können Sie verwalten, wie Tracking-Parameter zu den Tracking-Vorlagen/Ziel-URLs der Suchmaschine hinzugefügt werden. [Weitere Informationen finden Sie in den Beispielen für manuelles Tracking für die einzelnen Suchmaschinen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md).</li></ul> |

1. Wählen Sie im Abschnitt **[!UICONTROL Zuordnung]** aus, welche Report Suite(s) mit diesem Suchmaschinenkonto verknüpft werden soll(en). Sie müssen mindestens eine Report Suite angeben, bevor Sie das Werbekonto speichern können. Sie können mehrere Konten verschiedenen Report Suites zuordnen (1:1, 1:n, n:n). Beachten Sie, dass die Daten, die AMO aus der Suchmaschine abruft, einfach in die zugeordnete Report Suite kopiert werden. Die Daten werden also nicht aufgeteilt.

   >[!IMPORTANT]
   >
   >Nur Report Suites, die einer Experience Cloud-Organisation zugeordnet sind, können ausgewählt werden. Wenn Ihre Report Suite nicht aufgeführt ist, suchen Sie im Abschnitt [Problembehebung in Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md) nach weiteren Informationen.

   Legen Sie die **[!UICONTROL Zuordnungseinstellungen]** gemäß folgenden Richtlinien fest:

   | Einstellung | Beschreibung |
   | --- | --- |
   | Report Suite Zuordnen | Die Report-Suite-Zuordnung bestimmt die Report Suite, die mit diesem Suchmaschinenkonto verknüpft werden soll. Anders ausgedrückt: Sie bestimmt, an welche Report Suite(s) die Daten der Suchmaschine gesendet werden. |


1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Nachdem Sie auf „Speichern“ geklickt haben, wird ein Haftungsausschluss mit einer Reihe von Hinweisen angezeigt. Sie werden dazu aufgefordert zu bestätigen, dass Sie die Vereinbarung gelesen und verstanden haben. Aktivieren Sie das Kontrollkästchen und klicken Sie auf **[!UICONTROL OK]**.

   Nun wird die [Verwaltungsoberfläche](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md) für Werbekonten angezeigt, in der das neu erstellte Konto aufgeführt sein sollte.

>[!NOTE]
>
>Es dauert in der Regel mindestens 24 Stunden, bis Suchmaschinendaten in Ihren Analytics-Berichten angezeigt werden.
