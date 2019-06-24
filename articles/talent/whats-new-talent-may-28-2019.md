---
title: Nyheder eller ændringer i Dynamics 365 for Talent (28. maj 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8b401717e598b8a37dc773cbe7ce1f15fa2f60e5
ms.sourcegitcommit: 291d90a857dd1be4ad58dc10d57415d6bddb09c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2019
ms.locfileid: "1616470"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-28-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (28. maj 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-home-page"></a>Jobgodkendelser på Startside

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id, titel, andre godkendere og tildelingsdato. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig har brug for at godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

I denne udgivelse understøtter følgende Common Data Service-enheder nu brugerdefinerede felter: Oplysninger om frynsegodeberegningssats, Arbejdskalenderferielinje og Ansættelse.

### <a name="copy-position-now-includes-payroll-details"></a>Kopiér stilling indeholder nu detaljer om løn.
Når du bruger **Kopiér stilling** og vælger alle indstillingerne, er lønoplysningerne nu medtaget i kopioplysningerne. 

## <a name="in-preview-in-core-hr"></a>Som eksempel i Core HR

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange forskellige typer orlov til medarbejdere. Nogle af disse orlovstyper er muligvis ikke egnede til, at medarbejderne sender anmodninger om fritid, og administreres af personale (HR) i stedet. Med denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side til validering af data i stillingshierarki

HR og administratorer kan validere ledelseshierarkiet for cirkulære referencer, der utilsigtet er importeret. Du kan få adgang til denne nye side fra **Virksomhedsadministration > Links > Stillinger > Validering af stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angiv årsagskoder for orlovstyper

Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger

Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri. Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav. Du kan angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale

Muligheden for at spor medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene Personale med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til fritidssaldiene.
