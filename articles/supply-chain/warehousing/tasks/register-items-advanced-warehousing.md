---
title: Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde
description: Denne procedure viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f8c39ade92b80c561c9e96220a59e7f222d77e6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216982"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="bcc2e-103">Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde</span><span class="sxs-lookup"><span data-stu-id="bcc2e-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcc2e-104">Denne procedure viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="bcc2e-105">Dette vil normalt blive udført af en modtagende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="bcc2e-106">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="bcc2e-107">Du skal have en bekræftet indkøbsordre med en åben indkøbsordrelinje, før du starter denne guide.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="bcc2e-108">Varen på linjen skal på lager, og den skal ikke bruge produktvarianter og ikke have sporingsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="bcc2e-109">Og varen skal tilknyttes en lagerstyringsprocesaktiveret lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="bcc2e-110">Det lagersted, der bruges, skal være aktiveret for lagerstyringsprocesser og den lokalitet, du bruger til modtagelse, skal være id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="bcc2e-111">Hvis du bruger USMF, kan du bruge regnskab 1001, lagersted 51 og vare M9200 til at oprette din IO.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="bcc2e-112">Noter nummeret på den indkøbsordre, du opretter, og bemærk også varenummeret og det sted, du har brugt til din indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="bcc2e-113">Oprette en varemodtagelseskladde</span><span class="sxs-lookup"><span data-stu-id="bcc2e-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="bcc2e-114">Gå til Varemodtagelse.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="bcc2e-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-115">Click New.</span></span>
3. <span data-ttu-id="bcc2e-116">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-117">Hvis du bruger USMF, kan du skrive WHS.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="bcc2e-118">Hvis du bruger andre data, skal kladden, hvis navn du vælger, have følgende egenskaber: Undersøg plukplads skal angives til Nej, og Karantænestyring skal angives til Nej.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="bcc2e-119">Skriv en værdi i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="bcc2e-120">Skriv en værdi i feltet Sted.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-121">Vælg det sted, du brugte til din indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="bcc2e-122">Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="bcc2e-123">Hvis du brugte lagersted 51 i USMF, skal du vælge sted 5.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="bcc2e-124">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-125">Vælg et lagersted, der er gyldigt for det sted, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="bcc2e-126">Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="bcc2e-127">Hvis du bruger eksempelværdierne i USMF, skal du vælge 51.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="bcc2e-128">Skriv en værdi i feltet Lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-129">Vælg en gyldig lokalitet på det lagersted, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="bcc2e-130">Lokaliteten skal knyttet til en lokalitetsprofil, som er nummerpladekontrolleret.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="bcc2e-131">Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="bcc2e-132">Hvis du bruger eksempelværdierne i USMF, skal du vælge Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="bcc2e-133">Højreklik på rullepilen i feltet Nummerplade, og vælg derefter Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="bcc2e-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-134">Click New.</span></span>
10. <span data-ttu-id="bcc2e-135">Skriv en værdi i feltet Nummerplade.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-136">Noter værdien.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="bcc2e-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-137">Click Save.</span></span>
12. <span data-ttu-id="bcc2e-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-138">Close the page.</span></span>
13. <span data-ttu-id="bcc2e-139">Skriv en værdi i feltet Nummerplade.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-140">Angiv værdien af den nummerplade, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="bcc2e-141">Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="bcc2e-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="bcc2e-143">Tilføj en linje</span><span class="sxs-lookup"><span data-stu-id="bcc2e-143">Add a line</span></span>
1. <span data-ttu-id="bcc2e-144">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-144">Click Add line.</span></span>
2. <span data-ttu-id="bcc2e-145">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="bcc2e-146">Angiv det varenummer, som du brugte på indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="bcc2e-147">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bcc2e-148">Angiv den mængde, du vil registrere.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="bcc2e-149">Feltet Dato angiver den dato, hvor den disponible mængde af denne vare registreres på lageret.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="bcc2e-150">Parti-id udfyldes af systemet, hvis det kan identificeres entydigt fra de givne oplysninger.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="bcc2e-151">Ellers skal du tilføje dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="bcc2e-152">Dette er et obligatorisk felt, der sammenkæder denne registrering med en bestemt kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="bcc2e-153">Fuldføre registreringen</span><span class="sxs-lookup"><span data-stu-id="bcc2e-153">Complete the registration</span></span>
1. <span data-ttu-id="bcc2e-154">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-154">Click Validate.</span></span>
    * <span data-ttu-id="bcc2e-155">Dette kontrollerer, at kladden er klar til at blive bogført.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="bcc2e-156">Hvis valideringen mislykkes, skal du rette fejlene, før du kan bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="bcc2e-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-157">Click OK.</span></span>
    * <span data-ttu-id="bcc2e-158">Når du har klikket på OK, kan du se meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="bcc2e-159">Der bør være en meddelelse om, at kladden er OK.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="bcc2e-160">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-160">Click Post.</span></span>
4. <span data-ttu-id="bcc2e-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-161">Click OK.</span></span>
    * <span data-ttu-id="bcc2e-162">Når du har klikket på OK, skal du tjekke meddelelseslinjen.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="bcc2e-163">Der bør være en meddelelse om, at handlingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="bcc2e-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-164">Close the page.</span></span>

