---
title: Oprette en fritekstfaktura
description: Dette emne forklarer, hvordan du opretter fritekstfakturaer.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1ac06e7d702ffe3a8cdb6bd2823f2ffdc055c722
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441427"
---
# <a name="create-a-free-text-invoice"></a>Oprette en fritekstfaktura

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter fritekstfakturaer. I proceduren skal du bruge **USMF**-demoregnskabet.

## <a name="create-a-free-text-invoice"></a>Opret en fritekstfaktura

1. Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.
2. Vælg **Ny**.
3. Vælg en værdi i feltet **Debitorkonto**.

    * Fakturakontoen er som standard konto, der er valgt som debitorkontoen.
    * Regnskabsstatus begynder med **Igangværende**, hvis fakturaen ikke er bogført.
    * Fakturanummeret tildeles, når fakturaen bogføres.
    * Hvis du bruger bemyndigelser af typen Fælles eurobetalingsområde (SEPA), angives bemyndigelsen til Direct Debit automatisk, når du vælger debitorkontoen.

4. Indtast en værdi i feltet **Beskrivelse**.
5. Angiv et kontonummer, der ikke har dimensioner, i feltet **Hovedkonto**. Du skal angive dimensioner senere i dette emne.

    Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde kontoen.

6. Vælg oversigtspanelet **Linjedetaljer** for at føje dimensioner til hovedkontoen.
7. Vælg fanen **Økonomisk dimensionslinje**.

    * Dimensionerne er kun for den valgte linje.
    * Momsgruppen udfyldes som standard fra debitoren. Hvis debitoren ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.
    * Varemomsgruppen udfyldes fra hovedkontoen. Hvis hovedkontoen ikke har en varemomsgruppe, bruges den varemomsgruppe, der er angivet i momsparametrene i Finans.

8. Valgfrit: Angiv et tal i feltet **Antal**.
9. Valgfrit: Angiv et nummer i feltet **Enhedspris**.

    Beløbet beregnes som antallet ganget med enhedsprisen. Du kan dog tilsidesætte denne beregning ved at angive et beløb.

10. Vælg **Moms** for at få vist den moms, der er beregnet for fakturaen.

    Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene under fanen **Regulering**.

11. Vælg **OK**.
12. Vælg **Gebyrer** for at føje et gebyr til fakturaen.
13. Skriv en værdi i feltet **Gebyrkode**.
14. Indtast et tal i feltet **Gebyrværdi**.
15. Luk siden.
16. Vælg **Totaler** for at få vist en opsummering af fakturadetaljerne og totalerne.
17. Vælg **Luk**.
18. Vælg **Bogfør** for at bogføre fakturaen. Du har stadig mulighed for at annullere, før du bogfører.

    * Du kan ændre tidspunktet for udskrivning af fakturaer. Vælg **Aktuel** for at udskrive hver faktura, når den opdateres. Vælg **Efter** for at udskrive alle fakturaer, der er blevet opdateret.
    * Hvis du vil ændre, hvordan debitors kreditmaksimum kontrolleres, før fakturaen bogføres, kan du ændre værdien i feltet **Kreditmaksimumtype**.
    * Vælg **Ja** i denne indstilling for at udskrive fakturaen.
    * Vælg **Ja** i denne indstilling for at bogføre fakturaen. Du kan udskrive fakturaen uden at bogføre den.

19. Vælg **OK**.

## <a name="copy-lines"></a>Kopiér linjer
Hvis du vil kopiere linjer i en fritekstfaktura, skal du vælge en eller flere linjer og derefter vælge **Kopier valgte linjer**. Du kan angive antallet kopier, der skal tages, og du kan også kopiere noter og vedhæftede filer. Du kan enten kopiere fordelingerne eller lade, at de oprettes igen, når du bogfører.

Når du har kopieret linjerne, kan du derefter redigere oplysningerne efter behov.

## <a name="create-a-free-text-invoice-from-a-template"></a>Oprette en fritekstfaktura fra en skabelon
Du kan oprette en fritekstfaktura fra en skabelon. Når du vælger **Ny ud fra skabelon** under fanen **Faktura**, kan du vælge et skabelonnavn og debitorkontoen for den nye fritekstfaktura. Standardværdier, f.eks. betalingsbetingelserne og betalingsmåden, kan udfyldes automatisk fra debitoren, eller du kan bruge de værdier, der blev gemt i skabelonen.

Der oprettes en ny fritekstfaktura, og du kan redigere værdierne efter behov.
