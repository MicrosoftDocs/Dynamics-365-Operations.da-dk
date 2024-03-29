---
title: Importér valutakurser
description: Denne artikel indeholder oplysninger om kravene til import af referencekurser for udenlandsk valuta, der udgives af valutakursudbydere.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 27f9b06646d9ce948a6b4528c38c5df9784b24b2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894929"
---
# <a name="import-currency-exchange-rates"></a>Importere valutakurser

[!include [banner](../includes/banner.md)]

Hvis en juridisk enhed har modtaget fakturaer i fremmed valuta, er det nødvendigt at omregne den udenlandske valuta til den lokale valuta. Det betyder, at der kræves opdaterede valutakurser for forskellige valutaer. Denne artikel indeholder en oversigt over de nødvendige indstillinger og behandling for import af udenlandske valutakursreferencer, der udgives af valutakursudbydere som den Europæiske Centralbank og den russiske centralbank.

I følgende afsnit beskrives strømmen af oplysninger, der bruges til konfiguration og behandling af importen af udenlandske valutakurser.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurere en valutakursudbyder
Før du kan importere valutakurser, skal du angive de oplysninger, der kræves af de udbydere, som tilbyder valutakurserne. Brug siden **Konfigurer valutakursudbydere** til at vælge valutakursudbyderne. Nogle valutakursudbydere er inkluderet i demodataene i Dynamics 365 Finance. Følgende tabel indeholder en beskrivelse af kontrolelementerne på denne side.

| Felt | Betegnelse                   |
|-----------|-----------------------------------|
| **Navn**  | Navnet på valutakursudbyderen.                                                                                                                                                                                     |
| **Nøgle**   | Det entydige id for hver konfigurationsoplysning, der er krævet af udbyderen. Disse oplysninger tilføjes automatisk for hver valutakursudbyder, som du tilføjer. |
| **Value** | Oplysninger for hver nøgle. Disse oplysninger tilføjes for hver valutakursudbyder, som du tilføjer.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importere valutakurser
Du kan importere valutakurser fra valutakursudbyderkilden og tilføje dem på siden **Valutakurser**. Brug siden **Importer valutakurser** side til at importere valutakurserne. Tabellen nedenfor indeholder beskrivelser af de felter, der er nødvendige for at fuldføre importprocessen.

| Felt | Betegnelse                   |
|-----------|-----------------------------------|
| **Valutakurstype**                 | En valutakurstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Valutakursudbyder**             | En valutakursudbyder.                                                                                                                                                                                                                                                                                                                                                  |
| **Importér fra og med**                       | Denne parameter styrer, om der skal importeres pr. dags dato eller et specifikt datointerval. Hvis du vil bruge et datointerval, skal du angive start- og slutdatoer.                                                                                                                                                                                                                |
| **Opret de påkrævede valutapar**    | Dette afkrydsningsfelt styrer den automatiske oprettelse af valutapar, hvis de valutapar, der importeres, ikke findes. Denne indstilling er muligvis ikke tilgængelige for alle udbydere.                                                                                                                                                                                               |
| **Ignorer eksisterende valutakurser**   | Dette afkrydsningsfelt styrer opdatering af den eksisterende valutakurs for et valutapar, når valutakursen for en bestemt dato allerede findes. Hvis du ikke markerer dette afkrydsningsfelt, bliver valutakursen for de bestemte datoer ikke importeret, hvis der allerede findes en anden valutakurs.                                                                                       |
| **Undgå import på helligdag** | Dette afkrydsningsfelt styrer importen af valutakursen for en dato, der er en helligdag. For eksempel, hvis du markerer dette afkrydsningsfelt og bruger den Europæiske Centralbank som valutakursudbyder, opdaterer systemet ikke valutakursen på en helligdag, der er relateret til den aktuelle juridiske enhed. Denne indstilling er muligvis ikke tilgængelige for alle udbydere. |
| **Kurs fra den forrige dag** | Dette afkrydsningsfelt er tilgængeligt, hvis du aktiverer funktonen **ECB-import på den aktuelle eller tidligere dato** på siden **Administration af funktioner**. Dette afkrydsningsfelt er kun tilgængeligt for udbyderen *Den Europæiske Centralbank*. Markér dette afkrydsningsfelt for at importere den valutakurs, der udgives af Den Europæiske Centralbank, den forrige arbejdsdag kl. ca. 16:00 CET. Afkrydsningsfeltet er som standard markeret. Fjern markeringen i dette afkrydsningsfelt for at importere den valutakurs, der er udgivet den samme arbejdsdag.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]