---
title: Oprette en profil for detailfunktionalitet
description: Dette emne beskriver, hvordan du opretter en profil for detailfunktionalitet i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002837"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="0cf28-103">Oprette en profil for detailfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="0cf28-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0cf28-104">Dette emne beskriver, hvordan du opretter en profil for detailfunktionalitet i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0cf28-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0cf28-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="0cf28-105">Overview</span></span>

<span data-ttu-id="0cf28-106">Profilen for detailfunktionalitet giver forskellige indstillinger, der bruges til onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="0cf28-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="0cf28-107">Hver detailkanal skal angive en profil for detailfunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="0cf28-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="0cf28-108">Oprette en profil for detailfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="0cf28-108">Create a retail functionality profile</span></span>

<span data-ttu-id="0cf28-109">Benyt følgende fremgangsmåde for at oprette en ny profil for detailfunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="0cf28-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="0cf28-110">I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> POS-profiler \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="0cf28-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="0cf28-111">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0cf28-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="0cf28-112">Angiv et id for profilen ("FN006" i eksempelbilledet nedenfor) i feltet **Profil**.</span><span class="sxs-lookup"><span data-stu-id="0cf28-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="0cf28-113">Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0cf28-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="0cf28-114">Vælg et land til **ISO**-landestandarden i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="0cf28-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="0cf28-115">Rediger andre indstillinger i sektionen **Generelt** efter behov.</span><span class="sxs-lookup"><span data-stu-id="0cf28-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="0cf28-116">I sektionen **Generelt** skal du vælge et **Kvitteringsprofil-id** for mailkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="0cf28-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="0cf28-117">Rediger indstillinger i sektionen **Funktioner** efter behov.</span><span class="sxs-lookup"><span data-stu-id="0cf28-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0cf28-118">Rediger indstillinger i sektionen **Beløb** efter behov.</span><span class="sxs-lookup"><span data-stu-id="0cf28-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="0cf28-119">Rediger indstillinger i sektionen **Infokoder** efter behov.</span><span class="sxs-lookup"><span data-stu-id="0cf28-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0cf28-120">Rediger indstillinger i sektionen **Kvitteringsnummerering** efter behov.</span><span class="sxs-lookup"><span data-stu-id="0cf28-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="0cf28-121">Følgende billede viser et eksempel på en profil for detailfunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="0cf28-121">The following image shows an example retail functionality profile.</span></span>
  
![Eksempel på profil for detailfunktionalitet](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="0cf28-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0cf28-123">Additional resources</span></span>

[<span data-ttu-id="0cf28-124">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="0cf28-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="0cf28-125">Oprette nyt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="0cf28-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="0cf28-126">Oversigt over skærmlayout</span><span class="sxs-lookup"><span data-stu-id="0cf28-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="0cf28-127">Konfigurere og installere Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="0cf28-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
