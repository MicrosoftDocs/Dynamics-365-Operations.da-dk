---
title: Oprette et anlægsaktiv
description: Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden med anlægsaktiver.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000237"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="5aa98-103">Oprette et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="5aa98-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5aa98-104">Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden **Anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="5aa98-105">Systemet tildeler aktivnummeret på basis af den nummerserie, der er tildelt anlægsaktivgruppen.</span><span class="sxs-lookup"><span data-stu-id="5aa98-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="5aa98-106">Hvis du bruger skabelonen for anlægsaktiver til at importere aktiver via Microsoft Excel-tilføjelsesprogrammet, eller hvis du bruger et andet importjob, opretter systemet automatisk anlægsaktivposter og øger aktivnummeret.</span><span class="sxs-lookup"><span data-stu-id="5aa98-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="5aa98-107">Hvis du vil oprette en aktivpost manuelt, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5aa98-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="5aa98-108">Gå til **Navigationsrude \> Moduler \> Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="5aa98-109">Gå til **handlingsruden** , og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="5aa98-110">Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="5aa98-111">Feltet **Nummer** bruges som standard, hvis du har aktiveret funktionen **Auto-nummerer anlægsaktiver** i **Anlægsaktivparametre** og **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="5aa98-112">Hvis ikke skal du angive et entydigt nummer, der identificerer anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="5aa98-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="5aa98-113">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="5aa98-114">Angiv yderligere oplysninger, som din virksomhed skal bruge til dette anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="5aa98-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="5aa98-115">Vælg **Bøger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="5aa98-116">Angiv en dato i feltet **Anskaffelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="5aa98-117">Angiv et tal i feltet **Anskaffelsespris**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="5aa98-118">Angiv yderligere oplysninger, som din virksomhed skal bruge til denne bog.</span><span class="sxs-lookup"><span data-stu-id="5aa98-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="5aa98-119">Angiv yderligere oplysninger, som din virksomhed skal bruge til resterende bøger.</span><span class="sxs-lookup"><span data-stu-id="5aa98-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="5aa98-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5aa98-120">Close the page.</span></span>

<span data-ttu-id="5aa98-121">Du kan også importere anlægsaktiver ved hjælp af Excel-tilføjelsesprogrammet eller ved at køre et importjob fra arbejdsområdet **Dataadministration**.</span><span class="sxs-lookup"><span data-stu-id="5aa98-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="5aa98-122">Før du kører importen, skal du angive værdierne for obligatoriske felter i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="5aa98-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="5aa98-123">Hvis du ikke har defineret anlægsaktivnummeret i skabelonen for Excel-tilføjelsesprogrammet eller i Dataadministration, opretter systemet et anlægsaktivnummer for hvert importerede aktiv og øger automatisk nummerserien for hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="5aa98-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="5aa98-124">Men hvis du importerer aktiver og definerer aktivnumre i skabelonen, øger systemet **ikke** automatisk nummerserien.</span><span class="sxs-lookup"><span data-stu-id="5aa98-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="5aa98-125">I dette tilfælde skal en administrator måske opdatere nummerserien manuelt.</span><span class="sxs-lookup"><span data-stu-id="5aa98-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="5aa98-126">Hvis du har defineret anlægsaktivnummeret i skabelonen til Excel-tilføjelsesprogrammet, bruger systemet det definerede anlægsaktivnummer og øger nummerserien.</span><span class="sxs-lookup"><span data-stu-id="5aa98-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>
