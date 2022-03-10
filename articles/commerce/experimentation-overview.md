---
title: Eksperimenteren i Dynamics 365 Commerce
description: Med eksperimenteren kan du oprette, redigere og administrere sidelayout og indholdsbehandlinger i webstedsgeneratoren. Understøttelse af eksperimenteren fra start til slut er aktiveret for e-handelssider og enheder på en side.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 292a8934e735c76389e36603a708fd2a1bbf7691
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986535"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimenteren i Dynamics 365 Commerce
Brug eksperimenteren i Dynamics 365 Commerce til at validere hypoteser om effektiviteten af dine e-handelssider, og tag beslutninger med databaseret sikkerhed. Commerce understøtter A/B-test på sider, moduler og fragmenter og giver dig mulighed for at måle virkningen af foreslåede ændringer på dit websted.

Du kan oprette, redigere og administrere behandlinger af sider og indhold, der kaldes **variationer**, i Commerce-webstedsgeneratoren. Commerce kan integreres med tredjepartstjenester, som du kan bruge til at oprette eksperimenter og behandlingstildelinger. Hændelsesstrømme i realtid, der er registreret i Commerce, giver den analyse, der definerer eksperimenters resultater i tredjepartstjenesten. Du kan derefter udnytte analyserne til support eller afvise din hypotese.

## <a name="set-up-prerequisites"></a> Angiv forudsætninger
1. **Få den korrekte version af Commerce** – Opgrader dit modulbibliotek, SDK for onlinekanaludvidelser og Commerce Scale Unit til Commerce version 10.0.13 eller nyere.
1. **Konfigurere en eksperimenteren-connector** - En eksperimenteren-connector giver mulighed for, at Commerce kan oprette forbindelse til tredjepartstjenester for at hente listen over eksperimenter og bestemme, hvornår et eksperiment skal vises for en bruger. Du kan købe en tredjeparts-connector fra [AppSource](https://appsource.microsoft.com). Følg de opsætningsinstruktioner, der er angivet af udgiveren. Du kan også bruge eksempeltest-connectoren fra Commerce til at teste arbejdsprocessen for eksperimenteren, uden at du behøver at konfigurere en ekstern tjeneste. Du kan finde flere oplysninger i [Konfigurere og aktivere connectorer](e-commerce-extensibility/connectors.md). 
1. **Slå funktionsflagene for Eksperimenteren til i Commerce** - Du kan aktivere Eksperimenteren på lejerniveau ved at gå til **Lejerindstillinger > Funktioner** eller på webstedsniveau i **Webstedsindstillinger > Funktioner**.
    - Aktivér **Eksperimenteren**-flaget for at oprette eksperimentvariationer af moduler på en side uden at påvirke eller kopiere andet indhold, der ikke er en del af eksperimentet. Dette sikrer, at løbende indholdsopdateringer uden for eksperimentet forbliver synkroniseret under eksperimentets livscyklus. Deaktivering af dette flag forhindrer alle eksperimenter i at blive vist for brugerne og fjerner alle redigeringsfunktioner i webstedsgeneratoren.
    - Aktivér flaget **Eksperiment på sider eller fragmenter** for at udføre eksperimenter på en side eller et fragment. Derved oprettes en fuld forekomstkopi af hele siden eller fragmentet for alle moduler på siden eller fragmentet. Brug denne tilstand, når du vil teste omfattende ændringer af indholdet, eller hvor synkronisering af igangværende indholdsændringer på tværs af forekomster ikke er et problem. Deaktivering af dette flag forhindrer oprettelse og redigering af nye eksperimenter på sider og fragmenter.
    > [!NOTE]
    > **Eksperimenteren**-flaget skal også være aktiveret for at få **Eksperiment på sider eller fragmenteringer**-funktionen til at fungere.
    
## <a name="experimentation-lifecycle"></a>Eksperimenterens livscyklus
Det er en iterativ proces at konfigurere et eksperiment, oprette variationer og køre et eksperiment. Nedenstående diagram viser livscyklussen for Eksperimenteren i Commerce og tredjepartstjenesten. 

[ ![Eksperimenterens livscyklus.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Du kan finde flere oplysninger om hvert trin i eksperimenteren-processen under følgende emner.
- [Identificere en hypotese og fastslå målepunkter for et eksperiment](experimentation-identify.md)
- [Opsætning af et eksperiment](experimentation-setup.md)
- [Oprette forbindelse til og redigere et eksperiment](experimentation-connect-edit.md)
- [Se prøveversion og publicere et eksperiment](experimentation-preview-publish.md)
- [Køre og overvåge et eksperiment](experimentation-run-monitor.md)
- [Hæv en variation og fuldfører et eksperiment](experimentation-review-complete.md)

> [!NOTE]
> Hvis du vil vide, hvor et eksperiment er i livscyklussen, skal du vælge **Eksperimenter** i venstre navigationsrude af webstedsgeneratoren. Der vises en liste over eksperimenter med status for hvert eksperiment i både Commerce og tredjepartstjenesten. Du kan finde flere oplysninger i [Gennemgå status for et eksperiment](experimentation-status.md).

## <a name="next-step"></a>Næste trin
[Identificere en hypotese og fastslå succesmålepunkter for et eksperiment](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]