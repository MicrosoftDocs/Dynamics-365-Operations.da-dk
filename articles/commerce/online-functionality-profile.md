---
title: Oprette en onlinefunktionalitetsprofil
description: Dette emne beskriver, hvordan du opretter en onlineprofil for funktionalitet i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477726"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="69d82-103">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="69d82-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69d82-104">Dette emne indeholder en oversigt over opsætningen af en onlinefunktionalitetsprofil til Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="69d82-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="69d82-105">Profilen for onlinefunktionalitet giver forskellige indstillinger, der bruges til onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="69d82-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="69d82-106">Hver onlinekanal skal angive en profil for onlinefunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="69d82-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="69d82-107">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="69d82-107">Create an online functionality profile</span></span>

<span data-ttu-id="69d82-108">Følgende procedure forklarer, hvordan du kan oprette en onlinefunktionalitetsprofil i Commerce Headquarters-appen.</span><span class="sxs-lookup"><span data-stu-id="69d82-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="69d82-109">I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="69d82-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="69d82-110">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="69d82-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="69d82-111">Angiv et id for profilen i feltet **Profil**.</span><span class="sxs-lookup"><span data-stu-id="69d82-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="69d82-112">Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="69d82-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="69d82-113">Rediger indstillingerne for **Indkøbskurv**, **Detaildebitorer** eller **Betaling ved kassen** i sektionen **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="69d82-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="69d82-114">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="69d82-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="69d82-115">Følgende billede viser et eksempel på en profil for onlinefunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="69d82-115">The following image shows an example online functionality profile.</span></span>
  
![Eksempel på profil for onlinefunktionalitet](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="69d82-117">Funktioner</span><span class="sxs-lookup"><span data-stu-id="69d82-117">Functions</span></span>

- <span data-ttu-id="69d82-118">**Samling af produkter**: Når funktionen er aktiveret, tillader den, at der opdateres antal i indkøbskurven, når samme vare tilføjes flere gange.</span><span class="sxs-lookup"><span data-stu-id="69d82-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="69d82-119">**Tillad udtjekning uden betaling ved kassen**: Når funktionen er aktiveret, vil den håndtere scenariet, når varer, der føjes til indkøbsvognen, har en pris på 0,00 kr.</span><span class="sxs-lookup"><span data-stu-id="69d82-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="69d82-120">**Opret kunde i asynkron tilstand**: Dette er en ældre indstilling, der gælder for tredjeparts e-handelskanaler, og som ikke kan anvendes på Dynamics 365 e-handelsstedet.</span><span class="sxs-lookup"><span data-stu-id="69d82-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69d82-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="69d82-121">Additional resources</span></span>

[<span data-ttu-id="69d82-122">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="69d82-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="69d82-123">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="69d82-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="69d82-124">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="69d82-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="69d82-125">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="69d82-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="69d82-126">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="69d82-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
