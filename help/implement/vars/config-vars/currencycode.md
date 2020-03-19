---
title: currencyCode
desciption: For eCommerce sites, set the currency the page deals in.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# currencyCode

Bei Sites, die Commerce verwenden, sind Umsatz und Währung ein wichtiger Bestandteil von Analytics. Viele Websites, insbesondere solche, die sich über mehrere Länder erstrecken, verwenden verschiedene Währungen. Verwenden Sie die `currencyCode` Variable, um sicherzustellen, dass die Umsatzattribute der richtigen Währung entsprechen.

Wenn `currencyCode` nicht definiert ist, werden die Währungswerte, die die Variablen- und [`products`](../page-vars/products.md) Währungswerte definieren, so behandelt, als wären sie mit der Währung der Report Suite identisch. Siehe [Allgemeine Kontoeinstellungen](/help/admin/admin/general-acct-settings-admin.md) im Admin-Benutzerhandbuch, um die Währung der Report Suite anzuzeigen.

Wenn definiert `currencyCode` ist und mit der Währung der Report Suite übereinstimmt, wird keine Währungsumrechnung angewendet.

Wenn definiert `currencyCode` ist und sich von der Währung der Report Suite unterscheidet, wendet Adobe eine Währungsumrechnung auf der Grundlage des aktuellen Tageswechselkurses an. Adobe arbeitet mit [XE](https://xe.com) zusammen, um täglich Währungen umzurechnen. Alle in Datenerfassungsservern gespeicherten Werte werden letztendlich in der Währung der Report Suite gespeichert.

> [!IMPORTANT] Wenn ein ungültiger Wert `currencyCode` enthalten ist, wird der gesamte Treffer verworfen und führt zu Datenverlust. Stellen Sie sicher, dass diese Variable korrekt definiert ist, wenn Sie sie in Ihrer Implementierung verwenden.

Diese Variable bleibt nicht zwischen Treffern bestehen. Vergewissern Sie sich, dass diese Variable auf jeder Seite definiert ist, die Umsatz- oder Währungs-Ereignis enthält.

## Währungscode beim Start der Adobe Experience Platform

Währungscode ist ein Feld unter dem [!UICONTROL General] Akkordeon, wenn die Adobe Analytics-Erweiterung konfiguriert wird.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL General] Akkordeon, das das [!UICONTROL Currency Code] Feld aufdeckt.

Sie können entweder einen voreingestellten Währungscode oder einen benutzerdefinierten Währungscode verwenden. Wenn Sie einen benutzerdefinierten Währungscode verwenden, stellen Sie sicher, dass der Code gültig ist.

## s.currencyCode in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.currencyCode` Variable ist eine Zeichenfolge mit einem aus 3 Buchstaben bestehenden Großbuchstabencode, der die Währung auf der Seite darstellt.

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
| `ANG` | Niederlande Atilles Gulden |
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
| `NIO` | Nicaragua-Gold-Cordoba |
| `NOK` | Norwegen Krone |
| `NPR` | Nepal Rupie |
| `NZD` | Neuseeland Dollar |
| `OMR` | Oman Rial |
| `PAB` | Panama Balboa |
| `PEN` | Peru Nuevo Sol |
| `PGK` | Papua Neuguinea Kina |
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
| `STD` | Sao-Tome und Principe-Dobras |
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
| `XDR` | Sonderziehungsrecht des Internationalen Währungsfonds |
| `XOF` | Communauté Financière Africaine Francs B |
| `XPD` | Palladiumunzen |
| `XPF` | Comptoirs Français du Pacifique Francs |
| `XPT` | Platinunzen |
| `YER` | Yemen Rial |
| `ZAR` | Südafrika Rand |
| `ZMK` | Sambia Kwacha |
| `ZWD` | Simbabwe-Dollar |
