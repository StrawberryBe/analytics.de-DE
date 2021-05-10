---
description: Beschreibt, wie Sie Zielwährungs-Codes definieren, damit die Unterstützung mehrerer Währungen funktioniert.
title: Unterstützung mehrerer Währungen
uuid: null
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
translation-type: tm+mt
source-git-commit: f3eb3c024a80d0b65729929960173f8b3a4267b0
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 100%

---

# Unterstützung mehrerer Währungen

In diesem Dokument wird beschrieben, wie Sie Zielwährungs-Codes für die Unterstützung mehrerer Währungen definieren.

Zielwährungs-Codes werden auf drei Ebenen definiert:

## Seitenebene

Sie können eine JavaScript-Variable für die Zielwährung auf Seitenebene festlegen. Der Site-Eigentümer legt diese Variable mit dem entsprechenden dreistelligen ISO-4217-Währungs-Code fest (wie unten in diesem Dokument aufgeführt). Wenn die Variable [currencyCode](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/config-vars/currencycode.html) nicht auf dieser Ebene eingestellt ist, ist die Standardwährung die in der Report Suite angegebene Währung. Wenn die Variable auf Seitenebene mit der in der Report Suite angegebenen Variablen in Konflikt steht, hat die Variable in der Report Suite Vorrang.


## Report Suite-Ebene

