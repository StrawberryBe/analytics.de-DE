---
title: Migration von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung
description: Aktualisieren Sie Ihre Analytics-Implementierung auf Adobe Experience Platform-Datenerfassungs-Tags, um die Web SDK-Erweiterung zu verwenden.
source-git-commit: d4c9bddf18311e13d025ed9d62c0636a33eb7b85
workflow-type: tm+mt
source-wordcount: '1704'
ht-degree: 2%

---

# Migration von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung

Dieser Implementierungspfad umfasst einen methodischen Migrationsprozess, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md): Ein reibungsloser und methodischer Ansatz für die Migration zum Web SDK, mit der Ausnahme, dass keine Tags verwendet werden. Stattdessen müssen Sie die Adobe Analytics-Datenerfassungsbibliothek (`AppMeasurement.js`) und ersetzen Sie sie durch die JavaScript-Bibliothek des Web SDK (`alloy.js`).
* [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md): Eine neue Web SDK-Installation, bei der Sie die Implementierung mithilfe von Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.
* [JavaScript-Bibliothek des Web SDK](web-sdk-javascript-library.md): Eine neue Web SDK-Installation mit der Web SDK JavaScript-Bibliothek (`alloy.js`). Verwalten Sie die Implementierung selbst, anstatt die Tags-Benutzeroberfläche zu verwenden. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.

## Vorteile und Nachteile dieses Implementierungspfads

Die Verwendung dieses Migrationsansatzes hat sowohl Vor- als auch Nachteile. Legen Sie bei jeder Option sorgfältig ab, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Keine Codeänderungen auf Ihrer Site**: Da Ihre Implementierung bereits Tags installiert hat, können alle Migrationsaktualisierungen in der Tag-Oberfläche vorgenommen werden.</li><li>**Verwendet Ihre vorhandene Implementierung**: Für diesen Ansatz ist keine neue Implementierung erforderlich. Sie benötigen zwar neue Regelaktionen, können aber Ihre vorhandenen Datenelemente und Regelbedingungen mit minimalen Änderungen wiederverwenden.</li><li>**Erfordert kein Schema**: Für diese Phase der Migration zum Web SDK benötigen Sie kein XDM-Schema. Stattdessen können Sie die `data` -Objekt, das Daten direkt an Adobe Analytics sendet. Nachdem die Migration zum Web SDK abgeschlossen ist, können Sie ein Schema für Ihre Organisation erstellen und die Datastraam-Zuordnung verwenden, um die entsprechenden XDM-Felder auszufüllen. Wenn in dieser Phase des Migrationsprozesses ein Schema erforderlich ist, muss Ihr Unternehmen ein Adobe Analytics-XDM-Schema verwenden. Die Verwendung dieses Schemas erschwert es Ihrem Unternehmen, in Zukunft Ihr eigenes Schema zu verwenden.</li></ul> | <ul><li>**Technische Schulden der Implementierung**: Da dieser Ansatz eine modifizierte Form Ihrer vorhandenen Implementierung verwendet, kann es schwieriger sein, die Implementierungslogik zu verfolgen und bei Bedarf Änderungen vorzunehmen. Das Debuggen von benutzerspezifischem Code kann besonders schwierig sein.</li><li>**Erfordert Zuordnung zum Senden von Daten an Platform**: Wenn Ihr Unternehmen für die Verwendung von Customer Journey Analytics bereit ist, müssen Sie Daten an einen Datensatz in Adobe Experience Platform senden. Diese Aktion erfordert, dass jedes Feld in `data` -Objekt ein Eintrag im Tool zur Datenasterzuordnung sein, der es einem XDM-Schemafeld zuordnet. Die Zuordnung muss nur einmal für diesen Workflow durchgeführt werden. Es müssen keine Implementierungsänderungen vorgenommen werden. Es handelt sich jedoch um einen zusätzlichen Schritt, der beim Senden von Daten in ein XDM-Objekt nicht erforderlich ist.</li></ul> |

Adobe empfiehlt, diesem Implementierungspfad in den folgenden Szenarien zu folgen:

