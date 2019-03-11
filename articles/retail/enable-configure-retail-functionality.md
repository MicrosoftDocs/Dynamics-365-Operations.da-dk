---
title: Initialisere oprindelsesdata i nye detailmiljøer
description: I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327889"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Initialisere oprindelsesdata i nye Retail-miljøer

[!include [banner](includes/banner.md)]

I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.

Når detailløsningen er blevet installeret via Microsoft Dynamics Lifecycle Services (LCS), skal du initialisere detailkonfigurationen for at oprette de grundlæggende konfigurationsdata.

> [!IMPORTANT]
> Før du initialiserer detailkonfiguration, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere detailbutikker. Dette trin skal udføres for hver juridisk enhed, du bruger til detailsalg.

Hvis du vil initialisere detailkonfigurationen, skal du følge disse trin.

1. Start Dynamics 365 for Retail-klienten.
2. Klik på **Detail** &gt; **Konfiguration af hovedkontor** &gt; **Parametre** &gt; **Detailparametre**.
3. Klik på **Initialiser**.

Initialiseringen opretter følgende standardkonfigurationsdata:

- Retail planlægger-job og -underjob
- Detailkanalskema
- Distributionstidsplaner for detail
- Standardskærmlayout, der indeholder knapmatrixer, billeder og temaer
- Oplysninger om tidszone
- POS-handlinger:
- POS-rettigheder
- Kanalrapporter
- Attributmetadata
- Skabeloner til validering af enheder
- Batchjob til fjernelse af Commerce Data Exchange-sessionshistorik

Derudover er logføring, der er relateret til betalingskortindustrien (PCI), aktiveret for Dynamics 365 for Retail-databasen.

> [!NOTE]
> Der er en indstilling til at konfigurere Retail planlægger separat. Denne indstilling gør det muligt at nulstille Retail planlægger-konfigurationen til dens standardindstillinger.

Når initialiseringen er fuldført, skal du konfigurere yderligere detaildata. Her er nogle eksempler:

- Detailparametre
- Parametre for Retail planlægger
- Detailkanaler
- Kasseapparater og enheder
- Udvalg
