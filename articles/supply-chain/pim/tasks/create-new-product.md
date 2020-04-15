---
title: Oprette et nyt produkt
description: Dette emne beskriver, hvordan et nyt delt produkt oprettes.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 611fc0cff7fe2d580e971149630e92afd16be228
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147842"
---
# <a name="create-a-new-product"></a><span data-ttu-id="6af27-103">Oprette et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="6af27-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6af27-104">Dette emne beskriver, hvordan et nyt delt produkt oprettes.</span><span class="sxs-lookup"><span data-stu-id="6af27-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="6af27-105">Den udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="6af27-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="6af27-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6af27-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="6af27-107">Oprette et produkt</span><span class="sxs-lookup"><span data-stu-id="6af27-107">Create a product</span></span>
1. <span data-ttu-id="6af27-108">I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Produkter**.</span><span class="sxs-lookup"><span data-stu-id="6af27-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="6af27-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6af27-109">Select **New**.</span></span>
3. <span data-ttu-id="6af27-110">Skriv en værdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="6af27-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="6af27-111">Hvis der ikke er konfigureret en nummerserie for produktnummeret, skal det angives manuelt.</span><span class="sxs-lookup"><span data-stu-id="6af27-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="6af27-112">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="6af27-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="6af27-113">Produktnavnet angives som standard til søgenavnet.</span><span class="sxs-lookup"><span data-stu-id="6af27-113">The product name defaults to the search name.</span></span> <span data-ttu-id="6af27-114">Du kan ændre dette efter behov.</span><span class="sxs-lookup"><span data-stu-id="6af27-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="6af27-115">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6af27-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="6af27-116">Konfigurere dimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="6af27-116">Set up dimension groups</span></span>
1. <span data-ttu-id="6af27-117">Vælg **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6af27-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="6af27-118">Indtast eller vælg en værdi i feltet **Lagringsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6af27-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="6af27-119">Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner du skal angive for hver transaktion for produktet, og hvordan den spores på lageret.</span><span class="sxs-lookup"><span data-stu-id="6af27-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="6af27-120">Indtast eller vælg en værdi i feltet **Sporingsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6af27-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="6af27-121">Lagringsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du skal angive for hver transaktion for produktet, og hvordan den håndteres på lageret.</span><span class="sxs-lookup"><span data-stu-id="6af27-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="6af27-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6af27-122">Select **OK**.</span></span>

