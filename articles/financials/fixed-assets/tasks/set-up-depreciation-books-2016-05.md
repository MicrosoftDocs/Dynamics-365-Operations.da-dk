---
title: Oprette afskrivningsmodeller for anlægsaktiver (maj 2016)
description: Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839851"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="23943-103">Oprette afskrivningsmodeller for anlægsaktiver (maj 2016)</span><span class="sxs-lookup"><span data-stu-id="23943-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23943-104">Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="23943-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="23943-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="23943-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="23943-106">Opret en afskrivningsmodel</span><span class="sxs-lookup"><span data-stu-id="23943-106">Create a depreciation book</span></span>
1. <span data-ttu-id="23943-107">Gå til Anlægsaktiver > Opsætning > Afskrivningsmodeller.</span><span class="sxs-lookup"><span data-stu-id="23943-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="23943-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="23943-108">Click New.</span></span>
3. <span data-ttu-id="23943-109">Skriv en værdi i feltet Afskrivningsmodel.</span><span class="sxs-lookup"><span data-stu-id="23943-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="23943-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="23943-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23943-111">Markér eller fjern markeringen af afkrydsningsfeltet Beregn afskrivning.</span><span class="sxs-lookup"><span data-stu-id="23943-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="23943-112">Klik på rullelisten i feltet Afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23943-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="23943-113">Find og vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="23943-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="23943-115">Klik på rullelisten i feltet Alternativ afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23943-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="23943-116">Vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="23943-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23943-118">Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="23943-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="23943-119">Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="23943-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="23943-120">Markér eller fjern markeringen af afkrydsningsfeltet Opret reguleringer af afskrivning med basisreguleringer.</span><span class="sxs-lookup"><span data-stu-id="23943-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="23943-121">Klik på rullelisten i feltet Kalender for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23943-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="23943-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="23943-123">Knyt afskrivningsmodellen til en anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="23943-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="23943-124">Klik på Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="23943-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="23943-125">Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23943-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="23943-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="23943-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23943-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="23943-128">Vælg en indstilling i feltet Afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="23943-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="23943-129">Angiv et tal i feltet Levetid.</span><span class="sxs-lookup"><span data-stu-id="23943-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="23943-130">Bemærk, at værdien i Afskrivningsperioder beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="23943-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

