---
title: Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering
description: Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9573fd220cd8b6a58f81e4d17ca65234f41beb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985335"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="7e587-103">Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering</span><span class="sxs-lookup"><span data-stu-id="7e587-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e587-104">Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.</span><span class="sxs-lookup"><span data-stu-id="7e587-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="7e587-105">Oprette en forældet tilstand</span><span class="sxs-lookup"><span data-stu-id="7e587-105">Create an obsolete state</span></span>
1. <span data-ttu-id="7e587-106">Gå til Administration af produktoplysninger > Konfiguration > Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="7e587-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="7e587-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7e587-107">Click New.</span></span>
3. <span data-ttu-id="7e587-108">Skriv en værdi i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="7e587-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="7e587-109">Vælg Nej i feltet Er aktiv for planlægning.</span><span class="sxs-lookup"><span data-stu-id="7e587-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="7e587-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7e587-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="7e587-111">Knytte den forældede tilstand til en frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="7e587-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="7e587-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7e587-112">Close the page.</span></span>
2. <span data-ttu-id="7e587-113">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="7e587-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="7e587-114">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="7e587-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7e587-115">Du kan for eksempel filtrere på feltet Søgenavn med værdien 'M00'.</span><span class="sxs-lookup"><span data-stu-id="7e587-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="7e587-116">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7e587-116">Click Edit.</span></span>
5. <span data-ttu-id="7e587-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7e587-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="7e587-118">Indtast eller vælg en værdi i feltet Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="7e587-118">In the Product lifecycle state field, enter or select a value.</span></span>

