---
title: Definere og administrere et program for ydelser
description: "Personale indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte. Denne artikel indeholder oplysninger om, hvordan du konfigurerer og administrerer frynsegoder."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definere og administrere et program for ydelser

Personale indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte. Dette emne indeholder oplysninger om, hvordan du konfigurerer en Administrer ydelser.

<a name="benefit-setup"></a>Opsætning af frynsegode
-------------

Før arbejdere kan tilmeldes frynsegoder, skal du oprette elementer for hvert frynsegode. Disse elementer kombinerer lignende frynsegodeplaner og definerer standardindstillinger, som satser for fradrag og regnskabsmæssige oplysninger. Mange af disse indstillinger kan justeres, når arbejdere senere er tilmeldt frynsegodet. En organisation kan tilbyde flere tilmeldingsmuligheder til hver frynsegodeplan, eller en arbejder kan melde sig ud af planen. 

[![Fordel procesflow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Frynsegodeelementer
Før du begynder at oprette for at oprette fordele og tilmelde arbejdere til dem, skal du definere de elementer, der udgør et frynsegode: type, plan og muligheder.

-   **Type** – en samling planer til et bestemt frynsegode, f.eks. sundhedsforsikring eller parkeringsplads.
-   **Plan** – et bestemt frynsegode, der er udført af en udbyder.
-   **Indstilling** – Disponeringsniveauet, f.eks. kun medarbejderen eller medarbejderen og ægtefællen/partneren.

For hver type ydelse, f.eks. briller eller tandlæge, kan en organisation tilbyde en eller flere planer til sine ansatte. Organisationen kan tilbyde forskellige muligheder for hver enkelt plan. Arbejdere kan for eksempel købe ekstra livsforsikringsdækning på én, to eller tre gange deres årlige løn. Hver kombination af en plan og muligheder bliver et frynsegode, som medarbejdere kan tilmeldes. 

[![fordel pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Berettigelse
Medarbejderens berettigelse til forskellige former for frynsegoder, som en arbejdsgiver tilbyder, afhænger af mange faktorer. Når du opretter en fordel i Microsoft Dynamics 365 for operationer, kan du angive typen af støtteberettigelse, der gælder for denne fordel. 

Du kan gøre en fordel tilgængelig for alle arbejdere. For eksempel tilbyder nogle firmaer parkering gennemløb til alle medarbejdere som en frynsegoder. Når du opretter dette frynsegode, angiver du berettigelsen til **Alle arbejdere er berettigede**. 

Berettigelse kan ikke anvendes til andre fordele, som udlæg og afgifter til skat. Valle, du opretter disse typer af ydelser, kan du indstille berettigelse **omgå berettigelsesprocessen**. 

Endelig kan frynsegodeberettigelse være baseret på regler. Eksempelvis tilbyder en virksomhed to typer af livsforsikring fordel medarbejdere. Ledende medarbejdere er berettiget til en livsforsikring plan, bør andre fuldtidsansatte er berettiget til anden livsforsikring planen. I Dynamics 365 for operationer, kan du oprette en frynsegodeberettigelsesregel til at finde alle ledende medarbejdere og en anden regel til at finde andre fuldtidsansatte og derefter anvende disse regler på den relevante fordel.

## <a name="enrollment"></a>Tilmelding
Når du har oprettet de fordele, din virksomhed tilbyder, og fastsat berettigelse, kan du tilmelde din arbejdere frynsegoder. Du kan tilmelde en enkelt arbejder frynsegoder, eller du kan tilmelde mange arbejdere en eller flere frynsegoder i én enkelt proces. 

Nogle gange holder en organisation op med at tilbyde bestemte fordele. I så fald skal du opdatere fordelen og de arbejdere, der er tilmeldt. Masse gode udløb kan du ændre udløbsdatoen for både en fordel og arbejder-tilmeldinger til denne fordel på samme tid. Du kan også vælge flere medarbejdere, der er tilmeldt et frynsegode, og ændre slutdatoen for deres disponering. 

På samme måde gør massefrynsegodeforlængelse det muligt at forlænge udløbsdatoen for både et frynsegode og arbejdertilmeldinger til det pågældende frynsegode, hvis du beslutter at tilbyde et frynsegode i længere tid end oprindeligt planlagt.

<a name="see-also"></a>Se også
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


