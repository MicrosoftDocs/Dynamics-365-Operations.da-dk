---
title: Oversigt over udskrivning af dokumenter
description: Du kan udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom:
- "69161"
- intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5a0d26836043ea225b9a6d3e62980ada2dc49b0a01a6dacec739b50f28e17bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728232"
---
# <a name="document-printing-overview"></a>Oversigt over udskrivning af dokumenter

[!include [banner](../includes/banner.md)]

Du kan udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives.

## <a name="printing-overview"></a>Oversigt over udskrivning

Programmet indeholder integrerede tjenester og klientapplikationer, der gør det nemt at oprette, gemme og distribuere dokumenter, der understøtter forretningsaktiviteter. Du kan udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Derudover kan du eksportere sider og rapporter direkte fra klienten som PDF-filer eller Microsoft Office-dokumenter. Endelig tillader den distribuerede arbejdsbyrde, at du udskriver forretningsdokumenter direkte fra en mobilenhed ved hjælp af netværksressourcer. Selvom udskrivningsbehov kan variere, skal alle brancher typisk oprette udskrifter af forretningsdokumenter ved hjælp af programmet. Udskrivning af dokumenter på netværksenheder fra tilknyttede programmer medfører en særlig række af udfordringer. Her er nogle eksempler:

- Printerdrivere er muligvis ikke tilgængelige på brugerens enhed.
- Brugerens enhed er muligvis ikke tilsluttet virksomhedens netværk.

Systemadministratorer kan konfigurere installationer ved at bruge en dedikeret vært og følge nogle få nemme trin, så brugerne kan udskrive direkte fra forretningsprogrammer på netværksenheder.

### <a name="application-printing-scenarios"></a>Programudskrivningsscenarier 

I følgende tabel beskrives de tre primære udskrivningsscenarier.

| Scenarie                        | Mål                                                      | Løsning |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Udskrivning af det, du kan se        | Udskriv det, der aktuelt vises i browseren.             | Der genereres en "udskriftsvenlig" version af websiden i browseren. |
| 2. Interaktiv udskrivning         | Udskriv et dokument med høj præcision på en lokalt tilsluttet enhed. | Du kan eksportere en PDF-version af rapporten og åbne den i browseren. |
| 3. Udskrivning på en netværksenhed | Send et dokument med høj præcision til en printerenhed for et domæne.     | Et præcisionsdokument sendes til et klientprogram, der kører på en server, der er tilknyttet kundens domæne. |

Eftersom løsningen varierer afhængigt af scenariet, tilbyder programmer indbyggede tjenester og værktøjer, der hjælper brugerne med at opfylde deres mål:

- **Eksempel 1** understøttes af browserens gengivelse af HTML5-klienten.
- **Scenarie 2** bruger klientprogrammer og Microsoft Office 365-tjenester.
- **Eksempel 3** kræver understøttelse fra klientprogrammer og tjenester, der er tilknyttet Microsoft Azure.

Ud over den platform, der er installeret under Azure-abonnementet, giver Finance and Operations-programmer kunderne et integreret, oprindeligt Azure-program, der gør det lettere at bruge domænetilknyttede enheder til at udskrive dokumenter.

## <a name="service-overview"></a>Serviceoversigt
Mens dokumenter, der fremstilles af de tilknyttede programmer, venter på at blive udskrevet på en netværkstilsluttet enhed, gemmes de i blob-lageret for Azure. [Installation af Dokumentets ruteplanlægningsagent for at aktivere netværksprint](install-document-routing-agent.md) bruger Azure-godkendelse til at oprette en sikker kanal for Azure-tjenesterne.

**Udførelsessekvens**

1. Rapporten oprettes af Microsoft SQL Server Reporting Services (SSRS) og gemmes i blob-lageret for Azure. Tilknyttede printerindstillinger gemmes sammen med dokumentet.
2. Dokumentets ruteplanlægningsagent forespørger Azure Service Bus-køen om aktive job.
3. Dokumentet hentes af dokumentruteplanlægningsagent og sættes i kø til netværksprinteren.

Den klientbaserede løsning lader kunder styre omfanget af deres udskrivningsbehov. Kunder med omfattende udskrivningsbehov kan installere flere dokumentruteplanlægningsagenter for at øge antallet af samtidige udskrivningshandlinger. Du kan også kræve nogle kunder meget få installationer af dokumentruteplanlægningsagent til at håndtere deres forventede behov for udskrivning.

### <a name="service-components-for-network-printing"></a>Servicekomponenter til netværksudskrivning

Følgende diagram viser de grundlæggende komponenter, der kan understøtte netværksudskrivning.

[![servicekomponenter-til-netværksudskrivning\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Bemærk, at en enkelt printer kan registreres med flere dokumentruteplanlægningsagenter. For at håndtere printerindstillingerne bruger den hostede tjeneste netværksstien, der entydigt identificerer hver netværksprinter. Når der registreres en printer af flere klienter, vises den således som et enkelt punkt på listen over printere, som er tilgængelige i programmer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]