---
description: Die serverseitige Weiterleitung ist für Kunden bestimmt, die Daten aus Analytics für andere Experience Cloud-Lösungen in Echtzeit freigeben möchten. Bei entsprechender Aktivierung ermöglicht die serverseitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.
solution: Audience Manager
title: Übersicht über die serverseitige Weiterleitung
uuid: 22ddbde5-6805-4eba-8f82-62772644dcaa
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Übersicht über die serverseitige Weiterleitung

Die serverseitige Weiterleitung ist für Kunden bestimmt, die Daten aus Analytics für andere Experience Cloud-Lösungen in Echtzeit freigeben möchten. Bei entsprechender Aktivierung ermöglicht die serverseitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.

Die serverseitige Weiterleitung führt aus folgenden Gründen zu Optimierungen bei der Datenerfassung:

* Reduzierung der Aufrufe auf der Seite. With server-side forwarding, [!DNL Audience Manager] customers no longer need to use DIL for data collection because it is being forwarded from Analytics. Das Entfernen von DIL bedeutet, einen `"/event"` Aufruf zu entfernen. Weniger Aufrufe bedeuten verbesserte Ladezeiten der Seite, wodurch sich die Benutzererfahrung auf Ihrer Site verbessert.
* Nutzung der Datenfreigabe für Experience Cloud-Lösungen.
* Konformität mit unseren bewährten Methoden für die Audience Manager-Codeimplementierung und -Bereitstellung.

>[!TIP]
>
>Aktuelle Audience Manager-Kunden, die Analytics verwenden, sollten zur serverseitigen Weiterleitung migrieren. Neukunden von Adobe Analytics und Audience Manager sollten die serverseitige Weiterleitung (anstelle von DIL) als Standardmethode zur Datenerfassung und -übertragung implementieren.

>[!IMPORTANT]
>Gemäß den Anforderungen der so genannten EU-Cookie-Richtlinie haben Datenverantwortliche (Analytics-Kunden) nun die Möglichkeit, die vor einer erfolgten Zustimmung zugänglichen Daten auf Adobe Analytics zu beschränken sowie die serverseitige Weiterleitung an Adobe Audience Manager (AAM) zu unterbinden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable, sofern festgelegt, verhindert, dass die Treffer vor einer Zustimmung an AAM weitergeleitet werden. Weitere Informationen finden Sie unter DSGVO_ePrivacy – Einhaltung und serverseitige Weiterleitung.

Wenn Sie nachvollziehen möchten, wo sich Ihre Organisation bezüglich der Implementierung der serverseitigen Weiterleitung befindet, führen Sie die folgenden Validierungsschritte durch:

## ![step1_icon.png image](assets/step1_icon.png) Verify MID service implementation

Überprüfen Sie, ob der Experience Cloud ID-(MID-)Dienst implementiert wurde, indem Sie die [Analytics-Verfolgungsanfrage](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-test-verify.html) prüfen.

Stellen Sie auf der Registerkarte Anfrage sicher, dass ein MID-Wert festgelegt wurde. Dies zeigt an, dass der Identitätsdienst korrekt implementiert ist, was eine Voraussetzung für die serverseitige Weiterleitung ist.

* Wenn ein MID-Wert angezeigt wird, fahren Sie mit Schritt 2 fort.
* If you do not see a MID value, [implement Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html) before proceeding to step 2.

## ![step2_icon.png image](assets/step2_icon.png) Überprüfen der Implementierungsversion für serverseitige Weiterleitung

Überprüfen Sie, ob bereits eine Version der serverseitigen Weiterleitung implementiert ist, indem Sie die Analytics-Verfolgungsanfrage [überprüfen](/help/admin/admin/c-server-side-forwarding/ssf-verify.md).

Überprüfen Sie auf der Registerkarte "Antwort", ob die Antwort Audience Manager-Daten enthält. Bei Anzeige des Folgenden gilt das Nachstehende:

* A **JSON response from Audience Manager that includes items such as "postbacks" or "dcs_region"**: you have some form of server-side forwarding already enabled. Fahren Sie mit Schritt 3 fort.
* The **"status":"SUCCESS"**: you have the Audience Management Module implemented, but do not have server side forwarding properly configured. Fahren Sie mit Schritt 3 fort.
* Ein **2-x-2-Bild**: Die serverseitige Weiterleitung oder das Zielgruppen-Management-Modul wurde nicht implementiert. Korrektur:

   * **AAM-Kunden mit DIL**: Koordinieren Sie die folgenden beiden Elemente in enger Verbindung:

      1. Entfernen Sie den DIL-Code, und installieren Sie den Seiten-Code für das [Zielgruppen-Management-Modul](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html).
      1. Aktivieren Sie die serverseitige Weiterleitung auf der Analytics Admin-Benutzeroberfläche, wie unter Schritt 3 beschrieben. Durch die Aktivierung dieser Einstellung vor dem Entfernen des DIL-Codes werden die Daten dupliziert, und es werden zusätzliche abgerechnete Serveraufrufe für Audience Manager erstellt.
   * **Neue AAM-Kunden**: Installieren Sie den Seiten-Code für das [Zielgruppen-Management-Modul](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html), und fahren Sie mit Schritt 3 fort. Es werden erst Daten an Audience Manager gesendet, nachdem die serverseitige Weiterleitung in Schritt 3 aktiviert wurde.


## ![step3_icon.png image](assets/step3_icon.png) Überprüfen der serverseitigen Weiterleitung der Report Suite

Überprüfen Sie, ob die serverseitige Weiterleitung auf Ebene der Report Suite implementiert wurde (anstelle des alten Verfolgungsserveransatzes).

Die serverseitige Weiterleitung auf Ebene der Report Suite wird dem alten Ansatz mit Verfolgungsserver vorgezogen, weil Sie detaillierter kontrollieren können, welche Daten aus Analytics freigegeben werden. Dies ist zudem eine Voraussetzung für diese Audience Analytics-Integration.

Go to **Analytics** &gt; **Admin** &gt; **Report Suites** &gt; (select **report suites**) &gt; **Edit Settings** &gt; **General** &gt; **Server Side Forwarding**. Wenn das Kontrollkästchen folgenden Zustand aufweist, gilt das Nachfolgende:

* **Inaktiv** (Sie können keine Auswahl treffen, oder das Menü ist nicht vorhanden): Die ausgewählten Report Suites sind der IMS-Org. nicht zugeordnet. Stellen Sie mithilfe der [Report Suite-Zuordnungs-UI](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html) sicher, dass die jeweiligen Report Suites der entsprechenden IMS-Org. zugeordnet sind.
* **Deaktiviert**: Die neue serverseitige Weiterleitung ist nicht aktiviert. Lesen Sie den Inhalt der Seite, und fahren Sie dann mit der Aktivierung der Funktion fort.
* **Aktiviert**: Die neue serverseitige Weiterleitung ist bereitgestellt. Sie können auch diese Audience Analytics-Integration einrichten.

<!-- Meike, check Report Suite Mapping UI link above -->

> [!NOTE] In anderen Experience Cloud-Lösungen wie [Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/c_aam_home.html) oder [Zielgruppen](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) werden erst nach Abschluss aller 3 Schritte Daten angezeigt. Nach der Aktivierung dauert es mehrere Stunden, bis diese Einstellungen wirksam werden.

