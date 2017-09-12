--- 
title: 'Konfigurere afskrivningsmodeller '
description: "Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d2001da7b3487a07a91abd406f74558916ac9f23
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="dd7f2-103">Konfigurere afskrivningsmodeller </span><span class="sxs-lookup"><span data-stu-id="dd7f2-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd7f2-104">Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="dd7f2-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="dd7f2-106">Opret en afskrivningsmodel</span><span class="sxs-lookup"><span data-stu-id="dd7f2-106">Create a depreciation book</span></span>
1. <span data-ttu-id="dd7f2-107">Gå til Anlægsaktiver > Opsætning > Afskrivningsmodeller.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="dd7f2-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-108">Click New.</span></span>
3. <span data-ttu-id="dd7f2-109">Skriv en værdi i feltet Afskrivningsmodel.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="dd7f2-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dd7f2-111">Markér eller fjern markeringen af afkrydsningsfeltet Beregn afskrivning.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="dd7f2-112">Klik på rullelisten i feltet Afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dd7f2-113">Find og vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="dd7f2-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dd7f2-115">Klik på rullelisten i feltet Alternativ afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dd7f2-116">Vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="dd7f2-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd7f2-118">Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="dd7f2-119">Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="dd7f2-120">Markér eller fjern markeringen af afkrydsningsfeltet Opret reguleringer af afskrivning med basisreguleringer.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="dd7f2-121">Klik på rullelisten i feltet Kalender for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dd7f2-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="dd7f2-123">Knyt afskrivningsmodellen til en anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="dd7f2-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="dd7f2-124">Klik på Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="dd7f2-125">Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dd7f2-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dd7f2-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dd7f2-128">Vælg en indstilling i feltet Afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="dd7f2-129">Angiv et tal i feltet Levetid.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="dd7f2-130">Bemærk, at værdien i Afskrivningsperioder beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="dd7f2-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


