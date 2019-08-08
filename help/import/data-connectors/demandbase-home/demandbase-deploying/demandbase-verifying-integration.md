---
description: Überprüfen Sie, ob die Integration Daten erfolgreich erfasst, indem Sie Live-Verfolgung und -berichterstellung überprüfen.
seo-description: Überprüfen Sie, ob die Integration Daten erfolgreich erfasst, indem Sie Live-Verfolgung und -berichterstellung überprüfen.
seo-title: Überprüfung der Integration
title: Überprüfung der Integration
uuid: a 9 a 0746 a -4845-41 ae -919 e-e 85 d 95 c 305
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Überprüfung der Integration{#verifying-the-integration}

Überprüfen Sie, ob die Integration Daten erfolgreich erfasst, indem Sie Live-Verfolgung und -berichterstellung überprüfen.

## Live-Verfolgung {#section-9c20e8ff6b404ae09387ee07d675c9e2}

Verwenden Sie das Debugger-Tool von digitalpulse, um zu überprüfen, ob die Demandbase-Dimensionsdaten an Adobe Analytics gesendet werden. Laden Sie nach dem Löschen der Cookies eine Seite auf Ihrer Website neu, auf der der Integrationscode bereitgestellt wurde. Wenn Ihre aktuelle IP einer von Demandbase erkannten Organisation zugeordnet wird, sollten Sie Ergebnisse sehen, die dem folgenden ähneln.

**Reports &amp; Analysen (zuvor sitecatalyst) umfasst die zwei Kontextbasiskontextdatenvariablen:**

![](assets/debugger1.png)

** Target Mbox enthält die Demandbase-Profilparameter: **

Dies wird nur angezeigt, wenn Sie Target auf der Seite implementiert haben UND diese Integration für Adobe Target konfiguriert ist - siehe Schritt 4 im Adobe-Integrationsassistenten.

![](assets/debugger2.png)

## Berichterstellung {#section-1792fe75dc3249d0ad063dfd87a89162}

Überprüfen Sie Ihre Demandbase-Berichte in Adobe Analytics mithilfe des Dashboards, das automatisch für Sie mithilfe des Adobe Integration-Assistenten (Schritt 7) erstellt wurde.

Sie können auch zur Demandbase-Berichterstellung innerhalb der Menüstruktur von Adobe Analytics navigieren - siehe Screenshots unten.

>[!NOTE]
>
>Diese Daten sollten innerhalb von 24 bis 48 Stunden nach erfolgreicher Bereitstellung angezeigt werden.

![](assets/reporting1.png)

![](assets/reporting2.png)

## Häufig gestellte Fragen {#section-d926b160a2ef4f07b43ea1bc67ac2a0a}

**Was bedeutet "[n/a]" ?**

Der Demandbase Data Connector zeigt an, wenn ein Attribut "Nicht verfügbar" ist, indem dieses Standardwert festgelegt wird. Es gibt zwei gängige Szenarien, in denen die Standardeinstellung festgelegt ist:

* Demandbase erkennt, dass der Besucher von einer IP-Adresse kommt, die nicht zu einem Unternehmen gehört.
* Ein Konto Watch Watch (beginnend mit "watch_ list" ) wird verwendet, das Unternehmen befindet sich jedoch nicht in Ihrer Kontoüberwachungsliste.

** Warum wird "[k/a]«für bestimmte Attribute häufiger angezeigt? **

Demandbase klassifiziert alle IP-Adressen und stellt die Attribute Zielgruppe und audience_ segment bereit, auch wenn der Besucher nicht aus einer Unternehmens-IP kommt. Wenn Zielgruppe Werte wie "Residenten" ," Wireless" und "Gastgewerbe" zurückgibt, sind die übrigen Attribute wahrscheinlich nicht verfügbar.

Manchmal ist die Zielgruppe eines Besuchers "SMB" , andere Attribute hingegen"[n/a]" . Dies bedeutet, dass Demandbase den Besucher als kleine Geschäftstätigkeit klassifizieren kann, aber das vollständige Unternehmensprofil ist nicht verfügbar. Dies geschieht üblicherweise für die kleinsten Unternehmen, wenn mehr als ein kleines Unternehmen denselben Service Provider oder denselben IP-Adressen-Block verwendet.

## Überlegungen zum Entwickler {#section-d33fff55bc4b4db99f82dee418ef1bc2}

Wenn Sie den Standardwert in Ihrer Implementierung anpassen müssen, aktualisieren Sie die Zeile:

```
_db._nonOrgMatchLabel = "[n/a]";
```

