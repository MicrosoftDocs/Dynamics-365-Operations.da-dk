---
title: Bestemme styklisteversionen
description: Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efc980e3a3dfff6d163812396613a1493f4428a4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213785"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="27a60-103">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="27a60-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27a60-104">Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning.</span><span class="sxs-lookup"><span data-stu-id="27a60-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="27a60-105">Lokationsdimensionen kendes altid og er anført i efterspørgselsposteringen.</span><span class="sxs-lookup"><span data-stu-id="27a60-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="27a60-106">Følgende proces bruges til fastlæggelse af den styklisteversion, der skal anvendes:</span><span class="sxs-lookup"><span data-stu-id="27a60-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="27a60-107">Hvis en styklisteversion er defineret for varen på efterspørgselslokationen, bruges den lokationsspecifikke stykliste.</span><span class="sxs-lookup"><span data-stu-id="27a60-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="27a60-108">Hvis der ikke er defineret en lokationsspecifik styklisteversion for en vare på efterspørgselslokationen, bruges der en generel stykliste.</span><span class="sxs-lookup"><span data-stu-id="27a60-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="27a60-109">En generel stykliste angiver ikke en lokation og er gyldig for flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="27a60-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="27a60-110">Hvis der findes en generel stykliste, bruges den.</span><span class="sxs-lookup"><span data-stu-id="27a60-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="27a60-111">Hvis der ikke findes en generel stykliste, som kan bruges, standser efterspørgselsudfoldningen her.</span><span class="sxs-lookup"><span data-stu-id="27a60-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="27a60-112">En gyldig styklisteversion skal opfylde de krævede kriterier for dato og antal, uanset om den er lokationsspecifik eller generel.</span><span class="sxs-lookup"><span data-stu-id="27a60-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





