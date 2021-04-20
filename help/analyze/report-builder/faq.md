---
title: Häufig gestellte Fragen zu Report Builder
description: Häufig gestellte Fragen zum Report Builder
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# Häufig gestellte Fragen zu Report Builder

Häufig gestellte Fragen rund um Report Builder.

## Kann ich die Funktion `TODAY()` oder `DATERANGE()` in Arbeitsmappen verwenden?

Die Funktion [`TODAY()`](https://support.microsoft.com/en-us/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel gibt den aktuellen Tag zurück. Die Funktion [`DATEVALUE()`](https://support.microsoft.com/en-us/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) wandelt eine Datums-Zeichenfolge in einen seriellen Wert um. Obwohl diese Funktionen für viele Funktionen in Excel hilfreich sind, empfiehlt Adobe dringend, diese Funktionen nicht als Teil der geplanten Report Builder-Anforderungen zu verwenden. Der Kundendienst von Adobe unterstützt keine der beiden Funktionen zur Fehlerbehebung.

Geplante Berichte werden auf Servern verarbeitet, die wahrscheinlich keine Zeitzonen als Report Suite haben. Der Wert `TODAY()`, den ein Benutzer erwartet, und der `TODAY()`, den der Verarbeitungsserver verwendet, kann häufig unterschiedlich sein. Außerdem basiert das verwendete Datum auf der Verarbeitung von Beginn. Wenn mehrere Berichte gleichzeitig ausgeführt werden, kann sich das Datum zwischen der angeforderten Zeit und dem Beginn der Verarbeitung aufgrund von Verzögerungen ändern. Dieses Problem tritt auf, wenn die geplante Zeit nahe um Mitternacht liegt.

Terminierte Berichte werden auch auf Servern verarbeitet, die wahrscheinlich keine Datumssyntax verwenden. Zum Beispiel kann `7/1/YYYY` je nach Land oder Region auf den 1. Juli oder den 7. Januar verweisen. Die Verwendung der Funktion `DATEVALUE()` an diesem Datum würde zu unterschiedlichen seriellen Werten führen, je nachdem, welcher Computer die Funktion ausführt.

Als Alternative zu diesen Excel-Funktionen empfiehlt Adobe dringend die Verwendung von Datumsbereichen innerhalb von Report Builder-Anforderungen. Wählen Sie auf der ersten Seite des Anforderungs-Assistenten **[!UICONTROL Vordefinierte Datumswerte]** in der Dropdown-Liste und dann unter &quot;Häufig verwendete Datumswerte&quot;die Option **[!UICONTROL Heute]** oder einen anderen gewünschten Datumsbereich. Diese Einstellung nimmt die Zeit in Anspruch, die die Report Suite zum Zeitpunkt der Ausführung hat, und nicht den Zeitpunkt, zu dem der Server die Anforderung verarbeitet.

## Wie groß und komplex kann ich meine Arbeitsmappen machen?

Report Builder unterstützt Arbeitsmappen bis zu den folgenden Einschränkungen:

* **1000 Anträge**: Eine Arbeitsmappe kann bis zu 1000 Datenanforderungen in einer einzigen Arbeitsmappe enthalten. Wenn Sie Berichte oder Projekte haben, für die mehr als 1000 Anforderungen erforderlich sind, empfiehlt Adobe, diese in mehrere Arbeitsmappen zu unterteilen.
* **20.000 Anfragen pro Firma**: Report Builder verwendet die Analytics Berichte-API zum Abrufen von Daten. Jede einzelne Anforderung verwendet einen API-Aufruf, wenn sie erstellt oder aktualisiert wird. Wenn Ihr Unternehmen mehr als 20.000 API-Aufrufe in einer bestimmten Stunde ansammelt, müssen Sie bis zur nächsten Stunde warten, um die Daten erneut abzurufen.
* **4-Stunden-Verarbeitungszeit**: Geplante Berichte werden nach der Verarbeitung nach 4 Stunden beendet. Wenn Ihre Arbeitsmappe viele komplexe Anforderungen mit großen Datensätzen enthält, kann der geplante Bericht fehlschlagen.
