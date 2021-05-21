---
title: Dynamische Variablen
description: Kopieren Sie Variablen, ohne die Bildanforderungslänge zu erhöhen.
exl-id: 41aab44d-01fd-45fe-892d-637d69488d98
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '359'
ht-degree: 100%

---

# Dynamische Variablen

Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die Bildanforderungslänge zu erhöhen. Sie sind hilfreich, wenn Sie dieselben Daten in mehreren Variablen erfassen.

In früheren Versionen von Analytics war die Länge der Bildanforderung wichtig, um abgeschnittene Daten zu verhindern. Verbesserungen an AppMeasurement ermöglichen wesentlich längere Abfragezeichenfolgen für Bildanforderungen, sodass dynamische Variablen normalerweise nicht benötigt werden.

Dynamische Variablen unterstützen Abfragezeichenfolgenparameter oder HTTP-Header in einer Bildanforderung. Eine vollständige Liste der verfügbaren Parameter, die referenziert werden können, finden Sie unter [Datenerfassungs-Abfrageparameter](../../validate/query-parameters.md). Eine vollständige Liste der verfügbaren HTTP-Anforderungsfelder, die referenziert werden können, finden Sie unter [Standardisierte Anfrage-Felder](https://de.wikipedia.org/wiki/Liste_der_HTTP-Headerfelder#Anfrage-Felder) in Wikipedia.

Wenn Adobe ein Präfix für dynamische Variablen erkennt, kopiert es automatisch die Abfragezeichenfolge oder den HTTP-Header-Wert in Ihre Report Suite. Diese Aktion erfolgt vor jeder anderen Verarbeitung, einschließlich Verarbeitungsregeln und VISTA-Regeln.

>[!TIP]
>
>Achten Sie beim Kopieren von Variablen auf maximale Zeichenbeschränkungen. Wenn Sie z. B. `eVar1` nach `prop1` kopieren, kann `prop1` einen abgeschnittenen Wert haben, da sie eine 100-Byte-Grenze hat (während `eVar1` eine 255-Byte-Grenze hat).

## Dynamische Variablen in Adobe Experience Platform Launch

Sie können dynamische Variablen in jedem Dimensionsfeld verwenden, das eine Zeichenfolge akzeptiert. Dimensionselemente werden normalerweise beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festgelegt.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie das gewünschte Dimensionselement.

Platzieren Sie das Präfix der dynamischen Variablen in das Textfeld, gefolgt vom Abfragezeichenfolgenparameter oder dem HTTP-Header, auf den Sie verweisen möchten. Standardmäßig ist das dynamische Variablenpräfix `D=`.

## Dynamische Variablen in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

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
