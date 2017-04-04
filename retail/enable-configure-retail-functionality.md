---
title: "Initialisere frø data i et nyt Retail-miljø"
description: "Denne artikel beskriver de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for operationer – Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisere frø data i et nyt Retail-miljø

Denne artikel beskriver de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for operationer – Retail.

Når detailløsningen er blevet installeret via Microsoft Dynamics livscyklus Services (LCS), skal du initialisere detailkonfigurationen for at oprette de grundlæggende konfigurationsdata. **Vigtigt::** Før du initialiserer detailkonfiguration, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere detailbutikker. Dette trin skal udføres for hver juridisk enhed, du bruger til detailsalg. Hvis du vil initialisere detailkonfigurationen, skal du følge disse trin.

1.  Start Dynamics-365 for klient operationer.
2.  Klik på **detail- og commerce**&gt;**opsætning Headquarters**&gt;**parametre**&gt;**Retail parametre**.
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

Derudover logføring, der er relateret til betaling kort industrien (PCI) er aktiveret for Dynamics-365 for operationer database. **Bemærk!** Der er en indstilling til at konfigurere Retail planlægger separat. Denne indstilling gør det muligt at nulstille Retail planlægger-konfigurationen til dens standardindstillinger. Når initialiseringen er fuldført, skal du konfigurere yderligere detaildata. Her er nogle eksempler:

-   Detailparametre
-   Parametre for Retail planlægger
-   Detailkanaler
-   Kasseapparater og enheder
-   Udvalg