* Sie verfügen über eine vorhandene Implementierung mit der Adobe Analytics-Tag-Erweiterung. Wenn Sie eine Implementierung mit AppMeasurement haben, folgen Sie den Anweisungen [Migration von AppMeasurement zum Web SDK](appmeasurement-to-web-sdk.md) anstatt.
* Sie beabsichtigen in Zukunft Customer Journey Analytics zu verwenden, möchten Ihre Analytics-Implementierung jedoch nicht von Grund auf durch eine Web SDK-Implementierung ersetzen. Die Ersetzung Ihrer Implementierung durch das Web SDK erfordert den größten Aufwand, bietet aber auch die praktikabelste langfristige Implementierungsarchitektur. Wenn Ihr Unternehmen bereit ist, die Implementierung eines sauberen Web SDK durchzuführen, lesen Sie [Daten über das Adobe Experience Platform Web SDK erfassen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) im Customer Journey Analytics-Benutzerhandbuch.

## Schritte für die Migration zum Web SDK

Die folgenden Schritte enthalten konkrete Ziele, auf die wir hinarbeiten müssen. Klicken Sie auf jeden Schritt, um detaillierte Anweisungen dazu zu erhalten.

+++**1. Erstellen und Konfigurieren eines Datenspeichers**

Erstellen Sie einen Datenspeicher in der Adobe Experience Platform-Datenerfassung. Wenn Sie Daten an diesen Datastream senden, leitet er Daten an Adobe Analytics weiter. Künftig leitet derselbe Datenspeicher Daten an Customer Journey Analytics weiter.

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com) und melden Sie sich mit Ihren Anmeldedaten an.
1. Verwenden Sie die Startseite oder die Produktselektor oben rechts, um zu **[!UICONTROL Datenerfassung]**.
1. Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL Datenspeicher]**.
1. Wählen Sie **[!UICONTROL Neuer Datenstrom]** aus.
1. Geben Sie den gewünschten Namen ein und wählen Sie **[!UICONTROL Speichern]**.
1. Nachdem der Datastream erstellt wurde, wählen Sie **[!UICONTROL Dienst hinzufügen]**.
1. Wählen Sie im Dropdown-Menü Dienst die Option **[!UICONTROL Adobe Analytics]**.
1. Geben Sie dieselbe Report Suite-ID ein wie die Site, an die Sie derzeit Analysedaten senden. Klicken Sie auf **[!UICONTROL Speichern]**.

![Hinzufügen des Adobe Analytics-Dienstes](assets/datastream-rsid.png) {style="border:1px solid gray"}

Ihr Datastream kann jetzt Daten empfangen und an Adobe Analytics weitergeben.

+++

+++**2. Hinzufügen der Web SDK-Erweiterung zu Ihrer Tag-Eigenschaft**

In diesem Abschnitt wird Ihr -Tag für den Großteil der Migrationsschritte vorbereitet, die im nächsten Schritt unternommen werden.

1. Klicken Sie oben links in der Adobe Experience Platform-Benutzeroberfläche auf das Hamburger-Symbol und wählen Sie **[!UICONTROL Tags]**.
1. Wählen Sie die gewünschte Tag-Eigenschaft aus.
1. Wählen Sie im linken Navigationsbereich der Tag-Eigenschaft die Option **[!UICONTROL Erweiterungen]**.
1. Auswählen **[!UICONTROL Katalog]** oben, um eine Liste aller verfügbaren Erweiterungen anzuzeigen.
1. Suchen Sie nach und wählen Sie **[!UICONTROL Adobe Experience Platform Web SDK]** Erweiterung und klicken Sie auf **[!UICONTROL Installieren]** rechts.

   ![Katalog](assets/catalog.png) {style="border:1px solid gray"}

1. Die Erweiterungskonfigurationseinstellungen werden angezeigt. Suchen Sie den Abschnitt &quot;Datenspeicher&quot;und wählen Sie den Datenspeicher aus, den Sie im vorherigen Schritt erstellt haben.

   ![Datenspeicherauswahl](assets/datastream-select.png) {style="border:1px solid gray"}

1. Wählen Sie **[!UICONTROL Speichern]** aus.

Für Ihre Tag-Eigenschaft ist jetzt das Web SDK installiert.

+++

+++**3. Datenobjektdatenelement erstellen**

Das Datenobjekt-Datenelement bietet ein intuitives Framework zum Konfigurieren einer Payload, die das Web SDK zum Senden an einen Datastream verwendet. Die meisten Regeln, die Sie im folgenden Schritt aktualisieren, interagieren mit diesem Datenelement.

