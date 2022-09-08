# Philips CM-153 LMSI Reproduction Card

![A 3d render of the board](EDA/card-render-partial.png "A render of the clone PCB")
 
This project aims to reproduce the LMSI CM-153 card needed to operate a Philips CM-100 CD-ROM drive. This drive was originally released in 1985 and used an early version of the LSMI protocol to connect. Later versions of LMSI cards, such as the CM-260, are not compatible with earlier drives (I do not know what the exactly compatibilities are). So an early card is required. The CM-153 is a very uncommon part to find due to it's limited use, high cost, and the fact that it would probably be tossed out with the computer when upgraded being separated from its original drive.

Thanks to Roland who has a [working CM-100 and CM-153](https://www.youtube.com/watch?v=fj-uSWg0LOY) we have some pretty high quality reference images of what this card looks like. It uses all off the shelf 74 series logic chips and one 8251A UART controller. It should therefore be possible to recreate without needing and rare chips or ROM dumps.

## Current Status

The card has been fully reverse engineered and all hidden traces have been hand verified on original card to be correct. A physical board will be produced soon and tested. The BOM has not been finalized but will be next.

## Parts List

*(Parts picked on 2022-09-07 and reflected best available stock)*

|RefDes|Original Part Number| Datasheet| Digikey Part|
--- | --- | ---|
|7101|PC74HCT245P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT245.pdf)|[CD74HCT245E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HCT245E/38454)|
|7102|PC74HCT244P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT244.pdf)|[CD74HCT244E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HCT244E/38450)|
|7104,7105|PC74HCT138P|[Datasheet](https://archive.org/details/74HCT138)|[CD74HCT138E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HCT138E/38262)|
|7106|PC74HC08P|[Datasheet](https://archive.org/details/manuallib-id-2654066)|[TC74HC08APF](https://www.digikey.com/en/products/detail/toshiba-semiconductor-and-storage/TC74HC08APF/870461)|
|7107,7108|PC74HC32P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT32.pdf)|**!M!**[NTE74HC32](https://www.digikey.com/en/products/detail/nte-electronics-inc/NTE74HC32/11650138)|
|7109|PC74HC368P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT368.pdf)|[SN74HC368N](https://www.digikey.com/en/products/detail/texas-instruments/SN74HC368N/376786)|
|7110|PC74HC04P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT04.pdf)|[SN74HC04N](https://www.digikey.com/en/products/detail/texas-instruments/SN74HC04N/277212)|
|7111|PC74HC125P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT125.pdf)|[CD74HC125E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HC125E/475901)|
|7112,7113|PC74HC74P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT74.pdf)|NOT AVAILABLE|
|7114,7115|PC74HC4024P|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC4024.pdf)|[CD74HC4024E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HC4024E/376737)|
|7116,7117,7118|MC74HC595AN|[Datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT595.pdf)|[CD74HC595E](https://www.digikey.com/en/products/detail/texas-instruments/CD74HC595E/1507396)|
|7119|P8251A|[Datasheet](http://map.grauw.nl/resources/midi/intel_8251.pdf)|NOT AVAILABLE|
|7120|DS26LS31CN|[Datasheet](https://www.ti.com/lit/ds/symlink/am26ls31.pdf)|NOT AVAILABLE|
|7121|DS26LS32CN|[Datasheet](https://www.ti.com/lit/ds/symlink/am26ls32am.pdf)|[AM26LS32ACN](https://www.digikey.com/en/products/detail/texas-instruments/AM26LS32ACN/277026)|
|X-TAL|4.9152MHz||[MP042](https://www.digikey.com/en/products/detail/cts-frequency-controls/MP042/67676)|
|Big cap|50V 10uF||[ECA-1HHG100B](https://www.digikey.com/en/products/detail/panasonic-electronic-components/ECA-1HHG100B/413608)|
|X5|2x8 pin IDC||[826925-8](https://www.digikey.com/en/products/detail/te-connectivity-amp-connectors/826925-8/2276259)|
|X2|2x4 pin IDC||[826656-2](https://www.digikey.com/en/products/detail/te-connectivity-amp-connectors/826656-2/2276228)|
|Y3|15 pin D-Sub||[D15S13B4GX00LF](https://www.digikey.com/en/products/detail/amphenol-cs-fci/D15S13B4GX00LF/1539503)|
