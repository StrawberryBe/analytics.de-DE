---
description: Die serverseitige Weiterleitung wurde für Kunden entwickelt, die Daten aus Analytics in Echtzeit an andere Experience Cloud-Lösungen weitergeben möchten. Bei Aktivierung ermöglicht die serverseitige Weiterleitung auch, dass Analytics Daten an andere Experience Cloud-Lösungen weiterleitet und dass diese Lösungen Daten während des Datenerfassungsprozesses an Analytics senden können.
solution: Audience Manager
title: Übersicht über die serverseitige Weiterleitung
uuid: 22ddbde5-6805-4eba-8f82-62772644dcaa
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht über die serverseitige Weiterleitung

Die serverseitige Weiterleitung wurde für Kunden entwickelt, die Daten aus Analytics in Echtzeit an andere Experience Cloud-Lösungen weitergeben möchten. Bei Aktivierung ermöglicht die serverseitige Weiterleitung auch, dass Analytics Daten an andere Experience Cloud-Lösungen weiterleitet und dass diese Lösungen Daten während des Datenerfassungsprozesses an Analytics senden können.

Die serverseitige Weiterleitung verbessert sich bei der Datenerfassung, da sie:

* Reduziert Aufrufe von der Seite. Mit der serverseitigen Weiterleitung müssen Kunden von [!DNL Audience Manager] für die Datenerfassung nicht mehr DIL verwenden, weil die Weiterleitung über Analytics erfolgt. Das Entfernen von DIL bedeutet, einen `"/event"`-Aufruf zu entfernen. Weniger Aufrufe tragen dazu bei, die Seitenladezeit zu verbessern, was eine bessere Kundenerfahrung auf Ihrer Site ermöglicht.
* Ermöglicht Ihnen die Nutzung der Datenfreigabe in Experience Cloud-Lösungen.
* Entspricht unseren Best Practices für die Implementierung und Bereitstellung von Audience Manager-Code.

>[!TIP]
>
>Audience Manager-Bestandskunden, die Analytics verwenden, sollten auf die serverseitige Weiterleitung migrieren. Neukunden von Adobe Analytics und Audience Manager sollten die serverseitige Weiterleitung (anstelle von DIL) als Standardmethode zur Datenerfassung und -übertragung implementieren.

>[!IMPORTANT]
>Gemäß den Anforderungen der so genannten EU-Cookie-Richtlinie haben Datenverantwortliche (Analytics-Kunden) nun die Möglichkeit, Daten vor der Einwilligung auf Adobe Analytics zu beschränken und zu verhindern, dass sie serverseitig an Adobe Audience Manager (AAM) weitergeleitet werden. Mit einer neuen Implementierungskontextvariablen können Sie Treffer kennzeichnen, bei denen die Zustimmung nicht eingegangen ist. Die Variable verhindert, dass diese Treffer nach ihrer Einstellung an AAM gesendet werden, bis die Zustimmung eingegangen ist. For more information, see [GDPR_ePrivacy compliance and server-side forwarding](/help/admin/admin/c-server-side-forwarding/ssf-gdpr.md).

Wenn Sie nachvollziehen möchten, wo sich Ihre Organisation bezüglich der Implementierung der serverseitigen Weiterleitung befindet, führen Sie die folgenden Validierungsschritte durch:

## ![Grafik step1_icon.png](assets/step1_icon.png) ECID-Dienstimplementierung überprüfen

