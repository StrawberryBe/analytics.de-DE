---
title: Was ist die Variable „currencyCode“ und wie verwende ich sie?
description: Legt für E-Commerce-Websites die Währung fest, die auf der jeweiligen Seite verwendet wird.
feature: Variables
exl-id: 3332c366-c472-4778-96c8-ef0aa756cca8
source-git-commit: 84a4d38a65769f028bac4aa5817cb4002c4b1f97
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 100%

---

# currencyCode

Bei Websites, die Commerce verwenden, sind Umsatz und Währung ein wichtiger Bestandteil von Analytics. Viele Websites, insbesondere solche, die sich über mehrere Länder erstrecken, verwenden verschiedene Währungen. Verwenden Sie die Variable `currencyCode`, um sicherzustellen, dass der Umsatz der richtigen Währung entspricht.

Die Währungsumrechnung verwendet bei jedem Treffer die folgende Logik. Diese Schritte gelten für Umsatzwerte, die die Variable [`products`](../page-vars/products.md) und alle als „Währung“ aufgelisteten Ereignisse in [Erfolgsereignissen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) in den Report Suite-Einstellungen festlegen.

* Wenn `currencyCode` nicht definiert ist, geht Adobe davon aus, dass alle Währungswerte der Report Suite-Währung entsprechen. Siehe [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in den Report Suite-Einstellungen, um die Report Suite-Währung anzuzeigen.
* Wenn `currencyCode` definiert ist und mit der Währung der Report Suite übereinstimmt, wird keine Währungsumrechnung angewendet.
* Wenn `currencyCode` definiert ist und sich von der Währung der Report Suite unterscheidet, wendet Adobe eine Währungsumrechnung auf der Grundlage des aktuellen Tageswechselkurses an. Adobe arbeitet mit [XE](https://xe.com) zusammen, um täglich Währungen umzurechnen. Alle in der Report Suite gespeicherten Werte beziehen sich auf die Report Suite-Währung.
* Wenn für `currencyCode` ein ungültiger Wert festgelegt ist, **wird der gesamte Treffer verworfen, was zu Datenverlust führt.** Stellen Sie sicher, dass diese Variable bei jeder Verwendung korrekt definiert ist.

Diese Variable bleibt nicht trefferübergreifend bestehen. Stellen Sie sicher, dass diese Variable auf jeder Seite definiert ist, die Umsatz- oder Währungsereignisse enthält, die nicht mit der Report Suite-Standardwährung übereinstimmen.

>[!NOTE]
>
>Während sich Währungs-Codes zwischen Seiten ändern können, müssen alle Währungsmetriken eines einzelnen Treffers dieselbe Währung verwenden.

Ein Punkt **muss** als Währungstrennzeichen für alle Währungen bei der Implementierung dieser Variablen verwendet werden. Beispielsweise muss die Schwedische Krone, die normalerweise ein Kommatrennzeichen aufweist, so geändert werden, dass sie einen Punkt in der `products`-Variable und allen Währungsereignissen verwendet. Adobe zeigt das richtige Währungstrennzeichen in Berichten an.

## Währungs-Code bei Verwendung des Web SDK

Der Währungs-Code ist [für Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) unter dem XDM-Feld `commerce.order.currencyCode` zugeordnet.

## Währung-Code bei Verwendung der Adobe Analytics-Erweiterung

Der Währungs-Code ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfigurierung der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Währungscode] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Währungscode verwenden. Wenn Sie einen benutzerdefinierten Währungscode verwenden, stellen Sie sicher, dass der Code gültig ist.

## Währungs-Code in Adobe Experience Platform Mobile SDK

Währungs-Code wird über Kontextdatenvariablen in der Adobe Analytics-Erweiterung an die Adobe Experience Platform Mobile SDKs übergeben.

1. Legen Sie den Währungs-Code in einer Kontextdatenvariablen während `trackState` oder `trackAction` fest.
1. Erstellen Sie eine Verarbeitungsregel für die Report Suite in der Adobe Analytics Admin Console. Legen Sie die Regel fest, um die Währungs-Code-Variable zu überschreiben.
1. Übergeben Sie den Währungs-Code an die `products`-Variable in Ihrem Aufruf an `trackState` oder `trackAction`.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Währungscode verwenden. Wenn Sie einen benutzerdefinierten Währungscode verwenden, stellen Sie sicher, dass der Code gültig ist.

## s.currencyCode in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `s.currencyCode` ist eine Zeichenfolge, die einen dreistelligen Code in Großbuchstaben enthält, der die Währung auf der Seite darstellt. Bei Werten wird zwischen Groß- und Kleinschreibung unterschieden.

```js
s.currencyCode = "USD";
```

Die folgenden Währungscodes sind gültig:

| Währungscode | Beschriftung |
| --- | --- |
| `AED` | Vereinigte Arabische Emirate Dirham |
| `AFA` | Afghanistan Afghani |
| `ALL` | Albanien Lek |
| `AMD` | Armenien Dram |
| `ANG` | Niederländische Antillen Gulden |
| `AOA` | Angola Kwanza |
| `ARS` | Argentinien Peso |
| `AUD` | Australien Dollar |
| `AWG` | Aruba Gulden |
| `AZM` | Aserbeidschan Manat |
| `BAM` | Bosnien-Herzegowina Konvertible Mark |
| `BBD` | Barbados Dollar |
| `BDT` | Bangladesch Taka |
| `BGN` | Bulgarien Lew |
| `BHD` | Bahrein Dinar |
| `BIF` | Burundi Franc |
| `BMD` | Bermuda Dollar |
| `BND` | Brunei Dollar |
| `BOB` | Bolivien Boliviano |
| `BRL` | Brasilien Real |
| `BSD` | Bahamas Dollar |
| `BTN` | Bhutan Ngultrum |
| `BWP` | Botswana Pula |
| `BYR` | Belarus Rubel |
| `BZD` | Belize Dollar |
| `CAD` | Kanada Dollar |
| `CDF` | Kongo/Kinshasa Franc |
| `CHF` | Schweiz Franken |
| `CLP` | Chile Peso |
| `CNY` | China Yuan Renminbi |
| `COP` | Kolumbien Peso |
| `CRC` | Costa-Rica Colon |
| `CSD` | Serbien Dinar |
| `CUP` | Kuba Peso |
| `CVE` | Kap Verde Escudo |
| `CYP` | Zypern Pfund |
| `CZK` | Tschechische Republik Krone |
| `DJF` | Dschibuti Franc |
| `DKK` | Dänemark Krone |
| `DOP` | Dominikanische Republik Peso |
| `DZD` | Algerien Dinar |
| `EEK` | Estland Krone |
| `EGP` | Ägypten Pfund |
| `ERN` | Eritrea Nakfa |
| `ETB` | Äthiopien Birr |
| `EUR` | Euro |
| `FJD` | Fidschi Dollar |
| `FKP` | Falkland-Inseln Pfund |
| `GBP` | Vereinigtes Königreich Pfund |
| `GEL` | Georgien Lari |
| `GGP` | Guernsey Pfund |
| `GHC` | Ghana Cedi |
| `GIP` | Gibraltar Pfund |
| `GMD` | Gambia Dalasi |
| `GNF` | Guinea Franc |
| `GTQ` | Guatemala Quetzal |
| `GYD` | Guyana Dollar |
| `HKD` | Hongkong Dollar |
| `HNL` | Honduras Lempira |
| `HRK` | Kroatien Kuna |
| `HTG` | Haiti Gourde |
| `HUF` | Ungarn Forint |
| `IDR` | Indonesien Rupiah |
| `ILS` | Israel Neuer Schekel |
| `IMP` | Isle of Man Pfund |
| `INR` | Indien Rupie |
| `IQD` | Irak Dinar |
| `IRR` | Iran Rial |
| `ISK` | Island Krone |
| `JEP` | Jersey Pfund |
| `JMD` | Jamaika Dollar |
| `JOD` | Jordanien Dinar |
| `JPY` | Japan Yen |
| `KES` | Kenia Schilling |
| `KGS` | Kirgisistan Som |
| `KHR` | Kambodscha Riel |
| `KMF` | Komoren Franc |
| `KPW` | Nordkorea Won |
| `KRW` | Südkorea Won |
| `KWD` | Kuwait Dinar |
| `KYD` | Cayman-Inseln Dollar |
| `KZT` | Kasachstan Tenge |
| `LAK` | Laos Kip |
| `LBP` | Libanon Pfund |
| `LKR` | Sri Lanka Rupie |
| `LRD` | Liberia Dollar |
| `LSL` | Lesotho Loti |
| `LTL` | Litauen Litas |
| `LVL` | Lettland Lats |
| `LYD` | Libyen Dinar |
| `MAD` | Marokko Dirham |
| `MDL` | Moldawien Leu |
| `MGA` | Madagaskar Ariary |
| `MKD` | Mazedonien Denar |
| `MMK` | Myanmar Kyat |
| `MNT` | Mongolei Tugrik |
| `MOP` | Macau Pataca |
| `MRO` | Mauretanien Ouguiya |
| `MTL` | Malta Lira |
| `MUR` | Mauritius Rupie |
| `MVR` | Malediven Rufiyaa |
| `MWK` | Malawi Kwacha |
| `MXN` | Mexiko Peso |
| `MYR` | Malaysia Ringgit |
| `MZM` | Mosambik Metical |
| `NAD` | Namibia Dollar |
| `NGN` | Nigeria Naira |
| `NIO` | Nicaragua Gold Cordoba |
| `NOK` | Norwegen Krone |
| `NPR` | Nepal Rupie |
| `NZD` | Neuseeland Dollar |
| `OMR` | Oman Rial |
| `PAB` | Panama Balboa |
| `PEN` | Peru Nuevo Sol |
| `PGK` | Papua-Neuguinea Kina |
| `PHP` | Philippinen Peso |
| `PKR` | Pakistan Rupie |
| `PLN` | Polen Zloty |
| `PYG` | Paraguay Guarani |
| `QAR` | Katar Riyal |
| `ROL` | Rumänien Leu |
| `RUR` | Russland Rubel |
| `RWF` | Ruanda Franc |
| `SAR` | Saudi-Arabien Riyal |
| `SBD` | Solomon-Inseln Dollar |
| `SCR` | Seychellen Rupie |
| `SDD` | Sudan Dinar |
| `SEK` | Schweden Krone |
| `SGD` | Singapur Dollar |
| `SHP` | St. Helena Pfund |
| `SIT` | Slowenien Tolar |
| `SKK` | Slowakei Krone |
| `SLL` | Sierra Leone Leone |
| `SOS` | Somalia Schilling |
| `SPL` | Seborga Luigino |
| `SRD` | Surinam Dollar |
| `SRG` | Surinam Gulden |
| `STD` | São Tomé und Príncipe |
| `SVC` | El Salvador Colon |
| `SYP` | Syrien Pfund |
| `SZL` | Swasiland Lilangeni |
| `THB` | Thailand Baht |
| `TJS` | Tadschikistan Somoni |
| `TMM` | Turkmenistan Manat |
| `TND` | Tunesien Dinar |
| `TOP` | Tonga Pa&#39;anga |
| `TRL` | Türkei Lira |
| `TTD` | Trinidad und Tobago Dollar |
| `TVD` | Tuvalu Dollar |
| `TWD` | Taiwan Neuer Dollar |
| `TZS` | Tansania Schilling |
| `UAH` | Ukrainische Hrywnia |
| `UGX` | Uganda Schilling |
| `USD` | US-Dollar |
| `UYU` | Uruguay Peso |
| `UZS` | Usbekistan Sum |
| `VEB` | Venezuela Bolivar |
| `VND` | Vietnam Dong |
| `VUV` | Vanuatu Vatu |
| `WST` | Samoa Tala |
| `XAF` | Communauté Financière Africaine Francs B |
| `XAG` | Silberunzen |
| `XAU` | Goldunzen |
| `XCD` | Ost-Karibik Dollar |
| `XDR` | Sonderziehung Internationaler Währungsfonds |
| `XOF` | Communauté Financière Africaine Francs B |
| `XPD` | Palladiumunzen |
| `XPF` | Comptoirs Français du Pacifique Francs |
| `XPT` | Platinunzen |
| `YER` | Yemen Rial |
| `ZAR` | Südafrika Rand |
| `ZMK` | Sambia Kwacha |
| `ZWD` | Simbabwe Dollar |
