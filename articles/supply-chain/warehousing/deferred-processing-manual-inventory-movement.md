---
title: Udskudt behandling af manuelle lagerbevægelser
description: Dette emne beskriver, hvordan du bruger udskudt behandling af manuelle lagerbevægelser i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a15c913c876e961c6824c1e8812ab2be2d6ffa4333cd0d4e6f80cae8bac79394
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746741"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Udskudt behandling af manuelle lagerbevægelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du bruger udskudt behandling af manuelle lagerbevægelser i Microsoft Dynamics 365 Supply Chain Management.

Udskudt behandling betyder, at lagermedarbejdere kan fortsætte med at udføre andet arbejde, mens en læg på lager-operation behandles i baggrunden. Udskudt behandling er nyttig, når serveren kan have lejlighedsvise eller ikke-planlagte stigninger i behandlingstiden, og den øgede behandlingstid kan påvirke arbejderens produktivitet. Arbejdstypen *Lagerbevægelse* er nu føjet til det sæt arbejdstyper, som denne funktion understøtter.

Baggrundsbehandling udføres med [funktionen Behandl app-hændelser for lagersted](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Du skal aktivere dem i følgende rækkefølge:

1. Blokering af arbejde i hele organisationen
1. Proces for hændelser for lagerapp
1. Udskudte læg på lager-handlinger
1. Udskudt behandling af manuel lagerbevægelseshandling

## <a name="configure-the-work-processing-policies"></a>Konfigurere politikker for arbejdsbehandling

Hvis du vil bruge udskudt behandling, skal du konfigurere og bruge en arbejdsbehandlingspolitik. For udskudt behandling af Læg på lager understøtter [funktionen Udskudt behandling af lagerstedsarbejde](deferred-put.md) følgende arbejdstyper: *Salgsordre*, *Flytteordreafgang* og *Opfyldning*. Funktionerne for *Udskudt behandling af manuel lagerbevægelsesoperation* tilføjer en ny arbejdstype: *Lagerbevægelser*.

Hvis du vil konfigurere en politik for arbejdsbehandling, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Arbejde \> Politikker for arbejdsbehandling**.
1. Vælg en eksisterende politik på listen, eller opret en ny politik ved at vælge **Ny** i handlingsruden. Overskriften for hver politik indeholder følgende felter:

    - **Navn på politik for arbejdsbehandling** – Navnet på politikken for arbejdsbehandling.
    - **Beskrivelse:** – En beskrivelse af politikken for arbejdsbehandling.

1. Konfigurer den samling af regler, som politikken skal gælde for, i oversigtspanelet **Behandlingsregler**. Brug følgende knapper på værktøjslinjen til at tilføje og fjerne regler efter behov. For hvert regelsæt skal du angive følgende felter:

    - **Arbejdsordretype** – Vælg den arbejdstype, som politikken gælder for.
    - **Operation** – Vælg den operation, som politikken skal behandle. Hvis du har valgt *Lagerbevægelse* i feltet **Arbejdsordretype**, behøver du ikke angive dette felt, da operationer for pluk og læg på lager behandles som en enkelt hændelse.
    - **Arbejdsbehandlingsmetode** – Vælg den metode, der skal bruges til behandling af arbejdslinjen. Hvis du vælger *Øjeblikkelig*, ligner funktionsmåden, når ingen arbejdsbehandlingspolitikker bruges til at behandle linjen. Hvis du vælger *Udskudt*, anvendes systemet udskudt behandling, der bruger batchstruktur.
    - **Udskudt behandlingsgrænse** – Hvis du angiver dette felt til *0* (nul), er der ingen tærskel. I dette tilfælde bruges behandlingsmetoden *Udskudt*, hvis det er muligt. Hvis den specifikke tærskelberegning er under tærsklen, anvendes metoden *Øjeblikkelig*. Ellers bruges metoden *Udskudt*, hvis det er muligt. For salgs- og overførselsrelateret arbejde beregnes tærsklen som antallet af tilknyttede kildelastlinjer, der behandles for arbejdet. For genopfyldningsarbejde beregnes tærsklen som antallet af arbejdslinjer, der genopfyldes af arbejdet. Ved at sætte en tærskel på for eksempel *5* for salg, sikrer du, at mindre opgaver med færre end fem oprindelige kildebelastningslinjer ikke bruger udskudt behandling, mens større opgaver gør det. Tærsklen har kun virkning, hvis feltet **Arbejdsbehandlingsmetode** er indstillet til *Udskudt*.
    - **Batchgruppe for udskudt behandling** – Angiv den batchgruppe, der bruges til behandling. Hvis du har valgt *Lagerbevægelse* i feltet **Arbejdsordretype**, behøver du ikke angive dette felt, da batchgruppen er markeret i dialogboksen **Behandl hændelser i lagerstedsapp**.

## <a name="assign-the-work-creation-policy"></a>Tildele politik for oprettelse af arbejde

Du kan finde flere oplysninger om, hvordan du tildeler en politik for oprettelse af arbejde, i [Udskudt behandling af lagerstedsarbejde](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere et batchjob, der skal behandle hændelser i lagerstedsapp

Hvis du vil bruge processen *Udskudt behandling af manuel lagerbevægelsesoperation*, skal du konfigurere et planlagt batchjob.

1. Gå til **Lokationsstyring \> Periodiske opgaver \> Hændelsesbehandling i lagerstedsapp**.
1. I dialogboksen **Behandl hændelser i lagerstedsapp** skal du i oversigtspanelet **Kør i baggrunden** angive indstillingen **Batchbehandling** til *Ja*.
1. Vælg **Gentagelse**, og opret en kørselsplan, der opfylder kravene i din virksomhed.
1. Vælg **OK** i hver dialogboks.

## <a name="inquire-about-the-warehouse-app-events"></a>Forespørge om hændelser i lagerstedsapp

Du kan få vist den hændelseskø og de hændelsesmeddelelser, som lagerstedsappen genererer, ved at gå til **Lagerstedsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.

Meddelelser om hændelsen *Lagerbevægelse* vil have statussen *Kø*, når de oprettes første gang. Denne status angiver, at batchjobbet **Behandl hændelser i lagerstedsapp** vil tage hændelsesmeddelelser og behandle dem. Når statussen er opdateret til *Fuldført*, slettes alle relaterede hændelser fra køen.

Alle hændelser for *Lagerbevægelse* samles under én samling pr. hændelsestype og lagersted.

Batchjobbet behandler hændelserne i lagerstedsappen ifølge den gentagelse, der er angivet i dialogboksen **Behandl hændelser i lagerstedsapp**. Indtil en meddelelse er behandlet, kan du derfor finde lagersteds-id'et ved at søge i feltet **Identifikator**.

Meddelelsens detaljer indeholder bevægelsesdetaljerne (f.eks. "fra"- og "til"-lokationer).

Du kan finde flere oplysninger under [Hændelsesbehandling i lagerstedsapp](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurere mobilenhedens menu til at springe over politikken for udskudt behandling

Yderligere oplysninger om, hvordan du konfigurerer mobilenhedsmenuen til at springe over politikken for udskudt behandling, finder du i [Udskudt behandling af lagerstedsarbejde](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Påvirkning af datoer for lukket arbejde

Du kan finde flere oplysninger om virkningen af lukkede arbejdsdatoer i [Udskudt behandling af lagerstedsarbejde](deferred-put.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Udskudt behandling af lagerstedsarbejde](deferred-put.md)
- [Hændelsesbehandling af lagerstedsapp](warehouse-app-events.md)
- [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
