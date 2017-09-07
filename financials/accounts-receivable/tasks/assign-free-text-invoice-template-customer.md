--- 
title: Tildele en skabelon til fritekstfakturaer til en debitor
description: Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: af9e5f499e6c162189443d95c90b15c17d910739
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Tildele en skabelon til fritekstfakturaer til en debitor

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor. Denne opgave bruger USMF-demofirmaet og er beregnet til den bruger, der er ansvarlig for håndtering af og behandling af debitorfakturaer.

1. Gå til Debitor > Kunder > Alle kunder.
2. Find og vælg den ønskede post på listen.
3. Klik på Faktura i handlingsruden.
4. Klik på Tilbagevendende fakturaer.
    * Du kan bruge denne side til at knytte fritekstfakturaskabeloner til debitorer og angive, hvor ofte fakturaer sendes til debitoren.  
5. Klik på Ny for at tildele en ny skabelon til debitoren.
6. Vælg den fritekstfakturaskabelon, du vil tildele debitoren.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Angiv den dato, hvor den første faktura vil blive genereret.
    * Angiv en tilbagevendende slutdato.  
    * Vælg en af følgende: Slutdato mangler – Fakturaer genereres i det uendelige, indtil skabelonen fjernes fra debitorkontoen.  Faktureringsslutdato – Vælg denne indstilling, og angiv den sidste dato, hvor fakturaen kan genereres.  
    * Maksimalt akkumuleret beløb, hvorefter genereringen af fakturaer stopper.  
    * Indtast det maksimale akkumulerede beløb, der kan nås med den valgte skabelon. Hvis du f.eks. indtaster 1.000,00 og genererer månedlige fakturaer for hver 100,00, stopper genereringen af fakturaer, når den 10. faktura er genereret.  
    * Generer tilbagevendende fakturaer ved hjælp af standardværdierne fra enten fritekstfakturaskabelonen eller debitorkontoen.  
    * Vælg, om du vil bruge skabelonen til fritekstfakturaer eller debitorkontoen til at bestemme standardværdierne for sprog, posteringsprofil, momsgruppe, varemomsgruppe, listekode, land/region til levering, valuta, betalingsbetingelser, betalingsmetode, betalingsspecifikation, betalingsplan, kasserabat, økonomiske dimensioner og giroindbetalingskort, når fakturaer oprettes.  
10. Vælg gentagelsesmønsteret.
    * Dagligt – Vælg denne indstilling, og indtast antallet af dage i feltet Pr. Hvis du f.eks. indtaster 15, genereres der en faktura til debitoren hver 15. dag.  Ugentligt – Vælg denne indstilling, og indtast antallet af uger i feltet Pr. Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hver anden uge.  Månedligt – Vælg denne indstilling, og indtast antallet af måneder i feltet Pr. Hvis du f.eks. indtaster 6, genereres der en faktura til denne debitor hver sjette måned.  Årligt – Vælg denne indstilling, og indtast antallet af år i feltet Pr. Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hvert andet år.  
11. Angiv et tal i feltet Pr.

