---
title: Oprette en detailfunktionalitetsprofil
description: I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791991"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="7df85-103">Oprette en detailfunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="7df85-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7df85-104">I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7df85-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7df85-105">Commerce-funktionalitetsprofilen giver forskellige indstillinger, der bruges til onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="7df85-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="7df85-106">Hver kanal skal angive en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="7df85-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="7df85-107">Opret en funktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="7df85-107">Create a functionality profile</span></span>

<span data-ttu-id="7df85-108">Benyt følgende fremgangsmåde for at oprette en ny funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="7df85-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="7df85-109">I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> POS-profiler \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="7df85-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="7df85-110">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7df85-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7df85-111">Angiv et id for profilen ("FN006" i eksempelbilledet nedenfor) i feltet **Profil**.</span><span class="sxs-lookup"><span data-stu-id="7df85-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="7df85-112">Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7df85-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="7df85-113">Vælg et land til **ISO**-landestandarden i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="7df85-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="7df85-114">Rediger andre indstillinger i sektionen **Generelt** efter behov.</span><span class="sxs-lookup"><span data-stu-id="7df85-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="7df85-115">I sektionen **Generelt** skal du vælge et **Kvitteringsprofil-id** for mailkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="7df85-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="7df85-116">Rediger indstillinger i sektionen **Funktioner** efter behov.</span><span class="sxs-lookup"><span data-stu-id="7df85-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="7df85-117">Rediger indstillinger i sektionen **Beløb** efter behov.</span><span class="sxs-lookup"><span data-stu-id="7df85-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="7df85-118">Rediger indstillinger i sektionen **Infokoder** efter behov.</span><span class="sxs-lookup"><span data-stu-id="7df85-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="7df85-119">Rediger indstillinger i sektionen **Kvitteringsnummerering** efter behov.</span><span class="sxs-lookup"><span data-stu-id="7df85-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="7df85-120">Følgende billede viser et eksempel på en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="7df85-120">The following image shows an example functionality profile.</span></span>
  
![Eksempel på funktionalitetsprofil](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="7df85-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7df85-122">Additional resources</span></span>

[<span data-ttu-id="7df85-123">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="7df85-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="7df85-124">Oprette nyt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="7df85-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="7df85-125">Oversigt over skærmlayout</span><span class="sxs-lookup"><span data-stu-id="7df85-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="7df85-126">Konfigurere og installere Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="7df85-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
