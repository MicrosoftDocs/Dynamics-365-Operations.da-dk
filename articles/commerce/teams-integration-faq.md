---
title: Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne indeholder svar på ofte stillede spørgsmål vedrørende Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019464"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration

[!include [banner](includes/banner.md)]

Dette emne indeholder svar på ofte stillede spørgsmål vedrørende Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Hvem i butikken bliver ejer af et team, når Teams klargøres fra Commerce? 

Alle butikschefer føjes automatisk til den tilsvarende teamgruppe som ejere, så de kan udføre handlinger, f.eks. tilføjelse af en privat kanal og tilføjelse eller sletning af medlemmer. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Hvordan tildeler jeg rollen "kommunikationschef" til en medarbejder i Commerce-hovedkontoret? 

Kommunikationschefer har i Microsoft Teams mulighed for at oprette og publicere opgavelister. Organisationsmedarbejdere, der har brug for at blive kommunikationschefer, skal have rollen "detailopgaveadministrator" tildelt i Commerce-hovedkontoret.

Hvis du vil tildele rollen detailopgaveadministrator til en medarbejder i Commerce-hovedkontoret, skal du udføre følgende trin.

1. Gå til **Retail og Commerce \> Medarbejdere \> Brugere**.
1. Vælg medarbejderen.
1. Klik på **Tildel roller** i oversigtspanelet **Brugers roller**.
1. Vælg rollen **Retail Jobliste** i dialogboksen **Tildel roller til bruger**, og vælg derefter **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Hvordan gør jeg et bestemt organisationshierarki tilgængeligt for upload til Microsoft Teams?

I Commerce-hovedkontoret er hver organisations hierarki tilknyttet et eller flere formål. Kontrollér, at det hierarki, du vil klargøre til Microsoft Teams, har formålet **Detailrapportering** tilknyttet, som vist i følgende billede af eksemplet nedenfor. 

![Eksempel på et formål med organisationshierarki i Commerce-hovedkontoret](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Hvordan sætter jeg detailbutiksmedarbejdere i stand til at logge på Commerce POS via Azure Active Directory (Azure AD)?

Du kan finde oplysninger om, hvordan du konfigurerer Commerce POS-logon til at bruge Azure AD-godkendelse, i [Aktivere Azure Active Directory-godkendelse for POS-logon](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Hvordan tilknytter jeg butikker og tilsvarende teams i Commerce-hovedkontoret, hvis min organisation allerede har oprettet teams i Microsoft Teams?

Oplysninger om, hvordan du kan tilknytte butikker og teams, hvis der findes eksisterende teams, finder du i [Tilknytte butikker og tilsvarende teams, hvis organisationen har eksisterende teams i Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Hvordan rydder jeg det Microsoft Graph API-token, der er gemt i sessionslageret?

En bruger, der har logget på POS POS med en Azure Active Directory-konto (Azure AD), skal logge af POS eller lukke programmet for at rydde sessionslageret. 

> [!TIP]
> Det anbefales at anvende den bedste fremgangsmåde, hvis butiksmedarbejdere altid låser POS-terminalen eller logger af en session, når de ikke bruger terminalen. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Hvad sker der, hvis en butik ikke har butikschefer?

Hvis en butik ikke har chefer, oprettes der ikke en teamgruppe for butikken eller i Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Hvad sker der, hvis en butikschef forlader firmaet?

Alle med ejerrollen kan tilføje en ny butikschef i Commerce-hovedkontoret og klargøre Teams igen, så den nye chef får de nødvendige rettigheder i Teams for gruppen. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)
