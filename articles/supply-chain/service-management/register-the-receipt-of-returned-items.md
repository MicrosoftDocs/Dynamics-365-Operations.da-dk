---
title: Registrere modtagelsen af returnerede varer
description: Du kan registrere modtagelsen af returnerede varer ved hjælp af formularen Modtagelsesoversigt eller formularen Registrering.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571068"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="1a30b-103">Registrere modtagelsen af returnerede varer</span><span class="sxs-lookup"><span data-stu-id="1a30b-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1a30b-104">Der findes to metoder til at registrere modtagelsen af returnerede varer.</span><span class="sxs-lookup"><span data-stu-id="1a30b-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="1a30b-105">Den første metode er en lagertilgangsproces, der bruger formularen **Modtagelsesoversigt**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="1a30b-106">Den anden bruger formularen **Registrering**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="1a30b-107">Registrere modtagelsen af returnerede varer i formen Modtagelsesoversigt</span><span class="sxs-lookup"><span data-stu-id="1a30b-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="1a30b-108">Du kan bruge formularen **Modtagelsesoversigt** til at identificere en returforsendelse ved dens RMA-nummer (Return Material Authorization).</span><span class="sxs-lookup"><span data-stu-id="1a30b-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="1a30b-109">Hvis der er defineret et kladdenavn under fanen **Opsætning**, og der findes kladdelinjer, som svarer til de linjer, der er valgt i formularen **Modtagelsesoversigt** , oprettes der et nyt kladdehoved, når du klikker på **Start modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="1a30b-110">Klik på **Lagerstyring** \> **Periodisk** \> **Modtagelsesoversigt**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="1a30b-111">I feltet **Opsætningsnavn** skal du vælge **Returordre** og derefter klikke på **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="1a30b-112">Du kan bruge <STRONG>Afgrænsning</STRONG>-felterne til at indsnævre søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="1a30b-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="1a30b-113">Du kan skrive eller vælge RMA-nummeret i feltet <STRONG>RMA-nummer</STRONG> for at få et præcist resultat.</span><span class="sxs-lookup"><span data-stu-id="1a30b-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="1a30b-114">Hvis du vil definere og gemme et sæt filtre, der begrænser, hvilke indgående modtagelser der skal vises, skal du klikke på fanen <STRONG>Opsætning</STRONG>. De tilgængelige filtre omfatter typer, lagersteder og modtagelsesområder.</span><span class="sxs-lookup"><span data-stu-id="1a30b-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="1a30b-115">Returordrer kan ikke blandes med andre modtagelsestyper i formularen <STRONG>Modtagelsesoversigt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1a30b-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="1a30b-116">Derfor er referencen altid en salgsordre, men der angives ikke et salgsordre-id angives på kladdehovedet.</span><span class="sxs-lookup"><span data-stu-id="1a30b-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="1a30b-117">Find den linje, der svarer til den vare, der returneres, i gitteret **Tilgange**, og markér derefter afkrydsningsfeltet i kolonnen **Vælg til modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="1a30b-118">Hvis du vil udelukke bestemte linjer fra returmodtagelse, f.eks. varer fra den oprindelige ordre, der ikke var medtaget i returforsendelsen, skal du fjerne markeringen i de tilknyttede **Vælg til modtagelse**-felter i tabellen **Linjer** i den nederste del af formularen.</span><span class="sxs-lookup"><span data-stu-id="1a30b-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="1a30b-119">Klik på knappen **Start modtagelse** for at oprette en modtagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="1a30b-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="1a30b-120">Du kan markere flere returordrer og medtage dem alle i en enkelt modtagelsesproces.</span><span class="sxs-lookup"><span data-stu-id="1a30b-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="1a30b-121">Hver returordrelinje kopieres til en tilsvarende linje i varemodtagelseskladden.</span><span class="sxs-lookup"><span data-stu-id="1a30b-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="1a30b-122">Du kan også oprette en modtagelseskladde manuelt ved hjælp af formularen <STRONG>Varemodtagelse</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1a30b-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="1a30b-123">Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Varemodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="1a30b-124">Vælg den modtagelseskladde, du lige har oprettet, og klik derefter på **Linjer** for at åbne formularen **Kladdelinjer, lokationer**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="1a30b-125">Juster evt. antallet i feltet **Antal** under fanen **Generelt**, og tildel derefter en dispositionskode i feltet **Dispositionskode**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="1a30b-126">Du kan også markere afkrydsningsfeltet **Karantænestyring** for at få de returnerede varer sendt via en inspektionsproces i forbindelse med en karantæneordre.</span><span class="sxs-lookup"><span data-stu-id="1a30b-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="1a30b-127">Hvis du sender de returnerede varer via karantæne, kan du ikke angive en dispositionskode.</span><span class="sxs-lookup"><span data-stu-id="1a30b-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="1a30b-128">Klik på knappen **Valider**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="1a30b-129">Hvis der ikke forekommer fejl under valideringen, skal du klikke på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="1a30b-130">Registrere modtagelsen af returnerede varer i formen Registrering</span><span class="sxs-lookup"><span data-stu-id="1a30b-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="1a30b-131">I stedet for at bruge formularen **Modtagelsesoversigt** kan du bruge formularen **Registrering** til at registrere modtagelsen af returnerede varer.</span><span class="sxs-lookup"><span data-stu-id="1a30b-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="1a30b-132">Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="1a30b-133">Opret en ny returordre, eller åbn returordren på listen.</span><span class="sxs-lookup"><span data-stu-id="1a30b-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="1a30b-134">Vælg returordrelinjen i oversigtspanelet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="1a30b-135">Klik på **Opdater linje**, og klik derefter på **Registrering**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="1a30b-136">Tildel en dispositionskode i feltet **Dispositionskode**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="1a30b-137">Du kan ikke sende varen til inspektion som en karantæneordre ved hjælp af formularen <STRONG>Registrering</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1a30b-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="1a30b-138">I gitteret **Transaktioner** skal du vælge den transaktion, der skal registreres.</span><span class="sxs-lookup"><span data-stu-id="1a30b-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="1a30b-139">I gitteret **Registrer nu** skal du klikke på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="1a30b-140">Gentag de forrige to trin, indtil alle de returnerede varer vises i gitteret **Registrer nu**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="1a30b-141">Klik på **Bogfør alle**.</span><span class="sxs-lookup"><span data-stu-id="1a30b-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a30b-142">Se også</span><span class="sxs-lookup"><span data-stu-id="1a30b-142">See also</span></span>

<span data-ttu-id="1a30b-143">[Modtagelsesoversigt (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="1a30b-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


