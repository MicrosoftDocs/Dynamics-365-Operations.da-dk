---
title: Initialisere oprindelsesdata i nye detailmiljøer
description: I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Dynamics 365 Commerce.
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022041"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Initialisere oprindelsesdata i nye Retail-miljøer

[!include [banner](includes/banner.md)]

I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Dynamics 365 Commerce.

Når Commerce-løsningen er blevet installeret via Microsoft Dynamics Lifecycle Services (LCS), skal du initialisere Commerce-konfigurationen for at oprette de grundlæggende konfigurationsdata.

> [!IMPORTANT]
> Før du initialiserer Commerce-konfigurationen, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere butikker. Dette trin skal udføres for hver juridisk enhed, du bruger til handel.

Hvis du vil initialisere konfigurationen, skal du følge disse trin.

1. Start Commerce-klienten.
2. Klik på **Retail og Commerce** &gt; **Konfiguration af hovedkontor** &gt; **Parametre** &gt; **Commerce-parametre**.
3. Klik på **Initialiser**.

Initialiseringen opretter følgende standardkonfigurationsdata:

- Commerce planlæggerjob og -underjob
- Handelskanalskema
- Commerce-distributionstidsplaner
- Standardskærmlayout, der indeholder knapmatrixer, billeder og temaer
- Oplysninger om tidszone
- POS-handlinger:
- POS-rettigheder
- Kanalrapporter
- Attributmetadata
- Skabeloner til validering af enheder
- Batchjob til fjernelse af Commerce Data Exchange-sessionshistorik

Derudover er logføring, der er relateret til betalingskortindustrien (PCI), aktiveret for Commerce-databasen.

> [!NOTE]
> Der er en indstilling til at konfigurere Commerce-planlægger separat. Denne indstilling gør det muligt at nulstille Commerce-planlæggerkonfigurationen til dens standardindstillinger.

Når initialiseringen er fuldført, skal du konfigurere yderligere handelsdata. Her er nogle eksempler:

- Handelsparametre
- Parametre for handelsplanlægger
- Handelskanaler
- Kasseapparater og enheder
- Udvalg
