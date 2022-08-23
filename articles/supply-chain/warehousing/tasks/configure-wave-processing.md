---
title: Konfigurere eksempel på behandling af bølge
description: Denne artikel viser et eksempel på, hvordan du konfigurerer de kriterier, der bestemmer, hvilket arbejde der genereres for et lagersted, når en bølge behandles, og om bølger behandles manuelt eller automatisk.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a8c088f8726573e4b1fcad1944676547391a9bf
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219622"
---
# <a name="configure-wave-processing-example"></a>Konfigurere eksempel på behandling af bølge

[!include [banner](../../includes/banner.md)]

Denne artikel viser et eksempel på, hvordan du konfigurerer de kriterier, der bestemmer, hvilket arbejde der genereres for et lagersted, når en bølge behandles, og om bølger behandles manuelt eller automatisk. Du angiver kriterierne ved at konfigurere bølgeskabeloner og forespørgsler, der svarer til en bølge med frigivne linjer i salgsordrer, produktionsordrer eller kanbanordrer.

## <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du bruge et system, hvor [standarddemodataene](../../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Du skal også vælge den juridiske enhed **USMF**, før du starter.

## <a name="example-scenario-configure-wave-processing"></a>Eksempelscenario: konfigurere behandling af bølge

I dette eksempel gennemgås mange af de forskellige indstillinger, der har indflydelse på, hvordan bølger oprettes, udfyldes, behandles og frigives.

1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Bølger > Bølgeskabeloner**.
1. Vælg **Ny**.
1. Indtast en værdi i feltet **Bølgeskabelonnavn**. Når du opretter en bølgeskabelon, kan du angive den rækkefølge, hvori skabelonerne knyttes til frigivne linjer på salgsordrer, produktionsordrer eller kanbans. Når en linje er frigivet til lagerstedet eller produktionen, bruges den første bølgeskabelon, den opfylder kriterierne for. Vi anbefaler, at du placerer skabeloner med de mest specifikke kriterier øverst på listen. Jo bredere kriterier, desto mere sandsynligt er det, at en linje opfylder kriterierne, og et kan medføre, at linjer tildeles til den forkerte bølge.  
1. Indtast en værdi i feltet **Beskrivelse af bølgeskabelon**.
1. Indtast eller vælg en værdi i feltet **Sted**. Hvis du bruger USMF, kan du vælge lokation 2.  
1. Indtast eller vælg en værdi i feltet **Lokation**. Hvis du bruger USMF, kan du vælge lagersted 24.  
1. Angiv feltet **Automatiser bølgeoprettelse** til **Ja**. Vælg denne indstilling for automatisk at oprette en bølge, når en salgsordre, produktionsordre eller kanban er frigivet til lagerstedet.  
1. Angiv indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** til **Ja**. Vælg denne indstilling for automatisk at behandle bølgen og oprette arbejde, når en linje er frigivet til lagerstedet.  
1. Angiv indstillingen **Automatiser frigivelse af bølge** til **Ja**. Vælg denne indstilling for at frigive bølgen automatisk. Plukkearbejdet oprettes og gøres tilgængeligt på mobilenheder.  
1. Angiv indstillingen **Tildel til åbne bølger** til **Ja**. Linjerne tildeles bølger ud fra forespørgselsfiltret til bølgeskabelonen.  
1. Angiv indstillingen **Udfør automatisk behandling af bølge ved grænseværdi** til **Ja**. Vælg denne indstilling for automatisk at behandle bølgen, når dens værdier når de grænser for vægt, levering, og linjer, der er angivet i feltgruppen **Grænser for bølge**. Denne indstilling kan kun benyttes, hvis der er valgt **Forsendelse** i feltet **Bølgeskabelontype**.  
1. Angiv indstillingen **Automatiser frigivelse af genopfyldningsarbejde** til **Ja**. Vælg denne indstilling for at oprette behovsbaseret genopfyldningsarbejde og frigive det automatisk. Du skal føje genbestillingsbølgemetoden til bølgeskabelonen og oprette en genbestillingsskabelon med typen **Bølgebehov**.  
1. Brug indstillingerne i **Standardværdier**-gruppen for at tildele bølgeattributter. Bølgeattributter, der fungerer som filtre til at begrænse, hvilken type varer der kan bruge bølgen. Du kan for eksempel angive en varegruppe.  
1. Udvid afsnittet **Metoder**, og angiv de handlinger, der skal udføres af bølgeskabelonen. Bølgeskabelonmetoder gør det muligt at styre den rækkefølge af aktiviteter, som hver bølge gennemgår når den er behandlet. Du kan for eksempel have en metode til bølgegenopfyldning. Når du tilføjer en metode, vises den automatisk på den korrekte placering i trinrækkefølgen. Hvis du har angivet indstillingen **Automatiser frigivelse af genopfyldningsarbejde** til **Ja**, skal du tilføje genopfyldningsmetoden her.  
1. Vælg **Gem**.
1. Luk siden.
1. Gå til **Lokationsstyring > Opsætning > Parametre til lokationsstyring**.
1. Udvid sektionen **Bølgebehandling**.
1. Indtast eller vælg en værdi i feltet **Batchgruppe til behandling af bølge**.
1. Angiv indstillingen **Udfør behandling af bølger i batch** til **Ja**.
1. I feltet **Vent på lås (ms.)** skal du angive et tal. Angiv tid i millisekunder, som et fordelingstrin venter på en systemressource, der er låst af et andet fordelingstrin. Når denne tid overskrides, behandles bølgen ikke, og der vises en fejlmeddelelse.  
1. Vælg **Gem**.
1. Luk siden.
1. Gå til **Navigationsrude > Moduler > Produktionsstyring > Konfiguration > Produktionsstyringsparametre**.
1. Vælg en indstilling i feltet **Frigiv til lagersted**.

    Når det gælder salgsordrer og kanban-ordrer, skal der reserveres lager, før ordren frigives til lagerstedet. Ellers kan varerne eller fordelingslinjerne ikke behandles i en bølge. Til produktionsordrer kan du også have mulighed for at vælge **Tillad delvis reservation**. Dette er f.eks. nyttigt, hvis du har de materialer, du skal bruge til at starte en produktion og kan vente med at fuldføre processen, indtil de ekstra materialer bliver tilgængelige. Hvis du vælger denne indstilling, skal du gentage frigivelsen til lagerprocessen manuelt, når de ekstra materialer bliver tilgængelige.
1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Bølgeoprettelse og -behandling](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
