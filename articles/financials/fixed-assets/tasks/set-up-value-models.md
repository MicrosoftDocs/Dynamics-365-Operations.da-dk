--- 
title: "Opret værdimodeller"
description: "Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e067173b27488422fd05ad45f37528f00f04a2bd
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-value-models"></a><span data-ttu-id="0e0f3-103">Opret værdimodeller</span><span class="sxs-lookup"><span data-stu-id="0e0f3-103">Set up value models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e0f3-104">Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="0e0f3-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="0e0f3-106">Opret en bog</span><span class="sxs-lookup"><span data-stu-id="0e0f3-106">Create a book</span></span>
1. <span data-ttu-id="0e0f3-107">Gå til Anlægsaktiver > Opsætning > Bøger.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="0e0f3-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-108">Click New.</span></span>
3. <span data-ttu-id="0e0f3-109">Skriv en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="0e0f3-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0e0f3-111">Hvis Beregn afskrivning er markeret, medtages den tilknyttede bog for anlægsaktiver i afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="0e0f3-112">Hvis feltet ikke er markeret, afskrives anlægskartotek ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="0e0f3-113">Vælg Ja i feltet Beregn afskrivning.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="0e0f3-114">Indtast eller vælg en værdi i feltet Afskrivningsprofil.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0f3-115">En alternativ afskrivningsprofil kaldes også en switch-over-metode til afskrivning.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="0e0f3-116">Afskrivningsforslaget skifter til denne profil, når den alternative profil beregner et afskrivningsbeløb, der er lig med eller større end standardafskrivningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="0e0f3-117">Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0e0f3-118">Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="0e0f3-119">Hvis Opret reguleringer af afskrivning med basisreguleringer er valgt, oprettes afskrivningsreguleringer automatisk, når værdien af aktivet opdateres.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="0e0f3-120">Hvis feltet ikke er markeret, påvirker den opdaterede aktivværdi kun afskrivningsberegninger fremadrettet.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="0e0f3-121">Vælg Ja i feltet Opret reguleringer af afskrivning med basisreguleringer.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="0e0f3-122">Transaktioner i bogen til anlægsaktiver bogføres som standard i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="0e0f3-123">Du kan deaktivere bogføring i finansmodulet for bogen ved at angive feltet Bogfør i finans til Nej.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="0e0f3-124">Bøger, der ikke bogføres i Finans, bruges typisk til momsrapporteringen.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="0e0f3-125">Det giver dig yderligere fleksibilitet til at slette historiske posteringer for anlægskartoteket, fordi de ikke er bundet til finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="0e0f3-126">Posteringslaget anvender som laget Nuværende, hvis bogen bogføres i finans, og Ingen, hvis den ikke bogføres i finans.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="0e0f3-127">Opdater posteringslag, hvis du har brug for, at transaktioner for denne bog bogføres til et andet lag.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="0e0f3-128">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0f3-129">Afledte bøger bogfører transaktioner til forskellige bøger på samme tid.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="0e0f3-130">Du kan oprette posteringer med den primære bog, og under bogføring bogføres en nøjagtig kopi af posteringen i den afledte bog.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="0e0f3-131">Der er ingen genberegning med afledte posteringer, så det ikke skal bruges til afskrivningsposteringer.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="0e0f3-132">Knyt bogen til en anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="0e0f3-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="0e0f3-133">Klik på Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0e0f3-134">Skriv eller vælg en værdi i feltet Anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="0e0f3-135">Angiv et tal i feltet Levetid.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0e0f3-136">Bemærk, at Afskrivningsperioder beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="0e0f3-137">Du kan angive afskrivningsprincippet som påkrævet af skattemæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="0e0f3-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


