---
title: Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder
description: Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818458"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="82fad-103">Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="82fad-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82fad-104">Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin.</span><span class="sxs-lookup"><span data-stu-id="82fad-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="82fad-105">Denne fremgangsmåde viser, hvordan du konfigurerer og kører processen for flere juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="82fad-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="82fad-106">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="82fad-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="82fad-107">Konfigurer kladder for kørsel af afskrivning på tværs af virksomheden</span><span class="sxs-lookup"><span data-stu-id="82fad-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="82fad-108">Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre.</span><span class="sxs-lookup"><span data-stu-id="82fad-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="82fad-109">Udvid sektionen Forslag til anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="82fad-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="82fad-110">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="82fad-110">Click Add.</span></span>
4. <span data-ttu-id="82fad-111">I feltet Posteringslag skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="82fad-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="82fad-112">Indtast eller vælg en værdi i feltet Kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="82fad-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="82fad-113">Gentag kladdeopsætningen på siden med parametre for anlægsaktiver i hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="82fad-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="82fad-114">Afskrivning</span><span class="sxs-lookup"><span data-stu-id="82fad-114">Depreciation run</span></span>
1. <span data-ttu-id="82fad-115">Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="82fad-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="82fad-116">I feltet Posteringslag skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="82fad-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="82fad-117">Kladdenavnet dannes som standard fra parametrene for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="82fad-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="82fad-118">Det kan ændres her for den aktuelle juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="82fad-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="82fad-119">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="82fad-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="82fad-120">Vælg de juridiske enheder, der skal medtages i afskrivningskørslen.</span><span class="sxs-lookup"><span data-stu-id="82fad-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="82fad-121">Kun juridiske enheder med kladder, der er angivet for anlægsaktivforslag på siden med parametre for anlægsaktiver, vises på listen.</span><span class="sxs-lookup"><span data-stu-id="82fad-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="82fad-122">Vælg Ja i feltet Bogfør kladder.</span><span class="sxs-lookup"><span data-stu-id="82fad-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="82fad-123">Filtreringsfelterne omfatter alle anlægsaktiver, grupper og bøger for de juridiske enheder, der er valgt for denne kørsel af afskrivning.</span><span class="sxs-lookup"><span data-stu-id="82fad-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="82fad-124">Indstillingen for batchbehandling er aktiveret som standard.</span><span class="sxs-lookup"><span data-stu-id="82fad-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="82fad-125">Når denne indstilling er aktiveret, kører oprettelse og bogføring af afskrivningskladden i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="82fad-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="82fad-126">Klik på Opret kladde.</span><span class="sxs-lookup"><span data-stu-id="82fad-126">Click Create journal.</span></span>
6. <span data-ttu-id="82fad-127">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="82fad-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]