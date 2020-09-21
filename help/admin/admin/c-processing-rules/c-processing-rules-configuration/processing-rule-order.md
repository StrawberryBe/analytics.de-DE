---
description: Um die Verarbeitungsregeln effektiv nutzen zu können, muss allen Beteiligten klar sein, zu welchem Zeitpunkt der Datenerfassung die Regeln angewendet werden.
subtopic: Processing rules
title: Verarbeitungsreihenfolge
topic: Admin tools
uuid: cea01d13-dfd5-40f7-8b2f-b6e2fe8354df
translation-type: ht
source-git-commit: 31506d4d3fa26a3012cce2c6a8fdeb7af52c2537
workflow-type: ht
source-wordcount: '505'
ht-degree: 100%

---


# Verarbeitungsreihenfolge

Um die Verarbeitungsregeln effektiv nutzen zu können, muss allen Beteiligten klar sein, zu welchem Zeitpunkt der Datenerfassung die Regeln angewendet werden.

![](assets/analytics_processing_order_test.png)

In den folgenden Tabellen sind die Daten aufgeführt, die in der Regel vor und nach der Anwendung der Verarbeitungsregeln verfügbar sind:

## Vor Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| Suche dynamischer Variablen | Variablen werden dynamisch ausgefüllt, indem Informationen aus HTTP-Kopfzeilen oder anderen Variablen abgerufen werden. So setzt z. B. `s.eVar5="D=c1"` den Wert von prop1 in eVar5. |
| AppMeasurement | Funktionen und Plug-ins, die in AppMeasurement genutzt werden, werden im Browser oder der Client-Anwendung ausgeführt. |
| Tag-Management | Die in Adobe Launch oder im Dynamic Tag Management festgelegten Regeln werden per Definition ausgeführt. |
| Bot-Regeln | Mit [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. |

## Nach Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| Von VISTA hinzugefügte Daten | Verarbeitungsregeln werden vor VISTA angewendet. |
| Anzahl besuchter Seiten | Im Allgemeinen beziehen sich Verarbeitungsregeln nur auf die im aktuellen Treffer befindlichen Daten. Die Anzahl besuchter Seiten wird nach der Anwendung der Verarbeitungsregeln kompiliert. |
| Falls Seitenname nicht festgelegt ist, wird bereinigte URL-Adresse verwendet | Nachdem die Verarbeitungsregeln und die VISTA-Regeln angewendet wurden, wird die bereinigte URL-Adresse als Seitenname hinzugefügt, insofern kein Seitenname festgelegt wurde. Da dies nach der Anwendung der Verarbeitungsregeln geschieht, sollten Sie mit Hilfe einer Bedingung prüfen, ob die Angabe für den Seitennamen leer ist.  Wenn Sie unter „Site-Content“ die Option „Seitenberichte“ aufrufen und dort für Seitennamen „https://“-Werte angegeben sind, ist der Eintrag für den Seitennamen aller Wahrscheinlichkeit nach leer, und die URL-Adresse wird verwendet.  Sie können eine Bedingung einrichten, um zu prüfen, ob der Seitennamen-Eintrag leer ist bzw. ob dieser Eintrag bzw. der Eintrag für die URL-Adresse der Seite einen bestimmten Wert aufweist. Der Seitenname kann anschließend nach Bedarf festgelegt werden. |
| Marketingkanal-Verarbeitungsregeln | Mit Hilfe von Verarbeitungsregeln können Sie Daten für die Verarbeitung mit [Marketingkanal-Regeln](https://docs.adobe.com/content/help/de-DE/analytics/components/marketing-channels/c-rules.html) vorbereiten. |
| GEO-Suche | Dies betrifft die Werte „Bundesstaat des Besuchers“ und „Postleitzahl des Besuchers“. |
| eVars-Speicherung | eVars aus einem vorherigen Treffer werden bei der Regelverarbeitung nicht bei jedem Treffer beibehalten. Es stehen jeweils nur die beim aktuell verarbeiteten Treffer festgelegten eVars zur Verfügung. |

## So werden Verarbeitungsregeln beim Kopieren von Hits mit VISTA angewandt  {#section_576EE8C240A24CBA979BD614E8D5338D}

Wenn Sie eine VISTA-Regel zum Kopieren von Treffern in eine andere Report Suite konfiguriert haben, werden die Treffer über sämtliche in der anderen Report Suite definierten Verarbeitungsregeln versendet.

Wenn Sie Verarbeitungsregeln nutzen, die für die ursprüngliche Report Suite definiert sind, können diese je nachdem angewandt werden, wie die VISTA-Regel durch den technischen Support konfiguriert wurde. Um dies herauszufinden, können Sie Ihren Implementierungsspezialisten fragen, ob die VISTA-Regel die „prä“- oder „post“-Werte in die zusätzliche Report Suite kopiert. Wenn der „prä“-Wert kopiert wird, werden die in der ursprünglichen Report Suite definierten Verarbeitungsregeln nicht angewandt. Wenn der „post“-Wert kopiert wird, werden Verarbeitungsregeln angewandt, bevor der Hit kopiert wird.
