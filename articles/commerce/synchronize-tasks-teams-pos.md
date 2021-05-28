---
title: Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS
description: Dette emne beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.
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
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020621"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.

Et af de væsentligste formål med Teams-integration er at aktivere synkronisering af opgavestyring mellem POS-programmet og Teams. På den måde kan butiksansatte enten bruge POS-programmet eller Teams til at administrere opgaver og behøver ikke skifte program.

Da Planner bruges som lager for opgaver i Teams, skal der være et link mellem Teams og Dynamics 365 Commerce. Dette link oprettes ved hjælp af et bestemt plan-id for et bestemt butiksteam.

Følgende procedurer viser, hvordan du kan konfigurere synkronisering af opgavestyring mellem POS- og Teams-applikationerne.

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

## <a name="link-pos-and-teams-for-task-management"></a>Forbinde POS og Teams til opgavestyring

Benyt følgende fremgangsmåde for at sammenkæde POS- og Microsoft Teams-programmer til opgavestyring i Commerce-hovedkontoret.

1. Gå til **Retail og Commerce \> Opgavestyring \> Opgaveintegration med Microsoft Teams**.
1. Vælg **Rediger** i handlingsruden.
1. Indstil **Aktivér integration af opgavestyring** til **Ja**.
1. Vælg **Gem** i handlingsruden.
1. Vælg **Konfigurer opgavestyring** i handlingsruden. Du skal modtage en besked om, at der oprettes et batchjob med navnet **Teams-klargøring**.
1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**, og find det seneste job, der indeholder beskrivelsen **Teams-klargøring**. Vent, indtil jobbet er kørt færdig.
1. Kør **CDX-job 1070** for at publicere plan-id'et og butiksreferencerne til Retail Server.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
