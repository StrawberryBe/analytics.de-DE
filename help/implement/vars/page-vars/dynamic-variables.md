---
title: Dynamische Variablen
description: Kopieren Sie Variablen, ohne die Bildanforderungslänge zu erhöhen.
feature: Variables
exl-id: 41aab44d-01fd-45fe-892d-637d69488d98
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 77%

---

# Dynamische Variablen

Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die Bildanforderungslänge zu erhöhen. Sie sind hilfreich, wenn Sie dieselben Daten in mehreren Variablen erfassen.

In früheren Versionen von Analytics war die Länge der Bildanforderung wichtig, um abgeschnittene Daten zu verhindern. Verbesserungen an AppMeasurement ermöglichen wesentlich längere Abfragezeichenfolgen für Bildanforderungen, sodass dynamische Variablen normalerweise nicht benötigt werden.

Dynamische Variablen unterstützen Abfragezeichenfolgenparameter oder HTTP-Header in einer Bildanforderung. Eine vollständige Liste der verfügbaren Parameter, die referenziert werden können, finden Sie unter [Datenerfassungs-Abfrageparameter](../../validate/query-parameters.md). Eine vollständige Liste der verfügbaren HTTP-Anforderungsfelder, die referenziert werden können, finden Sie unter [Standardisierte Anfrage-Felder](https://de.wikipedia.org/wiki/Liste_der_HTTP-Headerfelder) in Wikipedia.

Wenn Adobe ein Präfix für dynamische Variablen erkennt, kopiert es automatisch die Abfragezeichenfolge oder den HTTP-Header-Wert in Ihre Report Suite. Diese Aktion erfolgt vor jeder anderen Verarbeitung, einschließlich Verarbeitungsregeln und VISTA-Regeln.

>[!TIP]
>
>Achten Sie beim Kopieren von Variablen auf maximale Zeichenbeschränkungen. Wenn Sie z. B. `eVar1` nach `prop1` kopieren, kann `prop1` einen abgeschnittenen Wert haben, da sie eine 100-Byte-Grenze hat (während `eVar1` eine 255-Byte-Grenze hat).

## Dynamische Variablen mit dem Web SDK

Verwenden Sie die Datastream-Zuordnung, um Daten von einem einzelnen XDM-Feld an mehrere Analytics-Variablen zu senden.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken **[!UICONTROL Datenspeicher]** in der linken Leiste.
1. Klicken Sie auf den gewünschten Datastream.
1. Klicken **[!UICONTROL Zuordnung bearbeiten]** rechts.
1. Ordnen Sie die gewünschte [!UICONTROL Quellfeld] auf die gewünschte [!UICONTROL Zielfeld]. Ein einzelnes Quellfeld kann einer beliebigen Anzahl von Zielfeldern zugeordnet werden.

## Dynamische Variablen mit der Adobe Analytics-Erweiterung

Sie können dynamische Variablen in jedem Dimensionsfeld verwenden, das eine Zeichenfolge akzeptiert. Dimensionselemente werden normalerweise beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festgelegt.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie das gewünschte Dimensionselement.

Platzieren Sie das Präfix der dynamischen Variablen in das Textfeld, gefolgt vom Abfragezeichenfolgenparameter oder dem HTTP-Header, auf den Sie verweisen möchten. Standardmäßig ist das dynamische Variablenpräfix `D=`.

## Dynamische Variablen in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Dynamische Variablen sind Textzeichenfolgen, die anderen Variablen zugewiesen werden. Standardmäßig ist das dynamische Variablenpräfix `D=`. Bei dynamischen Variablen wird zwischen Groß- und Kleinschreibung unterschieden.

```js
// Copy eVar1 into eVar2. The query string parameter of eVar1 is v1.
s.eVar1 = "Example value";
s.eVar2 = "D=v1";

// Take the user agent string found in the image request HTTP header and place it in eVar1.
s.eVar1 = "D=User-Agent";

// Copy the page URL and place it in eVar1. The query string parameter of page URL is g.
s.eVar1 = "D=g";
```

>[!NOTE]
>
>Dynamische Variablen werden beim Debugging Ihrer Implementierung als Zeichenfolgen angezeigt. Die Werte werden Server-seitig von Adobe-Datenerfassungs-Servern kopiert.
