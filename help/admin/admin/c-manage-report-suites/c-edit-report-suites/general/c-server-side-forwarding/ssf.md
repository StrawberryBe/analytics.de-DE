---
description: Die serverseitige Weiterleitung ist für Kunden bestimmt, die Daten aus Analytics für andere Experience Cloud-Lösungen in Echtzeit freigeben möchten. Bei entsprechender Aktivierung ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.
solution: Analytics
title: Übersicht über die Server-seitige Weiterleitung
feature: Server-Side Forwarding
exl-id: e3cd72d2-9588-4770-a7c2-64b13a1e9519
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 95%

---

# Übersicht über die Server-seitige Weiterleitung

Die serverseitige Weiterleitung ist für Kunden bestimmt, die Daten aus Analytics für andere Experience Cloud-Lösungen in Echtzeit freigeben möchten. Bei entsprechender Aktivierung ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.

Die serverseitige Weiterleitung führt aus folgenden Gründen zu Optimierungen bei der Datenerfassung:

* Reduzierung der Aufrufe auf der Seite. Mit der serverseitigen Weiterleitung müssen Kunden von [!DNL Audience Manager] für die Datenerfassung nicht mehr DIL verwenden, weil die Weiterleitung über Analytics erfolgt. Das Entfernen von DIL bedeutet, einen `"/event"`-Aufruf zu entfernen. Weniger Aufrufe bedeuten verbesserte Ladezeiten der Seite, wodurch sich die Benutzererfahrung auf Ihrer Site verbessert.
* Nutzung der Datenfreigabe für Experience Cloud-Lösungen.
* Konformität mit unseren Best Practices für die Implementierung und Bereitstellung von Audience Manager-Code.

>[!TIP]
>
>Audience Manager-Bestandskunden, die Analytics verwenden, sollten auf die serverseitige Weiterleitung migrieren. Neukunden von Adobe Analytics und Audience Manager sollten die serverseitige Weiterleitung (anstelle von DIL) als Standardmethode zur Datenerfassung und -übertragung implementieren.

>[!IMPORTANT]
>Gemäß den Anforderungen der so genannten EU-Cookie-Richtlinie haben Datenverantwortliche (Analytics-Kunden) nun die Möglichkeit, Daten vor der Einwilligung auf Adobe Analytics zu beschränken und zu verhindern, dass sie serverseitig an Adobe Audience Manager (AAM) weitergeleitet werden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable, sofern festgelegt, verhindert, dass die Treffer vor einer Zustimmung an AAM weitergeleitet werden. Weitere Informationen finden Sie unter [DSGVO_ePrivacy – Einhaltung und serverseitige Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md).

Wenn Sie nachvollziehen möchten, wo sich Ihre Organisation bezüglich der Implementierung der serverseitigen Weiterleitung befindet, führen Sie die folgenden Validierungsschritte durch:

## ![Grafik step1_icon.png](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/assets/step1_icon.png) ECID-Dienstimplementierung überprüfen

