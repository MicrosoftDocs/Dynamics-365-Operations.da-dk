---
title: Nyheder eller ændringer i Dynamics 365 Talent (9. juli 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528024"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (9. juli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Kommer snart i Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Jobgodkendelser vises på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id'et, jobtitlen, andre godkendere og datoen, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig skal godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Platform update 28 til Finance and Operations

Du kan finde yderligere oplysninger om Platform update 28 til Finance and Operations under [Funktioner i prøveversionen af Dynamics 365 Finance and Operations (28- juli 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Enhedsunderstøttelse i Common Data Service af brugerdefinerede felter 

Følgende enheder understøtter brugerdefinerede felter: 

- **Kompensation - fast struktur**
- **Opsætning af kompensationsreferencepunkt**
- **Opsætningslinje for kompensationsreferencepunkt**
- **Lønkode**
- **Lønperiode**
- **Hændelse for fast løn**
- **Kompensationsgitter**

Sådan får du vist alle opdaterede objekter i Talent:

1. Vælg **Systemadministration**, vælg **Links**, og vælg derefter **Konfiguration af Common Data Service**.
2. Vælg rullemenuen **CDS-enhedsnavn**. Alle de viste enheder findes på den nyeste version. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Det fulde navn, der er føjet til arbejderenheden i Common Data Service

Feltet **Fulde navn** er blevet føjet til **Arbejder**-enheden.

### <a name="full-time-equivalent-higher-than-10"></a>Fuldtidsækvivalent højere end 1,0

Der vises nu en advarsel, hvis der er angivet en værdi, der er større end 1,0, for en fuldtidsmedarbejder på en stilling. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>En advarsel vises ikke længere på siden Arbejder, når der ikke er nogen ansættelse med fremtidig dato

Du modtager ikke længere en meddelelse, der angiver, at der findes en fremtidig ansættelse, når du navigerer til siden **Arbejder** fra listen **Naturlig afgang** i arbejdsområdet **Personalestyring**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>En forretningsproces kan ikke slettes i Talent

Du kan nu slette forretningsprocesser i arbejdsområdet **Forretningsproces**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Orlovssaldo viser ikke længere nul for planer uden periodiseringer, når saldoen bruges pr. periodiseringsperiode

Planer, der er oprettet uden periodiseringer, kan nu vise en saldo.

## <a name="in-preview"></a>Som eksempel

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Visningsfunktioner er kun aktiverede i sandkasseforekomster

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**. Forekomster af typen **Sandkasse** giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange forskellige typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Få vist udvidede oplysninger om performance i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye gennemgange, som deres medarbejdere kan være med til at styre. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede. 

### <a name="entities-supporting-custom-fields"></a>Enheder, der understøtter brugerdefinerede felter

Følgende enheder aktiveres for brugerdefinerede felter i Common Data Service: 

- **Orlovstype**
- **Arbejders bankkonto**
- **Arbejdskalender**


[!INCLUDE[footer-include](../includes/footer-banner.md)]