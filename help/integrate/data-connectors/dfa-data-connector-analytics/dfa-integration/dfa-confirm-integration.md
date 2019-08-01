---
description: Nachdem Sie alle notwendigen Websiteaktualisierungen vorgenommen haben, können Sie einen Viewer für den Datenverkehr im Netzwerk wie Charles*, Chrome Developer Tools oder Firebug* verwenden, um zu überprüfen, ob DFA mit den Adobe-Erfassungsservern kommuniziert.
keywords: DFA
seo-description: Nachdem Sie alle notwendigen Websiteaktualisierungen vorgenommen haben, können Sie einen Viewer für den Datenverkehr im Netzwerk wie Charles*, Chrome Developer Tools oder Firebug* verwenden, um zu überprüfen, ob DFA mit den Adobe-Erfassungsservern kommuniziert.
seo-title: Bestätigung einer erfolgreichen DFA-Integration
solution: Analytics
title: Bestätigung einer erfolgreichen DFA-Integration
topic: Data Connectors
uuid: d 658 cd 7 c -6377-439 a -850 c-ecea 8 c 41 f 970
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Bestätigung einer erfolgreichen DFA-Integration{#confirming-a-successful-dfa-integration} befolgen

Nachdem Sie alle notwendigen Websiteaktualisierungen vorgenommen haben, können Sie einen Viewer für den Datenverkehr im Netzwerk wie Charles*, Chrome Developer Tools oder Firebug* verwenden, um zu überprüfen, ob DFA mit den Adobe-Erfassungsservern kommuniziert.

Verwenden Sie den Viewer für den Datenverkehr im Netzwerk, nachdem Sie die DFA-aktivierte `s_code.js`-Datei bereitgestellt haben, um die Anfragen zwischen DFA und den Adobe-Datenerfassungsservern anzuzeigen und nach Folgendem zu suchen:

* A request to DFA's `fls.doubleclick.net/json` service. Die Reaktion dieses Service kann je nach verwendeter DFA-Version unterschiedlich ausfallen. Mit DFA-Integrationsversion 1.5:

   * HTTP-302-Weiterleitung auf [!DNL ad.doubleclick.net] Dadurch wird mit der Reaktion ein „Ort:“-Tag gesendet, in dem Informationen zum Anzeigenbesucher enthalten sind.
   * This Location tag causes a redirect to [!DNL integrate.112.2o7.net/dfa_echo]. Mit diesem Service werden die Informationen über Anzeigenbesucher in einen verschlüsselten JSON-String (JavaScript Object Notation) übertragen. Diese Daten werden mit einer HTTP-200-Reaktion „OK“ zurückgegeben.

* DFA-Integrationsversion 2.0 (erweitertes AdServing aktiviert):

   * [!DNL fls.doubleclick.net] gibt direkt 200 „OK“ zurück.

In jedem Fall erzeugt eine erfolgreich durchgeführte Anfrage eine Abfrage der Adobe-Datenerfassungsserver, die den Parameter vX enthält. X ist dabei die Durchsichts-eVar-Nummer. Dieser Parameterwert liegt in diesem Format vor: DFA-XXXX-XXXX- XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX. Dieser String enthält Informationen zum letzten Klick und zur letzten Impression für den aktuellen Besucher.
