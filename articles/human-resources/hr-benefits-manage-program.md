---
title: Definere og administrere et frynsegodeprogram
description: Human Resources indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte. Denne artikel indeholder oplysninger om, hvordan du konfigurerer og administrerer frynsegoder.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 60264d246e1173c25e4383cc79836126126fcba5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111992"
---
# <a name="define-and-manage-a-benefits-program"></a>Definere og administrere et frynsegodeprogram

Human Resources indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte. Denne artikel indeholder oplysninger om, hvordan du konfigurerer og administrerer frynsegoder.

## <a name="benefit-setup"></a>Frynsegodeopsætning

Før arbejdere kan tilmeldes frynsegoder, skal du oprette elementer for hvert frynsegode. Disse elementer kombinerer lignende frynsegodeplaner og definerer standardindstillinger, som satser for fradrag og regnskabsmæssige oplysninger. Mange af disse indstillinger kan justeres, når arbejdere senere er tilmeldt frynsegodet. En organisation kan tilbyde flere tilmeldingsmuligheder til hver frynsegodeplan, eller en arbejder kan melde sig ud af planen. 

[![Procesforløb for frynsegoder](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Frynsegodeelementer

Før du begynder at oprette fordele og tilmelde arbejdere til dem, skal du definere de elementer, der udgør et frynsegode: type, plan og muligheder.

-   **Type** – en samling planer til et bestemt frynsegode, f.eks. sundhedsforsikring eller parkeringsplads.
-   **Plan** – et bestemt frynsegode, der er udført af en udbyder.
-   **Indstilling** – Disponeringsniveauet, f.eks. kun medarbejderen eller medarbejderen og ægtefællen/partneren.

For hver type ydelse, f.eks. briller eller tandlæge, kan en organisation tilbyde en eller flere planer til sine ansatte. Organisationen kan tilbyde forskellige muligheder for hver enkelt plan. Arbejdere kan for eksempel købe ekstra livsforsikringsdækning på én, to eller tre gange deres årlige løn. Hver kombination af en plan og muligheder bliver et frynsegode, som medarbejdere kan tilmeldes. 

[![billede af frynsegode](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Berettigelse
Medarbejderens berettigelse til forskellige former for frynsegoder, som en arbejdsgiver tilbyder, afhænger af mange faktorer. Når du opretter et frynsegode i Dynamics 365 Human Resources, kan du angive typen af berettigelse, der gælder for dette frynsegode. 

Du kan gøre et frynsegode tilgængelig for alle arbejdere. For eksempel tilbyder nogle firmaer parkeringskort til alle medarbejdere som et frynsegode. Når du opretter dette frynsegode, angiver du berettigelsen til **Alle arbejdere er berettigede**. 

For andre frynsegoder, f.eks. udlæg og afgifter, kan berettigelse ikke anvendes. Når du opretter disse typer af frynsegoder, kan du indstille berettigelse til **Tilsidesæt berettigelsesprocessen**. 

Endelig kan frynsegodeberettigelse være baseret på regler. Eksempelvis tilbyder en virksomhed frynsegoder i form af to typer af livsforsikring for medarbejderne. Ledende medarbejdere er berettiget til en livsforsikringsplan, mens andre fuldtidsansatte er berettiget til den anden livsforsikringsplan. I Human Resources kan du oprette en frynsegodeberettigelsesregel for at finde alle ledende medarbejdere og en anden regel for at finde andre fuldtidsansatte og derefter anvende disse regler på den relevante frynsegode.

## <a name="enrollment"></a>Tilmelding
Når du har oprettet de fordele, din virksomhed tilbyder, og fastsat berettigelse, kan du tilmelde din arbejdere frynsegoder. Du kan tilmelde en enkelt arbejder frynsegoder, eller du kan tilmelde mange arbejdere en eller flere frynsegoder i én enkelt proces. 

Nogle gange holder en organisation op med at tilbyde bestemte fordele. I så fald skal du opdatere frynsegodet og de arbejdere, der er tilmeldt. Med massefrynsegodeudløb kan du ændre udløbsdatoen for et frynsegode og arbejdertilmeldingerne for dette frynsegode samtidig. Du kan også vælge flere medarbejdere, der er tilmeldt et frynsegode, og ændre slutdatoen for deres disponering. 

På samme måde gør massefrynsegodeforlængelse det muligt at forlænge udløbsdatoen for både et frynsegode og arbejdertilmeldinger til det pågældende frynsegode, hvis du beslutter at tilbyde et frynsegode i længere tid end oprindeligt planlagt.




[!INCLUDE[footer-include](../includes/footer-banner.md)]