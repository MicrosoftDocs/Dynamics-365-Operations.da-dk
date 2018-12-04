---
title: Butikslagerstyring
description: Denne artikel beskriver de typer af dokumenter, du kan bruge til at administrere lager.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="store-inventory-management"></a>Butikslagerstyring

[!include [banner](includes/banner.md)]

Denne artikel beskriver de typer af dokumenter, du kan bruge til at administrere lager.

Du kan bruge følgende typer dokumenter til at administrere organisationens lager.

## <a name="purchase-orders"></a>Indkøbsordrer
Indkøbsordrer oprettes på hovedkontoret. Hvis et detaillagersted er medtaget i indkøbsordrehovedet, kan ordren modtages i butikken ved hjælp af Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail. Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere. Alternativt kan antallet bindes og sendes til hovedkontoret. På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på indkøbsordren.

## <a name="transfer-orders"></a>Flytteordrer
En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan afsendes fra. I dette tilfælde vises flytteordren i butikken som en plukanmodning i MPOS eller Cloud POS. Når de antal, der er anmodet om, er blevet plukket, gøres de bindende og sendes til hovedkontoret. På hovedkontoret vises det antal, der er plukket i butikken, i Dynamics 365 for Retail, i feltet **Afsend nu** i flytteordren. En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan sendes til. I dette tilfælde vises flytteordren i butikken som en tilgangsanmodning i MPOS eller Cloud POS. Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere. Alternativt kan antallet bindes og sendes til hovedkontoret. På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på flytteordren.

## <a name="stock-counts"></a>Lagerstatus
Status kan enten være planlagt eller ikke-planlagt. Planlagte statusopgørelser startes i hovedkontoret, der angiver, hvilke varer der skal optælles. Hovedkontoret opretter et optællingsdokument, som kan modtages i butikken, hvor antallet af den disponible beholdning angives i MPOS eller Cloud POS. Ikke-planlagte statusoptællinger startes i en butik, og antal i den disponible lagerbeholdning opdateres i enten i MPOS eller Cloud POS. I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer. Når en status af en af typerne er fuldført, gøres den bindende og sendes til hovedkontoret. På hovedkontoret valideres antallet og bogføres.

## <a name="inventory-lookup"></a>Lagersøgning
Det aktuelle antal disponible produkter for flere butikker og lagersteder kan ses på siden Lagersøgning. Udover den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik. Det gør du ved at vælge den butik, du vil have vist DTT for, og derefter klikke på **Vis butikkens tilgængelighed**.





