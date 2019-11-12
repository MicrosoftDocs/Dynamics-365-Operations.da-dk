---
title: Oversigt over transportstyring
description: Dette emne giver et overblik over funktionerne til transportstyring i Supply Chain Management.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa59a8e6e4744c776ec0e1dc84b1f004dbd796f6
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653573"
---
# <a name="transportation-management-overview"></a>Oversigt over transportstyring

[!include [banner](../includes/banner.md)]

Dette emne giver et overblik over funktionerne til transportstyring i Supply Chain Management.

Med Transportstyring kan du bruge virksomhedens transport og også identificere kreditor- og routingløsninger for indgående og udgående ordrer. For eksempel kan du identificere den hurtigste rute eller den billigste sats for en forsendelse. Følgende tabel indeholder beskrivelser af hovedscenarierne for brug af transportstyring.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarie</th>
<th>Sådan kan du udnytte transportstyring</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Brug eksterne logistikudbydere til transportaktiviteter.</td>
<td>Brug transportstyring til indgående og/eller udgående transport.</td>
</tr>
<tr class="even">
<td>Virksomhedens egen flåde er klar til levering/afhentning, og leveringsgebyrer sendes videre til kunderne.</td>
<td>Du kan bruge transportstyring ved udgående processer til at bestemme transportgebyrerne for transport og sende dem videre til kunder. Dog er fragtmandens fakturaafstemningsproces ikke påkrævet.</td>
</tr>
<tr class="odd">
<td>Virksomhedens egen flåde er klar til levering/afhentning, men leveringsgebyrer videreformidles ikke til kunder, fordi produktpriser omfatter transport.</td>
<td>Mange af funktionerne til projektstyring transport er ikke påkrævede. Du kan dog bruge transportstyring til at bestemme transportsatserne og justere salgsprisen i overensstemmelse hermed.</td>
</tr>
<tr class="even">
<td>Logistiktjenesten leveres fra en anden juridisk enhed i samme firma.</td>
<td><ul>
<li>Du kan bruge transportstyring ved at behandle den andre juridiske enhed som enhver anden fragtmand. Du kan ikke automatisere de økonomiske transaktioner mellem juridiske enheder. Du skal derfor håndtere disse transaktioner manuelt (for eksempel ved at oprette en indkøbsordre).</li>
<li>I den juridiske enhed, der leverer logistiktjenesterne, kan transportstyring bruges til at bestemme transportsatser.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Planlægning af transport i Supply Chain Management
I transportstyring kan transportplanlægning baseres på ordrer eller på de forsendelser, der oprettes på grundlag af disse ordrer. Forsendelserne findes altid på et eller andet tidspunkt, men er ikke påkrævet for transportplanlægning. Flytteordrer er en del af det udgående scenario og kan planlægges sammen med salgsordrer. 

![Indlæs tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Indgående transport
Når du bestiller varer fra en leverandør, og varerne skal leveres til dit lagersted, kan du selv arrangere transport af varerne, hvis du ønsker det. Du kan bruge Supply Chain Management til at planlægge transport og modtagelse af den indgående last. Følgende illustration viser forretningsprocessen for planlægning af transport for en indgående belastning. 

![Forretningsprocesflow for transport af indgående laster](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Udgående transport
Du kan planlægge og behandle en udgående belastning for at levere bestemte varer fra et firmas lager til en kunde. Du kan bruge Supply Chain Management til at planlægge transport og forsendelse af en udgående last. Følgende illustration viser forretningsprocessen for planlægning og behandling af udgående belastninger for levering. 

![Planlægning og behandling af udgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Lastopbygning
Supply Chain Management indeholder en lastopbygningsstrategi, der hedder Volumenbaseret lastopbygningsstrategi. Denne strategi gør det muligt for dig at bruge de maksimumværdier, der er angivet for højde og vægt i lastskabelonen, eller du kan tilsidesætte indstillingerne ved at angive nye værdier. Hvis du vil bruge denne strategi, skal du vælge den i feltet **Lastopbygningsstrategi** i oversigtspanelet **Opsætning** på siden **Lastopbygningspanel**. Du kan desuden tilføje dine egne lastopbygningsstrategier ved at oprette en ny klasse i AOT (Application Object Tree).



