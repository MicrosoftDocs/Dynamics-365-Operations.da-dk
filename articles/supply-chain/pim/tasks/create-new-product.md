---
title: Oprette et nyt produkt
description: Dette emne beskriver, hvordan et nyt delt produkt oprettes.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d313d76d40476bec5c8bc9c8ea5fc93b217e7e87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007560"
---
# <a name="create-a-new-product"></a><span data-ttu-id="285a3-103">Oprette et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="285a3-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="285a3-104">Dette emne beskriver, hvordan et nyt delt produkt oprettes.</span><span class="sxs-lookup"><span data-stu-id="285a3-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="285a3-105">Den udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="285a3-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="285a3-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="285a3-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="285a3-107">Oprette et produkt</span><span class="sxs-lookup"><span data-stu-id="285a3-107">Create a product</span></span>
1. <span data-ttu-id="285a3-108">I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Produkter**.</span><span class="sxs-lookup"><span data-stu-id="285a3-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="285a3-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="285a3-109">Select **New**.</span></span>
3. <span data-ttu-id="285a3-110">Skriv en værdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="285a3-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="285a3-111">Hvis der ikke er konfigureret en nummerserie for produktnummeret, skal det angives manuelt.</span><span class="sxs-lookup"><span data-stu-id="285a3-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="285a3-112">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="285a3-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="285a3-113">Produktnavnet angives som standard til søgenavnet.</span><span class="sxs-lookup"><span data-stu-id="285a3-113">The product name defaults to the search name.</span></span> <span data-ttu-id="285a3-114">Du kan ændre dette efter behov.</span><span class="sxs-lookup"><span data-stu-id="285a3-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="285a3-115">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="285a3-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="285a3-116">Konfigurere dimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="285a3-116">Set up dimension groups</span></span>
1. <span data-ttu-id="285a3-117">Vælg **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="285a3-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="285a3-118">Indtast eller vælg en værdi i feltet **Lagringsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="285a3-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="285a3-119">Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner du skal angive for hver transaktion for produktet, og hvordan den spores på lageret.</span><span class="sxs-lookup"><span data-stu-id="285a3-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="285a3-120">Indtast eller vælg en værdi i feltet **Sporingsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="285a3-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="285a3-121">Lagringsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du skal angive for hver transaktion for produktet, og hvordan den håndteres på lageret.</span><span class="sxs-lookup"><span data-stu-id="285a3-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="285a3-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="285a3-122">Select **OK**.</span></span>

