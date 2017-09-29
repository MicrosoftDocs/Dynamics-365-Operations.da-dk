---
title: Oprette et callcenter-katalog
description: Denne artikel indeholder en oversigt over processen til oprettelse af et katalog for et callcenter.
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
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 28aaa84c11a897b895b2a106ca5f0cd6168997b2
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="create-a-call-center-catalog"></a>Oprette et callcenter-katalog

[!include[banner](includes/banner.md)]


Denne artikel indeholder en oversigt over processen til oprettelse af et katalog for et callcenter. 

I et call center kan du bruge produktkataloger til at identificere de produkter, du vil tilbyde kunderne. Call centre bruger typisk trykte kataloger. Udformning og produktion af et trykt katalog håndteres uden for Microsoft Dynamics 365 for Retail. Du kan dog oprette og gemme en digital udgave af et katalog ved hjælp af de samme formularer, som du bruger til at konfigurere detailkataloger. Før du kan oprette et katalog, skal du konfigurere produktsortimenter og tildele sortimenterne til et call center. Derefter føjer du produkter til kataloget ved at vælge produkter fra disse sortimenter. Når der er føjet produkter til kataloget, og kataloget er fuldført, skal du validere kataloget for at kontrollere dataene. Derefter skal du sende kataloget til gennemsyn og godkendelse. Når kataloget er godkendt, kan det udgives. Når der er oprettet et call center-katalog, kan du tage et øjebliksbillede af katalogdataene på det tidspunkt, hvor kataloget udgives. Den funktion til øjebliksbillede giver dig adgang til en bestemt version af kataloget, selvom kataloget senere bliver ændret og opdateret. Call center-kataloger kan også konfigureres til at medtage følgende valgfri funktioner.

-   **Kildekoder** – Koder, der bruges til at spore kunderespons på bestemte katalogudsendelser.
-   **Gratis produkter** – Produkter, der indgår i en kundes ordre uden merpris. Disse produkter føjes automatisk til ordren, når kildekoden til kataloget er angivet i orden.
-   **Scripts** – Tekster, som en arbejder i et call center læser op for en debitor, når der oprettes en ordre. Scripts kan omfatte hilsener eller indkøbsforslag.
-   **Mersalg/tillægssalg af varer** Varer, der vises som forslag, når et bestemt produkt føjes til ordren.

Disse indstillinger skal konfigureres, før kataloget godkendes og udgives.

## <a name="prerequisites"></a>Forudsætninger
Følgende opgaver skal være fuldført, før du starter:

-   Konfiguration af produkter og produktudvalg.
-   Konfigurer detailprodukter.
-   Opsætning af et udvalg.
-   Oprettelse af et call center.
-   Konfigurer et call center.
-   Tilføjelse af call centret til et organisationshierarki.
-   Oprettelse eller redigering af et organisationshierarki.

## <a name="create-a-catalog"></a>Oprette et katalog
Du skal først oprette et katalog, føje produkter til kataloget og derefter gennemse attributterne for produkterne.

## <a name="validate-the-catalog"></a>Validere kataloget
Når du er færdig med at konfigurere kataloget, skal du køre validere det. I valideringsprocessen kontrolleres det, at de data, der kræves til kanalattributter og produktattributter, er fuldstændige og gyldige, og at kataloget kan udgives.

## <a name="submit-the-catalog-for-review-and-approval"></a>Send kataloget til gennemsyn og godkendelse
Når et katalog er godkendt, kan du sende det til gennemsyn og godkendelse. Et katalog skal godkendes, før det kan udgives. Du kan konfigurere en arbejdsgang, så kataloger godkendes automatisk eller manuelt.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Valgfrit: Tilføj kildekoder, gratis produkter og scripts
Du kan også føje følgende elementer til et call center-katalog. Disse elementer er valgfrie.

-   **Kildekoder** kan bruges af firmaer, der fremstiller trykte kataloger til at spore kunderesponsen på bestemte kataloger. Kildespor udskrives ofte på bagsiden af et katalog og er angivet på salgsordren, når en kunde foretager et køb. Hvis du vil tilføje en kildekode i kataloget, skal du først oprette en målgruppe. Målmarkedet er normalt knyttet til en ejet eller lejet adresseliste.
-   **Gratis produkter** er salgsfremmende varer, der følger gratis med kundens ordre, når der henvises til kataloget.
-   **Scripts** kan hjælpe arbejderen med at interagere med kunder inden for rammerne for et katalog eller et produkt i et katalog.

## <a name="publish-the-catalog"></a>Udgive kataloget
Ved at udgive et katalog for et call center kan du færdiggøre produktoplysningerne i kataloget. Publikationen angiver også, at kataloget er klar til flere handlinger, du vil udføre. Du kan f.eks. oprette et trykt katalog. Du kan udgive dine kataloger manuelt, eller du kan bruge en batchproces til udgivelse på baggrund af en tidsplan. Før du kan udgive et katalog, skal kataloget være valideret og godkendt. Hvis du vil ændre kataloget, når det er udgivet, kan du trække det tilbage og derefter udgive det igen.



