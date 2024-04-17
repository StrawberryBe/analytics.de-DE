---
title: Senden von Daten an Adobe Analytics mithilfe der Web SDK-JavaScript-Bibliothek
description: Beginnen Sie mit einer sauberen Web SDK-Implementierung, um mithilfe der JavaScript-Bibliothek Daten an Adobe Analytics zu senden.
hide: true
hidefromtoc: true
source-git-commit: d4c9bddf18311e13d025ed9d62c0636a33eb7b85
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Senden von Daten an Adobe Analytics mithilfe der Web SDK-JavaScript-Bibliothek

Dieser Implementierungspfad umfasst eine neue Web SDK-Installation unter Verwendung der Web SDK JavaScript-Bibliothek. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md): Eine neue Web SDK-Installation mit der Web SDK-Tag-Erweiterung. Ähnlich wie der JavaScript-Bibliotheksansatz des Web SDK (diese Seite), mit dem Unterschied, dass Sie die Implementierung mit Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.
* [Analytics-Erweiterung auf Web SDK-Erweiterung](analytics-extension-to-web-sdk.md): Verwenden Sie einen reibungslosen und methodischen Ansatz, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Dieser Ansatz unterdrückt die Notwendigkeit, XDM zu verwenden, bis Ihr Unternehmen für die Verwendung von Adobe Experience Platform-Diensten wie Customer Journey Analytics bereit ist. Verwenden Sie die `data` -Objekt anstelle des `xdm` -Objekt zum Senden von Daten an Adobe.
* [AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md): Ein reibungsloser und methodischer Ansatz für die Migration zum Web SDK, mit der Ausnahme, dass keine Tags verwendet werden. Stattdessen können Sie die Adobe Analytics-Datenerfassungsbibliothek (`AppMeasurement.js`) und ersetzen Sie sie durch die JavaScript-Bibliothek des Web SDK (`alloy.js`).

## Vorteile und Nachteile dieses Implementierungspfads

Die Verwendung der JavaScript-Bibliothek des Web SDK zum Senden von Daten an Adobe Analytics hat sowohl Vor- als auch Nachteile. Legen Sie bei jeder Option sorgfältig ab, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Direkter Ansatz**: Dieser Implementierungspfad ist einfacher als Ansätze, die vorhandene Adobe Analytics-Implementierungen verschieben. Wenn Sie keine aktuelle Adobe Analytics-Implementierung haben, um die Sie sich Sorgen machen müssen, füllen Sie die entsprechenden Web SDK-XDM-Felder aus.</li><li>**Vordefiniertes Schema**: Wenn Ihr Unternehmen kein eigenes Schema benötigt, können Sie einfach das für Adobe Analytics geeignete Schema verwenden. Dieses Konzept gilt auch bei der Umstellung auf Customer Journey Analytics. Das Konzept der Props und eVars gilt nicht für Customer Journey Analytics, Sie können aber Props und eVars weiterhin als einfache benutzerdefinierte Dimensionen verwenden.</li></ul> | <ul><li>**Implementierungsänderungen erfordern eine Intervention von Entwicklern**: Wenn Sie Änderungen an Ihrer Web SDK-Implementierung vornehmen möchten, müssen Sie sich an Ihr Entwicklungsteam wenden, um den Code auf Ihrer Site zu bearbeiten. Der Ansatz, der die [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md) vermeidet diesen Nachteil.</li><li>**Verwendung eines bestimmten Schemas blockiert**: Wenn Ihr Unternehmen zu Customer Journey Analytics wechselt, müssen Sie das Adobe Analytics-Schema weiterhin verwenden oder zum Schema Ihres eigenen Unternehmens migrieren (bei dem es sich um einen separaten Datensatz handelt). Wenn Ihr Unternehmen beim Wechsel zu Customer Journey Analytics sowohl das Adobe Analytics-Schema als auch die Migration zu einem separaten Datensatz vermeiden möchte, empfiehlt Adobe eine der beiden folgenden Methoden:</li><ul><li>Verwenden Sie die `data` -Objekt: Die `data` -Objekt können Sie Daten an Adobe Analytics senden, ohne ein XDM-Schema zu erfüllen. Nachdem das Schema Ihres Unternehmens erstellt wurde, können Sie die Zuordnung mithilfe der Datastream-Zuordnung vornehmen `data` -Objektfelder in XDM. Beide [Analytics-Erweiterung auf Web SDK-Erweiterung](analytics-extension-to-web-sdk.md) und [AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md) Verwenden Sie diese `data` -Objekt.</li><li>Adobe Analytics vollständig überspringen: Wenn Sie das Web SDK implementieren, können Sie diese Daten zur Verwendung in Customer Journey Analytics an einen Datensatz in Adobe Experience Platform senden. Sie können ein beliebiges Schema verwenden. Adobe Analytics ist an diesem Workflow überhaupt nicht beteiligt und benötigt daher keine Adobe Analytics ExperienceEvent-Feldergruppe. Bei dieser Methode entsteht der geringste technische Schuldenstand, aber auch Adobe Analytics wird vollständig ausgeschlossen.</li></ul></ul> |
