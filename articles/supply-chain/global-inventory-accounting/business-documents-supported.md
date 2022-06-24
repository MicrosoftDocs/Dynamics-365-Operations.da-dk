---
title: Forretningsdokumenter, der understøttes af Global Inventory Accounting
description: Denne artikel indeholder en oversigt over de forretningsdokumenter, der understøttes af Global Inventory Accounting. Det indeholder også et detaljeret eksempel på indkøbsordredokumenter.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: dc88d095c039b22ac347db949f6b61d5a89dc4b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875417"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Forretningsdokumenter, der understøttes af Global Inventory Accounting

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Når tilføjelsesprogrammet Global Inventory Accounting er konfigureret fuldt ud, er det klar til at behandle lagerrelaterede dokumenter, der indtastes i Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Understøttede forretningsdokumenter

Der findes to typer forretningsdokumenter:

- **Dokumenter, der har en kladde** – Disse dokumenter omfatter dokumenter af typen produktkvittering, indkøbsfaktura, følgeseddel og salgsfaktura.
- **Dokumenter, der ikke har en kladde** – Disse dokumenter omfatter optællings-, bevægelses- og lagerreguleringsdokumenter.

Senere i denne artikel bruges indkøbsordrer som eksempel til at illustrere processen.

Følgende tabel indeholder de dokumenter, som den aktuelle version understøtter.

| Dokumenttype      | Dokument        |
|--------------------|-----------------|
| Indkøbsordre     | Produktkvittering |
| Indkøbsordre     | Fakturaer         |
| Salgsordre        | Følgeseddel    |
| Salgsordre        | Fakturaer         |
| Lagerkladder | Bevægelse        |
| Lagerkladder | Tilpasning      |
| Lagerkladder | Tælling        |
| Lagerkladder | Overførsel        |
| Flytteordre     | Forsendelse        |
| Flytteordre     | Modtag         |

> [!IMPORTANT]
> Global Inventory Accounting behandler de dokumenter, der er angivet i Supply Chain Management, asynkront. Der vises ingen fejlmeddelelser for problematiske dokumenter.

## <a name="example-purchase-order"></a>Eksempel: Indkøbsordre

### <a name="product-receipt"></a>Produktkvittering

Bogfør produktkvitteringer, som du plejer. Vælg en indkøbsordre på siden **Alle indkøbsordrer**, og vælg derefter **Produktkvittering** under fanen **Modtag** i handlingsruden for at åbne siden **Produktkvitteringskladde**. Der genereres en handlingshændelse og en Global Inventory Accounting-hændelse for hver linje. Vælg derfor fanen **Linjer**, og vælg derefter **Lager \> Hændelser og målinger** for at åbne siden **Hændelser og målinger**.

Global Inventory Accounting er et regnskabssystem, der er baseret på hændelser og målinger. Gitteret for målingslinjen på siden **Hændelser og målinger** viser en liste over målinger. Hver måling har en liste over dimensioner.

For hver handlingshændelse er der to typer måling:

- **Handlingsmålinger** – Disse målinger beskriver forretningsdokumenter i generelle termer. En måling er det produktantal, der bruger den måleenhed, som anvendes i dokumentet. Der er også målinger, der påvirker lagerværdien, for eksempel udvidet pris, rabat, rabatprocent og linjegebyr.
- **Ressourceregnskabsmålinger** – Disse målinger er beregnet ud fra lagerregisteret. De beskriver dokumentets indflydelse på lageret i måleenheden for lageret. Hvis der er flere lagerregistreringer, er der flere linjer med regnskabsmålinger for ressourcer.

Dimensionerne er organiseret på følgende måde:

- **Dualitet** – Dualitet beskriver de agenter, der deltager i de økonomiske hændelser. I forbindelse med eksterne forretningsdokumenter beskriver de primære dimensioner den juridiske enhed, hvor dokumentet angives, mens dobbeltdimensionerne beskriver kreditor, debitor osv. I forbindelse med interne forretningsdokumenter (for eksempel flytteordrer) beskriver dobbeltdimensionerne de tilsvarende lagersteder.
- **Dimensionstype** – Dimensionstyper kategoriserer dimensionerne.
- **Dimension** – Navnet på dimensionen.
- **Dimensionsværdi** – Værdien for dimensionen.

### <a name="global-inventory-accounting-event"></a>Global Inventory Accounting-hændelse

Global Inventory Accounting bruger driftshændelser og målinger som input. Derefter anvendes det relevante regnskab for hver relateret finanskonto ud fra den tilknyttede valuta og det tilknyttede princip. Du kan vælge **Hændelser og målinger for globalt lagerregnskab** for at få vist Global Inventory Accounting-hændelsen. Global Inventory Accounting-hændelsen følger samme metode som driftshændelser, men den bruger forskellige målinger. Der findes tre større målingstyper: produktomkostningsantal, produktomkostning og afvigelse.

Reskontrokonti bruges til yderligere at klassificere målingerne. Der kan være flere finanskonti. Disse finanskonti er knyttet til den juridiske enhed, hvor dokumentet angives. Du kan få vist hændelser og målinger for hver finanskonto ved at ændre værdien i feltet **Finans**.

### <a name="cost-element"></a>Omkostningselement

Baseret på den politik for omkostningselementer, der er knyttet til finanskontoen, tildeler systemet et omkostningselement til hver enkelt bogført driftshændelsesmåling, der påvirker lageromkostningen. Disse målinger omfatter udvidet pris, rabat, rabatprocent og linjegebyr.

### <a name="measurement-line-details"></a>Detaljer om målelinje

Fanen **Oversigt** viser detaljer om de tilknyttede politikker. Omkostningsobjektdimensionerne viser omkostningsobjektet på baggrund af politikken for omkostningsobjekter. Specifikke identifikationsdimensioner viser batchnummeret, hvis det antages, at forudsætningen for omkostningsforløbet *Specifik – Batch*.

### <a name="purchase-invoice"></a>Indkøbsfaktura

Bogfør fakturaen, som du plejer. I handlingsruden under fanen **Faktura** i gruppen **Kladder** skal du derefter vælge **Faktura** for at åbne fakturajournalen. Der genereres en handlingshændelse og en Global Inventory Accounting-hændelse for hver linje. Vælg derfor fanen **Linjer**, og vælg derefter **Lager \> Hændelser og målinger** for at åbne siden **Hændelser og målinger**. Siden **Hændelser og målinger** viser samme måletype. Men da siden viser en anden målerolle og målemodifikator, er effekten på agenten (den juridiske enhed) forskellig.

Vælg **Hændelser og målinger for globalt lagerregnskab** for at få vist Global Inventory Accounting-hændelsen. Lagerantallet og kostprisen går nu fra reskontrokontoen *Varer, der er modtaget, ikke faktureret lager* til reskontrokontoen *Købte varer*.
