---
title: Dynamische Suchen
description: Erfahren Sie, was dynamische Suchen sind und wie sie aktiviert werden. Enthält Träger, Attribute für Mobilgeräte und Betriebssystemtypen.
source-git-commit: b6084fc34165ea602fce616e13b3adfcd7bdfdbd
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamische Suchen

Mit dynamischen Suchen können Sie zusätzliche Lookup-Dateien in Ihrem Daten-Feed erhalten, falls diese sonst nicht verfügbar sind. Mit dieser Einstellung können die folgenden Suchtabellen mit jeder Daten-Feed-Datei gesendet werden:

* **Betreibername**: Bietet zusätzlichen Kontext für die `carrier` Spalte. Der enthaltene Dateiname lautet `carrier.tsv`.
* **Mobile Attribute**: Bietet zusätzlichen Kontext für die `mobile_id` , einschließlich aller für jedes Mobilgerät verfolgten Funktionen. Der enthaltene Dateiname lautet `mobile_attributes.tsv`.
* **Betriebssystemtyp**: Bietet einen alternativen Kontext für die `os` Spalte. Beide `operating_systems.tsv` und `operating_system_type.tsv` die `os` -Spalte als Schlüssel, jedoch nur `operating_system_type.tsv` ist eine dynamische Suche.

## Dynamische Suchen aktivieren

Wenn Sie die erwähnten Lookup-Dateien erhalten möchten, müssen Sie alle folgenden Voraussetzungen erfüllen:

* Die Schlüsselspalte muss im Daten-Feed enthalten sein.
   * Für `carrier.tsv`, müssen Sie `carrier`.
   * Für `mobile_attributes.tsv`, müssen Sie `mobile_id`.
   * Für `operating_system_type.tsv`, müssen Sie `os`.
* Die folgenden Spalten müssen **ausgeschlossen**. Wenn eine dieser Spalten im Daten-Feed enthalten ist, sind die zusätzlichen Suchtabellen nicht enthalten.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

Sobald Ihr Daten-Feed die Aufnahme- und Ausschlussanforderungen für Spalten erfüllt, wenden Sie sich mit der Daten-Feed-ID an die Kundenunterstützung und fordern Sie die Aktivierung dynamischer Suchen an.

## Lookup-Kopfzeilenreferenz

Spaltenüberschriften für diese Lookup-Dateien ändern sich im Laufe der Zeit nicht, sodass Header nicht in jeder Daten-Feed-Datei enthalten sind. Verwenden Sie diese Spaltenüberschriften als Referenz oder laden Sie die entsprechenden herunter `.tsv` -Datei.

+++**Betreibername**
Download [carrier_headers.tsv](assets/carrier_headers.tsv) oder referenzieren Sie die folgenden Header.

`carrier`
`Carrier Name`
+++

+++**Mobile Attribute**
Download [mobile_attributes_headers.tsv](assets/mobile_attributes_headers.tsv) oder referenzieren Sie die folgenden Header.

`mobile_id`
`Manufacturer`
`Device`
`Device Type`
`Operating System`
`Diagonal Screen Size`
`Screen Height`
`Screen Width`
`Cookie Support`
`Color Depth`
`MP3 Audio Support`
`AAC Audio Support`
`AMR Audio Support`
`Midi Monophonic Audio Support`
`Midi Polyphonic Audio Support`
`QCELP Audio Support`
`GIF87 Image Support`
`GIF89a Image Support`
`PNG Image Support`
`JPG Image Support`
`3GPP Video Support`
`MPEG4 Video Support`
`3GPP2 Video Support`
`WMV Video Support`
`MPEG4 Part 2 Video Support`
`Stream MP4 AAC LC Video Support`
`Stream 3GP H264 Level 10b Video Support`
`Stream 3GP AAC LC Video Support`
`3GP AAC LC Video Support`
`Stream MP4 H264 Level 11 Video Support`
`Stream MP4 H264 Level 13 Video Support`
`Stream 3GP H264 Level 12 Video Support`
`Stream 3GP H264 Level 11 Video Support`
`Stream 3GP H264 Level 10 Video Support`
`Stream 3GP H264 Level 13 Video Support`
`3GP AMR NB Video Support`
`3GP AMR WB Video Support`
`MP4 H264 Level 11 Video Support`
`3GP H263 Video Support`
`MP4 H264 Level 13 Video Support`
`Stream 3GP H263 Video Support`
`Stream 3GP AMR WB Video Support`
`3GP H264 Level 10b Video Support`
`MP4 ACC LC Video Support`
`Stream 3GP AMR NB Video Support`
`3GP H264 Level 10 Video Support`
`3GP H264 Level 13 Video Support`
`3GP H264 Level 11 Video Support`
`3GP H264 Level 12 Video Support`
`Stream HTTP Live Streaming Video Support`
+++

+++**Betriebssystemtyp**
Download [operating_system_type_headers.tsv](assets/operating_system_type_headers.tsv) oder referenzieren Sie die folgenden Header.

`os`
`Operating System Type`
+++