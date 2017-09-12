--- 
title: "Tildeling og tilsidesættelser af moms"
description: Denne procedure viser, hvordan du kan tildele momsgrupper til detailkanaler.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b3f13738044c81d32098072f26f204a4acb2d08d
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="797b7-103">Tildeling og tilsidesættelser af moms</span><span class="sxs-lookup"><span data-stu-id="797b7-103">Sales tax assignment and overrides</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="797b7-104">Denne procedure viser, hvordan du kan tildele momsgrupper til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="797b7-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="797b7-105">Den gennemgår også processen til oprettelse af en ny momsændring og tildeling af ændringen til en eksisterende momsændringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="797b7-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="797b7-106">Denne procedure</span><span class="sxs-lookup"><span data-stu-id="797b7-106">This procedure</span></span>

<span data-ttu-id="797b7-107">bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="797b7-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="797b7-108">Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="797b7-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="797b7-109">På listen skal du klikke på linket Detailkanal-id for "Houston".</span><span class="sxs-lookup"><span data-stu-id="797b7-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="797b7-110">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="797b7-110">Click Edit.</span></span>
    * <span data-ttu-id="797b7-111">Feltet "Momsgruppe" indeholder listen over momsgrupper for det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="797b7-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="797b7-112">Den aktuelt tildelte gruppe er en generisk momsgruppe i "Texas".</span><span class="sxs-lookup"><span data-stu-id="797b7-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="797b7-113">Der findes også momsgrupper for "Washington" og "Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="797b7-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="797b7-114">Momsgrupper kan omfatte afgifter til flere kommuner.</span><span class="sxs-lookup"><span data-stu-id="797b7-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="797b7-115">Feltet "Momsændring" er det sted, hvor momsændringsgrupper kan knyttes til kanalen.</span><span class="sxs-lookup"><span data-stu-id="797b7-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="797b7-116">Momsændringsgrupper kan bruges til at gruppe momsændringer, der fungerer for flere butikker.</span><span class="sxs-lookup"><span data-stu-id="797b7-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="797b7-117">I stedet for at tildele momsændringer én ad gangen manuelt kan gruppen oprettes og tildeles direkte til kanalerne for at spare tid.</span><span class="sxs-lookup"><span data-stu-id="797b7-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="797b7-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="797b7-118">Click Save.</span></span>
5. <span data-ttu-id="797b7-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="797b7-119">Close the page.</span></span>
6. <span data-ttu-id="797b7-120">Gå til Detail og handel > Konfiguration af kanal > Moms > Momsændringer.</span><span class="sxs-lookup"><span data-stu-id="797b7-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="797b7-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="797b7-121">Click New.</span></span>
8. <span data-ttu-id="797b7-122">Angiv et navn til din nye ændring i feltet Momsændring.</span><span class="sxs-lookup"><span data-stu-id="797b7-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="797b7-123">Angiv en beskrivelse af ændringen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="797b7-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="797b7-124">Angiv status til "Aktivér".</span><span class="sxs-lookup"><span data-stu-id="797b7-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="797b7-125">Vis eller skjul sektionen Tilsidesæt.</span><span class="sxs-lookup"><span data-stu-id="797b7-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="797b7-126">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="797b7-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="797b7-127">Varemomsgrupper kan bruges til at tilsidesætte moms for bestemte varer, der tilhører gruppen.</span><span class="sxs-lookup"><span data-stu-id="797b7-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="797b7-128">For eksempel beskattes fødevarer normalt på en anden måde end varige forbrugsgoder og vil sandsynligvis have sin egen momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="797b7-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="797b7-129">Momsgrupper er grupper af skatter og afgifter, der gælder for en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="797b7-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="797b7-130">Hvis en kanal f.eks. sælger både detail og til andre virksomheder, kan der bruges forskellige varemomsgrupper.</span><span class="sxs-lookup"><span data-stu-id="797b7-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="797b7-131">Alle gældende afgifter ville være tilknyttet momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="797b7-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="797b7-132">Nu kan du vælge afgifterne "Fra" og "Til" eller "Fra momsgruppe" og "Til momsgruppe" for at oprette din momsændring.</span><span class="sxs-lookup"><span data-stu-id="797b7-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="797b7-133">Feltet "Fra" angiver den moms eller momsgruppe, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="797b7-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="797b7-134">Ændring af varemomsgruppen giver andre indstillinger end ændring af en momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="797b7-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="797b7-135">Momsændringer kan konfigureres til at ændre moms på hele posteringer eller på bestemte linjer i transaktionen.</span><span class="sxs-lookup"><span data-stu-id="797b7-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="797b7-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="797b7-136">Click Save.</span></span>
14. <span data-ttu-id="797b7-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="797b7-137">Close the page.</span></span>
15. <span data-ttu-id="797b7-138">Gå til Detail og handel > Konfiguration af kanal > Moms > Momsændringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="797b7-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="797b7-139">I dette trin tildeler du den nyoprettede momsændring til den momsændringsgruppe, der er tildelt Houston-kanalen.</span><span class="sxs-lookup"><span data-stu-id="797b7-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="797b7-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="797b7-140">Click Edit.</span></span>
17. <span data-ttu-id="797b7-141">Udvid eller skjul sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="797b7-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="797b7-142">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="797b7-142">Click Add.</span></span>
19. <span data-ttu-id="797b7-143">Klik på rullelisten i feltet Momsændring for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="797b7-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="797b7-144">Vælg den tidligere oprettede momsændring på listen.</span><span class="sxs-lookup"><span data-stu-id="797b7-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="797b7-145">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="797b7-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="797b7-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="797b7-146">Click Save.</span></span>