1. Wählen Sie in der linken Navigation der Tags-Benutzeroberfläche die Option **[!UICONTROL Datenelemente]**.
1. Auswählen **[!UICONTROL Datenelement hinzufügen]**
1. Legen Sie für das Datenelement die folgenden Einstellungen fest:
   * [!UICONTROL Name]: Alles, was Sie möchten, z. B. &quot;Datenschicht&quot;oder &quot;Datenobjekt&quot;
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Variable]: [!UICONTROL Variable]
   * Kontrollkästchen können unverändert bleiben
1. Wählen Sie rechts die folgenden Einstellungen aus:
   * Optionsfeld &quot;Eigenschaft&quot;: [!UICONTROL Daten]
   * Lösung: [!UICONTROL Adobe Analytics]
1. Wählen Sie **[!UICONTROL Speichern]** aus.

![Datenelement erstellen](assets/create-data-element.png) {style="border:1px solid gray"}

Ihre Tag-Eigenschaft verfügt jetzt über alles, was zum Aktualisieren der einzelnen Regeln erforderlich ist.

+++

+++**4. Aktualisieren von Regeln zur Verwendung der Web SDK-Erweiterung anstelle der Analytics-Erweiterung**

Dieser Schritt enthält den Großteil des für die Migration zum Web SDK erforderlichen Aufwands und erfordert Kenntnisse darüber, wie Ihre Implementierung funktioniert. Im Folgenden finden Sie ein Beispiel für die Bearbeitung einer typischen Tag-Regel. Aktualisieren Sie alle Tag-Regeln in Ihrer Implementierung, um alle Verweise auf die Adobe Analytics-Erweiterung durch die Web SDK-Erweiterung zu ersetzen.

1. Wählen Sie in der linken Navigation der Tags-Benutzeroberfläche die Option **[!UICONTROL Regeln]**.
1. Wählen Sie eine zu bearbeitende Regel aus.
1. Aktion auswählen **[!UICONTROL Adobe Analytics - Variablen festlegen]**
1. Beachten Sie alle in dieser Regel festgelegten Analytics-Variablen. Beachten Sie sowohl die in den Dropdown-Menüs festgelegten Variablen als auch die in benutzerdefiniertem Code festgelegten Variablen.
1. Ändern Sie die [!UICONTROL Aktionskonfiguration] zu den folgenden Einstellungen hinzufügen:
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Aktionstyp]: Variable aktualisieren
1. Stellen Sie sicher, dass Ihr Datenobjekt in der Dropdown-Liste auf der rechten Seite ausgewählt ist.
1. Legen Sie die Analytics-Variablen auf die gleichen Werte fest wie in der Analytics-Erweiterung konfiguriert.
   * Variablen, die in der Tag-Oberfläche festgelegt werden, können direkt in dieselben Werte übersetzt werden.
   * Zeichenfolgenvariablen, die in benutzerdefiniertem Code festgelegt werden, erfordern minimale Anpassungen. Statt die `s` Objekt, verwenden `data.__adobe.analytics` anstatt. Beispiel: `s.eVar1` würde übersetzen in `data.__adobe.analytics.eVar1`.
   * Analytics-Konfigurationsvariablen und Methodenaufrufe in benutzerdefiniertem Code können eine geänderte Implementierungslogik erfordern. Siehe die jeweiligen [Variable](/help/implement/vars/overview.md) , um zu bestimmen, wie die Entsprechung mit dem Web SDK erreicht wird.
1. Nachdem alle Regellogik mit der Web SDK-Erweiterung repliziert wurde, wählen Sie **[!UICONTROL Änderungen beibehalten]**.
1. Wiederholen Sie diese Schritte für jede Aktionskonfiguration, in der die Adobe Analytics-Erweiterung zum Festlegen von Werten verwendet wird. Dieser Schritt umfasst sowohl Variablen, die mithilfe der Tag-Oberfläche festgelegt werden, als auch Variablen, die mithilfe von benutzerdefiniertem Code festgelegt werden. Benutzerdefinierte Codeblöcke können nicht auf die `s` -Objekt an einer beliebigen Stelle ein.

Die obigen Schritte gelten nur für Regeln, die Werte festlegen. Die folgenden Schritte ersetzen alle Aktionen, die die [!UICONTROL Aktionskonfiguration] [!UICONTROL Beacon senden].

