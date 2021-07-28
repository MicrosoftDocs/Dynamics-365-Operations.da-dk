---
title: Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams
description: I dette emne kan du se, hvordan du kan tilknytte butikker og tilsvarende teams i Dynamics 365 Commerce-hovedkontoret, hvis din organisation allerede har oprettet teams i Microsoft Teams inden Commerce-integrationen.
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
ms.openlocfilehash: c75525749d9015387cc112beda104238a93698e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346686"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams

[!include [banner](includes/banner.md)]

I dette emne kan du se, hvordan du kan tilknytte butikker og tilsvarende teams i Dynamics 365 Commerce-hovedkontoret, hvis din organisation allerede har oprettet teams i Microsoft Teams inden Commerce-integrationen.

Der kan være oprettet teams i din organisation for nogle af eller alle dine butikker, før Dynamics 365 Commerce og Microsoft Teams integreres. Hvis det er tilfældet, skal du oprette opgavesynkronisering mellem Commerce POS og Microsoft Teams, og du skal angive tilknytningen af butikker og det tilsvarende team i Commerce-hovedkontoret.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Tilknytte butikker og tilsvarende teams i Commerce-hovedkontor 

Følg disse trin for at tilknytte butikker og tilsvarende teams i Commerce-hovedkontor.

1. Gå til **Systemadministration \> Arbejdsområde \> Datastyring**.
1. Vælg **Eksportér**. 
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv "Eksportér tilknytning af teams" under **Gruppenavn**.
1. Vælg **Tilføj enhed** i oversigtspanelet **Valgte enheder**. Dialogboksen **Tilføj enhed** vises.  
1. Vælg **Teams-tilknytning mellem kilde og team** på rullelisten **Enhedsnavn**.
1. Vælg **CSV** på rullelisten **Måldataformat**.
1. Vælg **Tilføj**, og vælg derefter **Luk**.
1. Vælg **Eksportér nu** øverst til venstre under handlingsruden.
1. Vælg **Download fil** under **Status for enhedsbehandling**.
1. I den eksporterede CSV-fil skal du angive værdier for **SOURCETYPE**, **SOURCEID** og **TEAMID** på følgende måde:
    - Indtast "RetailStore" for **SOURCETYPE**. 
    - For **SOURCEID** skal du angive butiksnummeret (f.eks. "000135" for San Francisco-butikken). Du kan finde butiksnumre i **Retail og Commerce \> Kanaler \> Butikker**.
    - For **TEAMID** skal du angive det tilsvarende team-id fra Microsoft Teams (f.eks. "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Du kan finde oplysninger om team-id'er på [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Gem CSV-filen på din lokale computer.
1. Gå til **Systemadministration \> Arbejdsområde \> Datastyring**, og vælg **Import**..
1. Vælg **Tilføj fil** i oversigtspanelet **Valgte enheder**. Dialogboksen **Tilføj fil** vises.
1. Vælg **Teams-tilknytning mellem kilde og team** på rullelisten **Enhedsnavn**.
1. Vælg **CSV** på rullelisten **Kildedataformat**.
1. Vælg **Upload og tilføj**, vælg den CSV-fil, du har gemt tidligere, og vælg derefter **Åbn**.
1. Vælg **Luk** i dialogboksen **Tilføj fil**.
1. Vælg **Gem** i handlingsruden, og vælg derefter **Import**.

I følgende eksempelbillede vises gruppen **Eksportér tilknytning af teams** i Commerce med **Tilføj enhed**-elementer og de eksporterede CSV-filhoveder fremhævet.

![Gruppen Eksportér tilknytning af teams i Commerce med Tilføj enhed-elementer og de eksporterede CSV-filhoveder fremhævet.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Når du har fuldført de forudgående trin, skal du udføre trinnene i [Synkronisere opgavestyring mellem Microsoft Teams og POS](synchronize-tasks-teams-pos.md) for at synkronisere opgavestyring. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
