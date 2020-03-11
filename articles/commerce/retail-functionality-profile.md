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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057342"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="a9dde-103">Oprette en detailfunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="a9dde-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a9dde-104">I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9dde-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a9dde-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="a9dde-105">Overview</span></span>

<span data-ttu-id="a9dde-106">Commerce-funktionalitetsprofilen giver forskellige indstillinger, der bruges til onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="a9dde-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="a9dde-107">Hver kanal skal angive en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="a9dde-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="a9dde-108">Opret en funktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="a9dde-108">Create a functionality profile</span></span>

<span data-ttu-id="a9dde-109">Benyt følgende fremgangsmåde for at oprette en ny funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="a9dde-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="a9dde-110">I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> POS-profiler \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="a9dde-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="a9dde-111">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a9dde-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a9dde-112">Angiv et id for profilen ("FN006" i eksempelbilledet nedenfor) i feltet **Profil**.</span><span class="sxs-lookup"><span data-stu-id="a9dde-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="a9dde-113">Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a9dde-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="a9dde-114">Vælg et land til **ISO**-landestandarden i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="a9dde-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="a9dde-115">Rediger andre indstillinger i sektionen **Generelt** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9dde-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="a9dde-116">I sektionen **Generelt** skal du vælge et **Kvitteringsprofil-id** for mailkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="a9dde-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="a9dde-117">Rediger indstillinger i sektionen **Funktioner** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9dde-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="a9dde-118">Rediger indstillinger i sektionen **Beløb** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9dde-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="a9dde-119">Rediger indstillinger i sektionen **Infokoder** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9dde-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="a9dde-120">Rediger indstillinger i sektionen **Kvitteringsnummerering** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9dde-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="a9dde-121">Følgende billede viser et eksempel på en funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="a9dde-121">The following image shows an example functionality profile.</span></span>
  
![Eksempel på funktionalitetsprofil](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="a9dde-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a9dde-123">Additional resources</span></span>

[<span data-ttu-id="a9dde-124">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="a9dde-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="a9dde-125">Oprette nyt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="a9dde-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="a9dde-126">Oversigt over skærmlayout</span><span class="sxs-lookup"><span data-stu-id="a9dde-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="a9dde-127">Konfigurere og installere Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="a9dde-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
