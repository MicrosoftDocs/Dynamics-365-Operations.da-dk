---
title: Grovplanlægning
description: Dette emne indeholder en beskrivelse af grovplanlægning. Du kan bruge grovplanlægning til at få et generelt estimat af produktionsprocessens over tid.
author: ChristianRytt
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16b05bfe2a8deec365bdccf56ddbb375e9c4becd
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190010"
---
# <a name="operations-scheduling"></a>Grovplanlægning

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af grovplanlægning. Du kan bruge grovplanlægning til at få et generelt estimat af produktionsprocessens over tid.

Du kan planlægge produktion på driftsniveau og jobniveau. Modsat finplanlægning udfolder grovplanlægning ikke operationerne til produktionsruten i job. Hvis du vil medtage flere detaljer i planlægningen, f.eks oplysninger om den aktuelle kapacitet, kan du køre finplanlægning efter grovplanlægning. Du kan også nøjes med at køre finplanlægning. Finplanlægning bruges typisk til at planlægge individuelle job i produktionen til en aktuel eller kortsigtet tidsramme.

## <a name="components-of-operations-scheduling"></a>Komponenter i grovplanlægning
Hovedkomponenter i grovplanlægning er planlægningsvej, ressourcekapacitet og materialeoptimering. Ved hjælp af grovplanlægning kan du opnå følgende:

-   Styre planlægningsmetoden ved at planlægge før eller efter en bestemt dato.
-   Optimere brugen af ressourcer via produktionsplanlægning, der er baseret på ressourcernes kapacitet. Dette er også en hjælp, når du skal bruge alternative ressourcer.
-   Optimere brugen af materialer ved produktionsplanlægning, der er baseret på tilgængeligheden af de nødvendige materialer.
-   Planlægge og synkronisere referenceproduktioner. Datoerne for referenceproduktioner justeres, når der foretages ændringer i produktionsordrens tidsplan.

Før du kan køre grovplanlægning, skal du vurdere omkostningerne for en produktionsordre. Hvis du ikke allerede har foretaget et estimat, foretages det automatisk, før grovplanlægning påbegyndes. I en grovplanlægning angives følgende:

-   Det produkt, der er planlagt til produktion
-   Konfigurationen af produktet
-   De mængder, der er involveret i produktionen
-   Datoerne for start og afslutning af produktionen
-   Kapacitetsreservationer for de ressourcer, der udfører produktionsaktiviteterne

Opstillingstid, procestid og kørselstidspunkt defineres for operationer i produktionen. Når du kører en grovplanlægning, er status for produktionsordren **Planlagt**, og alle operationer planlægges i den rækkefølge, der er angivet i produktionsruten. Der tages dog kun højde for varigheden af operationen. Start- og sluttidspunkter er ikke planlagt.

## <a name="scheduling-direction-and-date"></a>Planlægningsvej og -dato
Planlægningsvejen er grundlæggende for planlægningsprocessen. Produktionen kan planlægges fremad eller bagud fra en vilkårlig dato, afhængigt af tids- og planlægningsbehov.

-   **Fremad fra planlægningsdatoen** – Du kan planlægge, at produktionen skal starte så tidligt som muligt. Den kan startes i dag, i morgen eller fra en given dato i fremtiden. Produktionen planlægges fremad i tid til den tidligst mulige slutdato.
-   **Bagud fra planlægningsdatoen** – Du kan planlægge, at produktionen skal starte så sent som muligt. Planlægning bagud er baseret på den dato, hvor produktionen skal være afsluttet. Tidsplanen tæller baglæns fra denne dato til den seneste mulige dato, hvor produktionen kan startes og stadig være færdig til tiden.

## <a name="resource-scheduling"></a>Ressourceplanlægning
Når du kører en grovplanlægning, er hver enkelt operation i produktionsruten planlagt til den ressource, der er angivet til operationen. Desuden er varigheden af hver operation specificeret i produktionsruten. Hvis der er angivet en ressourcegruppe for en operation, reserveres der i planlægningen kapacitet til gruppen. Men i modsætning til finplanlægning vælges der i grovplanlægningen ikke specifikke ressourcer i gruppen. Hvis du arbejder med kapacitetsbegrænsning, afhænger tidsplanen af tilgængeligheden af de ressourcer, der skal bruges til at fuldføre produktionen. Grovplanlægning følger rækkefølgen af operationer, der er angivet i produktionsruten. Grovplanlægningen reserverer kapacitet på ressourcegrupperne baseret på de operationstider, der er defineret for produktionsruten. Summen af tilgængelig kapacitet i de involverede ressourcer bestemmer kapaciteten for ressourcegruppen. Kapacitetsreservationer, der allerede findes for ressourcerne, betragtes som ikke-tilgængelig kapacitet. Hvis der ikke er nok tilgængelig kapacitet til produktion, kan produktionsordrer udskydes eller endda stoppes. Du kan også angive den effektivitet, du forventer fra ressourcerne, der er involveret i produktionen. Du angiver effektiviteten i procent for ressourcen. Effektivitetsprocenten justerer gennemløbet for ressourcen. Dette påvirker den tid, der er reserveret til ressourcen. Leveringstider for de operationer, der bruger ressourcen, justeres også i overensstemmelse med dette.

## <a name="operations-scheduling-and-master-planning"></a>Grovplanlægning og behovsplanlægning
Grovplanlægning styrer også varedisponering og bestemmer beregninger af materialebehov. Der tages i grovplanlægning højde for følgende:

-   **Produktioner i ordrebeholdning** – Produkter, der er planlagt, frigivet eller igangsat
-   **Tilgængelighed af materiale** – Lager, underproduktion og leverandører
-   **Kapacitetstilgængelighed** – Ressourcer, der kræves til produktion

> [!NOTE]
> Hvis du bruger flertrådet varedisponering og grovplanlægning, tages der ikke hensyn til kapacitetsbegrænsningen. 

## <a name="cancellations"></a>Annulleringer
Når du kører grovplanlægning, kan du annullere visse dele af ruteplanlægningen. Disse omfatter køtid, opstillingstid, procestid, overlapstid og transporttider.

## <a name="finite-materials"></a>Materialebegrænsning
Hvis du arbejder med materialebegrænsning, afhænger planlægningen også af tilgængeligheden af de materialer, der skal bruges til produktion. Hvis de tilgængelige komponenter ikke er tilstrækkelige til produktionen, kan produktionen forsinkes. Du kan basere planlægningen på brugen af materialer ved at angive de materialer, der skal være tilgængelige til produktionen. Når du optimerer både ressourcekapacitet og tilgængeligheden af materialer, beregnes produktion i overensstemmelse med disse begrænsninger. En produktionsordre kan ikke planlægges til at starte, før kapacitet og materialer er tilgængelige på samme tid og i de krævede mængder.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indstillinger for grovplanlægning](operation-scheduling-options.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]