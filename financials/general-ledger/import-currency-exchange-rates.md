---
title: "Importér valutakurser"
description: "Hvis en juridisk enhed har modtaget fakturaer i fremmed valuta, er det nødvendigt at konvertere den udenlandske valuta til den lokale valuta. Det betyder, at der kræves opdaterede valutakurser for forskellige valutaer. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling for import af udenlandsk valutakursreferencer, der udgives via internettet af valutakursudbydere, som den Europæiske Centralbank og den russiske centralbank."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 2d0654d6dbed3b4fe56b8918194132787f66af80
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="import-currency-exchange-rates"></a>Importér valutakurser

[!include[banner](../includes/banner.md)]


Hvis en juridisk enhed har modtaget fakturaer i fremmed valuta, er det nødvendigt at konvertere den udenlandske valuta til den lokale valuta. Det betyder, at der kræves opdaterede valutakurser for forskellige valutaer. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling for import af udenlandsk valutakursreferencer, der udgives via internettet af valutakursudbydere, som den Europæiske Centralbank og den russiske centralbank.

I følgende afsnit beskrives strømmen af oplysninger, der bruges til konfiguration og behandling af importen af udenlandske valutakurser.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurere en valutakursudbyder
Før du kan importere valutakurser, skal du angive de oplysninger, der kræves af de udbydere, som tilbyder valutakurserne. Brug siden **Konfigurer valutakursudbydere** til at vælge valutakursudbyderne. Nogle udbydere er inkluderet i demodataene i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Følgende tabel indeholder en beskrivelse af kontrolelementerne på denne side.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt** | **Beskrivelse**                                                                                                                                                                                                             |
| **Navn**  | Navnet på valutakursudbyderen.                                                                                                                                                                                     |
| **Nøgle**   | Det entydige id for hver konfigurationsoplysning, der er krævet af udbyderen. Disse oplysninger føjes automatisk til hver valutakursudbyder, som du tilføjer, når du klikker på knappen **Tilføj**. |
| **Værdi** | Oplysninger for hver nøgle. Disse oplysninger føjes til hver valutakursudbyder, som du tilføjer, når du klikker på knappen **Tilføj**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importér valutakurser
Du kan importere valutakurser fra valutakursudbyderkilden og konfigurere dem på siden **Valutakurser**. Brug siden **Importer valutakurser** side til at importere valutakurserne. Tabellen nedenfor indeholder beskrivelser af de felter, der er nødvendige for at fuldføre importprocessen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt**                              | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                             |
| **Valutakurstype**                 | En valutakurstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Valutakursudbyder**             | En valutakursudbyder.                                                                                                                                                                                                                                                                                                                                                  |
| **Importér fra og med**                       | Denne parameter styrer, om der skal importeres pr. dags dato eller et datointerval. Hvis du vil bruge et datointerval, skal du angive eller vælge start- og slutdatoer.                                                                                                                                                                                                                |
| **Opret de påkrævede valutapar**    | Dette afkrydsningsfelt styrer den automatiske oprettelse af valutapar, hvis de valutapar, der importeres, ikke findes. Denne indstilling er muligvis ikke tilgængelige for alle udbydere.                                                                                                                                                                                               |
| **Ignorer eksisterende valutakurser**   | Dette afkrydsningsfelt styrer opdatering af den eksisterende valutakurs for et valutapar, når valutakursen for en bestemt dato allerede findes. Hvis du ikke markerer dette afkrydsningsfelt, bliver valutakursen for de bestemte datoer ikke importeret, hvis der allerede findes en anden valutakurs.                                                                                       |
| **Undgå import på helligdag** | Dette afkrydsningsfelt styrer importen af valutakursen for en dato, der er en helligdag. For eksempel, hvis du markerer dette afkrydsningsfelt og bruger den Europæiske Centralbank som valutakursudbyder, opdaterer systemet ikke valutakursen på en helligdag, der er relateret til den aktuelle juridiske enhed. Denne indstilling er muligvis ikke tilgængelige for alle udbydere. |






