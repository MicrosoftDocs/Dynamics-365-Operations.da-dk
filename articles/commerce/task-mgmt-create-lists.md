---
title: Oprette opgavelister og tilføje opgaver
description: Dette emne indeholder en beskrivelse af, hvordan du opretter opgavelister og føjer opgaver til dem i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2e6bd69435ee8fe58dbbf66eb0c5eee3d2ec09ee1998ef0218cdef643522c5bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756519"
---
# <a name="create-task-lists-and-add-tasks"></a>Oprette opgavelister og tilføje opgaver

[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du opretter opgavelister og føjer opgaver til dem i Microsoft Dynamics 365 Commerce.

En *opgave* definerer et bestemt arbejde eller en handling, som en anden skal udføre på eller før en angivet forfaldsdato. I Dynamics 365 Commerce kan en opgave indeholde detaljerede instruktioner og oplysninger om en kontaktperson. Den kan også indeholde links til bagbutikshandlinger, POS-handlinger eller webstedssider, som medvirker til at forbedre produktiviteten og levere den kontekst, som opgaveejeren kræver for at kunne fuldføre opgaven effektivt.

En *opgaveliste* er en samling opgaver, der skal fuldføres som en del af en forretningsproces. Der kan f.eks. være en opgaveliste, som en ny arbejder skal udfylde under indlæringen, en opgaveliste til kasserere, der arbejder på et skiftehold, eller en opgaveliste, der skal fuldføres for at forberede butikken på den kommende ferie. I Commerce kan alle de opgavelister, der har en måldato, tildeles et vilkårligt antal butikker eller medarbejdere, og den kan konfigureres til at gentages.

Både ledere og arbejdere kan oprette opgavelister på Commerce-bagkontor og derefter knytte dem til et sæt butikker.

## <a name="create-a-task-list"></a>Opret en opgaveliste

Brug følgende trin for at oprette en opgaveliste.

1. Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.
1. Vælg **Ny**, og angiv derefter værdier i felterne **Navn**, **Beskrivelse** og **Ejer**.
1. Vælg **Gem**.

## <a name="add-tasks-to-a-task-list"></a>Føje opgaver til en opgaveliste

Følg disse trin for at føje opgaver til en opgaveliste.
 
1. Vælg **Ny** i oversigtspanelet **Opgaver** af en eksisterende opgaveliste for at tilføje en opgave.
1. Skriv et navn på opgaven i feltet **Navn** i dialogboksen **Opret en ny opgave**.
1. Angiv en positiv eller negativ heltalsværdi i feltet **Forskydning af forfaldsdato fra måldato**. Skriv f.eks. **-2** , hvis opgaven skal fuldføres to dage før opgavelistens forfaldsdato.
1. Angiv detaljerede instruktioner i feltet **Bemærkninger**.
1. Skriv navnet på en ekspert på emnet, som opgaveejeren kan kontakte, hvis han eller hun har brug for hjælp, i feltet **Kontaktperson**.
1. Skriv et link baseret på opgavens art i feltet **Opgavelink**.

> [!TIP]
> Selvom du kan bruge feltet **Tildelt til** for at tildele opgaver til en person, mens du opretter en opgaveliste, anbefaler vi, at du undgår at tildele opgaver under oprettelse af opgaveliste. I stedet skal du tildele opgaverne, når listen er instantieret for de enkelte butikker.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Brug opgavelinks som en hjælp til at forbedre medarbejderens produktivitet

Med Commerce kan du sammenkæde opgaver med bestemte POS-handlinger, f.eks. køre en salgsrapport, få vist en video med onlineundervisning til orientering for nye medarbejder eller udføre en sikkerhedskopiering af et kontor. Denne funktion hjælper opgaveejere med at få de oplysninger, de skal bruge til at udføre en opgave mere effektivt.

Hvis du vil tilføje opgavelinks, mens du opretter en opgave, skal du følge disse trin.

1. Vælg **Rediger** i oversigtspanelet **Opgaver** af en eksisterende opgaveliste.
1. Vælg en eller flere af følgende indstillinger i feltet **Opgavelink** i dialogboksen **Rediger opgave**:

    - Vælg **Menupunkt** for at konfigurere en butikshandling, f.eks. "Produktpakker".
    - Vælg **POS-handling** for at konfigurere en POS-handling, f.eks. "Salgsrapporter".
    - Vælg **URL-adresse** for at konfigurere en absolut URL-adresse.

I følgende illustration vises valget af opgavelinks i dialogboksen **Rediger opgave**.

![Vælge opgavelinks i dialogboksen Rediger opgave.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Konfigurere en POS-handling, så den kan kædes sammen med en opgave

Du konfigurerer en POS-handling, så den kan kædes sammen med en opgave, ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.
1. Vælg **Rediger**, find POS-handlingen, og vælg derefter afkrydsningsfeltet **Aktivér opgavestyring** for den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over opgavestyring](task-mgmt-overview.md)

[Konfigurer opgavestyring](task-mgmt-configure.md)

[Tildele opgavelister til butikker eller medarbejdere](task-mgmt-assign-lists.md)

[Opgavestyring i POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
