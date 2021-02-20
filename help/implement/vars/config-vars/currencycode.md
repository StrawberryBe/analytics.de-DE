---
title: currencyCode
desciption: For eCommerce sites, set the currency the page deals in.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 100%

---


# currencyCode

Bei Websites, die Commerce verwenden, sind Umsatz und Währung ein wichtiger Bestandteil von Analytics. Viele Websites, insbesondere solche, die sich über mehrere Länder erstrecken, verwenden verschiedene Währungen. Verwenden Sie die `currencyCode`-Variable, um sicherzustellen, dass die Umsatzattribute der richtigen Währung entsprechen.

Wenn `currencyCode` nicht definiert ist, werden die für die [`products`](../page-vars/products.md)-Variablen und die Währungsereignisse definierten Geldwerte so behandelt, als ob sie mit der Währung der Report Suite identisch wären. Informationen zur Währung einer Report Suite finden Sie unter [Allgemeine Kontoeinstellungen](/help/admin/admin/general-acct-settings-admin.md) im Admin-Benutzerhandbuch.

Wenn `currencyCode` definiert ist und mit der Währung der Report Suite übereinstimmt, wird keine Währungsumrechnung angewendet.

Wenn `currencyCode` definiert ist und sich von der Währung der Report Suite unterscheidet, wendet Adobe eine Währungsumrechnung auf der Grundlage des aktuellen Tageswechselkurses an. Adobe arbeitet mit [XE](https://xe.com) zusammen, um täglich Währungen umzurechnen. Alle in Datenerfassungs-Servern gespeicherten Werte werden letztendlich in der Währung der Report Suite gespeichert.

>[!IMPORTANT]
>
>Wenn `currencyCode` einen ungültigen Wert enthält, wird der gesamte Treffer verworfen, was zu Datenverlust führt. Stellen Sie sicher, dass diese Variable korrekt definiert ist, wenn Sie sie in Ihrer Implementierung verwenden.

Diese Variable bleibt nicht zwischen Treffern bestehen. Stellen Sie sicher, dass diese Variable auf jeder Seite definiert ist, die Umsatz- oder Währungsereignisse enthält.

## Währungscode in Adobe Experience Platform Launch

Währungscode ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfigurierung der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Währungscode] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Währungscode verwenden. Wenn Sie einen benutzerdefinierten Währungscode verwenden, stellen Sie sicher, dass der Code gültig ist.

## Währungs-Code in Adobe Experience Platform Mobile SDK

Währungs-Code wird über Kontextdatenvariablen in der Adobe Analytics-Erweiterung an die Adobe Experience Platform Mobile SDKs übergeben.

1. Legen Sie den Währungs-Code in einer Kontextdatenvariablen während `trackState` oder `trackAction` fest.
2. Erstellen Sie eine Verarbeitungsregel für die Report Suite in der Adobe Analytics Admin Console. Legen Sie die Regel fest, um die Währungs-Code-Variable zu überschreiben.
3. Übergeben Sie den Währungs-Code an die `products`-Variable in Ihrem Aufruf an `trackState` oder `trackAction`.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Währungscode verwenden. Wenn Sie einen benutzerdefinierten Währungscode verwenden, stellen Sie sicher, dass der Code gültig ist.

## s.currencyCode in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.currencyCode`-Variable ist eine Zeichenfolge, die einen dreistelligen Code in Großbuchstaben enthält, der die Währung auf der Seite darstellt.

```js
s.currencyCode = "USD";
```

Die folgenden Währungscodes sind gültig:

| Währungscode | Währungsbeschreibung |
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
| `BYR` | Weißrussland Rubel |
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
| `DJF` | Dschibouti Franc |
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
| `IQD` | Iraq Dinar |
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
| `SRD` | Suriname Dollar |
| `SRG` | Suriname Gulden |
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
