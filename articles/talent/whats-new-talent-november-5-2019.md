---
title: Nyheder eller ændringer i Dynamics 365 Talent (5. november 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896767"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (5. november 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2598. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Kopier en Core HR-forekomst

I denne uges udgivelse kan du bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Talent: Core HR-database til et sandkasse-miljø. Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø. Du kan finde flere oplysninger i:

- [Bredere miljøstyring](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) i Dynamics 365: 2019 Frigivelsesbølge 2-plan

- [Kopier en Core HR-forekomst](hr-copy-instance.md) i Talent-dokumentation

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service-integrationsbatchjob oprettes ikke, når Common Data Service-integration er aktiveret (388030)

Denne ændring vil oprette batchjob til Common Data Service-integration, når den er aktiveret.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity ændrer ikke størrelsen på personbilledet, når det overføres (369469)

Denne uges udgivelse ændrer, hvordan billedernes størrelse tilpasses for at opnå en bedre ydeevne, når de importeres via datastyring.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>En stillings "Tilgængelig for tildelingsdato" kan ligge før Aktiveringsdatoen (340103)

Med denne ændring vises der en advarsel, hvis du vælger en **Tilgængelig for tildelingsdato**, der ligger før stillingens **Aktiveringsdato**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Der kan ikke oprettes en ændringsanmodning om kompensation i selvbetjening for medarbejder for trinbaserede planer (376872)

Denne version retter et problem, som opstår, når der anmodes om kompensationsændringer via selvbetjningstjenesten for medarbejdere for trinbaserede planer. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Årsagskoden synkroniseres ikke med Common Data Service, hvis beskrivelsen er længere end 30 tegn; Core HR tillader 60 (352682)

med denne ændring vil årsagskoder med mere end 30 tegn blive opdateret i Common Data Service. Ændringer, der foretages i Common Data Service, afspejles også i Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adresseintegration fra Talen til Finance and Operations (351961)

Denne udgivelse løser et problem, hvor adresser, der opdateres i Talent, ikke blev opdateret i Finance and Operations. Ændringer i adresseblokke opdateres nu.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.

### <a name="feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Funktioner tilføjes og opdateres i alle versioner. Administrationen af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.

Du kan få mere at vide om de ændringer, der kommer til funktionsstyring, under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
