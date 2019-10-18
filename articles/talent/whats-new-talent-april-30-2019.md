---
title: Nyheder eller ændringer i Dynamics 365 Talent (30. april 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38158948dbcf8966edf49bcce5b1e5da7eddb8dc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026027"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (30. april 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

De ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2270. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Giv tilbagemelding

Muligheden for at give feedback findes i menuen **Hjælp** (**?**) i Talent. Denne menu giver adgang til følgende ressourcer:

- Tilbagemelding
- Hjælp
- Introduktion
- Support
- Ideer
- Om

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Forbedringer i brugergrænsefladen for duplikeret medarbejderregistrering

På grund af denne ændring registreres dubletter nu, når du angiver navnefelter, og en statusindikator viser antallet af dubletter, der er registreret. Et link, der angives, åbner en side, hvor du kan vurdere, om du skal bruge en af de to dubletter. For at undgå forstyrrelser i forbindelse med indtastning af data åbnes dubletsiden ikke automatisk. Du skal vælge linket for at åbne siden.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

I denne uges udgivelse understøtter følgende enheder nu brugerdefinerede felter: Ansættelse, Frynsegodetype og Betalingscyklus.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Der opstår en fejl, når en offboarding-kontrolliste tildeles (299877)

Denne ændring retter fejlen i en fejlmeddelelse, der vises, når du tildeler en offboarding-kontrolliste til en medarbejder uden for fratrædelsesprocessen.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Linket til de arbejdere, der har forladt virksomheden, åbner den forkerte arbejder (309939)

Denne ændring retter et problem, der opstår, når du er ved at ansætte en medarbejder fra en anden juridisk enhed og forsøger at gå til medarbejderen fra listen over arbejdere, der har forladt virksomheden.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Selvbetjeningskortet til medarbejderkompensation viser ikke opsummeringsværdier, når avanceret sikkerhed er slået til (315231)

Denne ændring retter et problem, der opstår, når du bruger den avancerede kompensationssikkerhed. Når avanceret sikkerhed er slået til, viser medarbejderselvbetjening nu oversigtskompensationsbeløbene for både medarbejdere og ledere. Før denne ændring blev opsummeringsværdier vist som 0 (nul).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Hvis der oprettes en stilling uden en titel i Common Data Service, oprettes der ikke en stilling i Talent (314562)

Denne uges ændringer løser et problem, der opstår, når du opretter stillinger i Common Data Service, men ikke angiver en titel.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Fejlmeddelelse i performancekladdeposteringer i medarbejderselvbetjening (314134)

Denne ændring løser et problem, der opstår, når du knytter performancemål til performancekladdeposter i medarbejderselvbetjening.

## <a name="in-preview"></a>Som eksempel

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tilladelse til angivelse af årsagskoder for orlovstyper

Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger

Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri. Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav. Du kan nu angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale

Muligheden for at spor medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene Personale med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til saldiene.

## <a name="coming-soon"></a>Kommer snart

### <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser

Med Platform update 26 til Finance and Operations kan brugerne oprette påmindelsesregler, som automatisk sender mailbeskeder til kontakter, når beskeder udløses af en hændelse.
