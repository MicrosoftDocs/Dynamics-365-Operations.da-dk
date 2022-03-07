---
title: Definere og vedligeholde detailkanaler
description: Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes butikker i Dynamics 365 Commerce. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en butik.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2ac4a4a42447e4ee57d24548a79f43b88b03927
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213692"
---
# <a name="define-and-maintain-retail-channels"></a>Definere og vedligeholde detailkanaler

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes butikker i Dynamics 365 Commerce. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en butik.

Commerce understøtter flere detailkanaler, f.eks. onlinebutikker, callcentre og fysiske butikker. En fysisk butik kaldes en butik. Hver butik kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere. Du skal oprette alle disse elementer for en butik, før du opretter den. Når du har oprettet butikken, kan du tildele de produkter, som skal føres i denne butik. Du skal også knytte medarbejdere, kasseapparater og kunder til butikken. Endelig kan føje den nye butik til et organisationshierarki.

## <a name="setting-up-stores"></a>Konfigurere butikker

Før du kan konfigurere en butik i Commerce, skal du udføre nogle nødvendige opgaver. Du kan derefter oprette butikken og tilføje oplysninger.

### <a name="prerequisites"></a>Forudsætninger

Du skal fuldføre følgende opgaver, før du kan konfigurere en butik:

1. Konfigurer organisationsstrukturen, og opret organisationshierarkier for detailudvalg, genopfyldning og rapportering.
2. Opret et lager, der repræsenterer butikken.
3. Definer nummerserier til butikker, butiksopgørelser og opgørelsesbilag.
4. Konfigurer parametre for Commerce.
5. Konfigurer betalingsmetoderne, som butikken accepterer.
6. Hvis du vil behandle kreditkorttransaktioner på butikkens POS-kasseapparater, kan du også konfigurere betalingstjenester.
7. Konfigurer momsgrupper.
8. konfigurer produkter. Som en del af denne opgave skal du oprette produkthierarkier, produktvarianter og produktudvalg.
9. Konfigurer produktprisgrupper.
10. Konfigurer produktpriser. Som en del af denne opgave skal du også konfigurere prisjusteringer, rabatter og rabatperioder.
11. Opsætning af medarbejdere.

    > [!NOTE]
    > Du skal også tildele relevante tilladelser til arbejdstagerne, så de kan logge på og udføre opgaver ved hjælp af POS-systemet.

12. Konfigurer de POS-profiler, som du vil tildele til butikken. Denne opgave omfatter mange andre opgaver, f.eks. opsætning af registre, konfiguration af offlineprofiler samt opsætning af kvitteringsformater og -profiler.

Gennemse alle de opgaver, der er inkluderet i forudsætningerne, og udfør kun de opgaver, der gælder for dig.

### <a name="set-up-a-store"></a>Opsætning af en butik

Når du har fuldført de nødvendige opgaver, skal du udføre disse opgaver for at konfigurere oplysninger til butikken:

1. Opret en butik.
2. Knyt en momsgruppe til butikken.
3. Tildel de accepterede betalingsmetoder til butikken.
4. Føj oplysninger til produktbeskrivelserne for de produkter, du tilbyder i dine butikker. Du kan for eksempel tilføje RTF-tekst og billeder. Disse produktoplysninger vises i forskellige sammenhænge som på POS-kasseapparat eller på udskrevne etiketter.
5. Føj butikken til det standardorganisationshierarki, der er tildelt med formålet **Detailudvalg**, **Detailgenopfyldning** eller **Detailrapportering**.

### <a name="after-you-set-up-a-store"></a>Når du har oprettet en butik

Når du har angivet oplysningerne om butikken, skal du udføre disse opgaver for at sende de nye butiksdata til POS:

1. Konfigurer POS-kasseapparaterne til butikken.
2. Tildel produktudvalg til butikken.
3. Du kan behandle udvalg for at oprette listen over produkter, der indgår i udvalget, og for at gøre produkterne tilgængelige i butikken.
4. Send data som f.eks. nummerserier, hardwareprofiler og layout for POS-skærmen til POS-kasseapparaterne.
5. Udgiv butikken for at sende lagringsdata til POS.
6. Kør jobbene for at sende dataene til POS.

## <a name="organization-hierarchies"></a>Organisationshierarkier

Commerce bruger organisationshierarkier til at strukturere kanaler. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af. Når du opretter butikker, kan du føje dem til et organisationshierarki. Butikkerne deler derefter data, der bruges til udvalg, genbestilling og rapportering.

> [!NOTE]
> Hvis du vil bruge funktionaliteten Commerce Sales, skal konfigurationsnøglen for **Flere leveringssteder** være aktiveret. Denne konfigurationsnøgle kan findes i **Konfigurationsnøgler til handel** under **Systemadministration**\> **Opsætning** \> **Licenskonfiguration**. Dette er påkrævet på grund af forskellige valideringer, som er baseret på den leveringsadresse, der er konfigureret på salgsordrelinjeniveau.



[!INCLUDE[footer-include](../includes/footer-banner.md)]