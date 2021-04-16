---
title: Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde
description: Dette emne præsenterer et scenario, der viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830828"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="bf6ad-103">Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde</span><span class="sxs-lookup"><span data-stu-id="bf6ad-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf6ad-104">Dette emne præsenterer et scenario, der viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="bf6ad-105">Dette vil normalt blive udført af en modtagende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="bf6ad-106">Aktivér eksempeldata</span><span class="sxs-lookup"><span data-stu-id="bf6ad-106">Enable sample data</span></span>

<span data-ttu-id="bf6ad-107">Hvis du vil gennemgå dette scenario ved hjælp af de eksempelposter og værdier, der er angivet i dette emne, skal du bruge et system, hvor standarddemodataene er installeret, og du skal vælge den juridiske enhed *USMF*, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="bf6ad-108">Du kan i stedet gennemgå dette scenario ved at erstatte værdier fra dine egne data, hvis du har følgende tilgængelige data:</span><span class="sxs-lookup"><span data-stu-id="bf6ad-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="bf6ad-109">Du skal have en bekræftet indkøbsordre med en åben indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="bf6ad-110">Varen på linjen skal være på lager.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-110">The item on the line must be stocked.</span></span> <span data-ttu-id="bf6ad-111">Den må ikke bruge produktvarianter og må ikke have sporingsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="bf6ad-112">Varen skal være tilknyttet en lagringsdimensionsgruppe, hvor lagerstyringsproces er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="bf6ad-113">Det lagersted, der bruges, skal være aktiveret for lagerstyringsprocesser og den lokalitet, du bruger til modtagelse, skal være id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="bf6ad-114">Oprette en overskrift til varemodtagelseskladde, der bruger lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="bf6ad-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="bf6ad-115">I følgende scenario vises, hvordan du kan oprette en overskrift til varemodtagelseskladden, der bruger lokationsstyring:</span><span class="sxs-lookup"><span data-stu-id="bf6ad-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="bf6ad-116">Kontrollér, at systemet indeholder en bekræftet indkøbsordre, der opfylder de krav, der er beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="bf6ad-117">I dette scenario bruges en indkøbsordre for firmaet *USMF*, leverandørkonto *1001*, lagersted *51*, med en ordrelinje på *10 PL* (10 paller) af varenummer *M9200*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="bf6ad-118">Notér dig købsordrenummeret, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="bf6ad-119">Gå til **Lagerstyring \> Kladdeposteringer \> Varemodtagelse \> Varemodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="bf6ad-120">Vælg **Ny** i handlingsrude.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="bf6ad-121">Dialogboksen **Opret lokationsstyringskladde** åbnes.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="bf6ad-122">Vælg et kladdenavn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="bf6ad-123">Hvis du bruger eksempeldataene *USMF*, skal du vælge *WHS*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="bf6ad-124">Hvis du bruger dine egne data, skal den kladde, du vælger, have **Undersøg plukplads** angivet til *Nej*, og **Karantænestyring** skal være angivet til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="bf6ad-125">Indstil **Reference** til *Indkøbsordre*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="bf6ad-126">Angiv **Kontonummer** til *1001*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="bf6ad-127">Angiv **Nummer** til nummeret på den indkøbsordre, du har identificeret til denne øvelse.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="bf6ad-128">![Varemodtagelseskladde](../media/item-arrival-journal-header.png "Varemodtagelseskladde")</span><span class="sxs-lookup"><span data-stu-id="bf6ad-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="bf6ad-129">Vælg **OK** for at oprette kladdehovedet.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="bf6ad-130">Vælg **Tilføj linje** i sektionen **Kladdelinjer**, og angiv følgende data:</span><span class="sxs-lookup"><span data-stu-id="bf6ad-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="bf6ad-131">**Varenummer** – Angiv til *M9200*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="bf6ad-132">**Lokation**, **Lagersted** og **Antal** angives på basis af lagertransaktionsdataene for de 10 paller (1000 hver).</span><span class="sxs-lookup"><span data-stu-id="bf6ad-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="bf6ad-133">**Lokation** – Angiv til *001*.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="bf6ad-134">Denne specifikke lokation sporer ikke nummerplader.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="bf6ad-135">![Varemodtagelseskladdelinje](../media/item-arrival-journal-line.png "Varemodtagelseskladdelinje")</span><span class="sxs-lookup"><span data-stu-id="bf6ad-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="bf6ad-136">Feltet **Dato** angiver den dato, hvor det disponible antal af denne vare registreres på lageret.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="bf6ad-137">**Parti-id** udfyldes af systemet, hvis det kan identificeres entydigt fra de givne oplysninger.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="bf6ad-138">Ellers skal du angive det manuelt.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="bf6ad-139">Dette er et påkrævet felt, der sammenkæder denne registrering med en bestemt kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="bf6ad-140">Vælg **Valider** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="bf6ad-141">Dette kontrollerer, at kladden er klar til at blive bogført.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="bf6ad-142">Hvis valideringen mislykkes, skal du rette fejlene, før du kan bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="bf6ad-143">Dialogboksen **Kontrollér kladde** åbnes.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="bf6ad-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-144">Select **OK**.</span></span>
1. <span data-ttu-id="bf6ad-145">Gennemgå meddelelseslinjen.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-145">Review the message bar.</span></span> <span data-ttu-id="bf6ad-146">Der bør være en meddelelse om, at handlingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="bf6ad-147">Vælg **Bogfør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="bf6ad-148">Dialogboksen **Bogfør kladde** åbnes.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="bf6ad-149">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-149">Select **OK**.</span></span>
1. <span data-ttu-id="bf6ad-150">Gennemgå meddelelseslinjen.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-150">Review the message bar.</span></span> <span data-ttu-id="bf6ad-151">Der bør være en meddelelse om, at handlingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="bf6ad-152">Vælg **Funktioner > Produktkvittering** i handlingsruden for at opdatere indkøbsordrelinjen og bogføre en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
