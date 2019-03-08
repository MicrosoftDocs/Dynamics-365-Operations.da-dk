---
title: Butikslagerstyring
description: I dette emne beskrives de typer af dokumenter, du kan bruge til at lagerstyring.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "339228"
---
# <a name="store-inventory-management"></a>Butikslagerstyring

[!include [banner](includes/banner.md)]

I dette emne beskrives de typer af dokumenter, du kan bruge til at lagerstyring.

Du kan bruge følgende typer dokumenter til at administrere organisationens lager.

Når du arbejder med lager i Dynamics 365 for Retail og bruger POS-programmet, det er vigtigt at bemærke, at POS yder begrænset understøttelse til lagerdimensioner og visse lagervaretyper.  

POS-løsningen understøtter ikke følgende varekonfigurationer:
- Styklistevarer (undtagen pakkeprodukter, som anvender nogle komponenter af styklistestrukturen)
- Fastvægtvarer
- Batchstyrede varer

POS-programmet understøtter i øjeblikket ikke følgende sporingsdimensioner i POS:
- Batchsporingsdimension
- Ejerdimension

POS-løsningen har begrænset understøttelse af følgende dimensioner. Begrænset understøttelse angiver, at en POS evt. vil bruge standardværdien for nogle af disse dimensioner i lagerposteringer, der automatisk baseres på konfigurationen af lagersted/butiksopsætning. POS understøtter ikke dimensionerne fuldstændigt på den måde, de understøttes, hvis en salgstransaktion angives manuelt i ERP. 

- Placering
- Id (kun relevant, når **Brug lokationsstyringsprocesser** er aktiveret på varen og butikkens lagersted)
- Serienummer
- Lagerstatus

> [!NOTE]
> Alle organisationer skal teste varekonfigurationer via POS i udviklings- eller testmiljøer, inden de installeres til produktion. Test dine varer ved at udføre almindelige cash and carry-salgstransaktioner og oprette kundeordrer (hvis relevant) via POS med dine varer. Test skal omfatte kørsel af en fuldstændig redegørelse for bogføringsprocesser i testmiljøet og skal kontrollere, at der ikke er nogen problemer.
> Hvis varer konfigureres på en måde, der ikke understøttes af POS-programmet, uden grundige test, kan det medføre, at der opstår fejl i dine bogføringsprocesser i produktionen, og at der ikke er nogen nem måde at løse problemet på. Partner- eller kundetilpasninger til programmet kan eventuelt komme i betragtning, så disse bogføringsprocesser kan fuldføres. Hvis tilpasninger ikke er nødvendige, skal organisationen sikre, at produktkonfigurationen af dine produkter er udført på en måde, der understøttes af det POS-program/den ordreoprettelse/bogføring af opgørelsesprocessen, der bruges som standard.

## <a name="purchase-orders"></a>Indkøbsordrer

Indkøbsordrer oprettes på hovedkontoret. Hvis et detaillagersted er medtaget i indkøbsordrehovedet, kan ordren modtages i butikken ved hjælp af Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail. Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere. Alternativt kan antallet bindes og sendes til hovedkontoret. Det antal, der er modtaget i butikken, vises i Dynamics 365 for Retail i feltet **Modtag nu** på indkøbsordren.

## <a name="transfer-orders"></a>Flytteordrer

En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan afsendes fra. I dette tilfælde vises flytteordren i butikken som en plukanmodning i MPOS eller Cloud POS. Når de antal, der er anmodet om, er blevet plukket, gøres de bindende og sendes til hovedkontoret. Det antal, der plukket i butikken, vises i Dynamics 365 for Retail i feltet **Afsend nu** på flytteordren. En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan sendes til. I dette tilfælde vises flytteordren i butikken som en tilgangsanmodning i MPOS eller Cloud POS. Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere. Alternativt kan antallet bindes og sendes til hovedkontoret. Det antal, der er modtaget i butikken, vises i Dynamics 365 for Retail i feltet **Modtag nu** på flytteordren.

## <a name="stock-counts"></a>Lagerstatus

Status kan enten være planlagt eller ikke-planlagt. Planlagte statusopgørelser startes i hovedkontoret, der angiver, hvilke varer der skal optælles. Hovedkontoret opretter et optællingsdokument, som kan modtages i butikken, hvor antallet af den disponible beholdning angives i MPOS eller Cloud POS. Ikke-planlagte statusoptællinger startes i en butik, og antal i den disponible lagerbeholdning opdateres i enten i MPOS eller Cloud POS. I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer. Når en status af en af typerne er fuldført, gøres den bindende og sendes til hovedkontoret. På hovedkontoret valideres antallet og bogføres.

## <a name="inventory-lookup"></a>Lagersøgning

Det aktuelle antal disponible produkter for flere butikker og lagersteder kan ses på siden Lagersøgning. Udover den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik. Det gør du ved at vælge den butik, du vil have vist DTT for, og derefter klikke på **Vis butikkens tilgængelighed**.
