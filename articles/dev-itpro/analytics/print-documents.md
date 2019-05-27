---
title: Dokumentudskrivning
description: I Microsoft Dynamics 365 for Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fd20022ff91fedb6d0323e82fbe3c1acae38e48
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551641"
---
# <a name="document-printing"></a>Dokumentudskrivning

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 for Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives.

## <a name="printing-overview"></a>Oversigt over udskrivning

Microsoft Dynamics 365 for Finance and Operations indeholder integrerede tjenester og klientapplikationer, der gør det nemt at oprette, gemme og distribuere dokumenter, der understøtter forretningsaktiviteter. I Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Derudover kan du eksportere sider og rapporter i Finance and Operations direkte fra klienten som PDF-filer eller Microsoft Office-dokumenter. Endelig tillader den distribuerede arbejdsbyrde, at du udskriver forretningsdokumenter direkte fra en mobilenhed ved hjælp af netværksressourcer. Selvom udskrivningsbehov kan variere, skal alle brancher typisk oprette udskrifter af forretningsdokumenter ved hjælp af Finance and Operations. Udskrivning af dokumenter på netværksenheder fra tilknyttede programmer medfører en særlig række af udfordringer. Her er nogle eksempler:

- Printerdrivere er muligvis ikke tilgængelige på brugerens enhed.
- Brugerens enhed er muligvis ikke tilsluttet virksomhedens netværk.

Systemadministratorer kan konfigurere installationer ved at bruge en dedikeret vært og følge nogle få nemme trin, så brugerne kan udskrive direkte fra forretningsprogrammer på netværksenheder.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Udskrivningsscenarier i Finance and Operations-programmer

I følgende tabel beskrives de tre primære udskrivningsscenarier i Finance and Operations-programmer.

| Scenario                        | Mål                                                      | Løsning |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Udskrivning af det, du kan se        | Udskriv det, der aktuelt vises i browseren.             | Der genereres en "udskriftsvenlig" version af websiden i browseren. |
| 2. Interaktiv udskrivning         | Udskriv et dokument med høj præcision på en lokalt tilsluttet enhed. | Du kan eksportere en PDF-version af rapporten og åbne den i browseren. |
| 3. Udskrivning på en netværksenhed | Send et dokument med høj præcision til en printerenhed for et domæne.     | Et præcisionsdokument sendes til et klientprogram, der kører på en server, der er tilknyttet kundens domæne. |

Eftersom løsningen varierer afhængigt af scenariet, tilbyder Finance and Opersations-programmer indbyggede tjenester og værktøjer, der hjælper brugerne med at opfylde deres mål:

- **Eksempel 1** understøttes af browserens gengivelse af HTML5-klienten.
- **Eksempel 2** bruger klientprogrammer og Microsoft Office 365-tjenester.
- **Eksempel 3** kræver understøttelse fra klientprogrammer og tjenester, der er tilknyttet Microsoft Azure.

Ud over den platform, der er installeret under Azure-abonnementet, giver Finance and Opersations-programmer kunderne et integreret, oprindeligt Azure-program, der gør det lettere at bruge domænetilknyttede enheder til at udskrive dokumenter.

## <a name="service-overview"></a>Serviceoversigt
Mens dokumenter, der fremstilles af de tilknyttede programmer, venter på at blive udskrevet på en netværkstilsluttet enhed, gemmes de i blob-lageret for Azure. [Dokumentets ruteplanlægningsagent](install-document-routing-agent.md) bruger Azure-godkendelse til at oprette en sikker kanal for Azure-tjenesterne.

**Udførelsessekvens**

1. Rapporten oprettes af Microsoft SQL Server Reporting Services (SSRS) og gemmes i blob-lageret for Azure. Tilknyttede printerindstillinger gemmes sammen med dokumentet.
2. Dokumentets ruteplanlægningsagent forespørger Azure Service Bus-køen om aktive job.
3. Dokumentet hentes af dokumentruteplanlægningsagent og sættes i kø til netværksprinteren.

Den klientbaserede løsning lader kunder styre omfanget af deres udskrivningsbehov. Kunder med omfattende udskrivningsbehov kan installere flere dokumentruteplanlægningsagenter for at øge antallet af samtidige udskrivningshandlinger. Du kan også kræve nogle kunder meget få installationer af dokumentruteplanlægningsagent til at håndtere deres forventede behov for udskrivning.

### <a name="service-components-for-network-printing"></a>Servicekomponenter til netværksudskrivning

Følgende diagram viser de grundlæggende komponenter, der kan understøtte netværksudskrivning.

[![servicekomponenter-til-netværksudskrivning\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Bemærk, at en enkelt printer kan registreres med flere dokumentruteplanlægningsagenter. For at håndtere printerindstillingerne bruger den hostede tjeneste netværksstien, der entydigt identificerer hver netværksprinter. Når der registreres en printer af flere klienter, vises den således som et enkelt punkt på listen over printere, som er tilgængelige i Finance and Opersations-programmer.
