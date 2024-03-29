---
title: Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS
description: Denne artikel beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746091"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.

Et af de væsentligste formål med Teams-integration er at aktivere synkronisering af opgavestyring mellem POS-programmet og Teams. På den måde kan butiksansatte enten bruge POS-programmet eller Teams til at administrere opgaver og behøver ikke skifte program.

Da Planner bruges som lager for opgaver i Teams, skal der være et link mellem Teams og Dynamics 365 Commerce. Dette link oprettes ved hjælp af et bestemt plan-id for et bestemt butiksteam.

Følgende procedurer viser, hvordan du kan konfigurere synkronisering af opgavestyring mellem POS- og Teams-applikationerne.

## <a name="link-pos-and-teams-for-task-management"></a>Forbinde POS og Teams til opgavestyring

Benyt følgende fremgangsmåde for at sammenkæde POS- og Microsoft Teams-programmer til opgavestyring i Commerce Headquarters.

> [!NOTE]
> Før du forsøger at integrere Opgavestyring med Teams, skal du sørge for, at du er aktiveret [Dynamics 365 Commerce og Microsoft Teams-integration](enable-teams-integration.md). 

1. Gå til **Retail og Commerce \> Opgavestyring \> Opgaveintegration med Microsoft Teams**.
1. Vælg **Rediger** i handlingsruden.
1. Indstil **Aktivér integration af opgavestyring** til **Ja**.
1. Vælg **Gem** i handlingsruden.
1. Vælg **Konfigurer opgavestyring** i handlingsruden. Du skal modtage en besked om, at der oprettes et batchjob med navnet **Teams-klargøring**.
1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**, og find det seneste job, der indeholder beskrivelsen **Teams-klargøring**. Vent, indtil jobbet er kørt færdig.
1. Kør **CDX-job 1070** for at publicere plan-id'et og butiksreferencerne til Retail Server.

## <a name="publish-a-test-task-list-in-teams"></a>Publicere en testopgaveliste i Teams

I følgende procedure antages det, at butiksteamene bruger integration af Microsoft Teams-opgavestyring med Commerce for første gang.

Hvis du vil publicere en testopgaveliste i Teams, skal du udføre disse trin.

1. Log på Teams som kommunikationschef. Kommunikationschefer er typisk brugere, der har rollen **Regionschef** i Commerce.
1. Vælg **Opgaver efter planlægning** i den venstre navigationsrude.
1. Under fanen **Publicerede lister** skal du vælge **Ny liste** nederst til venstre og navngive den nye liste **Testopgaveliste**.
1. Vælg **Opret**. Den nye liste vises under **Kladder**.
1. Giv den første opgave titlen **Test af Teams-integration** under **Opgavetitel**. Vælg derefter **Angiv**.
1. Vælg opgavelisten på listen **Kladder**. Vælg derefter **Publicer** i øverste højre hjørne.
1. Vælg de teams, der skal modtage testopgavelisten, i dialogboksen **Vælg, hvem der skal publiceres til**.
1. Vælg **Næste** for at gennemse publikationsplanen. Hvis du skal foretage ændringer, skal du vælge **Tilbage**. 
1. Vælg **Bekræft, at du vil fortsætte**, og vælg derefter **Publicer**.
1. Når publiceringen er fuldført, angiver en meddelelse øverst under fanen **Publicerede lister**, om opgavelisten er blevet leveret.

Du kan finde flere oplysninger i [Publicere opgavelister for at oprette og spore arbejde i organisationen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> Når opgavelisten er udgivet i Teams, vises opgaverne i POS. POS-administratorer og kasserere skal derefter aktivere Azure AD-logon i POS. Du kan få flere oplysninger i artiklen [Aktivere Azure Active Directory-godkendelse for POS-logon](aad-pos-logon.md). 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
