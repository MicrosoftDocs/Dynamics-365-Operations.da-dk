---
title: Nyheder eller ændringer i Dynamics 365 Talent (6. maj 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f06d989ea4e927111729dfbd4bb7700745a16a54
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897505"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (6. maj 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Vælge valgfrie dokumenter ved oprettelse af tilbud

Når du vælger en skabelon til en tilbudspakke, bliver du nu spurgt, om du vil vælge de relevante valgfrie dokumenter fra pakkeskabelonen. Du kan tilføje andre valgfrie dokumenter, mens tilbuddet forberedes.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2282. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Platform update 26 til Finance and Operations

Du kan finde yderligere oplysninger om Platform update 26 til Finance and Operations under [Funktioner i prøveversionen af Dynamics 365 Finance and Operations Platform update 26 (maj 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

I denne uges udgivelse understøtter følgende enheder nu brugerdefinerede felter: Frynsegodeberegningsfrekvens, Frynsegodeberegningssats, Frynsegodetype, Arbejdskalender, Arbejdskalenderferie, Betalingscyklus og Arbejderidentifikationstyper.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Afslutning af massetilmelding og ændring af niveaugrundlaget til "anciennitetsdato" opdaterer ikke den indledende periodiseringssats (318526)

Når du massetilmelder medarbejdere og ændrer niveaugrundlaget, afspejler den indledende periodisering nu det valgte niveau.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Arbejdsgang, der viser dubletter af pladsholdere (313636)

Ændringer i denne version eliminerer duplikering af pladsholdere, når der sendes arbejdsgangsbeskeder.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensionsfelter opdateres ikke, når der bruges "Åbn i Excel" (176261)

Med denne version kan du nu opdatere den økonomiske dimension ved hjælp af **Åbn i Excel** fra siden **Arbejder**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>En arbejderadresse, der er oprettet i Common Data Service, synkroniseres ikke med Talent (317555)

Med denne ændring opdateres adresser, der er oprettet i Common Data Service, i Talent: Core HR.


## <a name="in-preview"></a>Som eksempel

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side til validering af data i stillingshierarki

Personale (HR) og administratorer kan nu validere ledelseshierarkiet for cirkulære referencer, der utilsigtet er importeret. Du kan få adgang til denne nye side fra **Virksomhedsadministration > Links > Stillinger > Validering af stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angiv årsagskoder for orlovstyper

Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger

Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri. Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav. Du kan nu angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale

Muligheden for at spor medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene Personale med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til saldiene.

## <a name="coming-soon"></a>Kommer snart

### <a name="indicate-instance-type-when-provisioning-talent"></a>Angive en forekomsttype under klargøring af Talent

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**, hvilket giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til Produktion-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til Sandkasse-forekomsttypen, skal du kontakte Support for at starte ændringsanmodningen.
