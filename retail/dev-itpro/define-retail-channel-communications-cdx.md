---
title: Definere detailkanalkommunikation (Commerce Data Exchange)
description: "Denne artikel indeholder en oversigt over Commerce Data Exchange og dets komponenter. Det forklarer den del, der hver komponent spiller i overførsel af data mellem Microsoft Dynamics 365 for operationer og detailkanaler."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Definere detailkanalkommunikation (Commerce Data Exchange)

Denne artikel indeholder en oversigt over Commerce Data Exchange og dets komponenter. Det forklarer den del, der hver komponent spiller i overførsel af data mellem Microsoft Dynamics 365 for operationer og detailkanaler.

<a name="overview"></a>Overblik
--------

Commerce Data Exchange er et system, der overfører data mellem Dynamics 365 for operationer og detailkanaler, som onlinebutikker eller mursten og mørtel butikker. Den database, der gemmer data for en detailkanal er adskilt fra Dynamics-365 for operationer database. Kanaldatabasen indeholder kun de data, der skal bruges til detailtransaktioner. Stamdata, der er konfigureret i Dynamics 365 for operationer og distribueres til kanaler. Transaktionsdata oprettes i systemet for salg (POS) eller den online gemmer, og derefter overført til Dynamics 365 for operationer. Datadistribution er asynkron. Processen med at indsamle og pakke data ved kilden sker med andre ord separat fra processen med at modtage og anvende data på destinationen. I nogle scenarier, som pris- og lageropslag, skal data hentes i realtid. For at understøtte disse scenarier, indeholder Commerce Data Exchange også en tjeneste, der gør kommunikation i realtid mellem Dynamics 365 for operationer og en kanal. 

[![opdateret-retail-grafik](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Service
Microsoft SQL Server-ændringer på Dynamics-365 for operationer database bruges til at bestemme de dataændringer, der skal sendes til kanaler. Baseret på en distributionsplan, Dynamics 365 til drift pakker, data og gemmer resultatet i central lagring (Azure blob storage). En separat batchproces bruger Commerce Data Exchange: Asynkron Client-biblioteket til at indsætte denne datapakke i kanaldatabasen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail planlægger

Planlæggerjob er mekanismer til distribution af data til og fra lokationer. Job består af underjob, der angiver de tabeller og tabelfelter, som indeholder dataene, du distribuerer. Dynamics 365 for operationer indeholder foruddefinerede planlægger-job og underjob, der opfylder kravene i de fleste organisationer replikering. Der oprettes følgende typer foruddefinerede job:

-   **Hent job** – Download job sender data, som er ændret fra Dynamics 365 for operationer til kanal databaser. Ændringer af poster registreres via registrering af ændringer til SQL Server.
-   **Overføre job (P-job)** – Upload job trække salgstransaktioner fra en kanal til Dynamics-365 for operationer database. P-job overfører data gradvist. Når et P-job køres, kontrollerer Async Client-biblioteket replikeringstælleren for poster, der allerede er modtaget fra en placering. En post overføres kun, hvis dens replikeringstæller er større end den største værdi, der er fundet. P-job opdaterer ikke data, der tidligere blev overført.

Distributionsplanen bruges til at køre dataoverførsel, enten manuelt eller ved at planlægge en kørsel i Dynamics 365 for operationer. En distributionsplan kan indeholde en eller flere kanaldatagrupper og en eller flere planlæggerjob.

## <a name="realtime-service"></a>Realtime Service
Commerce Data Exchange: Real-time Service er en integreret tjeneste, der leverer kommunikation i realtid mellem Dynamics 365 for operationer og detailkanaler. Real-time Service gør det muligt for enkelte POS-computere og onlinebutikker for at finde bestemte data fra Dynamics 365 for operationer i realtid. Selvom de fleste vigtige handlinger kan udføres i den lokale kanal database, kræver direkte adgang til de data, der er gemt i Dynamics 365 for operationer i følgende scenarier:

-   Udstedelse og indløsning af gavekort.
-   Indløsning af kundefordelspoint.
-   Udstedelse og indløsning af kreditnotaer.
-   Oprettelse og opdatering af kundeposter.
-   Oprettelse, opdatering og fuldførelse af salgsordrer.
-   Modtagelse af lager i henhold til en købsordre eller en flytteordre.
-   Udførelse af lageroptællinger.
-   Hentning af salgstransaktioner på tværs af butikker og fuldførelse af returtransaktioner.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Der oprettes et foruddefineret Real-time Service-profil.


