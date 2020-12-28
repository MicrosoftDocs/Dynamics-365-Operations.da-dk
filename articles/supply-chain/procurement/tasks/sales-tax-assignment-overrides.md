---
title: Tildeling og tilsidesættelser af moms
description: Denne procedure viser, hvordan du kan tildele momsgrupper til handelskanaler.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424678"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="48746-103">Tildeling og tilsidesættelser af moms</span><span class="sxs-lookup"><span data-stu-id="48746-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48746-104">Denne procedure viser, hvordan du kan tildele momsgrupper til handelskanaler.</span><span class="sxs-lookup"><span data-stu-id="48746-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="48746-105">Den gennemgår også processen til oprettelse af en ny momsændring og tildeling af ændringen til en eksisterende momsændringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="48746-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="48746-106">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="48746-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="48746-107">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="48746-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="48746-108">På listen skal du klikke på linket Kanal-id for "Houston".</span><span class="sxs-lookup"><span data-stu-id="48746-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="48746-109">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="48746-109">Click Edit.</span></span>
    * <span data-ttu-id="48746-110">Feltet "Momsgruppe" indeholder listen over momsgrupper for det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="48746-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="48746-111">Den aktuelt tildelte gruppe er en generisk momsgruppe i "Texas".</span><span class="sxs-lookup"><span data-stu-id="48746-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="48746-112">Der findes også momsgrupper for "Washington" og "Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="48746-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="48746-113">Momsgrupper kan omfatte afgifter til flere kommuner.</span><span class="sxs-lookup"><span data-stu-id="48746-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="48746-114">Feltet "Momsændring" er det sted, hvor momsændringsgrupper kan knyttes til kanalen.</span><span class="sxs-lookup"><span data-stu-id="48746-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="48746-115">Momsændringsgrupper kan bruges til at gruppe momsændringer, der fungerer for flere butikker.</span><span class="sxs-lookup"><span data-stu-id="48746-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="48746-116">I stedet for at tildele momsændringer én ad gangen manuelt kan gruppen oprettes og tildeles direkte til kanalerne for at spare tid.</span><span class="sxs-lookup"><span data-stu-id="48746-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="48746-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48746-117">Click Save.</span></span>
5. <span data-ttu-id="48746-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48746-118">Close the page.</span></span>
6. <span data-ttu-id="48746-119">Gå til Retail og Commerce > Konfiguration af kanal > Moms > Momsændringer.</span><span class="sxs-lookup"><span data-stu-id="48746-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="48746-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="48746-120">Click New.</span></span>
8. <span data-ttu-id="48746-121">Angiv et navn til din nye ændring i feltet Momsændring.</span><span class="sxs-lookup"><span data-stu-id="48746-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="48746-122">Angiv en beskrivelse af ændringen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="48746-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="48746-123">Angiv status til "Aktivér".</span><span class="sxs-lookup"><span data-stu-id="48746-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="48746-124">Vis eller skjul sektionen Tilsidesæt.</span><span class="sxs-lookup"><span data-stu-id="48746-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="48746-125">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="48746-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="48746-126">Varemomsgrupper kan bruges til at tilsidesætte moms for bestemte varer, der tilhører gruppen.</span><span class="sxs-lookup"><span data-stu-id="48746-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="48746-127">For eksempel beskattes fødevarer normalt på en anden måde end varige forbrugsgoder og vil sandsynligvis have sin egen momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="48746-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="48746-128">Momsgrupper er grupper af skatter og afgifter, der gælder for en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="48746-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="48746-129">Hvis en kanal f.eks. sælger både detail og til andre virksomheder, kan der bruges forskellige varemomsgrupper.</span><span class="sxs-lookup"><span data-stu-id="48746-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="48746-130">Alle gældende afgifter ville være tilknyttet momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="48746-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="48746-131">Nu kan du vælge afgifterne "Fra" og "Til" eller "Fra momsgruppe" og "Til momsgruppe" for at oprette din momsændring.</span><span class="sxs-lookup"><span data-stu-id="48746-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="48746-132">Feltet "Fra" angiver den moms eller momsgruppe, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="48746-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="48746-133">Ændring af varemomsgruppen giver andre indstillinger end ændring af en momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="48746-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="48746-134">Momsændringer kan konfigureres til at ændre moms på hele posteringer eller på bestemte linjer i transaktionen.</span><span class="sxs-lookup"><span data-stu-id="48746-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="48746-135">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48746-135">Click Save.</span></span>
14. <span data-ttu-id="48746-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48746-136">Close the page.</span></span>
15. <span data-ttu-id="48746-137">Gå til Retail og Commerce > Konfiguration af kanal > Moms > Momsændringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="48746-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="48746-138">I dette trin tildeler du den nyoprettede momsændring til den momsændringsgruppe, der er tildelt Houston-kanalen.</span><span class="sxs-lookup"><span data-stu-id="48746-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="48746-139">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="48746-139">Click Edit.</span></span>
17. <span data-ttu-id="48746-140">Udvid eller skjul sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48746-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="48746-141">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="48746-141">Click Add.</span></span>
19. <span data-ttu-id="48746-142">Klik på rullelisten i feltet Momsændring for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="48746-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="48746-143">Vælg den tidligere oprettede momsændring på listen.</span><span class="sxs-lookup"><span data-stu-id="48746-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="48746-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="48746-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="48746-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48746-145">Click Save.</span></span>

