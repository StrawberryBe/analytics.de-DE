---
description: Wo sich Verarbeitungsregeln in der übergeordneten Analytics-Daten-Pipeline befinden.
subtopic: Processing rules
title: Verarbeitungsreihenfolge
feature: Processing Rules
exl-id: c7143527-017c-4550-b55e-09ea437d7c85
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 52%

---

# Verarbeitungsreihenfolge

Damit Sie die Verarbeitungsregeln effektiv nutzen können, müssen Sie wissen, wann sie bei der Datenerfassung angewendet werden.

![Auftrag wird bearbeitet](assets/analytics_processing_order.png)

In den folgenden Tabellen sind die Daten aufgeführt, die in der Regel vor und nach der Anwendung der Verarbeitungsregeln verfügbar sind.

## Vor Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| [Dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) | Variablen, die dynamisch aufgefüllt werden, indem Informationen aus HTTP-Headern oder anderen Variablen abgerufen werden. |
| [AppMeasurement](/help/implement/home.md) | In AppMeasurement-Bibliotheken verwendete Funktionen und Plug-ins werden im Browser oder in der Clientanwendung ausgeführt. |
| [Tag-Implementierung](/help/implement/launch/overview.md) | In der Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung definierte Regeln. |
| [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/analytics-overview.html) | Über das Web SDK erfasste Daten werden an Adobe Experience Edge gesendet und dann an die gewünschte Report Suite weitergeleitet. |
| [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) | Ermöglicht Ihnen das Entfernen des von bekannten Spiders und Bots generierten Traffics. |

## Nach Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| Von VISTA hinzugefügte Daten | Verarbeitungsregeln werden vor VISTA angewendet. |
| Anzahl besuchter Seiten | Verarbeitungsregeln sind nur über die Daten informiert, die im aktuellen Treffer enthalten sind. Die Anzahl besuchter Seiten wird nach der Anwendung der Verarbeitungsregeln kompiliert. |
| Falls Seitenname nicht festgelegt ist, wird bereinigte URL-Adresse verwendet | Nachdem die Verarbeitungsregeln und die VISTA-Regeln angewendet wurden, wird die bereinigte URL-Adresse als Seitenname hinzugefügt, insofern kein Seitenname festgelegt wurde. Da diese Logik nach Anwendung der Verarbeitungsregeln auftritt, empfiehlt Adobe, eine Bedingung hinzuzufügen, um zu überprüfen, ob der Seitenname leer ist.  Wenn Sie die **[!UICONTROL Site-Content]** > **[!UICONTROL Seiten]** Berichte und Sie sehen URL-Werte für Seitennamen, ist es wahrscheinlich, dass die Variable für den Seitennamen leer ist.  Sie können eine Bedingung einrichten, um auf einen leeren Seitennamen zu testen oder zu testen, ob der Seitenname oder die Seiten-URL einen bestimmten Wert enthält. Der Seitenname kann anschließend nach Bedarf festgelegt werden. |
| Marketingkanal-Verarbeitungsregeln | Mit Hilfe von Verarbeitungsregeln können Sie Daten für die Verarbeitung mit [Marketingkanal-Regeln](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-rules.html?lang=de) vorbereiten. |
| GEO-Suche | Umfasst die Werte für Besucherstatus und Postleitzahl der Besucher. |
| eVars-Speicherung | eVars aus einem vorherigen Treffer werden bei der Regelverarbeitung nicht bei jedem Treffer beibehalten. Es stehen jeweils nur die beim aktuell verarbeiteten Treffer festgelegten eVars zur Verfügung. |

## So werden Verarbeitungsregeln beim Kopieren von Hits mit VISTA angewandt 

Wenn Sie eine VISTA-Regel zum Kopieren von Treffern in eine andere Report Suite konfiguriert haben, werden die Treffer über sämtliche in der anderen Report Suite definierten Verarbeitungsregeln versendet.

Wenn Sie Verarbeitungsregeln für die ursprüngliche Report Suite definiert haben, können diese Regeln je nachdem, wie die VISTA-Regel von Engineering Services konfiguriert wurde, angewendet werden. Um dies herauszufinden, können Sie Ihren Implementierungsspezialisten fragen, ob die VISTA-Regel die „prä“- oder „post“-Werte in die zusätzliche Report Suite kopiert. Wenn der „prä“-Wert kopiert wird, werden die in der ursprünglichen Report Suite definierten Verarbeitungsregeln nicht angewandt. Wenn der „post“-Wert kopiert wird, werden Verarbeitungsregeln angewandt, bevor der Hit kopiert wird.
