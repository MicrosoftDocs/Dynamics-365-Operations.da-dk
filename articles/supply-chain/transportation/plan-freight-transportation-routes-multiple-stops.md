---
title: Planlæg fragttransportruter med flere stop
description: I denne artikel beskrives de forskellige elementer, som du kan bruge til at planlægge transportruter i Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3d316b5bed67e84fdd5cec8b518069c053436d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671585"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Planlæg fragttransportruter med flere stop

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de forskellige elementer, som du kan bruge til at planlægge transportruter i Dynamics 365 Supply Chain Management.

Du kan bruge ruteplaner og rutevejledninger til komplekse transportruter, der har flere stop. Hvis den samme rute skal bruges regelmæssigt, kan du oprette en planlagt rute.

## <a name="route-plans"></a>Ruteplaner
En ruteplan indeholder rutesegmenter, der indeholder oplysninger om de stop, der besøges på ruten, og de fragtmænd, der bruges til hvert enkelt segment. Du skal du definere stop på ruten som hubs. En hub kan være en kreditor, et lagersted, en kunde eller måske blot et omladningssted, hvor du skifter fragtmand. Du kan definere "spotsatser" for forskellige gebyrer for hvert segment. Her er nogle eksempler:

-   Udgifter til rejser til de givne segmenter
-   Gebyrer for afhentning af varer
-   Gebyrer for aflevering af varer

Hver ruteplan skal være tilknyttet en rutevejledning.

## <a name="route-guides"></a>Rutevejledninger
En rutevejledning definerer kriterierne for at sammenholde en belastning med en bestemt ruteplan. Du kan f.eks. angive en oprindelseshub og en destinationshub, grænser for containervolumen eller vægt og en fragtmand, service eller gruppe. Rutevejledninger er tilgængelige på siden **Satsrutepanel**, hvor belastninger kan matches til ruter, enten manuelt eller automatisk. Hvis rutevejledningen er til en planlagt rute, er den også tilgængelig på siden **Lastopbygningspanel**.

## <a name="scheduled-routes"></a>Planlagte ruter
En planlagt rute er en foruddefineret ruteplan, der har en tidsplan for afsendelsesdatoerne. Planlagte ruter og ikke-planlagte ruter er forskellige i den måde, belastninger er knyttet til dem. Hvis du tildeler en ikke-planlagt rute ved hjælp af satsrutepanelet, valideres kun belastningen og rutevejledningen. Hvis du tildeler en planlagt rute, indgår også datoer og adresser fra ordrerne og hubberne og datoen på ruteplanen i betragtningerne. Du behøver ikke at bruge siden Satsrutepanel til manuelt at tildele belastninger til en planlagt rute. I stedet kan du bruge lastopbygningspanelet til at foreslå, at belastninger bygges baseret på kundeadresser og leveringsdatoer fra salgsordrer for en given planlagte rute. For planlagte ruter har ruteplanen faste oprindelses- og destinationshubs. Typisk er fragtmanden og servicen det samme for alle segmenter, men de kan være forskellige. Destinationshubberne oprettes ved hjælp af postnumre for de kunder, der besøges på ruten. Der kan defineres flere tidsplaner for ruten for én ruteplan. Ruteplanen skal være tilknyttet en rutevejledning. Men for planlagte ruter kan planen kun knyttes til én rutevejledning. Tidsplanen for ruten bruges kun til at oprette de faktiske ruter på siden **Ruteplan**. Du kan bruge standardlastskabelonen, når du foreslår belastninger i lastopbygningspanelet.

## <a name="load-building-workbench"></a>Lastopbygningspanel
Lastopbygningspanelet bruger kundeadresser og leveringsdatoer fra salgsordrer, og de planlagte ruter, der er tilgængelige, til at foreslå en belastning. Som standard angives værdierne fra ruten i panelet. Du kan dog vælge en "fra"-dato, der er tidligere end "fra"-datoen på ruten. Når der foreslås en belastning, kontrolleres leveringsadresse og leveringsdato for alle åbne salgsordrer. Hvis postnummeret på leveringsadressen svarer til postnummeret for en hub i ruteplanen, og hvis leveringsdatoen ligger inden for det område, der er valgt i kriterierne, foreslås salgsordren til belastningen. Lastskabelonens kapacitet tages også i betragtning. Der foreslås kun én belastning ad gangen. Hvis du har en salgsordre, der ikke er inkluderet, skal du muligvis bruge en anden lastskabelon (for eksempel en lastskabelon til en større lastbil eller container) eller planlægge en ekstra levering.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]