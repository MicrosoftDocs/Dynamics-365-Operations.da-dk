---
title: Oprette straksafskrivning
description: Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad1b7f584d2b2a63dba5f8519ada9d89d6265e7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815614"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="649ec-103">Oprette straksafskrivning</span><span class="sxs-lookup"><span data-stu-id="649ec-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="649ec-104">Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="649ec-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="649ec-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="649ec-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="649ec-106">Opret en særlig afskrivning</span><span class="sxs-lookup"><span data-stu-id="649ec-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="649ec-107">Gå til Anlægsaktiver > Opsætning > Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="649ec-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="649ec-108">Click New.</span></span>
3. <span data-ttu-id="649ec-109">Skriv en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="649ec-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="649ec-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="649ec-111">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="649ec-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="649ec-112">Hvis der ikke er angivet en procentdel, skal du angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="649ec-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="649ec-113">Knyt en særlig afskrivning til en bog for anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="649ec-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="649ec-114">Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="649ec-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="649ec-115">Vælg på listen den anlægsaktivgruppe, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="649ec-116">Klik på Bøger.</span><span class="sxs-lookup"><span data-stu-id="649ec-116">Click Books.</span></span>
4. <span data-ttu-id="649ec-117">Vælg på listen den bog, der er tilknyttet den særlige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="649ec-118">Klik på Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="649ec-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="649ec-119">Click New.</span></span>
7. <span data-ttu-id="649ec-120">Skriv eller vælg en værdi i feltet Særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="649ec-121">Procentdel eller Beløb hentes som standard fra konfigurationen af særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="649ec-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="649ec-122">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="649ec-122">In the Priority field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]