---
title: Häufig gestellte Fragen zu Report Buildern
description: Häufig gestellte Fragen zum Report Builder
translation-type: tm+mt
source-git-commit: 47b14bde1bb1217bcb172c6d4f01d68f917d44db
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# Häufig gestellte Fragen zu Report Buildern

Häufig gestellte Fragen rund um Report Builder.

## Kann ich die Funktion `TODAY()` oder `DATERANGE()` Funktion in Arbeitsmappen verwenden?

Die [`TODAY()` Funktion](https://support.microsoft.com/en-us/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel gibt den aktuellen Tag zurück. Die [`DATEVALUE()` Funktion](https://support.microsoft.com/en-us/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) wandelt eine Datums-Zeichenfolge in einen seriellen Wert um. Obwohl diese Funktionen für viele Funktionen in Excel hilfreich sind, empfiehlt Adobe dringend, diese Funktionen nicht als Teil der geplanten Report Builder-Anforderungen zu verwenden. Der Kundendienst von Adobe unterstützt keine der beiden Funktionen zur Fehlerbehebung.

Geplante Berichte werden auf Servern verarbeitet, die wahrscheinlich keine Zeitzonen als Report Suite haben. Der `TODAY()` Benutzer erwartet und der `TODAY()` vom Verarbeitungsserver verwendete Wert kann häufig unterschiedlich sein. Außerdem basiert das verwendete Datum auf der Verarbeitung von Beginn. Wenn mehrere Berichte gleichzeitig ausgeführt werden, kann sich das Datum zwischen der angeforderten Zeit und dem Beginn der Verarbeitung aufgrund von Verzögerungen ändern. Dieses Problem tritt auf, wenn die geplante Zeit nahe um Mitternacht liegt.

Terminierte Berichte werden auch auf Servern verarbeitet, die wahrscheinlich keine Datumssyntax verwenden. Sie `7/1/YYYY` können beispielsweise je nach Land oder Region auf den 1. Juli oder den 7. Januar verweisen. Die Verwendung der `DATEVALUE()` Funktion an diesem Datum würde je nach Computer, auf dem sie ausgeführt wird, zu unterschiedlichen seriellen Werten führen.

Als Alternative zu diesen Excel-Funktionen empfiehlt Adobe dringend die Verwendung von Datumsbereichen innerhalb von Report Builder-Anforderungen. Wählen Sie auf der ersten Seite des Anforderungs-Assistenten in der Dropdown-Liste die Option **[!UICONTROL Vordefinierte Datumswerte]** und wählen Sie dann unter &quot;Häufig verwendete Datumswerte&quot;die Option **[!UICONTROL Heute]** oder einen anderen gewünschten Datumsbereich. Diese Einstellung nimmt die Zeit in Anspruch, die die Report Suite zum Zeitpunkt der Ausführung hat, und nicht den Zeitpunkt, zu dem der Server die Anforderung verarbeitet.

## Wie groß und komplex kann ich meine Arbeitsmappen machen?

Report Builder unterstützt Arbeitsmappen bis zu den folgenden Einschränkungen:

* **1000 Anträge**: Eine Arbeitsmappe kann bis zu 1000 Datenanforderungen in einer einzigen Arbeitsmappe enthalten. Wenn Sie Berichte oder Projekte haben, für die mehr als 1000 Anforderungen erforderlich sind, empfiehlt Adobe, diese in mehrere Arbeitsmappen zu unterteilen.
* **20.000 Anfragen pro Firma**: Report Builder verwendet die Analytics Berichte-API zum Abrufen von Daten. Jede einzelne Anforderung verwendet einen API-Aufruf, wenn sie erstellt oder aktualisiert wird. Wenn Ihr Unternehmen mehr als 20.000 API-Aufrufe in einer bestimmten Stunde ansammelt, müssen Sie bis zur nächsten Stunde warten, um die Daten erneut abzurufen.
* **4-Stunden-Verarbeitungszeit**: Geplante Berichte werden nach der Verarbeitung nach 4 Stunden beendet. Wenn Ihre Arbeitsmappe viele komplexe Anforderungen mit großen Datensätzen enthält, kann der geplante Bericht fehlschlagen.
