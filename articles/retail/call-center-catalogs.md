---
title: Callcenter-kataloger
description: I denne artikel beskrives call center-specifikke funktioner for kataloger i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5a97ab749259fcc97b269b0134792820ebf13af
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-catalogs"></a>Callcenter-kataloger

[!include[banner](includes/banner.md)]


I denne artikel beskrives call center-specifikke funktioner for kataloger i Microsoft Dynamics 365 for Retail.

I et call center kan du bruge produktkataloger til at identificere de produkter, du vil tilbyde kunderne. Call centre bruger typisk trykte kataloger. Udformning og produktion af et trykt katalog håndteres uden for Microsoft Dynamics 365 for Retail. Du kan dog oprette og gemme en digital udgave af et katalog ved hjælp af de samme sider, som du bruger til at konfigurere detailkataloger. Før du kan oprette et katalog, skal du konfigurere produktsortimenter og tildele sortimenterne til et call center. Derefter føjer du produkter til kataloget ved at vælge produkter fra disse sortimenter. Når der er føjet produkter til kataloget, og kataloget er fuldført, skal du validere kataloget for at kontrollere dataene. Derefter skal du sende kataloget til gennemsyn og godkendelse. Når kataloget er godkendt, kan det udgives. Når der er oprettet et call center-katalog, kan du tage et øjebliksbillede af katalogdataene på det tidspunkt, hvor kataloget udgives. Den funktion til øjebliksbillede giver dig adgang til en bestemt version af kataloget, selvom kataloget senere bliver ændret og opdateret. Call center-kataloger kan også konfigureres til at medtage følgende valgfri funktioner:

-   **Kildekoder** – Kildekoder bruges til at spore kunderespons på bestemte katalogudsendelser.
-   **Gratis produkter** – Produkter,, der indgår i en kundes ordre uden merpris. Disse produkter føjes automatisk til en ordre, når kildekoden til kataloget er angivet i orden.
-   **Scripts** – Scripts er tekster, som en arbejder i et callcenter læser op for en debitor, når der oprettes en ordre. Scripts kan omfatte hilsener eller indkøbsforslag.
-   **Sidelayout** – Et sidelayout henter sideplacering af produkter i den trykte katalog. Disse oplysninger bruges til analyserapporten af katalogområde.





