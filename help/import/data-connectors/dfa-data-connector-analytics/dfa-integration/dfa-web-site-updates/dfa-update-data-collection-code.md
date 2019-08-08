---
description: Für die Genesis-Integration für DFA wird die DFA Floodlight-Konfigurations-ID (dfa_SPOTID) verwendet, wodurch die Berichtskonsistenz zwischen DFA und dem Adobe-Datenerfassungssystem verbessert wird.
keywords: DFA
seo-description: Für die Genesis-Integration für DFA wird die DFA Floodlight-Konfigurations-ID (dfa_SPOTID) verwendet, wodurch die Berichtskonsistenz zwischen DFA und dem Adobe-Datenerfassungssystem verbessert wird.
seo-title: Aktualisierung des Datenerfassungscodes Ihrer Website
solution: Analytics
title: Aktualisierung des Datenerfassungscodes Ihrer Website
topic: Data Connectors
uuid: a 97 d 1 b 62-f 883-48 b 1-9516-4 f 889 e 701901
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Aktualisierung des Datenerfassungscodes Ihrer Website{#update-your-web-site-s-data-collection-code}

Für die Genesis-Integration für DFA wird die DFA Floodlight-Konfigurations-ID (dfa_SPOTID) verwendet, wodurch die Berichtskonsistenz zwischen DFA und dem Adobe-Datenerfassungssystem verbessert wird.

>[!NOTE]
>
>Der Begriff Spotlight wurde in einer neuen Version von Google DFA in Floodlight geändert. Die Benennung des JavaScript-Parameters `dfa_SPOTID` basiert auf der Spotlight-Terminologie, wird aber für beide Versionen verwendet.

Aktualisieren Sie durch Hinzufügen folgender Elemente Ihren JavaScript-Datenerfassungscode, um die DFA-Integration auf Ihrer Website zu aktivieren:

* Integrate-Modul für DFA
* Zusatz zu Ihrem Erfassungscode

## Integrate-Modul für DFA {#section-fa00e42a732a4e27a4ab3dfcfeae1a5b}

Für die DFA-Integration wird das Adobe Marketing Cloud Integrate-Modul verwendet, wodurch zusätzliche Funktionen zu Ihrem JavaScript-Datenerfassungscode (`s_code.js`) hinzugefügt werden. Das Integrate-Modul ist Teil der.zip, wenn Sie den appmeasurement for Javascript-Code aus dem [Code-Manager herunterladen](https://marketing.adobe.com/resources/help/en_US/reference/code_manager_admin.html). Wenden Sie sich an Ihren Adobe-Berater nur, wenn Sie weitere Hilfe benötigen.

Insert the Integrate Module code in the `Modules` section of your website's `s_code.js` file.

## Zusatz zu Ihrem Erfassungscode {#section-8f98c727f1ba414fb8b4f02d696b8791}

Basierend auf Ihren Einstellungen bei der Aktivierung der DFA-Integration im Integrationsassistenten wird von Data Connectors ein benutzerdefinierter Zusatz zu Ihrem JavaScript-Datenerfassungscode erstellt, den Sie per E-Mail erhalten. Geben Sie diesen Code in den Hauptabschnitt der Datei `s_code.js` (nicht in die Funktion `doPlugins` oder andere Funktionen) ein.

Der unten gezeigte Code dient nur zu Anschauungszwecken. Verwenden Sie den Code, den Sie nach Abschluss des Data Connectors-Integrationsassistenten per E-Mail erhalten haben.

Der Erfassungscode besteht aus folgenden Elementen:

* DFA Integrate-Einstellungen
* Für die Integration erforderliche Plug-ins

**DFA Integrate-Einstellungen**

```
/************************** DFA VARIABLES **************************/ 
var dfaConfig = { 
   CSID:              "1234567", 
   SPOTID:            "29876543", 
   tEvar:             "eVar17", 
   errorEvar:         "eVar59", 
   timeoutEvent:      "event76", 
   requestURL:         "http://fls.doubleclick.net/ 
json?spot=[SPOTID]&src=[CSID]&var=[VAR]&host=integrate.112.2o7.net%2 
Fdfa_echo%3Fvar%3D[VAR]%26AQE%3D1%26A2S%3D1&ord=[RAND]", 
 
   maxDelay:          "1500", 
   visitCookie:       "s_dfa", 
   clickThroughParam: "CID", 
   searchCenterParam: "s_kwcid", 
   newRsidsProp:      undefined 
}; 
/************************ END DFA Variables ************************/ 
```

Im DFA Integrate-Einstellungsblock werden die Variablen festgelegt, die für die DFA-Integration erforderlich sind. Die Werte für diese Variablen stammen aus folgenden Quellen:

**CSID**: Client-Site-ID. Wird nach dem Abschluss des Integrationsassistenten von DFA erstellt Diese Variable wird von Data Connectors mit Ihrer DFA-CSID ausgefüllt. Sie erhalten diesen Wert außerdem in der Einrichtungs-E-Mail nach Abschluss des Integrationsassistenten. Diese Variable ist nicht erforderlich, wenn in Ihrem Konto das erweiterte AdServing aktiviert ist.

**SPOTID**: Floodlight-Konfiguration (früher Spotlight-ID) Diese Variable wird auf Basis der von Ihnen im Integrationsassistenten angegebenen DFA-Kontoinformationen von Data Connectors mit Ihrer DFA Floodlight-Konfigurations-ID ausgefüllt.

**tEvar**: Übertragungsvariable Diese Variable wird von Data Connectors mit dem Analytics-Variablennamen ausgefüllt, den Sie im Integrationsassistenten für die Durchsichtsvariable festgelegt haben. Ändern Sie diesen Wert nicht, ohne dies vorher sorgfältig mit Adobe Engineering oder Engineering Services abzuklären.

**errorEvar**: Fehlervariable Diese Variable wird von Data Connectors mit dem Analytics-Variablennamen ausgefüllt, den Sie im Integrationsassistenten für die DFA-Abfragefehlervariable festgelegt haben.

**timeoutEvent**: Timeoutereignis Diese Variable wird von Data Connectors mit dem Analytics-Variablennamen ausgefüllt, den Sie im Integrationsassistenten für die Timeoutereignisvariable festgelegt haben.

**requestURL**: DFA-Remotehost zur Abfrage von Anzeigeninformationen Ändern Sie diesen Wert nur, wenn Sie eine entsprechende Anweisung von Adobe erhalten.

**maxDelay**: Anzahl der Millisekunden, die der JavaScript-Datenerfassungscode auf eine Reaktion vom DFA Floodlight-Server wartet. Adobe empfiehlt, mit diesem Wert etwas zu experimentieren, um die für den Datenverkehr auf Ihrer Site optimale Einstellung zu ermitteln. Generell werden durch das Erhöhen dieses Werts zum Beispiel mehr DFA-Daten erfasst, aber dabei steigt das Risiko, grundlegende Besucherdaten zu verlieren, wenn Besucher die Site während der Verzögerungsphase verlassen. Wenn Sie diesen Wert reduzieren, sinkt das Risiko, Trefferdaten zu verlieren, dadurch kann sich allerdings auch die Anzahl der DFA-Daten verringern, die mit den Adobe-Trefferdaten gesendet werden.

**visitCookie**: Name des Cookies, mit dem DFA-Aufrufe auf einen pro Besuch beschränkt werden.

**clickThroughParam**: Abfragestring, der normalerweise in allen Anzeigen enthalten ist und dem Integrate-Modul vermittelt, wenn ein Klick stattgefunden hat. Dieser Parameter im Abfragestring führt dazu, dass die Abfrage vom DFA Floodlight-Server stattfindet, auch wenn die Abfrage des Besuchers in den letzten 30 Minuten bereits stattgefunden hat.

**newRsidsProp**: (Optional) Einer nicht verwendeten Datenverkehrseigenschaftsvariablen zugeordnet Dieser Wert wird von der DFA-Integration im Besuchercookie erfasst und gespeichert, um so die Report Suites zu identifizieren, die Daten zu einem speziellen Besucher erfasst haben. Diese Eigenschaft ist nur für benutzerdefinierte Implementationen für Adobe Engineering Services erforderlich.

**Für die Integration erforderliche Plug-ins**

Der Erfassungscodezusatz enthält zusätzliche Plug-ins, die die Funktion der DFA-Integration verbessern:

* DFA-Abfragen werden auf eine pro Besuch beschränkt.
* Flexibilität bei Cookienamen ist gewährleistet. Die meisten Organisationen verwenden s_dfa, Sie können für die DFA-Integration aber jeden beliebigen zulässigen Cookienamen verwenden.
* Unnötige Weiterleitungen werden vermieden. Adobe-Erfassungsserver und DFA können praktisch bei jeder Seitenansicht Daten austauschen, da die Durchsichtsdaten in Echtzeit erfasst werden. Dieser Datenaustausch wird vom Plug-in verhindert, wenn die Informationen nicht notwendig sind.

>[!CAUTION]
>
>Eines der Mechanismen, mit dem das Plug-in unnötige DFA-Abfragen löscht, ist ein domänenbasiertes Besuchcookie. Eine Integrations-Report Suite, die mehrere Domänen umfasst, erhöht die Clickthrough- und Durchsichtsdaten, wenn Besucher nach einer DFA-basierten Durchsichts- oder Clickthrough-Aktion die Domäne wechseln.

