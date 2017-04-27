---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Retail og handel i Microsoft Dynamics 365 for Operations.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 01f249cbdabc6febf23dcd7103d4587cecdaad08
ms.lasthandoff: 03/31/2017


---

# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

[!include[banner](includes/banner.md)]


Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Retail og handel i Microsoft Dynamics 365 for Operations.

I Dynamics 365 for Operations - Retail kan du foretage prisreguleringer i forhold til produkter, og du kan også konfigurere rabatter, der gælder for en varelinje eller en transaktion på salgsstedet (POS), i salgsordren for et callcenter eller i en onlineordre. Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter. Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier. Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten. Dynamics 365 for Operations anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden. Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for. Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Detailparametre**, inden du definerer en ny prisjustering eller rabat. **Bemærk!** Du kan slette en prisjustering eller en rabat. Statistiske oplysninger går imidlertid tabt.

### <a name="types-of-discounts"></a>Rabattyper

Der findes fire typer detailrabatter:

-   **Enkel rabat** – en enkelt procent eller beløb.
-   **Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.
-   **Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.
-   **Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.

Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.




