---
title: "Initialisere oprindelsesdata i et nyt detailmiljø"
description: I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ac4f651cd7e5df912ea2535eafd5e54c11377253
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisere oprindelsesdata i et nyt detailmiljø

[!include[banner](includes/banner.md)]


I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.

Når detailløsningen er blevet installeret via Microsoft Dynamics livscyklus Services (LCS), skal du initialisere detailkonfigurationen for at oprette de grundlæggende konfigurationsdata. **Vigtigt::** Før du initialiserer detailkonfiguration, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere detailbutikker. Dette trin skal udføres for hver juridisk enhed, du bruger til detailsalg. Hvis du vil initialisere detailkonfigurationen, skal du følge disse trin.

1.  Start Dynamics 365 for Retail-klienten.
2.  Klik på **Detail** &gt; **Konfiguration af hovedkontor** &gt; **Parametre** &gt; **Detailparametre**.
3.  Klik på **Initialiser**.

Initialiseringen opretter følgende standardkonfigurationsdata:

-   Retail planlægger-job og -underjob
-   Detailkanalskema
-   Distributionstidsplaner for detail
-   Standardskærmlayout, der indeholder knapmatrixer, billeder og temaer
-   Oplysninger om tidszone
-   POS-handlinger:
-   POS-rettigheder
-   Kanalrapporter
-   Attributmetadata
-   Skabeloner til validering af enheder
-   Batchjob for at slette Commerce Data Exchange-sessionsoversigt

Derudover er logføring, der er relateret til betalingskortindustrien (PCI), aktiveret for Dynamics 365 for Retail-databasen. **Bemærk!** Der er en indstilling til at konfigurere Retail planlægger separat. Denne indstilling gør det muligt at nulstille Retail planlægger-konfigurationen til dens standardindstillinger. Når initialiseringen er fuldført, skal du konfigurere yderligere detaildata. Her er nogle eksempler:

-   Detailparametre
-   Parametre for Retail planlægger
-   Detailkanaler
-   Kasseapparater og enheder
-   Udvalg





