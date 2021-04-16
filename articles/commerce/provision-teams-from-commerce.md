---
title: Klargøre Microsoft Teams fra Dynamics 365 Commerce
description: I dette emne beskrives, hvordan Microsoft Teams kan klargøres ved hjælp af organisationsdata fra Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842638"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Klargøre Microsoft Teams fra Dynamics 365 Commerce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I dette emne beskrives, hvordan Microsoft Teams kan klargøres ved hjælp af organisationsdata fra Dynamics 365 Commerce.

Dynamics 365 Commerce er en nem måde at klargøre Teams på, hvis du endnu ikke har konfigureret teams til dine detailforretninger der. Ved at udnytte veldefinerede oplysninger fra Commerce, som du vil bruge i Teams, kan du hjælpe butiksmedarbejderne med at komme i gang i Teams. Disse oplysninger omfatter organisationshierarki, butiksnavne, medarbejderoplysninger og Azure Active Directory-konti (Azure AD). 

Klargøringsprocessen for Teams har to hovedtrin:

1. I Teams skal du oprette et team for hver detailbutik og tilføje butiksmedarbejdere som medlemmer af det relevante team. Hvis en medarbejder er tilknyttet mere end én detailbutik, afspejler teammedlemskab dette. Der oprettes et kommunikationsteam, der omfatter lokale ledere som medlemmer, som kan hjælpe med at publicere opgaver fra Teams.
1. Upload dit organisationshierarki fra Commerce til Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Klargøre Teams i Commerce-hovedkontor

Udfør følgende opgaver, før du klargør Microsoft Teams:

- Bekræft, at alle regionchefer er blevet gjort til kommunikationschefer.
- Bekræft, at Azure-kontoen for hver butikschef og medarbejder er blevet knyttet til den pågældende chefs eller medarbejders arbejderpost i Commerce-hovedkontoret.

Du kan klargøre Teams i Commerce-hovedkontoret ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.
1. Vælg **Klargør Teams** i handlingsruden. Der oprettes et batchjob med navnet **Teams-klargøring**.
1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**, og find det seneste job, der indeholder beskrivelsen **Teams-klargøring**. Vent, indtil jobbet er kørt færdig.

> [!TIP]
> Hvis ingen af dine lokale ledere, butikschefer og butiksmedarbejdere er blevet tilknyttet en Teams-licens, kan du få vist følgende fejlmeddelelse: "Det lykkedes ikke at hente brugbare SKU-kategorier for brugeren". Hvis du vil løse problemet, skal du vælge **Synkroniser teams og medlemmer** i handlingsruden.

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Validere klargøring af Teams i Teams Administration

Hvis du vil validere Microsoft Teams-klargøring i Microsoft Teams Administrationen, skal du følge disse trin.
    
1. Gå til [Teams Administration](https://admin.teams.microsoft.com/), og log på som administrator af din e-handelslejer.
1. Vælg **Teams** i venstre navigationsrude for at udvide den, og vælg derefter **Administrer teams**.
1. Bekræft, at der er oprettet ét team for hver Commerce-detailbutik.
1. Vælg et team, og bekræft, at butiksmedarbejdere er føjet til det som medlemmer.
1. Vælg **Brugere** i venstre navigationsrude, og bekræft, at alle butiksmedarbejdere i alle butikker er blevet tilføjet som brugere.

I følgende illustration vises et eksempel på siden **Administrer teams** i Teams Administration.

![Eksempel på siden Administrer teams i Teams Administration](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Uploade et Commerce-organisationshierarki til Teams
    
Commerce-organisationshierarkiet kan bruges i Microsoft Teams til at publicere opgaver til alle eller udvalgte butikker, der bruger samme hierarkistruktur.

Følg disse trin for at uploade et Commerce-organisationshierarki til Teams.
    
1. Gå i Commerce-hovedkontoret til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.
1. Vælg **Download målretningshierarki**, og vælg derefter **Detailbutikker efter område** for at downloade en kommasepareret fil (CSV) med organisationshierarkiet.
1. Installer Microsoft Teams PowerShell-modulet ved at følge trinnene i [Installere Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).
1. Når du bliver bedt om det i Teams PowerShell-vinduet, skal du logge på med administratorkontoen for din Azure AD-lejer.
1. Følg trinnene i [Konfigurere dit teammålretningshierarki](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) for at uploade CSV-filen til målretningshierarkiet.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Kontrollere, at organisationshierarkiet er blevet uploadet til Teams

Du kan kontrollere, at organisationshierarkiet er blevet uploadet til Microsoft Teams, ved at følge disse trin.

1. Log på Teams som kommunikationschef.
1. Vælg **Opgaver efter planlægning** i den venstre navigationsrude.
1. Opret en ny liste med en dummy-opgave under fanen **Publicerede lister**.
1. Vælg **Publicer**. Organisationshierarkiet skal vises i dialogboksen **Vælg, hvem der skal publiceres til**, som vist i eksemplet på følgende illustration.

![Eksempel på et organisationshierarki i dialogboksen Vælg, hvem der skal publiceres til](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
