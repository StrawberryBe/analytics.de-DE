---
description: Überblick über Variablen und deren Einschränkungen
keywords: Analytics Implementation;variable;limitations;limits
subtopic: Variables
title: Variablen und Einschränkungen
topic: Developer and implementation
uuid: 028677a7-2132-4ee7-9cc1-697c2c09b087
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Variablen und Einschränkungen

Überblick über Variablen und deren Einschränkungen

>[!NOTE]
>
>Unter [Konfigurationsvariablen](/help/implement/js-implementation/c-variables/configuration-variables.md) und [Seitenvariablen](/help/implement/js-implementation/page-variables/page-variables.md) erhalten Sie einen detaillierten Überblick über die häufigsten Analytics-Variablen.

Die folgende Tabelle enthält einen Überblick über [!DNL Analytics]-Variablen:

| Variable | Beschreibung |
|---|---|
| s_account | Bestimmt die Report Suite, in der die Daten gespeichert und für Berichte verwendet werden. |
| browserHeight | Gibt die Höhe des Browser-Fensters an. |
| browserWidth | Gibt die Breite des Browser-Fensters an. |
| Kampagne | Identifiziert Marketing-Kampagnen, die Besucher zu Ihrer Site bringen sollen. Der Wert von  *`campaign`* wird meist einem Abfragezeichenfolgen-Parameter entnommen. |
| kanal | Gibt meist einen Abschnitt der Website an. So könnten bei einem Händler zum Beispiel die Abschnitte „Elektronik“, „Spielzeug“ oder „Kleidung“ heißen. Eine Mediensite könnte die Abschnitte „Nachrichten“, „Sport“ oder „Wirtschaft“ enthalten. |
| charSet | Wandelt den Zeichensatz der Webseite in UTF-8 um. |
| colorDepth | Gibt an, mit wie vielen Bit die Farbe eines Pixels angezeigt wird. |
| connectionType | Gibt (in Microsoft Internet Explorer) an, ob der Browser für eine LAN- oder eine Modemverbindung konfiguriert ist. |
| cookieDomainPeriods | Bestimmt anhand der Anzahl der Punkte, die in der Domäne der Seiten-URL vorhanden sind, die Domäne, in der das [!DNL Analytics][!UICONTROL -Besucher-ID]-Cookie (s_vi) gesetzt wird. Für `www.mysite.com` sollte *`cookieDomainPeriods`* „2“ sein. Für `www.mysite.co.jp` sollte *`cookieDomainPeriods`* „3“ sein. |
| cookieLifetime | Wird sowohl von JavaScript als auch von [!DNL Analytics]-Servern verwendet, um die Lebensdauer eines Cookies zu bestimmen. |
| cookiesEnabled | Gibt an, ob JavaScript Sitzungscookies von Erstanbietern setzen darf. |
| currencyCode | Gibt den Konversionskurs an, zu dem Umsätze umgerechnet werden sollen, bevor sie in den [!DNL Analytics]-Datenbanken gespeichert werden. In [!DNL Analytics]-Datenbanken werden alle Geldbeträge in einer Währung Ihrer Wahl gespeichert. Wenn diese Währung die in *`currencyCode`* angegebene Währung ist oder wenn *`currencyCode`* leer ist, wird keine Konversion angewendet. |
| dc | Hiermit können Sie auswählen, zu welchem Data Center Ihre Daten gesendet werden. |
| doPlugins | *`doPlugins`* ist ein Verweis auf die Funktion *`s_doPlugins`*. Es ermöglicht, dass die *`s_doPlugins`* an der entsprechenden Stelle in der JavaScript-Datei aufgerufen wird. |
| dynamicAccountList | Wählt dynamisch eine Report Suite aus, zu der die Daten gesendet werden. Die Variable *`dynamicAccountList`* enthält die Regeln, mit denen die Ziel-Report Suite ermittelt wird. |
| dynamicAccountMatch | Ruft mithilfe des DOM-Objekts den Abschnitt der URL ab, auf den alle in *`dynamicAccountList`* aufgeführten Regeln angewendet werden. Diese Variable ist nur gültig, wenn *`dynamicAccountSelection`* auf „True“ festgelegt ist. |
| dynamicAccountSelection | Hiermit können Sie die Report Suite anhand der URL der jeweiligen Seite dynamisch auswählen. |
| dynamicVariablePrefix | Ermöglicht Implementierungen für Flag-Variablen, die dynamisch aufgefüllt werden müssen. Dynamisch aufgefüllt werden können Cookies, Anforderungsheader und Abfragezeichenfolgen-Parameter von Bildanforderungen. |
| eVarN | Dient zum Erstellen von benutzerdefinierten Berichten im [!DNL Analytics][!UICONTROL -Konversionsmodul]. Wenn eine eVar auf einen Wert für einen Besucher gesetzt wird, wird dieser Wert in [!DNL Analytics] automatisch bis zu seinem Ablauf gespeichert. Sämtliche Erfolgsereignisse, die bei einem Besucher auftreten, während der eVar-Wert aktiv ist, werden im eVar-Wert gezählt. |
| events | Zeichnet allgemeine Warenkorb-Erfolgsereignisse und benutzerspezifische Erfolgsereignisse auf. |
| fpCookieDomainPeriods | Bestimmt anhand der Anzahl der Punkte, die in der Domäne der Seiten vorhanden sind, die Domäne, in dem andere [!DNL Analytics]-Cookies als dem [!UICONTROL Besucher-ID]-Cookie (s_vi) gesetzt werden. |
| hierN | Bestimmt die Position einer Seite in der Hierarchie der Site. Bei Sites mit mehr als drei Ebenen in der Sitestruktur ist diese Variable besonders nützlich. |
| homepage | Gibt (in Internet Explorer) an, ob die aktuelle Seite als Homepage des Benutzers festgelegt ist. |
| javaEnabled | Zeigt an, ob Java im Browser aktiviert ist. |
| javascriptVersion | Gibt die vom Browser unterstützte JavaScript-Version an. |
| linkDownloadFileTypes | Eine kommagetrennte Liste mit Dateierweiterungen. Wenn Ihre Site Links zu Dateien mit diesen Dateierweiterungen enthält, werden die URLs dieser Links im [!UICONTROL Dateidownloadbericht] aufgeführt. |
| linkExternalFilters | Wenn Ihre Site viele Links zu externen Sites enthält und Sie nicht sämtliche Exitlinks verfolgen möchten, können Sie *`linkExternalFilters`* einsetzen, damit Berichte nur zu einer bestimmten Untermenge von Exitlinks erstellt werden. |
| linkInternalFilters | Bestimmt, welche Links auf Ihrer Site Exitlinks sind. Die Variable enthält eine kommagetrennte Liste mit Filtern, die die Links darstellen, die zu Ihrer Site gehören. |
| linkLeaveQueryString | Bestimmt, ob die Abfragezeichenfolge in den [!UICONTROL Exitlinks]- und [!UICONTROL Dateidownload]berichten enthalten sein soll. |
| linkName | Eine bei der [!UICONTROL Linktracking] verwendete optionale Variable, die den Namen eines benutzerspezifischen Links, eines Exitlinks oder Downloadlinks angibt. Die Variable *`linkName`* ist normalerweise nicht erforderlich, da diese Variable durch den dritten Parameter in der Funktion *`tl()`* ersetzt wird. |
| linkTrackEvents | Enthält die Ereignisse, die mit benutzerspezifischen, Download- und Exitlinks gesendet werden sollen. Diese Variable wird nur berücksichtigt, wenn *`linkTrackVars`* „Ereignisse“ enthält. |
| linkTrackVars | Eine kommagetrennte Liste von Variablen, die mit benutzerspezifischen, Ausstiegs- und Downloadlinks gesendet werden sollen. Wenn *`linkTrackVars`* auf „“ festgelegt ist, werden alle Variablen, die über Werte verfügen, mit den Linkdaten gesendet. |
| linkType | Eine bei der Linktracking verwendete optionale Variable, die bestimmt, in welchem Bericht (benutzerspezifische, Download- oder Exitlinks) ein Linkname oder eine URL aufgeführt sein soll. *`linkType`* ist normalerweise nicht erforderlich, da diese Variable durch den zweiten Parameter in der Funktion *`tl()`* ersetzt wird. |
| mediaLength | Gibt die Gesamtlänge des Mediums an, das abgespielt wird. |
| mediaName | Gibt den Namen des Video- oder Medienelements an. Diese Variable ist nur über die [!UICONTROL Dateneinfüge-API] und [!UICONTROL Vollständige Verarbeitung von Datenquelle] verfügbar. |
| mediaPlayer | Gibt den Player an, mit dem ein Video- oder Medienelement wiedergegeben wird. |
| mediaSession | Gibt an, welche Segmente eines Video- oder Medienelements abgespielt wurden. |
| Media.trackEvents | Gibt an, welche Ereignisse bei einem Medientreffer gesendet werden sollen. Gilt nur mit JavaScript [!UICONTROL ActionSource]. |
| Media.trackVars | Gibt an, welche Variablen bei einem Medientreffer gesendet werden sollen. Gilt nur mit JavaScript [!UICONTROL ActionSource]. |
| mobile | Steuert, in welcher Reihenfolge Cookies und Abonnenten-IDs zum Identifizieren von Besuchern eingesetzt werden. |
| s_objectID | Eine globale Variable, die im [!UICONTROL onClick]-Ereignis eines Links festgelegt wird. Durch Erstellung einer eindeutigen Objekt-ID für einen Link oder eine Link-Position auf einer Seite können Sie die ClickMap-Verfolgung verbessern oder bei Berichten zum Link-Typ oder zur Link-Position ClickMap anstelle der Link-URL verwenden. |
| pageName | Enthält den Namen der einzelnen Seiten Ihrer Website. Wenn *`pageName`* leer ist, wird die URL in [!DNL Analytics] als Seitenname angegeben. |
| pageType | Dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden). Ihr einziger möglicher Wert lautet „errorPage“. Auf einer 404-Fehlerseite sollte die Variable *`pageName`* nicht gefüllt werden. |
| pageURL | In seltenen Fällen kann es vorkommen, dass die URL der Seite nicht die ist, die in [!DNL Analytics]-Berichten aufgeführt wird. Um diesen Situationen Rechnung zu tragen, bietet [!DNL Analytics] die Variable *`pageURL`*, die die tatsächliche URL der Seite überschreibt. |
| plugins | Listet bei Netscape- und Mozilla-basierten Browsern die im Browser installierten Plug-ins auf. |
| products | Dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis). Die Variable *`products`* sollte immer in Verbindung mit einem Erfolgsereignis festgelegt werden. Die Variable *`products`* kann optional auch numerische und Währungs-Ereignisse sowie [!UICONTROL Merchandising]-eVars nachverfolgen. |
| propN | Dient zum Erstellen von benutzerdefinierten Berichten im [!DNL Analytics][!UICONTROL -Datenverkehrmodul]. [!UICONTROL Eigenschaftsvariablen] können als Zähler verwendet werden (um zu zählen, wie oft eine Seitenansicht gesendet wird), in Pfadsetzungsberichten oder in Korrelationsberichten. |
| purchaseID | Soll verhindern, dass eine Bestellung in [!DNL Analytics] mehrmals gezählt wird. Wann immer das Kaufereignis auf Ihrer Site verwendet wird, sollten Sie die Variable *`purchaseID`* verwenden. |
| referrer | Speichert verlorene Referrer-Informationen. |
| resolution | Gibt die Bildschirmauflösung des Besuchers an, der die Webseite anzeigt. |
| server | Gibt entweder die Domäne einer Webseite an (um zu erkennen, welche Domänen besucht werden) oder zeigt, von welchem Server die Seite stammt (als kurze Info für den Lastenausgleich). |
| state | Erfasst den Status, in dem sich ein Besucher auf Ihrer Site befindet. |
| trackDownloadLinks | Legen Sie *`trackDownloadLinks`* auf „true“ fest, wenn Sie Links für herunterladbare Dateien auf Ihrer Site verfolgen möchten. Wenn *`trackDownloadLinks`* „true“ ist, bestimmt *`linkDownloadFileTypes`*, welche Links herunterladbare Dateien sind. |
| trackExternalLinks | Wenn *`trackExternalLinks`* „true“ ist, bestimmen *`linkInternalFilters`* und *`linkExternalFilters`*, ob ein angeklickter Link ein Exitlink ist. |
| trackingServer | Gibt bei Erstanbieter-Cookie-Implementierungen an, in welcher Domäne die Bildanforderung und das Cookie gesetzt werden. Wird bei nicht sicheren Seiten verwendet. |
| trackingServerSecure | Gibt bei Erstanbieter-Cookie-Implementierungen an, in welcher Domäne die Bildanforderung und das Cookie gesetzt werden. Wird bei sicheren Seiten verwendet. |
| trackInlineStats | Bestimmt, ob Daten zur Besucherklickzuordnung gesammelt werden. |
| transactionID | Verknüpft Offlinedaten mit einer Onlinetransaktion (z. B. einem Lead oder online generierten Einkauf). Jede eindeutige an Adobe gesendete *`transactionID`* wird bei der Vorbereitung eines [!UICONTROL Data Sources]-Uploads von Offlineinformationen zu dieser Transaktion aufgezeichnet. Mehr dazu erfahren Sie im [Data Sources-Handbuch](https://marketing.adobe.com/resources/help/en_US/sc/datasources/). |
| s_usePlugins | Wenn die Funktion *`s_doPlugins`* verfügbar ist und brauchbaren Code enthält, muss [!UICONTROL s_usePlugins] auf „True“ gesetzt werden. Wenn [!UICONTROL usePlugins] auf „true“ gesetzt ist, wird die Funktion *`s_doPlugins`* vor jeder Bildanforderung aufgerufen. |
| visitorID | Besucher können anhand des Tags *`visitorID`* oder mittels IP-Adresse/Benutzeragent identifiziert werden. *`visitorID`* kann bis zu 100 alphanumerische Zeichen lang sein und darf keine Bindestriche enthalten. |
| visitorNamespace | Wenn *`visitorNamespace`* in Ihrer JavaScript-Datei verwendet wird, dürfen Sie sie weder löschen noch ändern. Anhand dieser Variablen wird die Domäne identifiziert, bei der Cookies gesetzt werden. Wenn *`visitorNamespace`* sich ändert, können alle in gemeldeten Besucher zu neuen Besuchern werden. [!DNL Analytics] Ändern Sie diese Variable daher nie ohne vorherige Genehmigung von einem Adobe-Berater! |
| zip | Erfasst die Postleitzahl von Besuchern Ihrer Site. |

