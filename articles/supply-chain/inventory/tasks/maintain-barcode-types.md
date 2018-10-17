--- 
title: Vedligehold stregkodetyper
description: Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="maintain-barcode-types"></a><span data-ttu-id="a8daa-103">Vedligehold stregkodetyper</span><span class="sxs-lookup"><span data-stu-id="a8daa-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8daa-104">Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten.</span><span class="sxs-lookup"><span data-stu-id="a8daa-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="a8daa-105">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a8daa-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="a8daa-106">Hvis du bruger USMF, kan du bruge eksempelværdier, der vises.</span><span class="sxs-lookup"><span data-stu-id="a8daa-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="a8daa-107">Disse opgaver udføres normalt af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="a8daa-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="a8daa-108">Gå til Stregkoder.</span><span class="sxs-lookup"><span data-stu-id="a8daa-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="a8daa-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a8daa-109">Click New.</span></span>
3. <span data-ttu-id="a8daa-110">Skriv en værdi i feltet Stregkodeopsætning.</span><span class="sxs-lookup"><span data-stu-id="a8daa-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="a8daa-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a8daa-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a8daa-112">Vælg en indstilling i feltet Stregkodetype.</span><span class="sxs-lookup"><span data-stu-id="a8daa-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="a8daa-113">Hvis du bruger USMF, kan du vælge "Kode 39".</span><span class="sxs-lookup"><span data-stu-id="a8daa-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="a8daa-114">Angiv et tal i feltet Størrelse.</span><span class="sxs-lookup"><span data-stu-id="a8daa-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="a8daa-115">Angiv et tal i feltet Maksimumlængde.</span><span class="sxs-lookup"><span data-stu-id="a8daa-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="a8daa-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a8daa-116">Click Save.</span></span>
9. <span data-ttu-id="a8daa-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a8daa-117">Close the page.</span></span>
10. <span data-ttu-id="a8daa-118">Gå til Parametre til lager- og lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="a8daa-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="a8daa-119">Indtast eller vælg en værdi i feltet Stregkodeopsætning.</span><span class="sxs-lookup"><span data-stu-id="a8daa-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="a8daa-120">Vælg den stregkodeopsætning, som du oprettede før, men vær opmærksom på, at stregkodeformatet skal svare til formatet for det entydige id for den posttype, der bruges i processen.</span><span class="sxs-lookup"><span data-stu-id="a8daa-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="a8daa-121">For eksempel bør stregkodeformatet til plukruter være samme format som til plukrutereferencen, der typisk er en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="a8daa-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="a8daa-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a8daa-122">Click Save.</span></span>
13. <span data-ttu-id="a8daa-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a8daa-123">Close the page.</span></span>


