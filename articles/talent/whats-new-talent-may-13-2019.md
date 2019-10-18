---
title: Nyheder eller ændringer i Dynamics 365 Talent (13. maj 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42feeb044d0a4cd25faf2d74863aa4e948c200fd
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008806"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (13. maj 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-home-page"></a>Jobgodkendelser på Startside

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id, titel, andre godkendere og tildelingsdato. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig har brug for at godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2297. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Angive en forekomsttype under klargøring af Talent

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**, hvilket giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

I denne uges udgivelse understøtter følgende Common Data Service-enheder nu brugerdefinerede felter: Ansættelse, Frynsegodeberegningsfrekvens, Frynsegodeberegningssats, Arbejdskalenderferie og Identifikationstype.

### <a name="common-data-service-integration-page"></a>Common Data Service-integrationsside

Denne version giver dig en ny indstilling i **Systemadministration > Links > Integrationer > Common Data Service > Konfiguration**. Indstillingen **Common Data Service-konfiguration** giver en administrator eller dataadministratorer en vis fleksibilitet og indsigt med Common Data Service. Med denne indstilling kan du aktivere eller deaktivere Common Data Service-integration med en Talent-forekomst og få vist synkroniseringsdetaljerne mellem Talent-forekomsten og Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Importere ydelsesdata med endelig medarbejderrangering (316710)

I denne version kan du importere historiske medarbejderrangeringsdata. Feltet **FinalEmployeeRatingId** har nu skrivetilladelse.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Det er ikke muligt at oprette arbejderadresse i Common Data Service og synkronisere den med Talent (317555)

Denne ændring gør det muligt at adresse data, der er oprettet i Common Data Service, til synkronisering med Talent.

## <a name="in-preview"></a>Som eksempel

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side til validering af data i stillingshierarki

Personale (HR) og administratorer kan validere ledelseshierarkiet for cirkulære referencer, der utilsigtet er importeret. Du kan få adgang til denne nye side fra **Virksomhedsadministration > Links > Stillinger > Validering af stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angiv årsagskoder for orlovstyper

Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger

Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri. Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav. Du kan angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale

Muligheden for at spor medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene Personale med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til fritidssaldiene.
