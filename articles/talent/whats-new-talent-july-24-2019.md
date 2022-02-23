---
title: Nyheder eller ændringer i Dynamics 365 Talent (23. juli 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 360574d3c8e0b349119e0987f2453a5d5be21e90
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528141"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (23. juli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="pdf-renderer-for-candidate-documents"></a>PDF-gengivelse til kandidatdokumenter

Brugere af Attract kan nu få vist vedhæftede PDF-filer for kandidater i dokumentfremviseren i stedet for at downloade de vedhæftede filer.

### <a name="signing-up-for-attract-user-research-group"></a>Tilmelding til Attract-brugerundersøgelsesgruppe 

Når vi planlægger nye produktegenskaber eller leverer prøvefunktioner, søger vi brugere, der kan være med til at styre os i den rette retning. Interesserede brugere kan nu tilmelde sig, så de bliver en del af vores brugerundersøgelsesgruppe, ved at bruge tilmeldingslinket i vores app.

### <a name="job-approvals-appear-on-the-home-page"></a>Jobgodkendelser vises på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id'et, jobtitlen, andre godkendere og datoen, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig skal godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2394.

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Enhedsunderstøttelse i Common Data Service af brugerdefinerede felter 

Med denne udgivelse understøtter **Arbejdskalender** og dag i **Arbejdskalender** nu brugerdefinerede felter i Common Data Service.

### <a name="restrict-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange forskellige typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

## <a name="in-preview"></a>Som eksempel

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Visningsfunktioner er kun aktiverede i sandkasseforekomster

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**. Forekomster af typen **Sandkasse** giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Få vist udvidede oplysninger om performance i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye gennemgange, som deres medarbejdere kan være med til at styre. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede. 

## <a name="coming-soon"></a>Kommer snart

### <a name="region-support-for-canada-and-southeast-asia"></a>Områdeunderstøttelse af Canada og Sydøstasien

Vi er glade for at kunne oplyse, at Canada og Sydøstasien vil være tilgængelige for Talent den 1. august 2019. Med denne ændring kan du oprette miljøer i de canadiske og asiatiske områder, og alle Talent-data vil blive opbevaret udelukkende inden for disse steder. Du kan oprette et miljø i disse nye områder ved at vælge stedet i dialogboksen Nyt miljø og bruge det pågældende miljø til at klargøre Talent i LCS som beskrevet her i [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Dataoverflytning af eksisterende projekter fra andre områder til de canadiske og asiatiske områder understøttes ikke. Det er kun nye projekter, der kan klargøres til disse nye understøttede områder.