Die **Basiswährung** wird beim [Erstellen von Report Suites](https://docs.adobe.com/content/help/de-DE/analytics/admin/manage-report-suites/new-report-suite/new-report-suite.html) angegeben. Dies ist die Standardeinstellung für die Währung und hat Vorrang vor Währungs-Codes, die auf Seitenebene festgelegt werden. Wenn also eine Report Suite Bestellungen in US-Dollar, Euro und Britischen Pfund akzeptiert und der standardmäßige Währungs-Code der Report Suite auf „US-Dollar“ gesetzt ist, übersetzt die Datenbank am Reporting-Backend alle Transaktionen in US-Dollar.

Marketing-Berichte verwenden zum Übersetzen der Seitenwährungswerte in die Standardwährungswerte der Report Suite den Wechselkurs, der zum Zeitpunkt der letzten Bildanforderung gültig ist. Report Suites verwenden „US-Dollar“ als Standardwährung.


## Berichtsebene

Anwender können die Standardberichtswährung für eine Anmeldesitzung festlegen. Dies ist über den Link **„Anzeigeoptionen“** in einem beliebigen Umrechnungsbericht möglich. Marketing-Berichte verwenden zum Übersetzen von Report Suite-Währungswerten in berichtsspezifische Währungswerte den Wechselkurs, der zum Zeitpunkt der Berichtsausführung gültig ist.

## Unterstützte Währungs-Codes (ISO 4217)

Analytics unterstützt derzeit die folgenden Währungsformate für Umrechnungstransaktionen:


„AFA“ Afghanistan, Afghani (AFA)

„AFN“ Afghanistan, Afghani (AFN)

„ALL“ Albanien, Lek (ALL)

„DZD“ Algerien, Dinar (DZD)

„AOA“ Angola, Kwanza (AOA)

„ARS“ Argentinien, Peso (ARS)

„AMD“ Armenien, Dram (AMD)

„AWG“ Aruba, Gulden (AWG)

„AUD“ Australien, Dollar (AUD)

„AZM“ Aserbaidschan, Manat (AZM)

„AZN“ Aserbaidschan, Neuer Manat (AZN)

„BSD“ Bahamas, Dollar (BSD)

„BHD“ Bahrain, Dinar (BHD)

„BDT“ Bangladesh, Taka (BDT)

„BBD“ Barbados, Dollar (BBD)

„BYR“ Belarus, Rubel (BYR)

„BZD“ Belize, Dollar (BZD)

„BMD“ Bermudas, Dollar (BMD)

„BTN“ Bhutan, Ngultrum (BTN)

„BOB“ Bolivien, Boliviano (BOB)

„BAM“ Bosnien-Herzegowina, Konvertible Marka (BAM)

„BWP“ Botswana, Pula (BWP)

„BRL“ Brasilien, Real (BRL)

„BND“ Brunei, Dollar (BND)

„BGN“ Bulgarien, Leva (BGN)

„BIF“ Burundi, Franc (BIF)

„KHR“ Kambodscha, Riel (KHR)

„CAD“ Kanada, Dollar (CAD)

„CVE“ Kap Verde, Escudo (CVE)

„KYD“ Kaimaninseln, Dollar (KYD)

„CLP“ Chile, Peso (CLP)

„CNY“ China, Yuan&#39;Renminbi (CNY)

„COP“ Kolumbien, Peso (COP)

„XOF“ Communauté Financière Africaine, Franc BCEAO (XOF)

„XAF“ Communauté Financière Africaine, Franc BEAC (XAF)

„KMF“ Komoren, Franc (KMF)

„XPF“ CFP, Franc (XPF)

„CDF“ Kongo, Franc (CDF)

„CRC“ Costa-Rica, Colón (CRC)

„HRK“ Kroatien, Kuna (HRK)

„CUC“ Kuba, Convertible Peso (CUC)

„CUP“ Kuba, Peso (CUP)

„CYP“ Zypern, Pfund (CYP)

„CZK“ Tschechien, Krone (CZK)

„DKK“ Dänemark, Krone (DKK)

„DJF“ Dschibuti, Franc (DJF)

„DOP“ Dominikanische Republik, Peso (DOP)

„XCD“ Ostkaribischer Dollar (XCD)

„EGP“ Ägypten, Pfund (EGP)

„SVC“ El Salvador, Colón (SVC)

„ERN“ Eritrea, Nakfa (ERN)

„XBT“ ERR (XBT)

„EEK“ Estland, Krone (EEK)

„ETB“ Äthiopien, Birr (ETB)

„EUR“ Euro (EUR)

„FKP“ Falkland-Inseln, Pfund (FKP)

„FJD“ Fidschi, Dollar (FJD)

„GMD“ Gambia, Dalasi (GMD)

„GEL“ Georgien, Lari (GEL)

„GHC“ Ghana, Cedi (GHC)

„GHS“ Ghana, Cedi (GHS)

„GIP“ Gibraltar, Pfund (GIP)

„XAU“ Goldunzen (XAU)

„GTQ“ Guatemala, Quetzal (GTQ)

„GGP“ Guernsey, Pfund (GGP)

„GNF“ Guinea, Franc (GNF)

„GYD“ Guyana, Dollar (GYD)

„HTG“ Haiti, Gourde (HTG)

„HNL“ Honduras, Lempira (HNL)

„HKD“ Hongkong, Dollar (HKD)

„HUF“ Ungarn, Forint (HUF)

„ISK“ Island, Krone (ISK)

„INR“ Indien, Rupie (INR)

„IDR“ Indonesien, Rupiah (IDR)

„XDR“ Sonderziehungsrechte des Internationalen Währungsfonds (XDR)

„IRR“ Iran, Rial (IRR)

„IQD“ Irak, Dinar (IQD)

„IMP“ Isle of Man, Pfund (IMP)

„ILS“ Israel, Neuer Schekel (ILS)

„JMD“ Jamaika, Dollar (JMD)

„JPY“ Japan, Yen (JPY)

„JEP“ Jersey, Pfund (JEP)

„JOD“ Jordan, Dinar (JOD)

„KZT“ Kasachstan, Tenge (KZT)

„KES“ Kenia, Schilling (KES)

„KWD“ Kuwait, Dinar (KWD)

„KGS“ Kirgisistan, Som (KGS)

„LAK“ Laos, Kip (LAK)

„LVL“ Lettland, Lati (LVL)

„LBP“ Libanon, Pfund (LBP)

„LSL“ Lesotho, Maloti (LSL)

„LRD“ Liberia, Dollar (LRD)

„LYD“ Libyen, Dinar (LYD)

„LTL“ Litauen, Litai (LTL)

„MOP“ Macau, Pataca (MOP)

„MKD“ Mazedonien, Denar (MKD)

„MGA“ Madagaskar, Ariary (MGA)

„MWK“ Malawi, Kwacha (MWK)

„MYR“ Malaysia, Ringgit (MYR)

„MVR“ Malediven, Rufiyaa (MVR)

„MTL“ Malta, Liri (MTL)

„MRO“ Mauretanien, Ouguiya (MRO)

„MUR“ Mauritius, Rupie (MUR)

„MXN“ Mexiko, Peso (MXN)

„MDL“ Moldawien, Lei (MDL)

„MNT“ Mongolei, Tugrik (MNT)

„MAD“ Marokko, Dirham (MAD)

„MZN“ Mosambik, Meticai (MZN)

„MZM“ Mosambik, Meticai (MZM)

„MMK“ Myanmar, Kyat (MMK)

„NAD“ Namibia, Dollar (NAD)

„NPR“ Nepal, Rupie (NPR)

„ANG“ Antillen, Gulden (ANG)

„NZD“ Neuseeland, Dollar (NZD)

„NIO“ Nicaragua, Cordoba (NIO)

„NGN“ Nigeria, Naira (NGN)

„KPW“ Nordkorea, Won (KPW)

„NOK“ Norwegen, Krone (NOK)

„OMR“ Oman, Rial (OMR)

„PKR“ Pakistan, Rupie (PKR)

„XPD“ Palladiumunzen (XPD)

„PAB“ Panama, Balboa (PAB)

„PGK“ Papua-Neuguinea, Kina (PGK)

„PYG“ Paraguay, Guarani (PYG)

„PEN“ Peru, Sol (PEN)

„PHP“ Philippinen, Peso (PHP)

„XPT“ Platinunzen (XPT)

„PLN“ Polen, Zloty (PLN)

„QAR“ Katar, Riyal (QAR)

„ROL“ Rumänien, Lei (ROL)

„RON“ Rumänien, Neuer Lei (RON)

„RUB“ Russland, Rubel (RUB)

„RUR“ Russland, Rubel (RUR)

„RWF“ Ruanda, Franc (RWF)

„SHP“ St. Helena, Pfund (SHP)

„WST“ Samoa, Tala (WST)

„STD“ São Tomé und Príncipe, Dobra (STD)

„SAR“ Saudi-Arabien, Riyal (SAR)

„SPL“ Seborga, Luigini (SPL)

„RSD“ Serbien, Dinar (RSD)

„CSD“ Serbien, Dinar (CSD)

„SCR“ Seychellen, Rupie (SCR)

„SLL“ Sierra-Leone, Leone (SLL)

„XAG“ Silberunzen (XAG)

„SGD“ Singapur, Dollar (SGD)

„SKK“ Slowakei, Krone (SKK)

„SIT“ Slowenien, Tolar (SIT)

„SBD“ Salomonen, Dollar (SBD)

„SOS“ Somalia, Schilling (SOS)

„ZAR“ Südafrika, Rand (ZAR)

„KRW“ Südkorea, Won (KRW)

„LKR“ Sri Lanka, Rupie (LKR)

„SDD“ Sudan, Dinar (SDD)

„SDG“ Sudan, Pfund (SDG)

„SRD“ Suriname, Dollar (SRD)

„SRG“ Suriname, Gulden (SRG)

„SZL“ Swasiland, Emalangeni (SZL)

„SEK“ Schweden, Krone (SEK)

„CHF“ Schweiz, Franken (CHF)

„SYP“ Syrien, Pfund (SYP)

„TWD“ Taiwan, Neuer Dollar (TWD)

„TJS“ Tadschikistan, Somoni (TJS)

„TZS“ Tansania, Schilling (TZS)

„THB“ Thailand, Baht (THB)

„TOP“ Tonga, Pa&#39;anga (TOP)

„TTD“ Trinidad und Tobago, Dollar (TTD)

„TND“ Tunesien, Dinar (TND)

„TRY“ Türkei, Lira (TRY)

„TRL“ Türkei, Lira (TRL)

„TMM“ Turkmenistan, Manat (TMM)

„TMT“ Turkmenistan, Neuer Manat (TMT)

„TVD“ Tuvalu, Dollar (TVD)

„UGX“ Uganda, Schilling (UGX)

„UAH“ Ukraine, Hrywnja (UAH)

„AED“ Vereinigte Arabische Emirate, Dirham (AED)

„GBP“ Vereinigtes Königreich, Pfund (GBP)

„USD“ USA, Dollar (USD) – ausgewählt

„UYU“ Uruguay, Peso (UYU)

„UZS“ Usbekistan, Sum (UZS)

„VUV“ Vanuatu, Vatu (VUV)

„VEB“ Venezuela, Bolivar (VEB)

„VEF“ Venezuela, Bolivar Fuerte (VEF)

„VND“ Vietnam, Dong (VND)

„YER“ Jemen, Rial (YER)

„ZMK“ Sambia, Kwacha (ZMK)

„ZMW“ Sambia, Kwacha (ZMW)

„ZWD“ Simbabwe, Dollar (ZWD)


## AppMeasurement.js-Beispiel

Die `currencyCode`-Variable kann global in der Datei „AppMeasurement.js“ definiert werden. Durch Definition der currencyCode-Variable in dieser Datei wird sichergestellt, dass alle Währungstransaktionen einen einheitlichen Währungs-Code verwenden. Im folgenden Beispiel wird Euro als `currencyCode`-Variable unter `CONFIG SECTION` der Datei „AppMeasurement.js“ angegeben. Alle Kaufereignisse werden durch die Meldung von Euro-Transaktionen interpretiert.

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
s.account="devnow"
s.currencyCode="EUR"
s.trackInlineStats=true 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
***
    
```

## Weitere Hinweise zur Implementierung

* Denken Sie daran, dass sich Währungs-Codes zwar von Seite zu Seite ändern können, aber alle für eine bestimmte Seitenanfrage definierten Umrechnungszeileneinträge dieselbe Währung verwenden müssen (beispielsweise können Euro, Britische Pfund und US-Dollar nicht für dieselbe Seitenansicht definiert werden). Wenn Sie keine Währungsumrechnung durchführen möchten, lassen Sie den Wert „currencyCode“ leer. Dadurch werden die gesendeten Werte ohne Umrechnung direkt an Berichte weitergeleitet.

* Wenn Sie einen ungültigen currencyCode festlegen (einen beliebigen Wert, der nicht in der Liste der unterstützten Währungs-Codes enthalten ist), wird der gesamte Treffer ausgeschlossen und die Daten für diese Transaktion werden nicht erfasst. Bevor Sie `currencyCode` in der Produktion festlegen, überprüfen Sie mit einer Report Suite, ob die Daten erfasst werden und die Währungsumrechnung richtig funktioniert.

* Währungen, in denen kein Punkt (.) als Trennzeichen verwendet wird, müssen geändert werden, sodass ein Punkt anstelle des typischen Trennzeichens verwendet wird. Beispielsweise müssen Schwedische Kronen, die ein Komma (,) verwenden, so geändert werden, dass sie stattdessen einen Punkt verwenden. Analytics verwendet das Komma zum Trennen von Werten – somit würden die Daten nicht richtig übergeben. Durch den Punkt werden Werte richtig an Berichte übergeben.
