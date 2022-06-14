---
description: Häufige Probleme bei der Verwendung von Report Builder mit Power BI.
title: Fehlerbehebung für die Power BI-Integration
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: a30564e9d8969457aaa8709c3aa3c17ba6d0a2d3
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 90%

---

# Fehlerbehebung für die Power BI-Integration

Ermitteln und Lösen von allgemeinen Problemen bei der Verwendung von Report Builder mit Power BI.

## Fehlschlagen der Veröffentlichung in Power BI

Geplante Arbeitsmappen, die in Power BI veröffentlicht werden sollen, hängen davon ab, dass Power BI-Dienste ausgeführt werden. Zwei Hauptgründe für das Fehlschlagen einer Veröffentlichung sind:

* Power BI-Dienste werden nicht ausgeführt.
* Der Benutzer, der die Veröffentlichung der Arbeitsmappe geplant hat, besitzt keine gültigen Microsoft-Kontoanmeldedaten mehr.

Für jede geplante Report Builder-Aufgabe werden drei Versuche pro geplanter Ausführung durchgeführt:

* Nach dem ersten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Microsoft Power BI veröffentlicht werden. Ein neuer Versuch erfolgt in Kürze.“
* Nach dem zweiten erfolglosen Versuch wird keine Meldung angezeigt.
* Nach dem dritten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Power BI veröffentlicht werden.“

## Beschädigte Visualisierungen in Power BI

Im Folgenden werden die wichtigsten Gründe für beschädigte Visualisierungen nach der Veröffentlichung von Report Builder-Anforderungen in Power BI aufgeführt:

* Sie haben eine Anforderung in Report Builder bearbeitet, z. B. durch Ändern der Metriken oder Dimensionen, und sie dann erneut in Power BI veröffentlicht. Durch Bearbeiten von Anforderungen können Ihre Visualisierungen beschädigt werden.
* Sie haben eine Anforderung gelöscht, die in einer Visualisierung verwendet wurde.

## Report Builder muss für den Zugriff auf die Ressourcen Ihrer Organisation autorisiert sein. Dieser Zugriff kann nur von einem Administrator gewährt werden. Bitten Sie einen Administrator, Ihnen die Berechtigung zu erteilen.

Bitten Sie einen Microsoft-Administrator, die Einstellung „Benutzer können Anwendung registrieren“ zu überprüfen unter: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL Benutzereinstellungen lassen Optionen zu]**. Wenn diese Option auf „Nein“ festgelegt ist, kann dieser Administrator diese Anwendungstypen registrieren.

Benutzer können über den folgenden [Link](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) Zugriff gewähren.

Administratoren gewähren über folgenden [Link](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) Zugriff für alle Benutzer.

## API-Limit erreichen

Die Berichterstellung in Power BI funktioniert mit der Analytics Reporting-API, sodass API-Schwellenwerte gelten. Weitere Informationen finden Sie unter [Wie hoch ist das Ratenlimit für API-Aufrufe?](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/#what-is-the-rate-limit-for-api-calls).
