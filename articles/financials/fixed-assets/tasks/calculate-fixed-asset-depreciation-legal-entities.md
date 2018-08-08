--- 
title: "Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder"
description: "Denne fremgangsmåde viser, hvordan du konfigurerer og kører afskrivningsprocessen for flere juridiske enheder."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="a5dde-103">Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="a5dde-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5dde-104">Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin.</span><span class="sxs-lookup"><span data-stu-id="a5dde-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="a5dde-105">Denne fremgangsmåde viser, hvordan du konfigurerer og kører processen for flere juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="a5dde-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="a5dde-106">Rollen Bogholder bruges.</span><span class="sxs-lookup"><span data-stu-id="a5dde-106">It uses the accountant role.</span></span>  

<span data-ttu-id="a5dde-107">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a5dde-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="a5dde-108">Trin (16) underopgave: Konfigurer kladder for kørsel af afskrivning på tværs af virksomheden.</span><span class="sxs-lookup"><span data-stu-id="a5dde-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="a5dde-109">Du skal først oprette de kladder, der skal bruges til kørsel af afskrivning på tværs af virksomheden, i hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="a5dde-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="a5dde-110">Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre.</span><span class="sxs-lookup"><span data-stu-id="a5dde-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="a5dde-111">Udvid sektionen Forslag til anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="a5dde-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="a5dde-112">Opret en post med kladdenavnet, der skal bruges for hvert posteringslag i den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="a5dde-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="a5dde-113">Hvis bøgerne ikke bogfører til Finans, så skal posteringslaget Ingen vælges i den tilknyttede kladde.</span><span class="sxs-lookup"><span data-stu-id="a5dde-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="a5dde-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="a5dde-114">Click Add.</span></span> 
4. <span data-ttu-id="a5dde-115">I feltet Posteringslag skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="a5dde-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="a5dde-116">Indtast eller vælg en værdi i feltet Kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="a5dde-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="a5dde-117">Gentag kladdeopsætningen på siden med parametre for anlægsaktiver i hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="a5dde-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="a5dde-118">Underopgave: Beregn afskrivning</span><span class="sxs-lookup"><span data-stu-id="a5dde-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="a5dde-119">Brug forslagssiden Opret afskrivning til at starte din afskrivning på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="a5dde-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="a5dde-120">Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="a5dde-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="a5dde-121">I feltet Posteringslag skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="a5dde-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="a5dde-122">Kladdenavnet dannes som standard fra parametrene for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="a5dde-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="a5dde-123">Det kan ændres her for den aktuelle juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="a5dde-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="a5dde-124">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="a5dde-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="a5dde-125">Vælg de juridiske enheder, der skal medtages i afskrivningskørslen.</span><span class="sxs-lookup"><span data-stu-id="a5dde-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="a5dde-126">Kun juridiske enheder med kladder, der er angivet for anlægsaktivforslag på siden med parametre for anlægsaktiver, vises på listen.</span><span class="sxs-lookup"><span data-stu-id="a5dde-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="a5dde-127">Når den er aktiveret, vil indstillingen Bogfør kladder automatisk bogføre afskrivningskladderne, når de oprettes.</span><span class="sxs-lookup"><span data-stu-id="a5dde-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="a5dde-128">Når de ikke er markeret, vil kladderne blive oprettet, men ikke bogført, så du kan gennemgå oplysningerne inden bogføringen.</span><span class="sxs-lookup"><span data-stu-id="a5dde-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="a5dde-129">Vælg Ja i feltet Bogfør kladder.</span><span class="sxs-lookup"><span data-stu-id="a5dde-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="a5dde-130">Filtreringsfelterne omfatter alle anlægsaktiver, grupper og bøger for de juridiske enheder, der er valgt for denne kørsel af afskrivning.</span><span class="sxs-lookup"><span data-stu-id="a5dde-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="a5dde-131">Indstillingen for batchbehandling er aktiveret som standard.</span><span class="sxs-lookup"><span data-stu-id="a5dde-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="a5dde-132">Når denne indstilling er aktiveret, kører oprettelse og bogføring af afskrivningskladden i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="a5dde-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="a5dde-133">Klik på Opret kladde.</span><span class="sxs-lookup"><span data-stu-id="a5dde-133">Click Create journal.</span></span> 
10. <span data-ttu-id="a5dde-134">Du skal få vist de afskrivningskladder, der er oprettet i de respektive juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="a5dde-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="a5dde-135">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="a5dde-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

