---
title: Angive en tilføjelse til et anlægsaktiv
description: Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142748"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="3060e-103">Angive en tilføjelse til et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="3060e-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3060e-104">Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="3060e-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="3060e-105">Formålet med tilføjelser til anlægsaktiv er at spore varetilføjelser, vedligeholdelse eller forbedringer for et aktiv og er kun til orientering.</span><span class="sxs-lookup"><span data-stu-id="3060e-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="3060e-106">Eventuelle ændringer af anlægsaktivværdien eller levetiden skal foretages separat.</span><span class="sxs-lookup"><span data-stu-id="3060e-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="3060e-107">Proceduren bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="3060e-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="3060e-108">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="3060e-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="3060e-109">På listen skal du finde og vælge anlægsaktivet for tilføjelsen.</span><span class="sxs-lookup"><span data-stu-id="3060e-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="3060e-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3060e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3060e-111">Klik på **Anlægsaktiv** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3060e-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="3060e-112">Klik på **Tilføjelser til anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="3060e-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="3060e-113">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3060e-113">Click **New**.</span></span>
7. <span data-ttu-id="3060e-114">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3060e-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="3060e-115">I feltet **Anskaffelsesdato** skal du angive datoen for tilføjelsen af køb eller tjeneste.</span><span class="sxs-lookup"><span data-stu-id="3060e-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="3060e-116">Angiv omkostningen for vare, vedligeholdelse eller anden forbedring for aktivet i feltet **Enhedskostpris**.</span><span class="sxs-lookup"><span data-stu-id="3060e-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="3060e-117">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="3060e-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="3060e-118">De samlede omkostninger har ingen indflydelse på værdien af anlægsaktivet og bruges udelukkende til sporing og orientering.</span><span class="sxs-lookup"><span data-stu-id="3060e-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="3060e-119">Hvis omkostningerne skal kapitaliseres, skal en opskrivningsregulering bogføres separat.</span><span class="sxs-lookup"><span data-stu-id="3060e-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="3060e-120">Klik på fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="3060e-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="3060e-121">Indstil **Øger levetiden** til **Ja**, hvis tilføjelsen øger aktivets levetid.</span><span class="sxs-lookup"><span data-stu-id="3060e-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="3060e-122">Feltet er kun til orientering.</span><span class="sxs-lookup"><span data-stu-id="3060e-122">This field is informational only.</span></span> <span data-ttu-id="3060e-123">Hvis du vil forøge levetiden, skal du ændre levetiden i værdimodellerne og/eller afskrivningsmodellerne for aktivet.</span><span class="sxs-lookup"><span data-stu-id="3060e-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

