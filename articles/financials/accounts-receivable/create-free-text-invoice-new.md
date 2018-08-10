--- 
title: Opret en fritekstfaktura
description: I denne artikel vises, hvordan du opretter en fritekstfaktura.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Opret en fritekstfaktura

[!include [banner](../includes/banner.md)]

I denne artikel vises, hvordan du opretter en fritekstfaktura. I denne procedure skal du bruge USMF-demoregnskabet.

## <a name="create-a-free-text-invoice"></a>Opret en fritekstfaktura

1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Vælg en værdi i feltet Debitorkonto.
    * Fakturakontoen er som standard den samme konto, der er brugt til debitorkontoen.   
    * Regnskabsstatus begynder med Igangværende, hvis fakturaen ikke er bogført.   
    * Fakturanummeret tildeles, når fakturaen bogføres.  
    * Hvis du bruger SEPA-bemyndigelser, udfyldes bemyndigelsen til Direct Debit automatisk med en bemyndigelse, når du vælger debitorkontoen.  
4. Skriv en værdi i feltet Beskrivelse.
5. Angive et kontonummer uden dimensioner i feltet Hovedkonto.
    * Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde din konto. Du skal angive dimensioner senere i denne vejledning.  
6. Udvid oversigtspanelet Linjedetaljer, så du kan føje dimensioner til din hovedkonto.
7. Klik på fanen Økonomisk dimensionslinje.
    * Dimensionerne er kun for den valgte linje.    
    * Momsgruppen udfyldes fra kunden. Hvis kunden ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.  
    * Varemomsgruppen hentes fra hovedkontoen. Hvis hovedkontoen ikke har en varemomsgruppe, bruges varemomsgruppen fra momsparametrene i Finans.    
8. Angiv et tal i feltet Antal.
    * Antallet er valgfrit.  
9. Angiv et tal i feltet Enhedspris.
    * Enhedsprisen er valgfri.  
    * Beløbet beregnes som antallet ganget med enhedsprisen. Du kan dog tilsidesætte denne beregning og angive et beløb.  
10. Klik på Moms for at få vist den moms, der er beregnet for din faktura.
    * Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene på fanen Regulering.  
11. Klik på OK.
12. Klik på Gebyrer for at føje et gebyr til din faktura. 
13. Skriv en værdi i feltet Gebyrkode.
14. Indtast et tal i feltet Gebyrværdi.
15. Luk siden.
16. Klik på Totaler for at få vist opsummerede fakturadetaljer og totaler.
17. Klik på Luk.
18. Klik på Bogfør for at bogføre fakturaen. Du kan annullere, før du bogfører.
    * Sådan ændrer du tidspunktet for fakturaudskrivning: Vælg Aktuel for at udskrive hver faktura, når den opdateres, eller vælg Efter for at udskrive alle fakturaer, der er blevet opdateret.  
    * Hvis du vil ændre, hvordan kundens kreditmaksimum kontrolleres før bogføring, skal du ændre kreditmaksimumtypen.  
    * Hvis du vil udskrive fakturaen, skal du vælge Ja.  
    * Hvis du vil bogføre fakturaen, skal du vælge Ja. Du kan udskrive fakturaen uden bogføring.  
19. Klik på OK.

## <a name="copy-lines"></a>Kopiér linjer
Hvis du vil kopiere linjer i fritekstfakturaen, skal du vælge en eller flere linjer og derefter klikke på Kopier valgte linjer. Du kan angive antallet kopier, du vil foretage, og du kan også kopiere noter og vedhæftede filer. Du kan kopiere fordelingerne, eller tillade at de oprettes igen, når du bogfører. Når du har kopieret linjerne, kan du derefter redigere oplysningerne efter behov. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Oprette en fritekstfaktura fra en skabelon
Du kan oprette en fritekstfaktura fra en skabelon. Når du vælger Ny ud fra skabelon under fanen Faktura, kan du vælge et skabelonnavn og debitorkontoen for den nye fritekstfaktura. Du kan også vælge at bruge standardværdier, f.eks. betalingsbetingelserne og betalingsmåden fra debitoren, eller du kan bruge de værdier, der blev gemt sammen med skabelonen. Der oprettes en ny fritekstfaktura, og du kan redigere værdierne i fakturaen. 