1. Wählen Sie eine Regel aus, die ein Beacon sendet.
1. Aktion auswählen **[!UICONTROL Adobe Analytics - Signal senden]**.
1. Notieren Sie den aktuellen Wert der [!UICONTROL Tracking] Optionsfeld rechts ([`s.t()`](../../vars/functions/t-method.md) oder [`s.tl()`](../../vars/functions/tl-method.md)).
1. Ändern Sie die [!UICONTROL Aktionskonfiguration] zu den folgenden Einstellungen hinzufügen:
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Aktionstyp]: [!UICONTROL Ereignis senden]
1. Ändern Sie rechts die Aktionseinstellungen in Folgendes:
   * [!UICONTROL Typ]: Für `s.t()`, verwenden **[!UICONTROL Seitenansichten der Web-SeiteDetails]**. Für `s.tl()`, verwenden **[!UICONTROL Link-Klicks für Web-Interaktionen]**. Wenn Sie [`s.tl()`](../../vars/functions/tl-method.md)müssen Sie außerdem die folgenden Felder in Ihr Datenobjekt aufnehmen. Diese Felder sind unter [!UICONTROL Zusätzliche Eigenschaften] beim Ausführen der [!UICONTROL Variable aktualisieren] Aktionskonfiguration:
      * [Link-Name](../../vars/functions/tl-method.md)
      * [Link-Typ ](../../vars/functions/tl-method.md)
      * [Link-URL](../../vars/config-vars/linkurl.md)
1. Wählen Sie **[!UICONTROL Änderungen beibehalten]** aus.
1. Wiederholen Sie diese Schritte für jede Aktionskonfiguration, bei der Adobe Analytics zum Senden eines Beacons verwendet wird.

+++

+++**5. Aktualisierte Regeln veröffentlichen**

Das Veröffentlichen aktualisierter Regeln folgt demselben Workflow wie jede andere Änderung an der Tag-Konfiguration.

1. Wählen Sie in der linken Navigation der Tags-Benutzeroberfläche die Option **[!UICONTROL Veröffentlichungsfluss]**.
1. Auswählen **[!UICONTROL Bibliothek hinzufügen]**.
1. Geben Sie diesem Tag einen Namen, z. B. &quot;Aktualisierung auf Web SDK&quot;.
1. Auswählen **[!UICONTROL Alle geänderten Ressourcen hinzufügen]**.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Der Veröffentlichungs-Workflow zeigt einen orangefarbenen Punkt an, der angibt, dass er erstellt wird. Sobald der Punkt grün wird, sind Ihre Änderungen in Ihrer Entwicklungsumgebung verfügbar.
1. Testen Sie Ihre Änderungen in Ihrer Entwicklungsumgebung, um sicherzustellen, dass alle Regeln ordnungsgemäß ausgelöst werden und dass das Datenobjekt mit den erwarteten Werten gefüllt wird.
1. Wenn die Bibliothek fertig ist, senden Sie sie zur Genehmigung, erstellen Sie sie zum Staging, genehmigen Sie sie schließlich und veröffentlichen Sie sie in der Produktion.

![Veröffentlichungsfluss](assets/publishing-flow.png) {style="border:1px solid gray"}

+++

+++**6. Analytics-Erweiterung deaktivieren**

Sobald Ihre Tag-Implementierung vollständig im Web SDK vorhanden ist, können Sie die Adobe Analytics-Erweiterung deaktivieren.

1. Wählen Sie in der linken Navigation der Tags-Benutzeroberfläche die Option **[!UICONTROL Erweiterungen]**.
1. Suchen und wählen Sie die [!UICONTROL Adobe Analytics] -Erweiterung. Wählen Sie rechts **[!UICONTROL Deaktivieren]**.
1. Führen Sie denselben obigen Veröffentlichungsarbeitsablauf aus, um die Entfernung des [!UICONTROL Adobe Analytics] -Erweiterung.
1. Nachdem die Erweiterung in der Produktion deaktiviert wurde, können Sie sie vollständig deinstallieren. Wählen Sie die Erweiterung aus, wählen Sie das Menü mit den drei Punkten auf der rechten Seite aus und klicken Sie auf **[!UICONTROL Deinstallieren]**.
1. Führen Sie denselben obigen Veröffentlichungsarbeitsablauf aus, um diese Änderungen in der Produktion zu veröffentlichen.

+++

Zu diesem Zeitpunkt befindet sich Ihre Analytics-Implementierung vollständig im Web SDK und ist angemessen darauf vorbereitet, in Zukunft zu Customer Journey Analytics zu wechseln.
