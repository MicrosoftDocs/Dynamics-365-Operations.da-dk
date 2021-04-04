---
title: Oprette en detailfunktionalitetsprofil
description: I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478302"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="4863d-103">Oprette en detailfunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="4863d-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4863d-104">I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4863d-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4863d-105">Commerce-funktionalitetsprofilen giver forskellige indstillinger, der bruges til onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="4863d-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="4863d-106">Hver kanal skal angive en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="4863d-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="4863d-107">Opret en funktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="4863d-107">Create a functionality profile</span></span>

<span data-ttu-id="4863d-108">Benyt følgende fremgangsmåde for at oprette en ny funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="4863d-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="4863d-109">I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> POS-profiler \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="4863d-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="4863d-110">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4863d-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4863d-111">Angiv et id for profilen ("FN006" i eksempelbilledet nedenfor) i feltet **Profil**.</span><span class="sxs-lookup"><span data-stu-id="4863d-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="4863d-112">Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="4863d-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="4863d-113">Vælg et land til **ISO**-landestandarden i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="4863d-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="4863d-114">Rediger andre indstillinger i sektionen **Generelt** efter behov.</span><span class="sxs-lookup"><span data-stu-id="4863d-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="4863d-115">I sektionen **Generelt** skal du vælge et **Kvitteringsprofil-id** for mailkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="4863d-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="4863d-116">Rediger indstillinger i sektionen **Funktioner** efter behov.</span><span class="sxs-lookup"><span data-stu-id="4863d-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="4863d-117">Rediger indstillinger i sektionen **Beløb** efter behov.</span><span class="sxs-lookup"><span data-stu-id="4863d-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="4863d-118">Rediger indstillinger i sektionen **Infokoder** efter behov.</span><span class="sxs-lookup"><span data-stu-id="4863d-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="4863d-119">Rediger indstillinger i sektionen **Kvitteringsnummerering** efter behov.</span><span class="sxs-lookup"><span data-stu-id="4863d-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="4863d-120">Følgende billede viser et eksempel på en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="4863d-120">The following image shows an example functionality profile.</span></span>
  
![Eksempel på funktionalitetsprofil](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="4863d-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4863d-122">Additional resources</span></span>

[<span data-ttu-id="4863d-123">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="4863d-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="4863d-124">Oprette nyt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="4863d-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="4863d-125">Oversigt over skærmlayout</span><span class="sxs-lookup"><span data-stu-id="4863d-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="4863d-126">Konfigurere og installere Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="4863d-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