Überprüfen Sie, ob der Experience Cloud ID-(ECID-)Dienst implementiert wurde, indem Sie die [Analytics-Tracking-Anfrage](https://marketing.adobe.com/resources/help/de_DE/mcvid/mcvid-test-verify.html) prüfen.

Stellen Sie auf der Registerkarte „Anfrage“ sicher, dass ein ECID-Wert festgelegt wurde. Dies gibt darüber Auskunft, dass der Identity Service korrekt implementiert wurde. Dies ist eine Voraussetzung für die serverseitige Weiterleitung.

* Wenn ein ECID-Wert angezeigt wird, fahren Sie mit Schritt 2 fort.
* Wenn kein ECID-Wert angezeigt wird, [implementieren Sie den Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/implementation/implementation-guides.html), bevor Sie den Vorgang bei Schritt 2 fortsetzen.

## ![Grafik step2_icon.png](assets/step2_icon.png) Implementierungsversion der serverseitigen Weiterleitung überprüfen

Überprüfen Sie, ob bereits eine Version der serverseitigen Weiterleitung implementiert ist, indem Sie die [Analytics-Tracking-Anforderung prüfen](/help/admin/admin/c-server-side-forwarding/ssf-verify.md).

Überprüfen Sie auf der Registerkarte „Antwort“, ob die Antwort Audience Manager-Daten umfasst. Bei Anzeige des Folgenden gilt das Nachstehende:

* Eine **JSON-Antwort von Audience Manager mit Elementen wie „postbacks“ oder „dcs_region“**: Es ist bereits eine Form der serverseitigen Weiterleitung aktiviert. Fahren Sie mit Schritt 3 fort.
* **&quot;status&quot;:&quot;SUCCESS&quot;**: Das Zielgruppen-Management-Modul ist zwar implementiert, die serverseitige Weiterleitung ist jedoch nicht ordnungsgemäß konfiguriert. Fahren Sie mit Schritt 3 fort.
* Ein **2 x 2-Bild**: Sie haben keine serverseitige Weiterleitung oder das Audience Management Module implementiert. So korrigieren Sie:

   * **AAM-Kunden mit DIL**: die folgenden zwei Elemente in enger Verbindung zu koordinieren:

      1. Entfernen Sie den DIL-Code und installieren Sie den Seitencode des [Audience Management Module](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) .
      1. Aktivieren Sie die serverseitige Weiterleitung in der Admin-Benutzeroberfläche von Analytics, wie in Schritt 3 beschrieben. Wenn Sie diese Einstellung vor dem Entfernen des DIL-Codes aktivieren, werden Daten Duplikat und zusätzliche Server-Aufrufe an Audience Manager erstellt.
   * **Neue AAM-Kunden** - Installieren Sie den Seiten-Code für das [Audience Management Module](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) und fahren Sie mit Schritt 3 fort. Daten werden erst dann an Audience Manager gesendet, wenn die serverseitige Weiterleitung in Schritt 3 aktiviert ist.


## ![Grafik step3_icon.png](assets/step3_icon.png) Implementierung der serverseitigen Weiterleitung der Report Suite überprüfen

Überprüfen Sie, ob die serverseitige Weiterleitung auf Report Suite-Ebene implementiert ist und nicht auf den alten Tracking-Server-Ansatz.

Eine serverseitige Weiterleitung auf Report Suite-Ebene wird gegenüber dem alten Tracking-Server-Ansatz empfohlen, da Sie auf einer genaueren Ebene steuern können, welche Daten von Analytics freigegeben werden. Es ist auch eine Voraussetzung für diese Audience der Analytics-Integration.

Gehen Sie zu **Analytics** > **Admin** > **Report Suites** > (**Report Suites** auswählen) > **Einstellungen bearbeiten** > **Allgemein** > **Serverseitige Weiterleitung**. Wenn das Kontrollkästchen folgenden Zustand aufweist, gilt das Nachfolgende:

* **Inaktiv** (Sie können keine Auswahl treffen, oder das Menü ist nicht vorhanden): Die ausgewählten Report Suites sind der IMS-Org. nicht zugeordnet. Stellen Sie mithilfe der [Report Suite-Zuordnungs-UI](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html) sicher, dass die jeweiligen Report Suites der entsprechenden Experience Cloud-Organisation zugeordnet sind.
* **Deaktiviert**: Die neue serverseitige Weiterleitung ist nicht aktiviert. Lesen Sie den Inhalt auf der Seite und fahren Sie mit der Aktivierung der Funktion fort.
* **Aktiviert**: Sie sind für die neue serverseitige Weiterleitung vorgesehen. Sie können diese Audience auch in Analytics integrieren.

>[!NOTE] In anderen Experience Cloud-Lösungen wie [Audience Manager](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/aam-home.translate.html) oder [Audiences](https://marketing.adobe.com/resources/help/de_DE/mcloud/audience_library.html) werden erst Daten angezeigt, nachdem alle drei Schritte abgeschlossen wurden. Nach der Aktivierung dauert es mehrere Stunden, bis diese Einstellungen wirksam werden.

