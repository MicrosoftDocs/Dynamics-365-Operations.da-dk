---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022048"
---
# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

[!include [banner](includes/banner.md)]

Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.

I Commerce kan du foretage prisjusteringer af produkter, og du kan også konfigurere rabatter, der anvendes på et linjeelement eller en transaktion på POS, i et callcenters salgsordre eller i en onlineordre. Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter. 

Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier. Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten. Commerce anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden. Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for. Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Commerce-parametre**, inden du definerer en ny prisjustering eller rabat.

> [!NOTE]
> Du kan slette en prisjustering eller en rabat. Statistiske oplysninger går imidlertid tabt.

## <a name="types-of-discounts"></a>Rabattyper

Der findes fire typer rabatter:

- **Enkel rabat** – en enkelt procent eller beløb.
- **Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.
- **Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.
- **Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.

Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.
