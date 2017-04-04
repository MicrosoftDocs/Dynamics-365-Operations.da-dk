---
title: "Importér valutakurser"
description: "Hvis en juridisk enhed, der har modtaget fakturaer i fremmed valuta, er det nødvendigt at konvertere den udenlandske valuta til den lokale valuta. Det betyder, at der kræves opdaterede valutakurser for forskellige valutaer. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling for import af udenlandsk valuta referencesatserne, der udgives via internettet af valutakursudbydere, som den Europæiske Centralbank og Centralbank i Rusland."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Importér valutakurser

Hvis en juridisk enhed, der har modtaget fakturaer i fremmed valuta, er det nødvendigt at konvertere den udenlandske valuta til den lokale valuta. Det betyder, at der kræves opdaterede valutakurser for forskellige valutaer. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling for import af udenlandsk valuta referencesatserne, der udgives via internettet af valutakursudbydere, som den Europæiske Centralbank og Centralbank i Rusland.

I følgende afsnit beskrives en række oplysninger, der bruges til oprettelse og behandling af importen af valutakurser.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurere en udbyder af valutakurs
Før du kan importere valutakurser, skal du angive de oplysninger, der kræves af de udbydere, som tilbyder kurserne. Brug af **Konfigurer valutakursudbydere** til at vælge valutakurs-udbydere. Nogle udbydere af valutakurs er inkluderet i demo-data i Microsoft Dynamics 365 for operationer. Følgende tabel indeholder beskrivelser af kontrolelementerne på denne side.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Navnet på valutakursudbyderen.                                                                                                                                                                                     |
| **Nøgle**   | Det entydige id for hver konfigurationsoplysning, der er krævet af udbyderen. Oplysningerne tilføjes automatisk for hver søgemaskine, valutakurs, du tilføjer, når du klikker på den **Tilføj** knap. |
| **Value** | Oplysninger for hver nøgle. Disse oplysninger er tilføjet for hver søgemaskine, valutakurs, du tilføjer, når du klikker på den **Tilføj** knap.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importér valutakurser
Du kan importere valutakurser fra kilden til kurs udbydere, og konfigurere dem i den **valutakurser** side. Brug af **importeres valutakurser** side til at importere valutakurser. Tabellen nedenfor indeholder beskrivelser af de felter, der er nødvendige for at fuldføre importprocessen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | En valutakurstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | En valutakurs-udbyder.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Denne parameter styrer, om der skal importeres pr. dags dato eller et datointerval. Hvis du vil bruge et datointerval, angive eller vælge start- og slutdatoer.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Dette afkrydsningsfelt styrer automatisk oprettelse af valutapar, hvis valutapar, der importeres ikke findes. Denne indstilling er muligvis ikke tilgængelige for visse providere.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Dette afkrydsningsfelt styrer opdatering af eksisterende kursen for et valutapar, når kursen for en bestemt dato allerede findes. Hvis du ikke markerer dette afkrydsningsfelt, er valutakursen for bestemte datoer ikke importeret, hvis der allerede findes en anden valutakurs.                                                                                       |
| **Prevent import on national holiday** | Dette afkrydsningsfelt styrer importen af valutakursen for en dato, der er en helligdag. For eksempel, hvis du markerer dette afkrydsningsfelt, kan du bruge den Europæiske Centralbank som udbyder valutakurs opdateres systemet ikke valutakursen på en helligdag, der er relateret til den aktuelle juridiske enhed. Denne indstilling er muligvis ikke tilgængelige for visse providere. |




