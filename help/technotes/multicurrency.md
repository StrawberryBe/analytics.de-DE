---
description: Beschreibt, wie Sie Zielwährungscodes definieren, damit die Unterstützung mehrerer Währungen funktioniert.
title: Unterstützung mehrerer Währungen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 63a6ca92ae5fe103648c74bd16bcdf90858c71f3

---


# Unterstützung mehrerer Währungen

In diesem Dokument wird beschrieben, wie Sie Zielwährungscodes für die Unterstützung mehrerer Währungen definieren.

Zielwährungscodes werden auf drei Ebenen definiert:

## Seitenebene

Sie können eine JavaScript-Variable für die Zielwährung auf Seitenebene festlegen. Der Site-Eigentümer legt diese Variable mit dem entsprechenden dreistelligen ISO 4217-Währungscode (wie unten in diesem Dokument aufgeführt) fest. Wenn die Variable &quot; [currencyCode](https://docs.adobe.com/content/help/en/analytics/implementation/vars/config-vars/currencycode.html) &quot;nicht auf dieser Ebene eingestellt ist, ist die Standardwährung die in der Report Suite angegebene Währung. Wenn die Variable auf Seitenebene mit der in der Report Suite angegebenen Variablen in Konflikt steht, hat die Variable in der Report Suite Vorrang.


## Report Suite-Ebene

Die **Basiswährung** wird beim [Erstellen von Report Suites](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/new-report-suite/new-report-suite.html)angegeben. Dies ist die Standardeinstellung für Währung und hat Vorrang vor Währungscodes, die auf Seitenebene festgelegt werden. Wenn also eine Report Suite Bestellungen in US-Dollar, Euro und Britischen Pfund akzeptiert und die Report Suite einen Standardwährungscode auf &quot;US-Dollar&quot;gesetzt hat, übersetzt die Berichterstellungs-Back-End-Datenbank alle Transaktionen in US-Dollar.

Marketing-Berichte verwenden den Wechselkurs zum Zeitpunkt der Bildanforderung, um Währungswerte auf Seitenebene in die Standardwährungswerte der Report Suite zu übersetzen. Report Suites verwenden &quot;US-Dollar&quot;als Standardwährung.


## Berichtsebene

Benutzer können die Standardberichtswährung für die Benutzeranmeldesitzung festlegen. Dies ist über den Link **„Anzeigeoptionen“** in einem beliebigen Umrechnungsbericht möglich. Marketing-Berichte verwenden den Wechselkurs zum Zeitpunkt der Ausführung des Berichts, um die Währungswerte der Report Suite in berichtsspezifische Währungswerte umzuwandeln.

## Unterstützte Währungscodes (ISO 4217)

Analytics unterstützt derzeit die folgenden Währungsformate für Konvertierungstransaktionen:


AFA Afghanistan Afghanis (AFA)

AFN Afghanistan Afghanis (AFN)

&quot;ALL&quot; Albanien Leke (ALL)

&quot;DZD&quot; Algerien Dinar (DZD)

&quot;AOA&quot; Angola Kwanza (AOA)

Argentinien Pesos (ARS)

&quot;AMD&quot; Armenien Drams (AMD)

&#39;AWG&#39; Aruba Gulden (AWG)

AUD Australischer Dollar (AUD)

AZM Aserbaidschan-Manat (AZM)

AZN Aserbaidschan Neue Manat (AZN)

&#39;BSD&#39; Bahamas Dollar (BSD)

&#39;BHD&#39; Bahrain Dinar (BHD)

&#39;BDT&#39; Bangladesh Taka (BDT)

&quot;BBD&quot; Barbados Dollar (BBD)

&#39;BYR&#39; Belarus Rubles (BYR)

&#39;BZD&#39; Belize Dollar (BZD)

&quot;BMD&quot; Bermuda Dollar (BMD)

&#39;BTN&#39; Bhutan Ngultrum (BTN)

&quot;BOB&quot; Bolivien Bolivianos (BOB)

&#39;BAM&#39; Bosnien und Herzegowina Konvertible Marka (BAM)

&#39;BWP&#39; Botswana Pulas (BWP)

&#39;BRL&#39; Brasilien Reais (BRL)

&quot;BND&quot; Brunei Dollar (BND)

&#39;BGN&#39; Bulgarien Leva (BGN)

BIF Burundi Franc (BIF)

&quot;KHR&quot; Kambodscha Riels (KHR)

&quot;CAD&quot; Kanada Dollar (CAD)

&quot;CVE&quot; Kap-Verde-Escudos (CVE)

&#39;KYD&#39; Cayman-Inseln Dollar (KYD)

CLP Chile Pesos (CLP)

&quot;CNY&quot; China Yuan Renminbi (CNY)

COP Kolumbien Pesos (COP)

&#39;XOF&#39; Communauté Financière Africaine Francs BCEAO (XOF)

&#39;XAF&#39; Communauté Financière Africaine Francs BEAC (XAF)

&quot;KMF&quot; Komoren-Franken (KMF)

&quot;XPF&quot;-Comptoirs Français du Pacifique Francs (XPF)

&quot;CDF&quot; Congo/Kinshasa Francs (CDF)

&quot;CRC&quot; Costa Rica Colones (CRC)

&quot;HRK&quot; Croatia Kuna (HRK)

&#39;CUC&#39; Cuba Convertible Pesos (CUC)

CUP Kuba Pesos (CUP)

CYP Zypern Pfund (CYP)

&#39;CZK&#39; Tschechische Republik Koruny (CZK)

DKK Dänemark Krone (DKK)

&quot;DJF&quot; Dschibuti Francs (DJF)

&#39;DOP&#39; Dominikanische Republik Pesos (DOP)

&quot;XCD&quot; Ostkaribische Dollar (XCD)

&quot;EGP&quot; Ägyptische Pfund (EGP)

&quot;SVC&quot; El Salvador Colones (SVC)

&quot;ERN&quot; Eritrea Nakfa (ERN)

&#39;XBT&#39; ERR (XBT)

EEK Estland Krone (EEK)

&quot;ETB&quot; Äthiopien Birr (ETB)

Euro (EUR)

&quot;FKP&quot; Falkland-Pfund (FKP)

&quot;FJD&quot; Fidschi-Dollar (FJD)

&#39;GMD&#39; Gambia Dalasi (GMD)

&#39;GEL&#39; Georgia Lari (GEL)

GHC Ghana Cedis (GHC)

GHS Ghana Cedis (GHS)

&#39;GIP&#39; Gibraltar Pfund (GIP)

&#39;XAU&#39;-Goldunzen (XAU)

&#39;GTQ&#39; Guatemala Quetzales (GTQ)

&#39;GGP&#39; Guernsey Pfund (GGP)

&quot;GNF&quot; Guinea Francs (GNF)

&#39;GYD&#39; Guyana Dollar (GYD)

&quot;HTG&quot; Haiti Gourdes (HTG)

&#39;HNL&#39; Honduras Lempiras (HNL)

HKD Hongkong-Dollar (HKD)

HUF Ungarn Forint (HUF)

ISK Island Kronur (ISK)

INR Indien Rupie (INR)

&quot;IDR&quot; Indonesia Rupiahs (IDR)

Sonderziehungsrechte des Internationalen Währungsfonds (XDR)

IRR Iran Rials (IRR)

&quot;IQD&quot; Iraq Dinars (IQD)

&#39;IMP&#39; Isle of Man Pfund (IMP)

&#39;ILS&#39; Israel New Shekels (ILS)

&#39;JMD&#39; Jamaika Dollar (JMD)

JPY Japan Yen (JPY)

&quot;JEP&quot; Jersey Pfund (JEP)

&#39;JOD&#39; Jordan Dinars (JOD)

KZT Kasachstan Tenge (KZT)

&quot;KES&quot; Kenya Shillings (KES)

&quot;KWD&quot; Kuwait Dinars (KWD)

&quot;KGS&quot; Kirgisistan Soms (KGS)

&quot;LAK&quot; Laos Kips (LAK)

&quot;LVL&quot; Latvia Lati (LVL)

&quot;LBP&quot; Libanonpfunde (LBP)

&#39;LSL&#39; Lesotho Maloti (LSL)

&quot;LRD&quot; Liberia Dollar (LRD)

&quot;LYD&quot; Libysche Dinar (LYD)

&quot;LTL&quot; Litauen Litai (LTL)

Macau Patacas (MOPP)

&quot;MKD&quot; Mazedonischer Denar (MKD)

&quot;MGA&quot; Madagaskar Ariary (MGA)

&#39;MWK&#39; Malawi Kwachas (MWK)

&#39;MYR&#39; Malaysia Ringgits (MYR)

&#39;MVR&#39; Malediven Rufiyaa (MVR)

&quot;MTL&quot; Malta Liri (MTL)

&quot;MRO&quot; Mauretanien Ouguiyas (MRO)

&#39;MUR&#39; Mauritius Rupes (MUR)

&quot;MXN&quot; Mexico Pesos (MXN)

MDL Moldawischer Lei (MDL)

&#39;MNT&#39; Mongolia Tugriks (MNT)

&quot;MAD&quot; Marokko Dirhams (MAD)

MZN Mosambik Meticais (MZN)

MZM Mosambik Meticais (MZM)

&#39;MMK&#39; Myanmar Kyats (MMK)

&#39;NAD&#39; Namibia Dollar (NAD)

&#39;NPR&#39; Nepal Rupie (NPR)

&#39;ANG&#39; Niederländische Antillen Gulden (ANG)

NZD Neuseeländische Dollar (NZD)

&quot;NIO&quot; Nicaragua Cordobas (NIO)

&quot;NGN&quot; Nigeria Nairas (NGN)

&quot;KPW&quot; Nordkorea Won (KPW)

&quot;NOK&quot; Norwegische Krone (NOK)

&#39;OMR&#39; Oman Rials (OMR)

PKR Pakistan Rupie (PKR)

&quot;XPD&quot;-Palladiumunzen (XPD)

&#39;PAB&#39; Panama Balboas (PAB)

&#39;PGK&#39; Papua-Neuguinea-Kina (PGK)

PYG Paraguay Guarani (PYG)

&#39;PEN&#39; Peru Nuevos Soles (PEN)

PHP Philippinen Pesos (PHP)

&#39;XPT&#39; Platinunzen (XPT)

PLN Polen Zlotych (PLN)

QAR&#39; Qatar Riyals (QAR)

&#39;ROL&#39; Romania Lei (ROL)

&#39;RON&#39; Romania New Lei (RON)

&quot;RUB&quot; Russland Rubel (RUB)

&quot;RUR&quot; Russland Rubel (RUR)

&quot;RWF&quot; Ruanda Francs (RWF)

&#39;SHP&#39; St Helena Pfund (SHP)

&#39;WST&#39; Samoa Tala (WST)

&#39;STD&#39; São Tome und Principe Dobras (STD)

SAR Saudi-Arabien Riyals (SAR)

&#39;SPL&#39; Seborga Luigini (SPL)

&quot;RSD&quot; Serbiens Dinar (RSD)

&quot;CSD&quot; Serbiens Dinar (CSD)

SCR Seychellen Rupie (SCR)

&quot;SLL&quot; Sierra Leone Leones (SLL)

&#39;XAG&#39; Silberunzen (XAG)

&quot;SGD&quot; Singapur Dollar (SGD)

&quot;SKK&quot; Slowakische Krone (SKK)

&quot;SIT&quot; Slowenien Tolar (SIT)

&#39;SBD&#39; Salomonen Dollar (SBD)

&quot;SOS&quot; Somalia Shillings (SOS)

&quot;ZAR&quot; Südafrikanischer Rand (ZAR)

&quot;KRW&quot; Südkorea Won (KRW)

&#39;LKR&#39; Sri Lanka Rupie (LKR)

&quot;SDD&quot; Sudan Dinar (SDD)

&quot;SDG&quot; Sudan Pfund (SDG)

&quot;SRD&quot; Suriname Dollar (SRD)

&#39;SRG&#39; Suriname Gulden (SRG)

&#39;SZL&#39; Swasiland Emalangeni (SZL)

&quot;SEK&quot; Schweden Krone (SEK)

CHF Schweiz Franken (CHF)

&quot;SYP&quot; Syriens Pfund (SYP)

TWD Taiwan - Neue Dollar (TWD)

TJS Tadschikistan Somoni (TJS)

&quot;TZS&quot; Tansania Schilling (TZS)

THB&#39; Thailand Baht (THB)

&#39;TOP&#39; Tonga Pa&#39;anga (TOP)

&quot;TTD&quot; Trinidad und Tobago Dollar (TTD)

‚TND‘ Tunesien Dinar (TND)

&#39;TRY&#39; Türkei Lira (TRY)

&#39;TRL&#39; Türkei Liras (TRL)

&#39;TMM&#39; Turkmenistan Manats (TMM)

&#39;TMT&#39; Turkmenistan New Manats (TMT)

&quot;TVD&quot; Tuvalu Dollar (TVD)

UGX Uganda Shillings (UGX)

&#39;UAH&#39; Ukraine Hryvnia (UAH)

&quot;AED&quot; Vereinigte Arabische Emirate Dirhams (AED)

&quot;GBP&quot; Vereinigtes Königreich Pfund (GBP)

&#39;USD&#39; ausgewählte US-Dollar (USD)

&#39;UYU&#39; Uruguay Pesos (UYU)

&quot;UZS&quot; Usbekistan Sums (UZS)

&#39;VUV&#39; Vanuatu Vatu (VUV)

&quot;VEB&quot; Venezuela Bolivares (VEB)

&quot;VEF&quot; Venezuela Bolivares Futes (VEF)

VND Vietnam Dong (VND)

YER Jemen Rials (YER)

&quot;ZMK&quot; Sambia Kwacha (ZMK)

&quot;ZMW&quot; Sambia Kwacha (ZMW)

ZWD Simbabwe Dollar (ZWD)


## AppMeasurement.js-Beispiel

Die `currencyCode` Variable kann global in der Datei AppMeasurement.js definiert werden. Durch die Definition der Variablen &quot;currencyCode&quot;in dieser Datei wird sichergestellt, dass alle Währungstransaktionen einen einheitlichen Währungscode verwenden. Im folgenden Beispiel wird Euros als `currencyCode` Variable in der Datei AppMeasurement.js `CONFIG SECTION` angegeben. Alle Kaufereignisse werden durch die Meldung von &quot;Euro&quot;-Transaktionen interpretiert.

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

Weitere Informationen zum Bearbeiten der Datei AppMeasurement.js finden Sie unter [Einfügen von Code in die Datei](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html)AppMeasurement.js.

## Weitere Hinweise zur Implementierung

* Denken Sie daran, dass sich Währungscodes zwar von Seite zu Seite ändern können, aber alle für eine bestimmte Seitenanforderung definierten Umrechnungszeilenelemente dieselbe Währung verwenden müssen (z. B. können Euro, Britische Pfund und US-Dollar nicht für dieselbe Seitenansicht definiert werden). Wenn Sie keine Währungsumrechnung durchführen möchten, sollten Sie den Wert &quot;currencyCode&quot;leer lassen. Dadurch werden die gesendeten Werte direkt an Berichte ohne Konvertierung weitergeleitet.

* Wenn Sie einen ungültigen currencyCode festlegen (einen beliebigen Wert, der nicht in der Liste der unterstützten Währungscodes enthalten ist), wird der gesamte Treffer ausgeschlossen und die Daten für diese Transaktion werden nicht erfasst. Bevor Sie `currencyCode` die Einstellung in der Produktion vornehmen, überprüfen Sie mit einer Report Suite, ob die Daten erfasst und die Währungskonversion korrekt ist.

* Währungen, in denen kein Punkt (.) als Trennzeichen verwendet wird, müssen geändert werden, sodass ein Punkt anstelle des typischen Trennzeichens verwendet wird. Beispielsweise müssen Schwedische Kronen, die ein Komma (,) verwenden, so geändert werden, dass sie stattdessen einen Punkt verwenden. Analytics verwendet das Komma zum Trennen von Werten, und die Daten werden nicht korrekt weitergegeben. Der Zeitraum gibt den Wert korrekt an Berichte weiter.
