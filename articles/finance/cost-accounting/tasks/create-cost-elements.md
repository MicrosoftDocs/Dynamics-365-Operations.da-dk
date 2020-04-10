---
title: Oprette omkostningselementer .
description: Du kan oprette omkostningselementer i omkostningsregnskab på flere måder.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14f3cbde07fab291a3a3bf05441a87e97a54a7b2
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161609"
---
# <a name="create-cost-elements"></a><span data-ttu-id="e0d34-103">Oprette omkostningselementer .</span><span class="sxs-lookup"><span data-stu-id="e0d34-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0d34-104">Du kan oprette omkostningselementer i omkostningsregnskab på flere måder.</span><span class="sxs-lookup"><span data-stu-id="e0d34-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="e0d34-105">Denne procedure viser, hvordan du opretter omkostningselementer ved at importere hovedkonti via en dataconnector.</span><span class="sxs-lookup"><span data-stu-id="e0d34-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="e0d34-106">Demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e0d34-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="e0d34-107">Denne fremgangsmåde er til en funktion for omkostningsregnskab, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="e0d34-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="e0d34-108">Opret nye omkostningselementer</span><span class="sxs-lookup"><span data-stu-id="e0d34-108">Create new cost elements</span></span>
1. <span data-ttu-id="e0d34-109">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="e0d34-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="e0d34-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e0d34-110">Click New.</span></span>
3. <span data-ttu-id="e0d34-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e0d34-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e0d34-112">Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e0d34-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="e0d34-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e0d34-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e0d34-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e0d34-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="e0d34-115">Konfigurer dataconnectoren</span><span class="sxs-lookup"><span data-stu-id="e0d34-115">Configure the data connector</span></span>
1. <span data-ttu-id="e0d34-116">Klik på Konfigurer leverandør af dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="e0d34-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="e0d34-117">Indtast eller vælg en værdi i feltet Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="e0d34-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="e0d34-118">Vælg Delt for at bruge den delte kontoplan.</span><span class="sxs-lookup"><span data-stu-id="e0d34-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="e0d34-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e0d34-119">Click New.</span></span>
4. <span data-ttu-id="e0d34-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e0d34-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e0d34-121">Du kan anvende filtre på konti, der opfylder dine kriterier.</span><span class="sxs-lookup"><span data-stu-id="e0d34-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="e0d34-122">Indtast eller vælg en værdi i feltet Fra hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="e0d34-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="e0d34-123">Indtast eller vælg en værdi i feltet Til hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="e0d34-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="e0d34-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e0d34-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="e0d34-125">Importér hovedkonti</span><span class="sxs-lookup"><span data-stu-id="e0d34-125">Import main accounts</span></span>
1. <span data-ttu-id="e0d34-126">Klik på Importér dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e0d34-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="e0d34-127">Hovedkonti importeres til omkostningsregnskab og bruges som omkostningselementer.</span><span class="sxs-lookup"><span data-stu-id="e0d34-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="e0d34-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e0d34-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="e0d34-129">Se importerede konti som omkostningselementer</span><span class="sxs-lookup"><span data-stu-id="e0d34-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="e0d34-130">Klik på Vis dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e0d34-130">Click View dimension members.</span></span>
    * <span data-ttu-id="e0d34-131">Se de importerede finanskonti som omkostningselementer i din virksomhed, som omkostninger kan flyde til.</span><span class="sxs-lookup"><span data-stu-id="e0d34-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

