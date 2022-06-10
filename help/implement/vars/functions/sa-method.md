---
title: sa
description: Ändern Sie die Report Suite jederzeit in Ihrer Implementierung.
feature: Variables
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 38%

---

# sa

Mit der `sa()`-Methode können Sie eine Report Suite jederzeit auf der Seite dynamisch ändern. Wenn Sie Daten ohne Seitenneuladung an andere Report Suites senden möchten, können Sie diese Methode verwenden.

## Umgang mit Report Suites mit dem Web SDK

Das Web SDK sendet Daten an einen bestimmten Datastream, der Daten an die gewünschten Analytics Report Suites weiterleitet. Ein einzelner Datastream kann Daten an mehrere Report Suites weiterleiten. Dieser Abschnitt gilt sowohl für die Web SDK-Erweiterung als auch für die manuelle Implementierung des Web SDK.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken **[!UICONTROL Datenspeicher]** auf der linken Seite.
1. Klicken Sie auf den gewünschten Datastream oder klicken Sie auf **[!UICONTROL Neuer Datenspeicher]**.
1. Klicken **[!UICONTROL Dienst hinzufügen]**, wählen Sie **[!UICONTROL Adobe Analytics]**.
1. Geben Sie die gewünschte Report Suite-ID ein. Wenn Sie dieselben Daten an mehrere Report Suites senden möchten, klicken Sie auf **[!UICONTROL Report Suite hinzufügen]**.
1. Nachdem alle gewünschten Report Suites eingegeben wurden, klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des gewünschten Datenspeichers mithilfe der Web SDK-Erweiterung

Die Web SDK-Erweiterung stellt für jede Umgebung ein Dropdown-Menü &quot;Datastream&quot;bereit. Alternativ können Sie die Datastream-ID manuell eingeben.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Erweiterungen] und klicken Sie auf die **[!UICONTROL Konfigurieren]** Schaltfläche unter [!UICONTROL Adobe Experience Platform Web SDK].
1. under [!UICONTROL Datenspeicher]wählen Sie den gewünschten Datastream aus der Dropdown-Liste für jede Umgebung aus.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des gewünschten Datastreams zur manuellen Implementierung des Web SDK

Legen Sie die `edgeConfigId` Konfigurationsvariable zur Datastream-ID hinzu. Die Datastream-ID befindet sich rechts beim Anzeigen eines Datastreams in der Adobe Experience Platform-Datenerfassung.

```js
alloy("configure", {
  "edgeConfigId": "example-a01f-4458-8cec-ef61de241c93",
});
```

Siehe [Web SDK konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) in der Web SDK-Dokumentation finden Sie weitere Informationen.

## Report Suite mithilfe der Adobe Analytics-Erweiterung ändern

Es gibt keine flexible Möglichkeit, die Report Suite in der Oberfläche zu ändern. Sie können die Report Suite bei der Konfiguration der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] festlegen. Sie können die Report Suite jedoch nicht mithilfe von Regeln ändern oder aktualisieren. Wenn Sie die Report Suite-Werte nach dem Festlegen aktualisieren möchten, verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.sa() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.sa()`-Methode auf, um die Ziel-Report Suite zu ändern. Das einzige Argument ist eine Zeichenfolge, die eine Report Suite-ID oder mehrere durch ein Komma getrennte Report Suite-IDs enthält. Das Argument der Report Suite-ID ist erforderlich. Verwenden Sie keine Leerzeichen im Zeichenfolgenargument.

```js
s.sa("examplersid");
```

Sie können beispielsweise die Report Suite ändern, wenn der Benutzer eine bestimmte Aktion auf Ihrer Site ausführt.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
