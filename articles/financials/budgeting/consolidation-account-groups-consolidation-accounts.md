---
title: Koncernkontogrupper og yderligere koncernkonti
description: Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af koncernkonti og om, hvordan de bruges i Microsoft Dynamics 365 for Finance and Operations.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f1c463ee54512b07f5e45c4df995aefed6110cb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "366391"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Koncernkontogrupper og yderligere koncernkonti

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af koncernkonti og om, hvordan de bruges i Microsoft Dynamics 365 for Finance and Operations.

<a name="consolidation-account-groups"></a>Koncernkontogrupper
----------------------------

Med koncernkontogrupper kan du oprette grupper af konti, du vil bruge til at konsolidere data. Oftest repræsenterer en koncernkontogruppe en lovpligtig kontoplan eller knytter konti til en gruppe, der er defineret af virksomhedens hovedkontor. Du kan finde koncernkontogrupper i **Opsætning**-området af modulet **Konsolideringer**. Når du tilføjer en ny gruppe, angiver du en entydig identifikator for kontogruppen og et navn.

## <a name="additional-consolidation-accounts"></a>Flere koncernkonti
Med flere koncernkonti kan du tildele en konto fra en eksisterende kontoplan til en koncernkontogruppe. Du kan derefter angive en værdi og et navn til koncernkontoen. 

Du kan finde flere koncernkonti i **Opsætning**-området af modulet **Konsolideringer**. Når du opretter en ny koncernkonto, skal du angive følgende oplysninger:

-   **Hovedkonto** – Dette felt er et opslag, der viser alle de hovedkonti, der er baseret på de kontoplaner, som du valgte på siden. Når du vælger en konto, angives navnet automatisk i feltet **Hovedkontonavn**.
-   **Koncernkontogruppe** – Brug dette felt til at angive den gruppe, kontoen skal tildeles til. Hvis du konsoliderer på to forskellige måder, skal du føje den samme konto til alle fire koncernkontogrupper.
-   **Koncernkonto** – Angiv værdien af koncernkontoen. Denne værdi behøver ikke være fra en kontoplan. Det kan være enhver værdi, som du har brug for.
-   **Navn på koncernkonto** – Angiv navnet på kontoen, som det skal vises i forespørgsler og rapporter.
-   **SAT niveau** – Dette felt bruges til at rapportere kontoudtog til de mexicanske myndigheder. 

Når du har oprettet dine koncernkontogrupper og ekstra koncernkonti, kan du vælge gruppen under onlinekonsolideringsprocessen.


Du kan finde flere oplysninger under [Oprette koncerngrupper og supplerende koncernkonti](../general-ledger/tasks/create-consolidation-groups.md) 



