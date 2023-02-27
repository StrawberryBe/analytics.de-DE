---
description: Übersicht der Daten, die Adobe Analytics erfasst, und sonstige Hinweise zum Datenschutz.
keywords: Datenschutz
title: Datenschutzübersicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 77e50dec593722855f30c517f63141e84f665519
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 96%

---

# Datenschutzübersicht

Adobe empfiehlt Ihnen, dass Sie den Besuchern Ihrer Website leicht auffindbare und leicht verständliche Informationen darüber bereitstellen, wie sie sich von der Erfassung von Browserinformationen durch Adobe-Produkte und -Dienste ausschließen lassen können.

Besucher können mehr darüber erfahren, wie Adobe die im [Adobe-Datenschutzzentrum](https://www.adobe.com/de/privacy.html) erfassten Informationen im Allgemeinen verwendet. Es ist Sache Ihres Unternehmens, ob Sie offenlegen möchten, wie Sie die Adobe-Produkte und -Dienste verwenden. Denn nur Ihre Organisation hat die Kontrolle darüber, wie die Adobe-Dienste implementiert werden. Sie sind selbst für die Erstellung Ihrer eigenen Datenschutzrichtlinien verantwortlich sowie für die Einhaltung Ihrer Datenschutzrichtlinien, die Einhaltung Ihres Servicevertrags mit Adobe und die Einhaltung jeglichen geltenden Rechts.

## Aufschlüsselung der Datenerfassung {#section_F59D958D7AE44747846993E643CD4BF2}

Adobe Analytics erfasst die folgenden Daten:

| Datentyp | Erfasst Adobe Analytics diese Daten? |
|---|---|
| URLs von Webseiten in Kunden-Sites | Ja |
| Name der Webseite | Ja |
| Besuchszeit pro Seite | Ja |
| Tageszeit | Ja |
| URLs von Webseiten auf Sites Dritter | **Nein** |
| Cookie-IDs (zufällig generiert) | Ja |
| URL der Seite, die der Benutzer vor Besuch der Kundenseite besucht hat | Ja |
| Suchabfrage, wenn Benutzer auf Link zur Kundenseite klickt | Ja |
| Browser-Typ | Ja |
| Gerätetyp | Ja |
| Betriebssystem | Ja |
| ISP-/Verbindungsgeschwindigkeit | Ja |
| Anzeigeeinstellungen (z. B. Bildschirmgröße und Auflösung) | Ja |
| IP-Adresse (zur Ermittlung des ungefähren Standorts) | Ja&#42; |
| Informationen, die Benutzer in Formulare auf der Kunden-Site eingeben | Ja |
| Informationen, die Benutzer in Formulare auf sozialen Sites eingeben | **Nein** |
| Ob der Benutzer auf eine Anzeige geklickt hat | Ja |
| Ob der Benutzer auf einen Link, ein Bild oder auf Text auf der Site geklickt hat | Ja |
| Ob der Benutzer eine Datei, ein Bild etc. heruntergeladen hat | Ja |
| Artikel, die der Benutzer gekauft hat | Ja |
| Artikel, die sich noch im Warenkorb befinden | Ja |
| Soziales Netzwerk-Informationen (einschließlich Fotos, Benutzer-ID, Alter, Geschlecht, Standort) | **Nein** |
| Persönliche Informationen, die der Benutzer außerhalb unserer Dienste angibt | Ja |
| Erfolgsraten von Werbekampagnen | Ja |
| Produktinformationen, z. B. Farben, Preise, Stile, Fotos | Ja |

&#42;Es sei denn, der Adobe-Kunde entfernt die IP.

## Sonstige Hinweise zum Datenschutz {#section_60AF6AD6FBD046EEAF9F083A9726EF8A}

| Region/Land | Übertragung |
|--- |--- |
| Global | Adobe empfiehlt seinen Kunden, auf keinen Fall persönlich identifizierbare Informationen (PII) an Adobe weiterzugeben, insbesondere in Situationen, in denen PII nicht für Analytics benötigt werden. |
| Global | Benutzer müssen bei der Profilierung Hinweise und Auswahlmöglichkeiten erhalten. In der europäischen Union (in einigen Ländern auf Opt-in-Basis), Kanada, Australien und vielen Ländern in Lateinamerika und im Asiatisch-Pazifischen Raum ist dies gesetzlich vorgeschrieben. |
| Global | Bei Verwendung von Erstanbieter-Cookies bezieht sich die Analytics-Abmeldung ausschließlich auf den jeweiligen Kunden. Die Abmeldung auf Adobe.com ist nicht ausreichend. |
| Global | Analysen von Erstanbietern sind nicht Teil des Self-Regulatory Program for Online Behavioral Advertising („AdChoices“). |
| Global | Geräteübergreifende Daten sollten zusammengeführt werden, außer sie sind an eine ID gebunden, die der Kunde zur Verfügung gestellt hat (z. B. einen Hash-Benutzernamen). |
| Global | Es gelten voraussichtlich Beschränkungen für die Kombination von Anzeigenimpressionen und PII für den Kunden. |
| Europa | Die meisten Länder der europäischen Union erachten Analyse-Cookies nicht als unbedingt erforderlich. |
| Europa | Adobe hat die Einstellung „IP-Verschleierung“ aktiviert: Aktiviert – IP entfernt (x.x.x.x), gilt standardmäßig für alle Kunden mit einer Report Suite in EMEA. Mit dieser Einstellung wird die IP-Adresse nach der Geo-Suche vollständig durch den Wert (x.x.x.x) ersetzt und ist nicht mehr als Datenpunkt verfügbar. Bei dieser grundlegenden Austauschmethode kann nicht durch Reverse Engineering auf eine eindeutige, spezifische IP-Adresse geschlossen werden. Weder der Kunde noch Adobe können auf die IP-Adresse zugreifen. Sie wird irreversibel anonymisiert. Weitere Informationen zu anderen IP-Verschleierungseinstellungen erhalten Sie unter [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) im Admin-Benutzerhandbuch. |
| Global | Ein Kunde kann die Variable für die Cookie-Lebensdauer im JavaScript-Messungs-Code auf den Wert „none“, „session“ oder einen anderen spezifischen, in Sekunden gemessenen Wert setzen. |
| Europa | Adobe verfügt über eine neue Einstellung für eingebauten Datenschutz, die jetzt mit Adobe ClientCare für die Versionen 14.9 und 15.4 von Adobe Analytics (früher SiteCatalyst) aktiviert werden können. Ist diese neue Einstellung aktiviert, wird das letzte Oktett (der letzte Teil) der IP-Adresse unverzüglich durch den Wert 0 ersetzt, sobald die IP-Adresse von Adobe erfasst wird. Diese Anonymisierung wird vor der Verarbeitung der IP-Adresse durchgeführt, also auch vor einer optionalen Geo-Suche und ISP-Suche der IP-Adresse. |
| Deutschland | Wenn SIe nicht bereits einen Vertrag über Auftragsdatenverarbeitung (ADV) für Adobe Analytics mit Adobe abgeschlossen haben, sollten Sie Ihren Adobe-Kundenbetreuer oder Customer Success Manager kontaktieren, der den ADV mit der Rechtsabteilung von Adobe abschließen wird. |

## EMEA-Rechenzentrumsstandort {#section_3DD2329B983849D3B8C24AEF7CD8DFB3}

Das folgende EMEA-Rechenzentrum hostet derzeit Adobe Analytics-Daten:

| Adobe-Name | Adresse | Anbietertyp (Operator) | Unterstützte Lösungskomponenten | Zertifizierungen |
|--- |--- |--- |--- |--- |
| LON5 | 3 Centro  Boundary Way Hemel Hempstead HP2 7SU Vereinigtes Königreich | Colocation Facility (Gyron) | Multichannel Analytics, Digital Analytics | SSAE 16 |