Überprüfen Sie, ob der Experience Cloud ID-(ECID-)Service implementiert wurde, indem Sie die [Analytics-Tracking-Anfrage](https://experienceleague.adobe.com/docs/id-service/using/implementation/test-verify.html?lang=de) prüfen.

Stellen Sie auf der Registerkarte „Anfrage“ sicher, dass ein ECID-Wert festgelegt wurde. Dies gibt darüber Auskunft, dass der Identity Service korrekt implementiert wurde. Dies ist eine Voraussetzung für die serverseitige Weiterleitung.

* Wenn ein ECID-Wert angezeigt wird, fahren Sie mit Schritt 2 fort.
* Wenn kein ECID-Wert angezeigt wird, [implementieren Sie den Identity Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-guides.html?lang=de), bevor Sie den Vorgang bei Schritt 2 fortsetzen.

## ![Grafik step2_icon.png](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/assets/step2_icon.png) Implementierungsversion der serverseitigen Weiterleitung überprüfen

Überprüfen Sie, ob bereits eine Version der serverseitigen Weiterleitung implementiert ist, indem Sie die [Analytics-Tracking-Anforderung prüfen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md).

Überprüfen Sie auf der Registerkarte „Antwort“, ob die Antwort Audience Manager-Daten umfasst. Bei Anzeige des Folgenden gilt das Nachstehende:

* Eine **JSON-Antwort von Audience Manager mit Elementen wie „postbacks“ oder „dcs_region“**: Es ist bereits eine Form der serverseitigen Weiterleitung aktiviert. Fahren Sie mit Schritt 3 fort.
* **&quot;status&quot;:&quot;SUCCESS&quot;**: Das Zielgruppen-Management-Modul ist zwar implementiert, die serverseitige Weiterleitung ist jedoch nicht ordnungsgemäß konfiguriert. Fahren Sie mit Schritt 3 fort.
* Ein **2-x-2-Bild**: Die serverseitige Weiterleitung oder das Zielgruppen-Management-Modul wurde nicht implementiert. Korrektur:

   * **AAM-Kunden mit DIL**: Koordinieren Sie die folgenden beiden Elemente in enger Verbindung:

      1. Entfernen Sie den DIL-Code, und installieren Sie den Seiten-Code für das [Zielgruppen-Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=de).
      1. Aktivieren Sie die serverseitige Weiterleitung auf der Analytics Admin-Benutzeroberfläche, wie unter Schritt 3 beschrieben. Durch die Aktivierung dieser Einstellung vor dem Entfernen des DIL-Codes werden die Daten dupliziert, und es werden zusätzliche abgerechnete Serveraufrufe für Audience Manager erstellt.
   * **Neue AAM-Kunden**: Installieren Sie den Seiten-Code für das [Zielgruppen-Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html), und fahren Sie mit Schritt 3 fort. Es werden erst Daten an Audience Manager gesendet, nachdem die serverseitige Weiterleitung in Schritt 3 aktiviert wurde.


## ![Grafik step3_icon.png](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/assets/step3_icon.png) Implementierung der serverseitigen Weiterleitung der Report Suite überprüfen

Überprüfen Sie, ob die serverseitige Weiterleitung auf Ebene der Report Suite implementiert wurde (anstelle des alten Verfolgungsserveransatzes).

Die serverseitige Weiterleitung auf Ebene der Report Suite wird dem alten Ansatz mit Verfolgungsserver vorgezogen, weil Sie detaillierter kontrollieren können, welche Daten aus Analytics freigegeben werden. Dies ist zudem eine Voraussetzung für diese Audience Analytics-Integration.

Gehen Sie zu **Analytics** > **Admin** > **Report Suites** > (**Report Suites** auswählen) > **Einstellungen bearbeiten** > **Allgemein** > **Serverseitige Weiterleitung**. Wenn das Kontrollkästchen folgenden Zustand aufweist, gilt das Nachfolgende:

* **Inaktiv** (Sie können keine Auswahl treffen oder das Menü existiert nicht): Sie verfügen nicht über die Zuordnung der ausgewählten Report Suites zu einer Organisations-ID. Wenden Sie sich an die Kundenunterstützung , um sicherzustellen, dass die Report Suite korrekt zugeordnet ist.
* **Deaktiviert**: Die neue serverseitige Weiterleitung ist nicht aktiviert. Lesen Sie den Inhalt der Seite, und fahren Sie dann mit der Aktivierung der Funktion fort.
* **Aktiviert**: Die neue serverseitige Weiterleitung ist bereitgestellt. Sie können auch diese Audience Analytics-Integration einrichten.

>[!NOTE]
>
>In anderen Experience Cloud-Lösungen wie [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=de) oder [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) werden erst Daten angezeigt, nachdem alle drei Schritte abgeschlossen wurden. Nach der Aktivierung dauert es mehrere Stunden, bis diese Einstellungen wirksam werden.
