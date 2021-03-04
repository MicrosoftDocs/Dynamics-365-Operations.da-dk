---
title: Nyheder eller ændringer i Dynamics 365 Talent (4. juni 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528029"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (4. juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-the-home-page"></a>Jobgodkendelser på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**. I dette afsnit vises job-id, titel, andre godkendere og den dato, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**. Denne sektion viser de godkendere, der stadig skal godkende det indsendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

De ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side til validering af data i stillingshierarki

Personale (HR) og administratorer kan validere ledelseshierarkiet for cirkulære referencer, der utilsigtet blev importeret. Du kan få adgang til denne nye side fra **Organisationsadministration \> Links \> Stillinger \> Validering af stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angiv årsagskoder for orlovstyper

Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger

Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri. Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav. Du kan angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale

Muligheden for at spore medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene personaleafdelingen med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til fritidssaldiene.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Hvis du sletter en post fra Talent, betyder det ikke, at posten fjernes fra Common Data Service

Poster, der fjernes fra Talent: Core HR, fjernes nu også fra Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Gyldig fra/til datoer for variabel lønstruktur bliver ikke accepteret

I denne version kan du ikke tilmelde en medarbejder til en variabel lønstruktur, hvis startdatoen ligger før planens startdato, eller slutdatoen er efter planens slutdato. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Kommentarer til gennemgang af performance fjernes, når brugerne vælger Annuller

Denne udgivelse retter et problem, hvor kommentarer til gennemgang fjernes, hvis en bruger begynder at ændre en kommentar, men derefter vælger **Annuller**. 

## <a name="in-preview"></a>Som eksempel

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Visningsfunktioner er kun aktiverede i sandkasseforekomster

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**. Forekomster af typen **Sandkasse** giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange forskellige typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Få vist udvidede oplysninger om performance i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye gennemgange, som deres medarbejdere kan være med til at styre. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede. 

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Medarbejdere, ledere og personaleafdelingen kan udskrive en medarbejders performancegennemgang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]