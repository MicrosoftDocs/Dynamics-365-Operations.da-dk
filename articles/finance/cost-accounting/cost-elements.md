---
title: Dimensioner for omkostningselement
description: Som et af de centrale elementer i omkostningsregnskabet bruges omkostningselementdimensioner til at kategorisere og spore, hvor omkostningerne flyder til.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 037d4971fe0a5a9d08f0ed20d2482b8feb9aa4f2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176985"
---
# <a name="cost-element-dimensions"></a>Dimensioner for omkostningselement

[!include [banner](../includes/banner.md)]

Som et af de centrale elementer i omkostningsregnskabet bruges omkostningselementdimensioner til at kategorisere og spore, hvor omkostningerne flyder til. 

Et omkostningselement svarer til et omkostningsrelevant element i kontoplanen. Grundlæggende kan det være en hvilken som helst type af element på det laveste niveau i en virksomhed, hvor omkostningerne kan flyde til. Omkostningselementer som et koncept går fra finanskonti til alle omkostningsrelevante ressourcer. I øjeblikket understøtter omkostningsregnskab finanskonti.

## <a name="two-types-of-cost-elements"></a>To typer omkostningselementer
Der findes to typer omkostningselementer: primære omkostningselementer og sekundære omkostningselementer. Følgende tabel beskriver forskellene mellem de to typer.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primære omkostningselementer</strong></td>
<td><strong>Sekundære omkostningselementer</strong></td>
</tr>
<tr class="even">
<td>De primære omkostningselementer repræsenterer strømmen af omkostninger fra finansregnskab til omkostningsregnskab. Strukturen af omkostningselementet svarer til driftskontostrukturen i Finans, hvor et omkostningselement kan svare til en hovedkonto. Ikke alle hovedkonti kan nødvendigvis være repræsenteret som omkostningselementer, afhængigt af virksomhedens behov. Eksempler på primære omkostningselementer omfatter:
<ul>
<li>Vareforbrug</li>
<li>Indirekte materialeomkostninger</li>
<li>Personaleomkostninger</li>
<li>Energiomkostninger</li>
</ul></td>
<td>De sekundære omkostningselementer repræsenterer internt flow af omkostninger, da disse omkostninger kun oprettes og bruges i forbindelse med omkostningsregnskab. De bruges til at sikre, at kilden til omkostningerne kan spores. Disse omkostningselementer bruges i omkostningsfordelinger og beregninger af faste omkostninger. Eksempler på sekundære omkostningselementer omfatter:
<ul>
<li>Produktionsomkostninger</li>
<li>Indirekte produktions, materiale- og marketingomkostninger</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Omkostningselementdimensioner og omkostningselementers dimensionsmedlemmer
Omkostningselementer omtales som *omkostningselementdimensioner*. De enkelte dimensionsværdier kaldes *omkostningselementers dimensionsmedlemmer*. For eksempel kan du have en dansk struktur for kontoplanen, der er grundlaget for lovpligtig rapportering. Kontoplanen anvendes som omkostningselementdimension. De konti, som er primære omkostningselementer, repræsenteres som omkostningselementets dimensionsmedlemmer i omkostningsregnskabet. Følgende skærmbillede vises et eksempel på hovedkonti som omkostningselementdimension med dets faktiske hovedkonti som dimensionsmedlemmer af omkostningselementet. 

[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Importere omkostningselementers dimensionsmedlemmer gennem dataforbindelser
For at forenkle opsætningen af omkostningselementets dimensionsmedlemmer i omkostningsregnskabet kan du bruge dataforbindelser, der enten er færdigbyggede eller tilpassede til at hente de primære omkostningselementer fra et eller flere kildesystemer.

## <a name="implementation-considerations"></a>Overvejelser i forbindelse med implementering
Da omkostningselementer repræsenterer det laveste niveau af oplysninger om omkostninger, skal du sikre dig, at alle de omkostningselementer, der kræves i den ledelsesmæssige rapportering, er medtaget, når du implementerer omkostningselementernes struktur. Det kan være en udfordring at finde et passende antal omkostningselementer til omkostningsstyring. Tusindvis af omkostningselementer kan gøre det svært at styre hvert omkostningselement. Som et alternativ kan du gruppere omkostningselementer og administrere omkostningsstyring på et samlet niveau.


