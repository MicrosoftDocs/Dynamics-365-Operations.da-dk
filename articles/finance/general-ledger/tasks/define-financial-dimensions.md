---
title: Definere økonomiske dimensioner
description: Denne opgave vejledning demonstrerer tilføjelse af en enhedsunderstøttet økonomisk dimension og en brugerdefineret økonomisk dimension.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c1520771c6266bdebe2c6fd058eab862460fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994584"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="bc0df-103">Definere økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="bc0df-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc0df-104">Denne opgave vejledning demonstrerer tilføjelse af en enhedsunderstøttet økonomisk dimension og en brugerdefineret økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="bc0df-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="bc0df-105">Guiden bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="bc0df-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="bc0df-106">Oprette en enhedsunderstøttet økonomisk dimension</span><span class="sxs-lookup"><span data-stu-id="bc0df-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="bc0df-107">Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Dimensioner > Økonomiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="bc0df-108">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-108">Click **New**.</span></span>
3. <span data-ttu-id="bc0df-109">Vælg en systemdefineret enhed, som den økonomiske dimension skal baseres på, i feltet **Brug værdier fra**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="bc0df-110">Skriv en værdi i feltet **Dimensionsnavn** for at beskrive den økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="bc0df-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="bc0df-111">Navnet kan være anderledes end det systemdefinerede objekt, men det må ikke indeholde mellemrum eller specialtegn.</span><span class="sxs-lookup"><span data-stu-id="bc0df-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="bc0df-112">Klik på **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-112">Click **Activate**.</span></span> <span data-ttu-id="bc0df-113">Aktivering af den økonomiske dimension opdaterer tabellen med navnet på den økonomiske dimension og fjerner slettede dimensioner.</span><span class="sxs-lookup"><span data-stu-id="bc0df-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="bc0df-114">Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension, men en økonomisk dimension kan ikke bruges, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="bc0df-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="bc0df-115">Klik på **Luk** i aktiveringsmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="bc0df-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="bc0df-116">Klik på **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-116">Click **Activate**.</span></span> <span data-ttu-id="bc0df-117">Dimensionsaktivering kan planlægges til at køre i batch på en bestemt dato og et bestemt klokkelslæt.</span><span class="sxs-lookup"><span data-stu-id="bc0df-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="bc0df-118">Klik på **Dimensionsværdier** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="bc0df-119">Nogle dimensionsværdier er firmaspecifikke.</span><span class="sxs-lookup"><span data-stu-id="bc0df-119">Some dimension values are company specific.</span></span> <span data-ttu-id="bc0df-120">Du kan kontrollere, om de er firmaspecifikke, hvis firmanavnet vises på listen med dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="bc0df-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="bc0df-121">Oprette en brugerdefineret økonomisk dimension</span><span class="sxs-lookup"><span data-stu-id="bc0df-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="bc0df-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bc0df-122">Close the page.</span></span>
2. <span data-ttu-id="bc0df-123">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-123">Click **New**.</span></span>
3. <span data-ttu-id="bc0df-124">Vælg **Brugerdefineret dimension** i feltet **Brug værdier fra**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="bc0df-125">Skriv en værdi i feltet **Dimensionsnavn** for at beskrive den økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="bc0df-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="bc0df-126">Navnet må ikke indeholde mellemrum eller specialtegn.</span><span class="sxs-lookup"><span data-stu-id="bc0df-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="bc0df-127">Du kan også angive en kontomaske for at begrænse mængden og typen af oplysninger, som du kan du angive for dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="bc0df-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="bc0df-128">Du kan skrive tegn, der forbliver ens for hver dimensionsværdi, f.eks. bogstaver eller en bindestreg.</span><span class="sxs-lookup"><span data-stu-id="bc0df-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="bc0df-129">Du kan også angive nummertegn (#) og &-tegn (&) som pladsholdere for bogstaver og tal, som ændres, hver gang der oprettes en dimensionsværdi.</span><span class="sxs-lookup"><span data-stu-id="bc0df-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="bc0df-130">Brug et nummertegn (#) som pladsholder for et tal, og tegnet (&) som pladsholder for et bogstav.</span><span class="sxs-lookup"><span data-stu-id="bc0df-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="bc0df-131">Eksempel: Hvis du vil begrænse dimensionsværdien til bogstaverne CC og tre tal, skal du angive CC-### som formatmaske.</span><span class="sxs-lookup"><span data-stu-id="bc0df-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="bc0df-132">Klik på **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-132">Click **Activate**.</span></span> <span data-ttu-id="bc0df-133">Aktivering af den økonomiske dimension opdaterer tabellen med navnet på den økonomiske dimension og fjerner slettede dimensioner.</span><span class="sxs-lookup"><span data-stu-id="bc0df-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="bc0df-134">Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension, men en økonomisk dimension kan ikke bruges, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="bc0df-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="bc0df-135">Klik på **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-135">Click **Activate**.</span></span> <span data-ttu-id="bc0df-136">Dimensionsaktivering kan planlægges til at køre i batch på en bestemt dato og et bestemt klokkelslæt.</span><span class="sxs-lookup"><span data-stu-id="bc0df-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="bc0df-137">Klik på **Dimensionsværdier** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="bc0df-138">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bc0df-138">Click **New**.</span></span>
9. <span data-ttu-id="bc0df-139">Skriv en værdi i feltet **Dimensionsværdi** for at beskrive din økonomiske dimensionsværdi.</span><span class="sxs-lookup"><span data-stu-id="bc0df-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="bc0df-140">Skriv en beskrivelse i feltet **Beskrivelse**, som beskriver din økonomiske dimensionsværdi.</span><span class="sxs-lookup"><span data-stu-id="bc0df-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

