---
title: Definere detailkanalkommunikation (Commerce Data Exchange)
description: "Denne artikel indeholder en oversigt over Commerce Data Exchange og dets komponenter. Den beskriver den rolle, som hver komponent spiller i overførslen af data mellem Microsoft Dynamics 365 for Retail og detailkanaler."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Definere detailkanalkommunikation (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over Commerce Data Exchange og dets komponenter. Den beskriver den rolle, som hver komponent spiller i overførslen af data mellem Microsoft Dynamics 365 for Retail og detailkanaler.

<a name="overview"></a>Overblik
--------

Commerce Data Exchange er et system, der overfører data mellem Dynamics 365 for Retail og detailkanaler, som f.eks. onlinebutikker eller fysiske butikker. Den database, der gemmer data for en detailkanal, er adskilt fra Dynamics 365 for Retail-databasen. Kanaldatabasen indeholder kun de data, der skal bruges til detailtransaktioner. Masterdata er konfigureret i Dynamics 365 for Retail og distribueres til kanaler. Transaktionsdata oprettes i POS-systemet eller onlinebutikken, og overføres derefter til Dynamics 365 for Retail. Datadistribution er asynkron. Processen med at indsamle og pakke data ved kilden sker med andre ord separat fra processen med at modtage og anvende data på destinationen. I nogle scenarier, som pris- og lageropslag, skal data hentes i realtid. For at understøtte disse scenarier indeholder Commerce Data Exchange også en tjeneste, der gør kommunikation i realtid mellem Dynamics 365 for Retail og en kanal mulig. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Service
Sporing af Microsoft SQL Server-ændringer i Dynamics 365 for Retail-databasen bruges til at bestemme de dataændringer, der skal sendes til kanaler. Baseret på en distributionsplan pakker Dynamics 365 for Retail disse data og gemmer dem på centrallageret (Azure Blob-lageret). En separat batchproces bruger Commerce Data Exchange: Asynkron Client-biblioteket til at indsætte denne datapakke i kanaldatabasen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail planlægger

Planlæggerjob er mekanismer til distribution af data til og fra lokationer. Job består af underjob, der angiver de tabeller og tabelfelter, som indeholder dataene, du distribuerer. Dynamics 365 for Retail indeholder foruddefinerede planlæggerjob og underjob, der opfylder replikeringskravene i de fleste organisationer. Der oprettes følgende typer foruddefinerede job:

-   **Hent job** – Hent job sender data, som er ændret, fra Dynamics 365 for Retail til kanaldatabaser. Ændringer af poster registreres via registrering af ændringer til SQL Server.
-   **Overførselsjob (P-job)** – Overførselsjob trække salgstransaktioner fra en kanal til Dynamics 365 for Retail-databasen. P-job overfører data gradvist. Når et P-job køres, kontrollerer Async Client-biblioteket replikeringstælleren for poster, der allerede er modtaget fra en placering. En post overføres kun, hvis dens replikeringstæller er større end den største værdi, der er fundet. P-job opdaterer ikke data, der tidligere blev overført.

Distributionsplanen bruges til at køre dataoverførsel, enten manuelt eller ved at planlægge et batchjob i Dynamics 365 for Retail. En distributionsplan kan indeholde en eller flere kanaldatagrupper og en eller flere planlæggerjob.

## <a name="realtime-service"></a>Realtime-service
Commerce Data Exchange: Real-time Service er en integreret tjeneste, der sørger for kommunikation i realtid mellem enkelte Dynamics 365 for Retail og detailkanaler. Real-time Service gør det muligt for de enkelte POS-computere og onlinebutikker at finde bestemte data fra Dynamics 365 for Retail i realtid. Selvom de fleste vigtige handlinger kan udføres i den lokale kanaldatabase, kræver følgende scenarier direkte adgang til de data, der er gemt i Dynamics 365 for Retail:

-   Udstedelse og indløsning af gavekort.
-   Indløsning af kundefordelspoint.
-   Udstedelse og indløsning af kreditnotaer.
-   Oprettelse og opdatering af kundeposter.
-   Oprettelse, opdatering og fuldførelse af salgsordrer.
-   Modtagelse af lager i henhold til en købsordre eller en flytteordre.
-   Udførelse af lageroptællinger.
-   Hentning af salgstransaktioner på tværs af butikker og fuldførelse af returtransaktioner.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Der oprettes en foruddefineret Real-time Service-profil.




