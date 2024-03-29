---
title: Tildele en skabelon til fritekstfakturaer til en debitor
description: Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49074c11659ae30fd2decdb93b4721441edff2c5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780472"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Tildele en skabelon til fritekstfakturaer til en debitor

[!include [banner](../../includes/banner.md)]

Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor. Denne opgave bruger USMF-demofirmaet og er beregnet til den bruger, der er ansvarlig for håndtering af og behandling af debitorfakturaer.

1. I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.
2. Find og vælg den ønskede post på listen.
3. Klik på **Faktura** i **handlingsruden**.
4. Klik på **Tilbagevendende fakturaer**. Du kan bruge denne side til at knytte fritekstfakturaskabeloner til debitorer og angive, hvor ofte fakturaer sendes til debitoren.  
5. Klik på **Ny** for at tildele debitoren en ny skabelon.
6. Vælg den fritekstfakturaskabelon, du vil tildele debitoren, i feltet **Skabelon**.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Angiv den dato, hvor den første faktura skal genereres, i feltet **Faktureringsstartdato**.
10. Angiv en slutdato for gentagelse i sektionen **Slut på gentagelse**.  
    Vælg en af følgende indstillinger: 
    - **Slutdato mangler** – Fakturaer genereres i det uendelige, indtil skabelonen fjernes fra debitorkontoen.
    - **Faktureringsslutdato** – Vælg denne indstilling, og angiv den sidste dato, hvor fakturaen kan genereres.  
11. Angiv det maksimale akkumulerede beløb, efter hvilket fakturagenerering skal stoppe, i feltet **Maksimalt akkumuleret beløb**. Indtast det maksimale akkumulerede beløb, der kan nås med den valgte skabelon. Hvis du f.eks. indtaster 1.000,00 og genererer månedlige fakturaer for hver 100,00, stopper genereringen af fakturaer, når den 10. faktura er genereret.  
12. I sektionen **Generer tilbagevendende fakturaer ved hjælp af standardværdierne fra** skal du enten vælge fritekstfakturaskabelonen eller debitorkontoen. Vælg, om du vil bruge skabelonen til fritekstfakturaer eller debitorkontoen til at bestemme standardværdierne for sprog, posteringsprofil, momsgruppe, varemomsgruppe, listekode, land/region til levering, valuta, betalingsbetingelser, betalingsmetode, betalingsspecifikation, betalingsplan, kasserabat, økonomiske dimensioner og giroindbetalingskort, når fakturaer oprettes.  
13. Vælg gentagelsesmønsteret i feltet **Gentagelsesmønster**.
    - **Dagligt** – Vælg denne indstilling, og indtast antallet af dage per felt. Hvis du f.eks. indtaster 15, genereres der en faktura til debitoren hver 15. dag.
    - **Ugentligt** – Vælg denne indstilling, og indtast antallet af uger i per felt. Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hver anden uge.
    - **Månedligt** – Vælg denne indstilling, og indtast antallet af måneder i per felt. Hvis du f.eks. indtaster 6, genereres der en faktura til denne debitor hver sjette måned.
    - **Årligt** – Vælg denne indstilling, og indtast antallet af år per felt. Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hvert andet år.  
14. Brug feltet **Pr.** til at angive et antal.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
