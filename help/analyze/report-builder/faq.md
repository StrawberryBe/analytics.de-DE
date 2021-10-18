---
title: Häufig gestellte Fragen zu Report Builder
description: Häufig gestellte Fragen zu Report Builder
feature: Report Builder
role: User, Admin
exl-id: 86604d39-2965-45a5-98ab-3ee4adcb7f97
source-git-commit: 51cac193cd2c88898139e079816a084c211a64f4
workflow-type: ht
source-wordcount: '420'
ht-degree: 100%

---

# Häufig gestellte Fragen zu Report Builder

Häufig gestellte Fragen rund um Report Builder.

## Kann ich die Funktion `TODAY()` oder `DATERANGE()` in Arbeitsmappen verwenden?

Die [`TODAY()`-Funktion](https://support.microsoft.com/de-de/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel gibt den aktuellen Tag zurück. Die [`DATEVALUE()`-Funktion](https://support.microsoft.com/de-de/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) wandelt eine Datumszeichenfolge in einen seriellen Wert um. Obwohl diese Funktionen für viele Funktionalitäten in Excel hilfreich sind, empfiehlt Adobe dringend, diese Funktionen nicht als Teil geplanter Report Builder-Anfragen zu verwenden. Die Adobe-Kundenunterstützung unterstützt keine Anfragen zur Fehlerbehebung mit einer dieser Funktionen.

Terminierte Berichte werden auf Servern verarbeitet, die wahrscheinlich nicht die gleichen Zeitzonen haben wie die Report Suite. Die Funktion `TODAY()`, die ein Benutzer erwartet, und die Funktion `TODAY()`, die der Verarbeitungs-Server verwendet, können häufig unterschiedlich sein. Außerdem basiert das verwendete Datum auf dem Beginn der Verarbeitung. Wenn mehrere Berichte gleichzeitig ausgeführt werden, kann sich aufgrund von Verzögerungen das Datum zwischen der angeforderten Zeit und dem Beginn der Verarbeitung ändern. Dieses Problem tritt auf, wenn die geplante Zeit nahe um Mitternacht liegt.

Terminierte Berichte werden auch auf Servern verarbeitet, die wahrscheinlich keine Datumssyntax verwenden. Zum Beispiel kann `7/1/YYYY` je nach Land oder Region auf den 1. Juli oder den 7. Januar verweisen. Die Anwendung der Funktion `DATEVALUE()` auf dieses Datum würde zu unterschiedlichen seriellen Werten führen, je nachdem, welcher Computer die Funktion ausführt.

Als Alternative zu diesen Excel-Funktionen empfiehlt Adobe dringend die Verwendung von Datumsbereichen innerhalb von Report Builder-Anfragen. Wählen Sie auf der ersten Seite des Anfrage-Assistenten in der Dropdown-Liste **[!UICONTROL Vordefinierte Datumswerte]** und dann unter „Häufig verwendete Datumswerte“ die Option **[!UICONTROL Heute]** oder einen anderen gewünschten Datumsbereich. Bei dieser Einstellung wird die Zeit der Report Suite zum Zeitpunkt der Ausführung berücksichtigt und nicht die Zeit, zu der der Server die Anforderung verarbeitet.

## Wie groß und komplex kann ich meine Arbeitsmappen machen?

Report Builder unterstützt Arbeitsmappen bis zu den folgenden Grenzen:

* **1.000 Anfragen**: Eine einzelne Arbeitsmappe kann bis zu 1.000 Datenanfragen enthalten. Wenn Sie Berichte oder Projekte haben, für die mehr als 1000 Anforderungen erforderlich sind, empfiehlt Adobe, diese in mehrere Arbeitsmappen aufzuteilen.
* **20.000 Anfragen pro Stunde und Firma**: Report Builder verwendet die Analytics-Reporting-API zum Abrufen von Daten. Jede einzelne Anfrage verwendet einen API-Aufruf, wenn sie erstellt oder aktualisiert wird. Wenn sich für Ihr Unternehmen mehr als 20.000 API-Aufrufe in einer bestimmten Stunde ansammeln, müssen Sie bis zur nächsten Stunde warten, um die Daten erneut abzurufen.
* **Vierstündige Verarbeitungszeit**: Terminierte Berichte werden beendet, wenn deren Verarbeitung mehr als vier Stunden dauert. Wenn Ihre Arbeitsmappe viele komplexe Anfragen mit großen Datensätzen enthält, kann der terminierte Bericht fehlschlagen.
