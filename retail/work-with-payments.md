---
title: Betalingsmetoder i et callcenter
description: I dette emne beskrives de forskellige betalingsformer, du kan bruge i et callcenter i Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 07cb1bcb3870b96e34f7f6725fe5b7da32628fde
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="payment-methods-in-a-call-center"></a>Betalingsmetoder i et callcenter

[!include[banner](includes/banner.md)]


I dette emne beskrives de forskellige betalingsformer, du kan bruge i et callcenter i Dynamics 365 for Retail.

De betalingsformer, der anvendes i andre kanaler, såsom kontanter, checks, kreditkort og gavekort, kan også bruges i callcentre. Når du har konfigureret en betalingsmetode for et callcenter, vises den som en af indstillingerne i sektionen **Betalinger** på siden **Salgsordre** for callcenter-brugere. Du kan desuden oprette kuponer for at tilbyde rabatter til kunder, som afgiver en ordre til din organisations callcenter. Kuponer kan være for en rabat på fast beløb eller for en procentdel af en varepris eller ordretotalen. For eksempel kan en beløbsbaseret kupon tilbyde kunderne en rabat på 75,00, når kunden bruger 750,00 eller mere. Du kan oprette forskellige typer af kuponer, definere overordnet/underordnet kuponer og kopiere eller annullere en kupon. Brug indstillingerne i følgende tabel til at oprette kuponer.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Attribut**             | I feltet **Indløsningssats** skal du angive den forventede indløsningssats på kuponen som en procentdel og derefter vælge, om kuponen kan bruges som en engangskupon, skal udstedes igen automatisk eller gælder specifikt for kunden.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Gyldig**                 | Angiv datoerne for den første og sidste dag, hvor kuponen gælder, i felterne **Startdato** og **Slutdato**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Medtag/udelad regler** | I felterne **Kataloger** og **Varer** skal du vælge, om alle kataloger eller varer skal medtages eller ej i kuponen. Hvis du vælger **Medtag** eller **Udeluk**, skal du klikke på **Opsætning**, vælge **Medtag/Udelad kataloger** eller **Medtag/Udelad produkter** og angive oplysninger om katalog eller vare. Hvis du vælger **Ingen** i disse felter, medtages alle kataloger eller varer i kuponen.                                                                                                                                                                                                                          |
| **Diverse**         | Hvis denne rabatkupon ikke kan bruges sammen med andre rabatter, skal du markere afkrydsningsfeltet **Eksklusiv**. I feltet **Oprindelse** skal du vælge, hvor kuponen kan bruges. Hvis denne kupon er en producents kupon, skal du markerer afkrydsningsfeltet **Producentens kupon**.                                                                                                                                                                                                                                                                                                                                                                |
| **Fremtidig kupon**         | Hvis denne kupon skal tilknyttes andre kuponer som overordnet kupon, skal du markere afkrydsningsfeltet **Overordnet kupon**. Hvis denne kupon skal tilknyttes en eksisterende kupon, skal du vælge den overordnede kupon i feltet **Overordnet kupon-id**. For eksempel kan du oprette en kupon for det kommende forårskatalog. Alle andre kuponer, som du opretter for forårskataloget, bliver underordnede kuponer til forårskatalogkuponen. Underordnede kuponer kan indeholde 20 procent rabat for nye kundeordrer, 10 procent rabat på en vare, der er udgivet for nylig, eller en rabat på 95,00 kr. på ordrer på 1.000,00 kr. eller derover. |

Hvis du sender en kreditkortbetaling fra siden **Salgsordrer** og modtager en meddelelse om, at kortet ikke er godkendt, kan du håndtere godkendelsen manuelt. Du kan godkende, afvise eller sende en transaktion med kreditkort fra siden **Administration af godkendelse**. Du kan bruge siden callcenter-parametre til at konfigurere yderligere indstillinger for betalingsbehandling:

-   Check på hold gør det muligt for medarbejdere i økonomiafdelingen at behandle ordrer, der er blevet sat på hold, fordi en check blev brugt som betalingsmetode, og grænsebeløbet for checken på hold blev overskredet. På hold kan frigives manuelt, eller det udløber automatisk i slutningen af den periode, der er konfigureret.
-   Du kan angive grænser, over hvilke refusioner, der udstedes via checks og kreditkort, skal godkendes manuelt. En refusion, der overstiger grænsebeløbet, føjes til godkendelseskøen. Når du godkender refusionen, kan retursalgsordren faktureres.





