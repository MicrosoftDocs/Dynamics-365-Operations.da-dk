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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968923"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="e5c77-103">Oprette straksafskrivning</span><span class="sxs-lookup"><span data-stu-id="e5c77-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5c77-104">Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="e5c77-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="e5c77-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="e5c77-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="e5c77-106">Opret en særlig afskrivning</span><span class="sxs-lookup"><span data-stu-id="e5c77-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="e5c77-107">Gå til Anlægsaktiver > Opsætning > Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="e5c77-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5c77-108">Click New.</span></span>
3. <span data-ttu-id="e5c77-109">Skriv en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="e5c77-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e5c77-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e5c77-111">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="e5c77-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="e5c77-112">Hvis der ikke er angivet en procentdel, skal du angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="e5c77-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="e5c77-113">Knyt en særlig afskrivning til en bog for anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="e5c77-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="e5c77-114">Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="e5c77-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="e5c77-115">Vælg på listen den anlægsaktivgruppe, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="e5c77-116">Klik på Bøger.</span><span class="sxs-lookup"><span data-stu-id="e5c77-116">Click Books.</span></span>
4. <span data-ttu-id="e5c77-117">Vælg på listen den bog, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="e5c77-118">Klik på Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="e5c77-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5c77-119">Click New.</span></span>
7. <span data-ttu-id="e5c77-120">Skriv eller vælg en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="e5c77-121">Procentdel eller Beløb hentes som standard fra konfigurationen af særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="e5c77-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="e5c77-122">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="e5c77-122">In the Priority field, enter a number.</span></span>

