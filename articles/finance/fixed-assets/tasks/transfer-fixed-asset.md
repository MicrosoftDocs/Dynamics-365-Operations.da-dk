---
title: Overføre et anlægsaktiv
description: Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138041"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="efd08-103">Overføre et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="efd08-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efd08-104">Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.</span><span class="sxs-lookup"><span data-stu-id="efd08-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="efd08-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="efd08-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="efd08-106">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="efd08-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="efd08-107">På listen skal du finde og vælge det anlægsaktiv, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="efd08-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="efd08-108">Klik på **Anlægsaktiv** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="efd08-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="efd08-109">Klik på **Overfør anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="efd08-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="efd08-110">Angiv en dato i feltet **Overførselsdato**.</span><span class="sxs-lookup"><span data-stu-id="efd08-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="efd08-111">Angiv kommentarer, der skal beskrive overførslen.</span><span class="sxs-lookup"><span data-stu-id="efd08-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="efd08-112">Denne liste viser alle bøger for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="efd08-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="efd08-113">Marker de bøger, du vil overføre til et nyt økonomisk dimensionssæt.</span><span class="sxs-lookup"><span data-stu-id="efd08-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="efd08-114">Denne liste viser de eksisterende økonomiske dimensionsværdier for den valgte bog.</span><span class="sxs-lookup"><span data-stu-id="efd08-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="efd08-115">Vælg den økonomiske dimension, du vil opdatere for den valgte anlægsaktivbog.</span><span class="sxs-lookup"><span data-stu-id="efd08-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="efd08-116">Klik på rullelisten i feltet **Økonomisk dimension** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="efd08-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="efd08-117">Angiv andre økonomiske dimensionsværdier efter behov.</span><span class="sxs-lookup"><span data-stu-id="efd08-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="efd08-118">Alle økonomiske dimensionsværdier ændres, når der sker en overførsel, uanset om der er angivet en værdi eller ej.</span><span class="sxs-lookup"><span data-stu-id="efd08-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="efd08-119">For eksempel hvis du har angivet en værdi for BusinessUnit og ikke har angivet de økonomiske dimensionsværdier CostCenter og afdeling.</span><span class="sxs-lookup"><span data-stu-id="efd08-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="efd08-120">Hvis din kontostruktur tillader tomme værdier for CostCenter og Afdeling, bør overførslen resultere i, at hver værdimodel har den nye værdi for BusinessUnit og en tom værdi for CostCenter og Afdeling.</span><span class="sxs-lookup"><span data-stu-id="efd08-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="efd08-121">Klik på **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="efd08-121">Click **Update**.</span></span>
    * <span data-ttu-id="efd08-122">Du har mulighed for at se en forhåndsvisning af ændringerne, før overførslen fuldføres.</span><span class="sxs-lookup"><span data-stu-id="efd08-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="efd08-123">Gennemgå resultaterne, før du overfører anlægsaktivbøgerne.</span><span class="sxs-lookup"><span data-stu-id="efd08-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="efd08-124">Klik på **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="efd08-124">Click **Transfer**.</span></span>

