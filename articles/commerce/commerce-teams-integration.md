---
title: Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
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
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021983"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="3ff23-103">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3ff23-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ff23-104">Dette emne giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.</span><span class="sxs-lookup"><span data-stu-id="3ff23-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="3ff23-105">Dynamics 365 Commerce integrerer med Teams for at hjælpe kunder og deres medarbejdere med at forbedre produktivitet ved at synkronisere opgavestyring mellem de to programmer.</span><span class="sxs-lookup"><span data-stu-id="3ff23-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="3ff23-106">Med den problemfri opgavestyring, som integration af Commerce og Teams giver, kan butikschefer og medarbejdere oprette opgavelister, tildele opgaver til flere butikker og spore status for opgaver på tværs af butikker fra det ene eller andet program.</span><span class="sxs-lookup"><span data-stu-id="3ff23-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="3ff23-107">Integration af Commerce og Teams er tilgængelig fra og med Commerce version 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="3ff23-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="3ff23-108">Hovedfunktioner</span><span class="sxs-lookup"><span data-stu-id="3ff23-108">Key features</span></span>

<span data-ttu-id="3ff23-109">Her er nogle af de vigtigste funktioner, som Commerce- og Microsoft Teams-integration indeholder:</span><span class="sxs-lookup"><span data-stu-id="3ff23-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="3ff23-110">Klargøre Teams ved at udnytte veldefinerede oplysninger fra Commerce, f.eks. organisationsstruktur og oplysninger om butikker, arbejdere, tilladelser og forretningssituation.</span><span class="sxs-lookup"><span data-stu-id="3ff23-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="3ff23-111">Nemt synkronisere løbende ændringer (f.eks. tilføjelse af nye butikker eller ansættelse af nye medarbejdere) mellem Commerce og Teams, men beholde Commerce som den overordnede kilde til data i organisationsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="3ff23-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="3ff23-112">Integrer opgavestyring mellem Commerce og Teams for at hjælpe butiksmedarbejdere, butikschefer, regionchefer og kommunikationsmedarbejdere med at håndtere opgavestyring fra begge programmer.</span><span class="sxs-lookup"><span data-stu-id="3ff23-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="3ff23-113">Forudsætninger for brug af integrationsfunktioner</span><span class="sxs-lookup"><span data-stu-id="3ff23-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="3ff23-114">Følgende forudsætninger skal være tilstede, før du kan begynde at bruge Microsoft Teams-integrationsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="3ff23-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="3ff23-115">Microsoft 365 Business-standardlicens (denne licens inkluderer Teams).</span><span class="sxs-lookup"><span data-stu-id="3ff23-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="3ff23-116">Azure Active Directory-konti (Azure AD) for alle butikschefer og arbejdere</span><span class="sxs-lookup"><span data-stu-id="3ff23-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="3ff23-117">POS-systemer, der er konfigureret med Azure AD-godkendelse</span><span class="sxs-lookup"><span data-stu-id="3ff23-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="3ff23-118">Grundlæggende arkitektur</span><span class="sxs-lookup"><span data-stu-id="3ff23-118">Conceptual architecture</span></span>

<span data-ttu-id="3ff23-119">I følgende illustration vises den grundlæggende arkitektur for integration af Dynamics 365 Commerce og Microsoft Teams med en San Francisco-butik som eksempel.</span><span class="sxs-lookup"><span data-stu-id="3ff23-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="3ff23-120">Både Teams og Commerce POS-programmet bruger Microsoft Planner som lager, så opgaver, der udgives fra Teams, vises i POS-programmet, og ad hoc-opgaver, der er oprettet af butikschefer i POS-programmet, vises i Teams, hvilket medfører en problemfri opgavestyring mellem programmerne.</span><span class="sxs-lookup"><span data-stu-id="3ff23-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Arkitektur for integration af Commerce og Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="3ff23-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3ff23-122">Additional resources</span></span>

[<span data-ttu-id="3ff23-123">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3ff23-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="3ff23-124">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3ff23-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="3ff23-125">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="3ff23-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="3ff23-126">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3ff23-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="3ff23-127">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3ff23-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="3ff23-128">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3ff23-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
