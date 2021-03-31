---
title: Oprette et anlægsaktiv
description: Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden med anlægsaktiver.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227034"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="d8a77-103">Oprette et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="d8a77-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8a77-104">Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden **Anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="d8a77-105">Systemet tildeler aktivnummeret på basis af den nummerserie, der er tildelt anlægsaktivgruppen.</span><span class="sxs-lookup"><span data-stu-id="d8a77-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="d8a77-106">Hvis du bruger skabelonen for anlægsaktiver til at importere aktiver via Microsoft Excel-tilføjelsesprogrammet, eller hvis du bruger et andet importjob, opretter systemet automatisk anlægsaktivposter og øger aktivnummeret.</span><span class="sxs-lookup"><span data-stu-id="d8a77-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="d8a77-107">Hvis du vil oprette en aktivpost manuelt, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d8a77-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="d8a77-108">Gå til **Navigationsrude \> Moduler \> Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="d8a77-109">Gå til **handlingsruden**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="d8a77-110">Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="d8a77-111">Feltet **Nummer** bruges som standard, hvis du har aktiveret funktionen **Auto-nummerer anlægsaktiver** i **Anlægsaktivparametre** og **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="d8a77-112">Hvis ikke skal du angive et entydigt nummer, der identificerer anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="d8a77-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="d8a77-113">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="d8a77-114">Angiv yderligere oplysninger, som din virksomhed skal bruge til dette anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="d8a77-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="d8a77-115">Vælg **Bøger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="d8a77-116">Angiv en dato i feltet **Anskaffelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="d8a77-117">Angiv et tal i feltet **Anskaffelsespris**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="d8a77-118">Angiv yderligere oplysninger, som din virksomhed skal bruge til denne bog.</span><span class="sxs-lookup"><span data-stu-id="d8a77-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="d8a77-119">Angiv yderligere oplysninger, som din virksomhed skal bruge til resterende bøger.</span><span class="sxs-lookup"><span data-stu-id="d8a77-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="d8a77-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d8a77-120">Close the page.</span></span>

<span data-ttu-id="d8a77-121">Du kan også importere anlægsaktiver ved hjælp af Excel-tilføjelsesprogrammet eller ved at køre et importjob fra arbejdsområdet **Dataadministration**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="d8a77-122">Før du kører importen, skal du angive værdierne for obligatoriske felter i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="d8a77-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="d8a77-123">Hvis du ikke har defineret anlægsaktivnummeret i skabelonen for Excel-tilføjelsesprogrammet eller i Dataadministration, opretter systemet et anlægsaktivnummer for hvert importerede aktiv og øger automatisk nummerserien for hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="d8a77-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="d8a77-124">Men hvis du importerer aktiver og definerer aktivnumre i skabelonen, øger systemet **ikke** automatisk nummerserien.</span><span class="sxs-lookup"><span data-stu-id="d8a77-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="d8a77-125">I dette tilfælde skal en administrator måske opdatere nummerserien manuelt.</span><span class="sxs-lookup"><span data-stu-id="d8a77-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="d8a77-126">Hvis du har defineret anlægsaktivnummeret i skabelonen til Excel-tilføjelsesprogrammet, bruger systemet det definerede anlægsaktivnummer og øger nummerserien.</span><span class="sxs-lookup"><span data-stu-id="d8a77-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="d8a77-127">Når afskrivningen er bogført, låses felterne **Placeret i tjeneste** og **Afskrivningsdato** på siden **Kartotek**.</span><span class="sxs-lookup"><span data-stu-id="d8a77-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="d8a77-128">Både feltet vil heller ikke blive opdateret fra dataenheden.</span><span class="sxs-lookup"><span data-stu-id="d8a77-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="d8a77-129">Anlægsaktivposten slettes ikke, hvis der er bogført posteringer i det tilknyttede kartotek, eller hvis det netop oprettede anlægsaktiv er angivet på en kladdelinje, men ikke bogført.</span><span class="sxs-lookup"><span data-stu-id="d8a77-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]