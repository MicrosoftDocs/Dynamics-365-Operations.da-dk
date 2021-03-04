---
title: Butikslagerstyring
description: I dette emne beskrives de typer af dokumenter, du kan bruge til at lagerstyring.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411094"
---
# <a name="store-inventory-management"></a>Butikslagerstyring

[!include [banner](includes/banner.md)]

Når du arbejder med lager i Microsoft Dynamics 365 Commerce og bruger POS-programmet (point of sale), er det vigtigt, at du er opmærksom på, at POS har begrænset understøttelse af visse lagerdimensioner og nogle lagervaretyper. POS-programmet understøtter ikke hele udvalget af varekonfigurationsfaciliteter, der er tilgængelige via varekonfigurationsindstillingerne i Dynamics 365 Supply Chain Management.

POS-løsningen understøtter i øjeblikket ikke følgende produktdimensioner og varekonfigurationer:

- Konfigurationsproduktdimension og styklistevarer (undtagen detailpakkeprodukter, der bruger visse komponenter i styklistestrukturen)
- Fastvægtvarer
- Versionsproduktdimension-styrede varer

POS-programmet understøtter i øjeblikket ikke følgende sporingsdimensioner i POS:

- Batchsporingsdimension
- Ejerdimension

POS har begrænset understøttelse af følgende dimensioner. POS kan med andre automatisk angive nogle af disse dimensioner i lagerposteringer baserest på konfigurationen af lagerstedet/butiksopsætningen. POS understøtter ikke dimensionerne fuldstændigt på den måde, de understøttes, hvis en salgstransaktion angives manuelt i Commerce Headquarters. 

- **Lagerstyringssted** – når de bruger de nye POS-handlinger [Indgående handling](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [Udgående handling](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kan brugerne vælge et lagerstyringssted, som de vil modtage varer til, eller forsende udgående ordrevarer ud fra. Hvis der bruges den forældede handling **Pluk og modtagelse**, er understøttelse af begrænset lokationsstyring tilgængelig for modtagelse og afsendelse af udgående overflytninger. Denne understøttelse er kun tilgængelig, hvis indstillingen **Brug proces til lagerstyringssted** er aktiveret for varen og butikkens lager. En lagerlokation kan ikke bruges i øjeblikket med handlingen **Status** eller **Lagersøgning**.
- **Nummerplade** – nummerplader er kun relevante, når indstillingen **Brug proces til lagerstyringssted** er aktiveret på varen og butikkens lager. I POS er det sådan, at hvis lageret modtages på en butiks lager sted ved hjælp af **Indgående handling** eller handlingen **Pluk og modtagelse**, hvor processen til lagerstyringsstedet er aktiveret, og hvis den placering, der er valgt til at modtage varen, er knyttet til en lokationsprofil, der kræver nummerpladekontrol, anvender POS-programmet automatisk en nummerplade på modtagelseslinjen. POS-brugere kan ikke ændre eller administrere disse id-data. Hvis det er nødvendigt med fuld styring af id'er, anbefaler via, at butikken bruger [lagerstyringsappen](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) eller administrationsklient til at styre modtagelsen af disse varer.
- **Serienummer** – POS-programmet giver understøttelse af registrering af et enkelt serienummer på en transaktions salgslinje for ordrer, der er oprettet i POS, og omfatter serialiserede varer. Dette serienummer bliver ikke valideret mod registrerede serienumre, der allerede findes på lageret. Hvis der oprettes en salgsordre i callcenterkanalen, eller den opfyldes via ERP, og der er registreret flere serienumre på en enkelt salgslinje under opfyldningsprocessen i ERP, kan disse serienumre ikke anvendes eller valideres, hvis en returværdi behandles for denne ordre i POS. Når lageret modtages ved hjælp af **Indgående handling**, kan brugere [registrere eller bekræfte de modtagne serienumre](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Lagerstatus** – for varer, der bruger lokationsstyringsprocessen og kræver en lagerstatus, kan dette statusfelt ikke angives eller ændres via POS-programmet. Standardlagerstatussen som defineret i konfigurationen af butikkens lagersted bruges, når varer modtages på lageret.

> [!NOTE]
> Alle organisationer skal teste varekonfigurationer via POS i udviklings- eller testmiljøer, inden de installerer disse varekonfigurationer til produktionsmiljøer. Test dine varer ved at bruge dem til at udføre almindelige cash and carry-salgstransaktioner og oprette kundeordrer (hvis relevant) via POS. Du skal også teste POS-opfyldnings- og -lagerprocesser (f.eks. handling med lagertilgang og ordreopfyldelse), før du implementerer nye varekonfigurationer, for at sikre, at POS-programmer kan understøtte dem. Test skal omfatte kørsel af en fuld bogføringsproces for opgørelse i testmiljøet og kontrollere, at der ikke opstår problemer, når der oprettes ordrer for disse varer, og de bogføres i Commerce Headquarters.
>
> Hvis der er konfigureret varer på en måde, som POS-programmet ikke understøtter, og der ikke udføres passende test, kan der opstå datafejl, som ikke er lette at rette, eller som ikke er dækket af standardproduktsupport, under processen til oprettelse af ordrer.

## <a name="purchase-orders"></a>Indkøbsordrer

Indkøbsordrer oprettes i Commerce Headquarters. Hvis en butiks lagersted er medtaget i indkøbsordrehovedet eller på indkøbsordrelinjer, kan linjerne modtages i butikken ved hjælp af [Indgående handling](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) i POS. 

## <a name="transfer-orders"></a>Flytteordrer

Flytteordrer kan oprettes i Commerce Headquarters eller enten ved hjælp af [Indgående handling](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) eller [Udgående handling](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) i POS. Brug den **Indgående handling** for POS til at oprette en anmodning om flytteordre for at få lager sendt til butikken fra et andet lagersted eller butikslokalitet. Brug den **Udgående handling** for POS til at oprette en anmodning om flytteordre for at få lager sendt fra butikken til et andet lagersted eller en anden butikslokalitet. Når en flytteordre for en butik er oprettet, kan den pågældende butik administrere modtagelsen af flytteordren via den **Indgående handling** i POS. Hvis butikken sender lager til en anden lokation, bruges den **Udgående handling** i POS til at administrere butikkens proces for udgående forsendelser.

## <a name="stock-counts"></a>Lagerstatus

Status kan enten være planlagt eller ikke-planlagt. Planlagte statusopgørelser oprettes via Commerce Headquarters ved at oprette et dokument som Optællingskladde , der er knyttet til butikkens lagersted. Denne kladde angiver de varer, der skal optælles. Butikken kan derefter få adgang til disse foruddefinerede optællingskladder og udføre handlinger på dem ved at bruge handlingen **Status** i POS. Butiksbrugere starter en ikke-planlagt status, som det er påkrævet, når de bruger handlingen **Status** i POS. I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer. Når en lagertælling af en af typerne er fuldført i POS, gøres den bindende og sendes til hovedkontoret. På hovedkontoret skal antallet valideres og bogføres i Commerce Headquarters som et separat trin.

## <a name="inventory-lookup"></a>Lagersøgning

Det antal produkter, der i øjeblikket er disponibelt for flere butikker og lagersteder, kan ses på siden **Lagersøgning**. Ud over den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik. Vælg den butik, du vil se DTT-mængder for, og vælg derefter **Vis butikkens tilgængelighed**. Få flere oplysninger om de konfigurationsindstillinger, der er tilgængelige, i afsnittet [Beregne lagertilgængelighed for detailkanaler](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).


[!INCLUDE[footer-include](../includes/footer-banner.md)]