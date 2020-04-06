---
description: Eine Webeigenschaft kann aus einer beliebigen Gruppierung von einer oder mehreren Domänen und Subdomänen mit einer Regelbibliothek bestehen, die in eingebettetem Code enthalten sind.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;web property;property
title: Webeigenschaft erstellen
topic: Developer and implementation
uuid: f19d5504-eb44-4d93-a387-7470ab4b3a3a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Webeigenschaft erstellen

Eine Webeigenschaft kann aus einer beliebigen Gruppierung von einer oder mehreren Domänen und Subdomänen mit einer Regelbibliothek bestehen, die in eingebettetem Code enthalten sind.

>[!NOTE] Nur Benutzer mit ausreichenden Admin-Rechten können eine Eigenschaft erstellen. Weitere Informationen zu Rollen finden Sie unter [Erstellen und Verwalten von Gruppen in DTM](https://marketing.adobe.com/resources/help/de_DE/dtm/groups.html) in der Produktdokumentation zu Dynamic Tag Management.

Sie können diese Assets mit DTM verwalten und verfolgen. Angenommen, Sie haben mehrere Websites, die auf einer Vorlage basieren, und Sie möchten dieselben Assets auf allen diesen Websites verfolgen. Sie können eine Webeigenschaft auf mehrere Domänen anwenden.

Allgemeine Informationen zu Webeigenschaften und Best Practices finden Sie unter [Web-Eigenschaften](https://marketing.adobe.com/resources/help/de_DE/dtm/web_property.html) in der Produktdokumentation zu Dynamic Tag Management.

1. Navigate to your company page, then click **[!UICONTROL Add Property]**.

   ![](assets/dtm-create-web-property.png)

1. Füllen Sie die Felder aus:

   <table id="table_376D72251C4D4C4CA878D10C18D2532C"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Element </th> 
    <th colname="col2" class="entry"> Beschreibung </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Name</span> </td> 
    <td colname="col2"> <p>Der Name Ihrer Eigenschaft. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> URL</span> </td> 
    <td colname="col2"> <p>Die Basis-URL der Eigenschaft. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol">Diese Website umfasst mehrere Domänen. </span> </td> 
    <td colname="col2"> <p>Sie können Domänen hinzufügen und entfernen, wenn die Daten des Besuchers zwischen Domänen beibehalten werden sollen. Wenn diese Option aktiviert ist, bleiben die Daten für den Besuch über Subdomänen hinweg erhalten. </p> <p>Mit dieser Einstellung können Sie angeben, wie Sie Traffic-Bewegungen zwischen Ihren verbundenen Subdomänen oder Domänen verfolgen möchten. Links zu Subdomänen werden als ausgehende Links betrachtet. Besuche von Subdomänen werden separat verfolgt. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. (Optional) Konfigurieren [!UICONTROL Advanced Settings].

   <table id="table_6E687FBE6ACC4301BCCD837F4DCBB9C9"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Element </th> 
    <th colname="col2" class="entry"> Beschreibung </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Genehmigungen für mehrere Regeln zulassen</span> </td> 
    <td colname="col2"> <p>Es können gleichzeitig mehrere Regeln für diese Eigenschaft genehmigt werden. Die Standardgenehmigung erlaubt nur die Genehmigung einer einzelnen Regel. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Selektive Veröffentlichung aktivieren</span> </td> 
    <td colname="col2"> <p>Gibt an, ob Benutzer auswählen können, welche genehmigten Regeln veröffentlicht werden. Dies ist die Standardoption. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Tracking-Cookie-Name</span> </td> 
    <td colname="col2"> <p>Überschreibt den Standard-Tracking-Cookie-Namen. Sie können den Namen anpassen, den das dynamische Tag-Management verwendet, um Ihren Ausschluss-Status beim Empfang anderer Cookies zu verfolgen. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Tag-Timeout</span> </td> 
    <td colname="col2"> <p>Gibt an, wie lange vom dynamischen Tag-Management gewartet wird, bis ein Tag ausgelöst wird, bevor die Tag-Anforderung beendet und abgebrochen wird. </p> <p> Aufgrund der Funktionsweise des dynamischen Tag-Managements sollten Sie sich keine Gedanken darüber machen, dass dies eine hohe Zahl ist. DTM verfügt über effektive Methoden, um sicherzustellen, dass langsame Tags die Benutzererfahrung nicht beeinträchtigen. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Verankerungsverzögerung</span> </td> 
    <td colname="col2"> <p>Gibt an, wie lange vom dynamischen Tag-Management gewartet wird, dass Tags bei angeklickten Links ausgelöst werden, bevor zur nächsten Seite gewechselt wird. Der Standardwert beträgt 100 Millisekunden. </p> <p>Größere Verzögerungen erhöhen die Genauigkeit der Verfolgung. Adobe empfiehlt eine Verzögerung von 500 Millisekunden oder weniger; eine solche wird vom Benutzer nicht wahrgenommen. </p> <p>Das dynamische Tag-Management wartet bis zur angegebenen Zeit, aber wenn der Beacon früher ausgelöst wird, wird die Verzögerung verkürzt. (Das bedeutet, dass der Benutzer nicht immer die volle Verzögerungsdauer abwarten muss.) </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Klicken Sie auf **[!UICONTROL Create Property]**.
