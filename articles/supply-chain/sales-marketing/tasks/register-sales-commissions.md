---
title: Registrere salgskommissioner
description: I dette emne beskrives, hvordan salgsprovisioner beregnes og registreres.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57e3b95cb1f4a13b49ddcd336efaeabb12e5defc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979520"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="28dc1-103">Registrere salgskommissioner</span><span class="sxs-lookup"><span data-stu-id="28dc1-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28dc1-104">I dette emne beskrives, hvordan salgsprovisioner beregnes og registreres.</span><span class="sxs-lookup"><span data-stu-id="28dc1-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="28dc1-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="28dc1-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="28dc1-106">Før du starter denne vejledning, skal du køre vejledningen "Konfigurer regler for salgsprovision" for at sikre, at du har den nødvendige provisionsberegningsopsætning.</span><span class="sxs-lookup"><span data-stu-id="28dc1-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="28dc1-107">Notér de kunde- og varenumre, du har valgt til provisionsprocessen, og brug dem, når du bliver bedt om at oprette en salgsordre i denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="28dc1-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="28dc1-108">Fakturere en salgsordre, der kvalificerer en sælger til en provision</span><span class="sxs-lookup"><span data-stu-id="28dc1-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="28dc1-109">Gå til **Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="28dc1-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-110">Select **New**.</span></span>
3. <span data-ttu-id="28dc1-111">Vælg den ønskede post på rullemenuen i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="28dc1-112">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-112">Select **OK**.</span></span>
5. <span data-ttu-id="28dc1-113">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="28dc1-114">Vælg **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-114">Select **Change view**.</span></span>
7. <span data-ttu-id="28dc1-115">Vælg **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-115">Select **Header view**.</span></span>
8. <span data-ttu-id="28dc1-116">Udvid sektionen **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="28dc1-117">Værdien i feltet **Salgsgruppe** repræsenterer en gruppe med en eller flere tilknyttede sælgere.</span><span class="sxs-lookup"><span data-stu-id="28dc1-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="28dc1-118">Personerne i gruppen er dem, der modtager provision, når ordren faktureres i henhold til foruddefinerede satser og fordeling.</span><span class="sxs-lookup"><span data-stu-id="28dc1-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="28dc1-119">Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="28dc1-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="28dc1-120">Gruppen Salg kopieres også til salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="28dc1-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="28dc1-121">Du kan ændre den, så den er anderledes end den i hovedet og/eller mellem linjerne.</span><span class="sxs-lookup"><span data-stu-id="28dc1-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="28dc1-122">Værdien i feltet **Provisionsgruppe** repræsenterer en gruppe, du har oprettet for en eller flere kunder med det formål at spore provisioner.</span><span class="sxs-lookup"><span data-stu-id="28dc1-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="28dc1-123">Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="28dc1-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="28dc1-124">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="28dc1-125">Vælg **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-125">Select **Change view**.</span></span>
11. <span data-ttu-id="28dc1-126">Vælg **Linjevisning**</span><span class="sxs-lookup"><span data-stu-id="28dc1-126">Select **Line view**.</span></span>
12. <span data-ttu-id="28dc1-127">Vælg den vare, du har konfigureret til provisioner, i rullemenuen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="28dc1-128">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="28dc1-129">Bemærk linjens nettobeløb.</span><span class="sxs-lookup"><span data-stu-id="28dc1-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="28dc1-130">Det repræsenterer salgsindtægter, som i dette eksempel danner grundlag for provisionsberegningen.</span><span class="sxs-lookup"><span data-stu-id="28dc1-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="28dc1-131">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-131">Select **Save**.</span></span>
15. <span data-ttu-id="28dc1-132">Vælg **Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="28dc1-133">Vælg **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="28dc1-134">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="28dc1-135">Vælg **Alle**" i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="28dc1-136">Vælg **Ja** i feltet **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="28dc1-137">Vælg **OK**, og vælg derefter **OK** i den næste rude.</span><span class="sxs-lookup"><span data-stu-id="28dc1-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="28dc1-138">Det kan tage omkring et minut at bogføre transaktionen.</span><span class="sxs-lookup"><span data-stu-id="28dc1-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="28dc1-139">Vent på, at behandlingen fuldføres, og luk ikke siden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="28dc1-140">Gennemse de registrerede salgsprovisioner</span><span class="sxs-lookup"><span data-stu-id="28dc1-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="28dc1-141">I handlingsruden skal du vælge **Faktura** og derefter vælge **Faktura** igen.</span><span class="sxs-lookup"><span data-stu-id="28dc1-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="28dc1-142">I handlingsruden skal du vælge **Faktura** og derefter vælge **Provisionsposter**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="28dc1-143">Fanen **Oversigt** viser linjer, der repræsenterer provisionsbeløb, der skal betales til sælgere, der er knyttet til fakturerede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="28dc1-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="28dc1-144">Lad os se nærmere på det.</span><span class="sxs-lookup"><span data-stu-id="28dc1-144">Let's review the details.</span></span>  
    - <span data-ttu-id="28dc1-145">Hvis du har brugt guiden "Konfigurer regler for salgsprovision" til at konfigurere gruppen **Provisionssalg**, er der to sælgere, som skal modtage en salgsprovision, og provisionen deles ligeligt mellem dem.</span><span class="sxs-lookup"><span data-stu-id="28dc1-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="28dc1-146">I dette eksempel beregnes det samlede provisionsbeløb som en procentdel af salgsindtægterne (nettobeløbet på ordrelinjen).</span><span class="sxs-lookup"><span data-stu-id="28dc1-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="28dc1-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="28dc1-147">Close the page.</span></span>
4. <span data-ttu-id="28dc1-148">Vælg **Bilag**.</span><span class="sxs-lookup"><span data-stu-id="28dc1-148">Select **Voucher**.</span></span> <span data-ttu-id="28dc1-149">Du kan gennemgå bilagsposteringer for provisionsbeløb, der er bogført til de foruddefinerede provisionsudgifts- og -kreditorkonti.</span><span class="sxs-lookup"><span data-stu-id="28dc1-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

