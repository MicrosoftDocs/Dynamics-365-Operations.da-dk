---
title: Oprette straksafskrivning
description: Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839875"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="67408-103">Oprette straksafskrivning</span><span class="sxs-lookup"><span data-stu-id="67408-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67408-104">Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="67408-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="67408-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="67408-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="67408-106">Opret en særlig afskrivning</span><span class="sxs-lookup"><span data-stu-id="67408-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="67408-107">Gå til Anlægsaktiver > Opsætning > Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="67408-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="67408-108">Click New.</span></span>
3. <span data-ttu-id="67408-109">Skriv en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="67408-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="67408-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="67408-111">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="67408-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="67408-112">Hvis der ikke er angivet en procentdel, skal du angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="67408-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="67408-113">Knyt en særlig afskrivning til en bog for anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="67408-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="67408-114">Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="67408-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="67408-115">Vælg på listen den anlægsaktivgruppe, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="67408-116">Klik på Bøger.</span><span class="sxs-lookup"><span data-stu-id="67408-116">Click Books.</span></span>
4. <span data-ttu-id="67408-117">Vælg på listen den bog, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="67408-118">Klik på Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="67408-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="67408-119">Click New.</span></span>
7. <span data-ttu-id="67408-120">Skriv eller vælg en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="67408-121">Procentdel eller Beløb hentes som standard fra konfigurationen af særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="67408-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="67408-122">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="67408-122">In the Priority field, enter a number.</span></span>

