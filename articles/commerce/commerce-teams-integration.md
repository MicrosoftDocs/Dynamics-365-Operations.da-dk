---
title: Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
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
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908461"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="0d509-103">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="0d509-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d509-104">Dette emne giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.</span><span class="sxs-lookup"><span data-stu-id="0d509-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="0d509-105">Dynamics 365 Commerce integrerer med Teams for at hjælpe kunder og deres medarbejdere med at forbedre produktivitet ved at synkronisere opgavestyring mellem de to programmer.</span><span class="sxs-lookup"><span data-stu-id="0d509-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="0d509-106">Med den problemfri opgavestyring, som integration af Commerce og Teams giver, kan butikschefer og medarbejdere oprette opgavelister, tildele opgaver til flere butikker og spore status for opgaver på tværs af butikker fra det ene eller andet program.</span><span class="sxs-lookup"><span data-stu-id="0d509-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="0d509-107">Integration af Commerce og Teams er tilgængelig fra og med Commerce version 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="0d509-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="0d509-108">Hovedfunktioner</span><span class="sxs-lookup"><span data-stu-id="0d509-108">Key features</span></span>

<span data-ttu-id="0d509-109">Her er nogle af de vigtigste funktioner, som Commerce- og Microsoft Teams-integration indeholder:</span><span class="sxs-lookup"><span data-stu-id="0d509-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="0d509-110">Klargøre Teams ved at udnytte veldefinerede oplysninger fra Commerce, f.eks. organisationsstruktur og oplysninger om butikker, arbejdere, tilladelser og forretningssituation.</span><span class="sxs-lookup"><span data-stu-id="0d509-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="0d509-111">Nemt synkronisere løbende ændringer (f.eks. tilføjelse af nye butikker eller ansættelse af nye medarbejdere) mellem Commerce og Teams, men beholde Commerce som den overordnede kilde til data i organisationsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="0d509-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="0d509-112">Integrer opgavestyring mellem Commerce og Teams for at hjælpe butiksmedarbejdere, butikschefer, regionchefer og kommunikationsmedarbejdere med at håndtere opgavestyring fra begge programmer.</span><span class="sxs-lookup"><span data-stu-id="0d509-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="0d509-113">Forudsætninger for brug af integrationsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0d509-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="0d509-114">Følgende forudsætninger skal være tilstede, før du kan begynde at bruge Microsoft Teams-integrationsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="0d509-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="0d509-115">Microsoft 365 Business-standardlicens (denne licens inkluderer Teams).</span><span class="sxs-lookup"><span data-stu-id="0d509-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="0d509-116">Azure Active Directory-konti (Azure AD) for alle butikschefer og arbejdere</span><span class="sxs-lookup"><span data-stu-id="0d509-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="0d509-117">POS-systemer, der er konfigureret med Azure AD-godkendelse</span><span class="sxs-lookup"><span data-stu-id="0d509-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="0d509-118">Grundlæggende arkitektur</span><span class="sxs-lookup"><span data-stu-id="0d509-118">Conceptual architecture</span></span>

<span data-ttu-id="0d509-119">I følgende illustration vises den grundlæggende arkitektur for integration af Dynamics 365 Commerce og Microsoft Teams med en San Francisco-butik som eksempel.</span><span class="sxs-lookup"><span data-stu-id="0d509-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="0d509-120">Både Teams og Commerce POS-programmet bruger Microsoft Planner som lager, så opgaver, der udgives fra Teams, vises i POS-programmet, og ad hoc-opgaver, der er oprettet af butikschefer i POS-programmet, vises i Teams, hvilket medfører en problemfri opgavestyring mellem programmerne.</span><span class="sxs-lookup"><span data-stu-id="0d509-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Arkitektur for integration af Commerce og Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="0d509-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0d509-122">Additional resources</span></span>

[<span data-ttu-id="0d509-123">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="0d509-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="0d509-124">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0d509-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="0d509-125">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="0d509-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="0d509-126">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d509-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="0d509-127">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d509-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="0d509-128">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="0d509-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
