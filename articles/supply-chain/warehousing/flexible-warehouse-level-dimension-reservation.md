---
title: Reservationspolitik for fleksibel dimension for lagerstedsniveau
description: I dette emne beskrives politikken for lagerreservation, hvor virksomheder, der sælger batchsporede produkter og kører deres logistik som WMS-aktiverede operationer, kan reservere bestemte batches for kundesalgsordrer, selvom det reservationshierarki, der er tilknyttet produkterne, ikke tillader reservation af bestemte batches.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7d855914e59d90dd082c9e9a027604579a2f411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235406"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="ae152-103">Reservationspolitik for fleksibel dimension for lagerstedsniveau</span><span class="sxs-lookup"><span data-stu-id="ae152-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae152-104">Når et lagerreservationshierarki af typen "Batch under\[lokation\]" er knyttet til produkter, kan virksomheder, der sælger batchsporede produkter og kører logistik som handlinger, der er aktiveret for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere bestemte batches af de pågældende produkter til kundesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ae152-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="ae152-105">På samme måde kan specifikke id'er ikke reserveres til produkter i salgsordrer, når disse produkter er knyttet til standardreservationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ae152-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="ae152-106">Dette emne beskriver den politik for lagerreservation, der giver disse virksomheder mulighed for at reservere bestemte batches eller id'er, selv når produkterne er knyttet til et reservationshierarki af typen "batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="ae152-107">Lagerreservationshierarki</span><span class="sxs-lookup"><span data-stu-id="ae152-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="ae152-108">I dette afsnit opsummeres det eksisterende lagerreservationshierarki.</span><span class="sxs-lookup"><span data-stu-id="ae152-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="ae152-109">Lagerreservationshierarkiet bestemmer, at med hensyn til lagringsdimensioner er det behovsordren, der har de obligatoriske dimensioner for websted, lagersted og lagerstatus, hvorimod lagerstedets logik er ansvarlig for at tildele en lokation til de ønskede antal og reserve lokationen.</span><span class="sxs-lookup"><span data-stu-id="ae152-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="ae152-110">I interaktionerne mellem behovsordren og lagerstedsoperationerne forventes det med andre ord, at behovsordren angiver, hvor ordren skal afsendes fra (dvs. hvilket sted og lagersted).</span><span class="sxs-lookup"><span data-stu-id="ae152-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="ae152-111">Lagerstedet er derefter afhængig af logikken for at finde det påkrævede antal på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="ae152-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="ae152-112">For at afspejle den operationelle model for virksomheden er sporingsdimensionerne (batch- og serienumre) dog underlagt større fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="ae152-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="ae152-113">Et lagerreservationshierarki kan tage højde for scenarier, hvor følgende betingelser gælder:</span><span class="sxs-lookup"><span data-stu-id="ae152-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="ae152-114">Virksomheden er afhængig af sin lagerdrift for at administrere plukning af antal, der har batch- eller serienumre, efter at antallene er fundet på lagerpladsen i lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="ae152-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="ae152-115">Denne model kaldes ofte *Batch-under\[lokation\]*.</span><span class="sxs-lookup"><span data-stu-id="ae152-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="ae152-116">Den bruges typisk, når et produkts batch- eller serienummeridentifikation ikke er vigtig for de kunder, der placerer efterspørgslen hos den sælgende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="ae152-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="ae152-117">Hvis batch- eller serienumre er en del af en kundes ordrespecifikation, og de registreres i behovsordren, er den lagerdrift, der finder antal på lagerstedet, begrænset af de specifikt ønskede numre, og de kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="ae152-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="ae152-118">Denne model kaldes ofte *Batch-over\[lokation\]*.</span><span class="sxs-lookup"><span data-stu-id="ae152-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="ae152-119">I disse scenarier er udfordringen, at der kun kan tildeles ét lagerreservationshierarki til hvert frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="ae152-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="ae152-120">For at WMS kan håndtere sporede varer, efter at hierarkitildelingen bestemmer, hvornår batch- eller serienummeret skal reserveres (enten når behovsordren udtages eller under pluk på lagerstedet), kan denne tidsindstilling ikke ændres på ad hoc-basis.</span><span class="sxs-lookup"><span data-stu-id="ae152-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="ae152-121">Fleksibel reservation for batchsporede varer</span><span class="sxs-lookup"><span data-stu-id="ae152-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="ae152-122">Forretningsscenarie</span><span class="sxs-lookup"><span data-stu-id="ae152-122">Business scenario</span></span>

<span data-ttu-id="ae152-123">I dette scenario bruger et firma en lagerstrategi, hvor færdigvarer spores efter batchnumre.</span><span class="sxs-lookup"><span data-stu-id="ae152-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="ae152-124">Dette firma bruger også WMS-arbejdsbyrden.</span><span class="sxs-lookup"><span data-stu-id="ae152-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="ae152-125">Da denne arbejdsbyrde har en veludviklet logik til planlægning og kørsel af lagerstedspluk- og forsendelsesoperationer for batchaktiverede varer, er de fleste af de færdige varer knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="ae152-126">Fordelen ved denne type driftsopsætning er, at beslutninger (der rent faktisk er reservationsbeslutninger) om, hvilke batches der skal plukkes, og hvor de skal placeres på lagerstedet, udskydes, indtil lagerstedsplukoperationerne er startet.</span><span class="sxs-lookup"><span data-stu-id="ae152-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="ae152-127">De foretages ikke, når kundeordren afgives.</span><span class="sxs-lookup"><span data-stu-id="ae152-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="ae152-128">Selvom reservationshierarkiet "Batch-under\[lokation\]" fungerer godt for firmaets forretningsmål, kræver mange af firmaets etablerede kunder samme batch, som de tidligere har købt, når de genbestiller produkter.</span><span class="sxs-lookup"><span data-stu-id="ae152-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="ae152-129">Derfor vil firmaet søge efter fleksibilitet i den måde, som reglerne for batchreservation håndteres på, så der sker følgende, afhængigt af kundernes behov for den samme vare:</span><span class="sxs-lookup"><span data-stu-id="ae152-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="ae152-130">Et batchnummer kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres under lagerdrift og/eller udtages af andre behov.</span><span class="sxs-lookup"><span data-stu-id="ae152-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="ae152-131">Denne funktionsmåde er en hjælp til at sikre, at det batchnummer, der blev bestilt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="ae152-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="ae152-132">Hvis batchnummeret ikke er vigtigt for kunden, kan lagerdriften bestemme et batchnummer under pluk, efter salgsordreregistrering og reservation er udført.</span><span class="sxs-lookup"><span data-stu-id="ae152-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="ae152-133">Tilladelse af reservation af en bestemt batch i salgsordren</span><span class="sxs-lookup"><span data-stu-id="ae152-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="ae152-134">For at give plads til den ønskede fleksibilitet i batchreservationens funktionsmåde for varer, der er knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]", skal lagerstyringen markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Batchnummer** på siden **Lagerreservationshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="ae152-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Angivelse af fleksibelt lagerreservationshierarki](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="ae152-136">Når niveauet **Batchnummer** i hierarkiet vælges, vil alle dimensioner over dette niveau og op gennem niveauet **Lokation** automatisk blive valgt.</span><span class="sxs-lookup"><span data-stu-id="ae152-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="ae152-137">(Som standard er alle dimensioner over niveauet **Lokation** niveauet forudvalgt). Denne funktionsmåde afspejler den logik, hvor alle dimensioner i intervallet mellem batchnummeret og lokationen også reserveres automatisk, når du reserverer et bestemt batchnummer på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-138">Afkrydsningsfeltet **Tillad reservation i behovsordre** gælder kun for reservationshierarkiniveauer, der er ligger under lagerstedets lokationsdimension.</span><span class="sxs-lookup"><span data-stu-id="ae152-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="ae152-139">**Batchnummer** og **id** er de eneste niveauer i hierarkiet, der er åbne for den fleksible reservationspolitik.</span><span class="sxs-lookup"><span data-stu-id="ae152-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="ae152-140">Du kan med andre ord ikke markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Lokation** eller **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="ae152-141">Hvis reservationshierarkiet indeholder serienummerdimensionen (der altid skal være under niveauet **Batchnummer**), og hvis du har aktiveret batchspecifik reservation for batchnummeret, fortsætter systemet med at håndtere serienummerreservation og plukoperationer baseret på de regler, der gælder for reservationspolitikken "Serie-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="ae152-142">Du kan på et hvilket som helst tidspunkt tillade batchspecifik reservation for et eksisterende reservationshierarki af typen "Batch-under\[lokation\]" i din installation.</span><span class="sxs-lookup"><span data-stu-id="ae152-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="ae152-143">Denne ændring påvirker ikke reservationer og åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="ae152-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="ae152-144">Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes lagertransaktioner af afgangstypen **Reserveret bestilt**, **Reserveret fysisk** eller **Bestilt** for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.</span><span class="sxs-lookup"><span data-stu-id="ae152-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-145">Hvis en vares eksisterende reservationshierarki ikke tillader batchspecifikation i ordren, kan du igen tildele det til et reservationshierarki, der tillader batchspecifikation, forudsat at strukturen i hierarkiniveauet er den samme i begge hierarkier.</span><span class="sxs-lookup"><span data-stu-id="ae152-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="ae152-146">Brug funktionen **Skift reservationshierarki til varer** til at udføre omfordelingen.</span><span class="sxs-lookup"><span data-stu-id="ae152-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="ae152-147">Denne ændring kan være relevant, når du vil forhindre fleksibel batchreservation af et undersæt af batchsporede varer, men tillade den for resten af produktsortimentet.</span><span class="sxs-lookup"><span data-stu-id="ae152-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="ae152-148">Hvis du ikke vil reservere et bestemt batchnummer for varen på en ordrelinje, så gælder standardlogikken for lagerdrift, der er gældende for et reservationshierarki af typen "Batch-under\[lokation\]", stadig, uanset om du har markeret afkrydsningsfeltet **Tillad reservation i behovsordre**.</span><span class="sxs-lookup"><span data-stu-id="ae152-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="ae152-149">Reservere et bestemt batchnummer til en kundeordre</span><span class="sxs-lookup"><span data-stu-id="ae152-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="ae152-150">Efter en batchsporet vares lagerreservationshierarki af typen "Batch-under\[lokation\]" er konfigureret til at tillade reservation af bestemte batchnumre i salgsordrer, kan salgsordrebehandlere udtage kundeordrer på samme vare på en af følgende måder afhængigt af kundens anmodning:</span><span class="sxs-lookup"><span data-stu-id="ae152-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="ae152-151">**Angiv ordredetaljer uden at angive et batchnummer** – denne tilgang skal bruges, når produktets batchspecifikation ikke er vigtig for kunden.</span><span class="sxs-lookup"><span data-stu-id="ae152-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="ae152-152">Alle eksisterende processer, der er knyttet til håndtering af en ordre af denne type i systemet, ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="ae152-153">Der kræves ingen yderligere overvejelser fra brugernes side.</span><span class="sxs-lookup"><span data-stu-id="ae152-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="ae152-154">**Angiv ordredetaljer, og reservér et bestemt batchnummer** – denne tilgang skal bruges, når kunden anmoder om en bestemt batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="ae152-155">Kunderne anmoder typisk om en bestemt batch, når de genbestiller et produkt, som de tidligere har købt.</span><span class="sxs-lookup"><span data-stu-id="ae152-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="ae152-156">Denne type batchspecifik reservation er en såkaldt *ordrebekræftet reservation*.</span><span class="sxs-lookup"><span data-stu-id="ae152-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="ae152-157">Følgende regelsæt er gældende, når antal behandles, og et batchnummer bekræftes for en bestemt ordre:</span><span class="sxs-lookup"><span data-stu-id="ae152-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="ae152-158">Hvis der skal kunne foretages reservation af et bestemt batchnummer for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet reservere alle dimensioner til og med lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="ae152-159">Dette område omfatter typisk id-dimensionen.</span><span class="sxs-lookup"><span data-stu-id="ae152-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="ae152-160">Lokationsvejledninger bruges ikke, når der oprettes plukarbejde for en salgslinje, hvor der bruges ordrebekræftet batchreservation.</span><span class="sxs-lookup"><span data-stu-id="ae152-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="ae152-161">Hverken brugeren eller systemet må ændre batchnummeret under lagerstedsbehandling af arbejde for ordrebekræftede batches.</span><span class="sxs-lookup"><span data-stu-id="ae152-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="ae152-162">(Denne behandling omfatter undtagelseshåndtering).</span><span class="sxs-lookup"><span data-stu-id="ae152-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="ae152-163">I følgende eksempel vises slutpunkt-til-slutpunkt-flowet.</span><span class="sxs-lookup"><span data-stu-id="ae152-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="ae152-164">Eksempel på scenario: batchnummertildeling</span><span class="sxs-lookup"><span data-stu-id="ae152-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="ae152-165">I dette eksempel skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ae152-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="ae152-166">Opret et lagerreservationshierarki for at tillade batchspecifik reservation</span><span class="sxs-lookup"><span data-stu-id="ae152-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="ae152-167">Gå til **Lokationsstyring** \> **Opsætning** \> **Lager \> Reservationshierarki**.</span><span class="sxs-lookup"><span data-stu-id="ae152-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="ae152-168">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ae152-168">Select **New**.</span></span>
3. <span data-ttu-id="ae152-169">Angiv et navn i feltet **Navn** (f.eks. **Batchfleks**).</span><span class="sxs-lookup"><span data-stu-id="ae152-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="ae152-170">Indtast en beskrivelse i feltet **Beskrivelse** (f.eks. **Batch under fleksibel**).</span><span class="sxs-lookup"><span data-stu-id="ae152-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="ae152-171">I feltet **Valgt** skal du vælge **Serienummer** og **Ejer** og derefter vælge den venstre pileknap for at flytte dem til feltet **Tilgængelig**.</span><span class="sxs-lookup"><span data-stu-id="ae152-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="ae152-172">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae152-172">Select **OK**.</span></span>
7. <span data-ttu-id="ae152-173">I rækken med dimensionsniveau for **Batchnummer** skal du markere afkrydsningsfeltet **Tillad reservation i behovsordre**.</span><span class="sxs-lookup"><span data-stu-id="ae152-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="ae152-174">Niveauerne **Nummerplade** og **Lokation** vælges automatisk, og du kan ikke fjerne markeringerne i afkrydsningsfelterne for dem.</span><span class="sxs-lookup"><span data-stu-id="ae152-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="ae152-175">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ae152-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="ae152-176">Opret et nyt frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="ae152-176">Create a new released product</span></span>

1. <span data-ttu-id="ae152-177">Angiv produktets tre masterdataparametre ved hjælp af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ae152-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="ae152-178">Vælg **Artikler** i feltet **Lagringsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="ae152-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="ae152-179">Vælg **Batch-fy** i feltet **Sporingsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="ae152-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="ae152-180">I feltet **Reservationshierarki** skal du vælge **Batchfleks**.</span><span class="sxs-lookup"><span data-stu-id="ae152-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="ae152-181">Opret to batchnumre f.eks. **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="ae152-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="ae152-182">Føj vareantal til disponibel lagerbeholdning ved hjælp af følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="ae152-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="ae152-183">Lagersted</span><span class="sxs-lookup"><span data-stu-id="ae152-183">Warehouse</span></span> | <span data-ttu-id="ae152-184">Batchnummer</span><span class="sxs-lookup"><span data-stu-id="ae152-184">Batch number</span></span> | <span data-ttu-id="ae152-185">Adresse</span><span class="sxs-lookup"><span data-stu-id="ae152-185">Location</span></span> | <span data-ttu-id="ae152-186">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="ae152-186">License plate</span></span> | <span data-ttu-id="ae152-187">Mængde</span><span class="sxs-lookup"><span data-stu-id="ae152-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="ae152-188">24</span><span class="sxs-lookup"><span data-stu-id="ae152-188">24</span></span>        | <span data-ttu-id="ae152-189">B11</span><span class="sxs-lookup"><span data-stu-id="ae152-189">B11</span></span>          | <span data-ttu-id="ae152-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="ae152-190">BULK-001</span></span> | <span data-ttu-id="ae152-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae152-191">None</span></span>          | <span data-ttu-id="ae152-192">10</span><span class="sxs-lookup"><span data-stu-id="ae152-192">10</span></span>       |
    | <span data-ttu-id="ae152-193">24</span><span class="sxs-lookup"><span data-stu-id="ae152-193">24</span></span>        | <span data-ttu-id="ae152-194">B11</span><span class="sxs-lookup"><span data-stu-id="ae152-194">B11</span></span>          | <span data-ttu-id="ae152-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="ae152-195">FL-001</span></span>   | <span data-ttu-id="ae152-196">LP11</span><span class="sxs-lookup"><span data-stu-id="ae152-196">LP11</span></span>          | <span data-ttu-id="ae152-197">10</span><span class="sxs-lookup"><span data-stu-id="ae152-197">10</span></span>       |
    | <span data-ttu-id="ae152-198">24</span><span class="sxs-lookup"><span data-stu-id="ae152-198">24</span></span>        | <span data-ttu-id="ae152-199">B22</span><span class="sxs-lookup"><span data-stu-id="ae152-199">B22</span></span>          | <span data-ttu-id="ae152-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="ae152-200">FL-002</span></span>   | <span data-ttu-id="ae152-201">LP22</span><span class="sxs-lookup"><span data-stu-id="ae152-201">LP22</span></span>          | <span data-ttu-id="ae152-202">10</span><span class="sxs-lookup"><span data-stu-id="ae152-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="ae152-203">Indtast oplysninger om salgsordrer</span><span class="sxs-lookup"><span data-stu-id="ae152-203">Enter sales order details</span></span>

1. <span data-ttu-id="ae152-204">Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="ae152-205">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ae152-205">Select **New**.</span></span>
3. <span data-ttu-id="ae152-206">Angiv **US-003** i feltet **Debitorkonto** i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="ae152-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="ae152-207">Tilføj en linje for den nye vare, og angiv **10** som antal.</span><span class="sxs-lookup"><span data-stu-id="ae152-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="ae152-208">Sørg for, at feltet **Lagersted** er angivet til **24**.</span><span class="sxs-lookup"><span data-stu-id="ae152-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="ae152-209">Vælg **Lager** i oversigtspanelet **Salgsordrelinjer**, og vælg derefter **Batchreservation** i gruppen **Vedligehold**.</span><span class="sxs-lookup"><span data-stu-id="ae152-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="ae152-210">På siden **Batchreservation** vises en liste over batches, der er tilgængelige til reservation for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="ae152-211">I dette eksempel vises antallet **20** for batchnummer **B11** og antallet **10** for batchnummer **B22**.</span><span class="sxs-lookup"><span data-stu-id="ae152-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="ae152-212">Bemærk, at der ikke kan opnås adgang til siden **Batchreservation** fra en linje, hvis varen på linjen er tilknyttet reservationshierarkiet "Batch-under\[lokation\]", medmindre den er konfigureret til at tillade batchspecifik reservation.</span><span class="sxs-lookup"><span data-stu-id="ae152-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-213">Hvis du vil reservere et bestemt batch til en salgsordre, skal du bruge siden **Batchreservation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="ae152-214">Hvis du angiver batchnummeret direkte på salgsordrelinjen, fungerer systemet, som om du har angivet en bestemt batchværdi for en vare, der er underlagt reservationspolitikken "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="ae152-215">Når du gemmer linjen, vil du modtage en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="ae152-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="ae152-216">Hvis du bekræfter, at batchnummeret skal angives direkte på ordrelinjen, håndteres linjen ikke af den almindelige lokationsstyringslogik.</span><span class="sxs-lookup"><span data-stu-id="ae152-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="ae152-217">Hvis du reserverer antallet fra siden **Reservation**, reserveres der ikke noget bestemt batch, og udførelsen af lagerdrift for linjen følger de regler, der gælder i henhold til reservationspolitikken "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="ae152-218">Generelt er funktionen og interaktionen med denne side meget lig den måde, der arbejdes og interageres med varer, som har et tilknyttet reservationshierarki af typen "Batch-over\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="ae152-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="ae152-219">Der gælder dog følgende undtagelser:</span><span class="sxs-lookup"><span data-stu-id="ae152-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="ae152-220">Oversigtspanelet **Batchnumre bundet til kildelinje** viser de batchnumre, der er reserveret til ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="ae152-221">Batchværdierne i gitteret vises under hele udførelsescyklussen for ordrelinjen, herunder lagerstedets behandlingsstadier.</span><span class="sxs-lookup"><span data-stu-id="ae152-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="ae152-222">Derimod vises der i oversigtspanelet **Oversigt** en almindelig ordrelinjereservation (dvs. reservation, der udføres for dimensionerne over niveauet **Lokation**) i gitteret op til det punkt, hvor der oprettes lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="ae152-223">Arbejdsenheden overtager derefter linjereservationen, og linjereservationen vises ikke længere på siden.</span><span class="sxs-lookup"><span data-stu-id="ae152-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="ae152-224">Oversigtspanelet **Batchnumre bundet til kildelinje** sikrer, at salgsordrebehandleren kan få vist de batchnumre, der er bundet til kundens ordre på et tidspunkt i løbet livscyklussen op til og med fakturering.</span><span class="sxs-lookup"><span data-stu-id="ae152-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="ae152-225">Ud over at reservere en bestemt batch kan en bruger manuelt vælge batchens specifikke lokation og id i stedet for at lade systemet vælge dem automatisk.</span><span class="sxs-lookup"><span data-stu-id="ae152-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="ae152-226">Denne funktion er relateret til designet af den ordrebekræftede batchreservationsmekanisme.</span><span class="sxs-lookup"><span data-stu-id="ae152-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="ae152-227">Når et batchnummer reserveres for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet som tidligere nævnt reservere alle dimensioner til og med lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="ae152-228">Lagerstedsarbejdet vil derfor indeholde de samme lagringsdimensioner, der blev reserveret af de brugere, der har arbejdet med ordrerne, og de repræsenterer muligvis ikke altid den varelagringsplacering, der er praktisk eller endda mulig for plukoperationer.</span><span class="sxs-lookup"><span data-stu-id="ae152-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="ae152-229">Hvis ordrebehandlere er opmærksomme på lagerbegrænsningerne, kan det være en god ide manuelt at vælge de specifikke lokationer og id'er, når de reserverer en batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="ae152-230">I dette tilfælde skal brugeren bruge funktionen **Vis dimensioner** i sidehovedet og tilføje lokationen og id'et i gitteret i oversigtspanelet **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="ae152-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="ae152-231">På siden **Batchreservation** skal du vælge linjen for batch **B11** og derefter vælge **Reserver linje**.</span><span class="sxs-lookup"><span data-stu-id="ae152-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="ae152-232">Der er ingen foruddefineret logik ved tildeling af lokationer og id'er under automatisk reservation.</span><span class="sxs-lookup"><span data-stu-id="ae152-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="ae152-233">Du kan angive antallet manuelt i feltet **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="ae152-234">Bemærk, at oversigtspanelet **Batchnumre bundet til kildelinje**, batch **B11** er vist som **Bindende**.</span><span class="sxs-lookup"><span data-stu-id="ae152-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tilknytning af et bestemt batchnummer til en salgsordrelinje på siden Batchreservation](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="ae152-236">Reservation af antallet i en salgsordrelinje kan udføres på tværs af flere batches.</span><span class="sxs-lookup"><span data-stu-id="ae152-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="ae152-237">På samme måde kan reservation af samme batch udføres mod flere lokationer og id'er (hvis der er aktiveret id'er for lokationerne).</span><span class="sxs-lookup"><span data-stu-id="ae152-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="ae152-238">Reservation af en bestemt batch for antallet på en salgsordrelinje kan også være delvis.</span><span class="sxs-lookup"><span data-stu-id="ae152-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="ae152-239">Det samlede antal på 100 enheder kan f.eks. reserveres, så en bestemt batch bekræftes til 20 enheder, hvorimod 80 enheder er reserveret på lokations- og lagerstedsniveauer for alle tilgængelige batches.</span><span class="sxs-lookup"><span data-stu-id="ae152-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="ae152-240">I dette tilfælde vil WMS håndtere plukoperationer ved hjælp af to separate arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="ae152-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="ae152-241">Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="ae152-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="ae152-242">Vælg din vare, og vælg derefter **Styr lager** \> **Vis** \> **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="ae152-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Ordrebekræftet reservation som en lagertransaktionstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="ae152-244">Gennemse varens lagertransaktioner, der er relateret til reservationen af salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="ae152-245">En transaktion, hvor feltet **Reference** er angivet til **Salgsordre**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="ae152-246">Ifølge varens lagerreservationshierarki er disse dimensioner lokation, lagersted og lagerstatus.</span><span class="sxs-lookup"><span data-stu-id="ae152-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="ae152-247">En transaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for den specifikke batch og alle lagerdimensionerne over den.</span><span class="sxs-lookup"><span data-stu-id="ae152-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="ae152-248">Ifølge varens lagerreservationshierarki er disse dimensioner batchnummer og lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="ae152-249">I dette eksempel er lokationen **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="ae152-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="ae152-250">Vælg **Lagersted** \> **Handlinger** \> **Frigiv til lagersted** i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="ae152-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="ae152-251">Ordrelinjen er nu i bølge, og der oprettes en belastning og et arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="ae152-252">Gennemse og behandl lagerstedsarbejde, der har ordrebekræftede batchnumre</span><span class="sxs-lookup"><span data-stu-id="ae152-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="ae152-253">I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted** \> **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="ae152-254">Det arbejde, der håndterer plukoperationen for batchantal, der er bundet til salgsordrelinjen, har følgende karakteristika:</span><span class="sxs-lookup"><span data-stu-id="ae152-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="ae152-255">For at kunne oprette arbejde bruger systemet arbejdsskabeloner, men ikke lokationsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="ae152-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="ae152-256">Alle de standardindstillinger, der er defineret for arbejdsskabeloner, f.eks. det maksimale antal pluklinjer eller en bestemt måleenhed, vil blive anvendt til at bestemme, hvornår der skal oprettes nyt arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="ae152-257">De regler, der er knyttet til lokationsvejledninger til identifikation af pluklokationer, tages dog ikke i betragtning, fordi den ordrebekræftede reservation allerede angiver alle lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="ae152-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="ae152-258">Disse lagerdimensioner omfatter dimensionerne på lagerstedets lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="ae152-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="ae152-259">Derfor arver arbejdet disse dimensioner, uden at lokationsvejledninger skal benyttes.</span><span class="sxs-lookup"><span data-stu-id="ae152-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="ae152-260">Batchnummeret vises ikke på pluklinjen (som det er tilfældet for den arbejdslinje, der er oprettet for en vare, der har et tilknyttet reservationshierarki for "Batch-over\[lokation\]"). I stedet vises batchnummeret "fra" og alle andre lagringsdimensioner i arbejdslinjens lagertransaktion, der refereres til fra de tilknyttede lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="ae152-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Lagersteds lagertransaktion for arbejde, der stammer fra ordrebekræftet reservation](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="ae152-262">Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="ae152-263">Lagertransaktionen, hvor feltet **Reference** er angivet til **Arbejde**, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.</span><span class="sxs-lookup"><span data-stu-id="ae152-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="ae152-264">Lagerdrift kan fortsætte med at håndtere udførelsen af arbejdet på sædvanlig vis.</span><span class="sxs-lookup"><span data-stu-id="ae152-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="ae152-265">Vejledningen på mobilenheden giver dog arbejderen besked på at vælge et bestemt batchnummer.</span><span class="sxs-lookup"><span data-stu-id="ae152-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="ae152-266">I lagermiljøer med id-styrede lokationer kan en arbejder, når vedkommende når en lokation, der gemmer samme batch med flere id'er, plukke fra et hvilket som helst id, der ikke allerede er reserveret (f.eks. af en anden ordrebekræftet reservation eller arbejde, der stammer fra en reservation af den pågældende type).</span><span class="sxs-lookup"><span data-stu-id="ae152-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="ae152-267">Hvis det bliver for upraktisk at plukke fra den lokation, der er angivet på arbejdslinjen, kan lageroperatøren bruge en af følgende handlinger til at omdirigere plukning af den specifikke batch fra en mere praktisk lokation:</span><span class="sxs-lookup"><span data-stu-id="ae152-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="ae152-268">Standardhandlingen **Tilsidesæt lokation** på en mobilenhed (hvis lagermedarbejderens indstilling **Tillad tilsidesættelse af pluklokation** er aktiveret)</span><span class="sxs-lookup"><span data-stu-id="ae152-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="ae152-269">Handlingen **Skift lokation** på siden **Arbejdslistedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="ae152-270">Udfør plukning og placering af arbejdet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="ae152-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="ae152-271">Antallet **10** for batchnummer **B11** plukkes nu for salgsordrelinjen og placeres på lokationen **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="ae152-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="ae152-272">På dette tidspunkt er det klar til at blive læsset på lastbilen og sendt til kundens adresse.</span><span class="sxs-lookup"><span data-stu-id="ae152-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="ae152-273">Fleksibel reservation af id</span><span class="sxs-lookup"><span data-stu-id="ae152-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="ae152-274">Forretningsscenarie</span><span class="sxs-lookup"><span data-stu-id="ae152-274">Business scenario</span></span>

<span data-ttu-id="ae152-275">I dette scenario bruger en virksomhed lokationsstyring og arbejdsbehandling og håndterer lastplanlægning på niveauet for individuelle paller/containere uden for Supply Chain Management, før arbejdet oprettes.</span><span class="sxs-lookup"><span data-stu-id="ae152-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="ae152-276">Disse containere repræsenteres ved id'er i lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="ae152-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="ae152-277">For denne fremgangsmåde skal bestemte id'er derfor forhåndstildeles salgsordrelinjer, før der udføres plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="ae152-278">Virksomheden søger efter fleksibilitet i den måde, hvorpå reglerne for id-reservation håndteres, så følgende funktionsmåder finder sted:</span><span class="sxs-lookup"><span data-stu-id="ae152-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="ae152-279">Et id kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres af andre behov.</span><span class="sxs-lookup"><span data-stu-id="ae152-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="ae152-280">Denne funktionsmåde er en hjælp til at sikre, at det id, der blev planlagt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="ae152-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="ae152-281">Hvis id'et ikke allerede er tilknyttet en salgsordrelinje, kan lagermedarbejderne vælge et id under plukarbejdet, når salgsordreregistrering og -reservation er fuldført.</span><span class="sxs-lookup"><span data-stu-id="ae152-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="ae152-282">Aktivere fleksibel reservation af id</span><span class="sxs-lookup"><span data-stu-id="ae152-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="ae152-283">Før du kan bruge fleksibel reservation af id, skal to funktioner være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="ae152-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="ae152-284">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges.</span><span class="sxs-lookup"><span data-stu-id="ae152-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="ae152-285">Du skal aktivere funktionerne i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="ae152-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="ae152-286">**Funktionsnavn:** *Fleksibel reservation for dimension på lagerstedsniveau*</span><span class="sxs-lookup"><span data-stu-id="ae152-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="ae152-287">**Funktionsnavn:** *Fleksibel reservation af ordrebekræftet id*</span><span class="sxs-lookup"><span data-stu-id="ae152-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="ae152-288">Reservere et bestemt id på salgsordren</span><span class="sxs-lookup"><span data-stu-id="ae152-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="ae152-289">Hvis du vil aktivere reservation af id på en ordre, skal du markere afkrydsningsfeltet **Tillad reservation på behovsordre** for niveauet **Id** på siden **Lagerreservationshierarkier** for det hierarki, der er knyttet til den relevante vare.</span><span class="sxs-lookup"><span data-stu-id="ae152-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Siden med lagerreservationshierarkier for et fleksibelt id-reservationshierarki](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="ae152-291">Du kan aktivere id-reservation på ordren på et hvilket som helst tidspunkt i din installation.</span><span class="sxs-lookup"><span data-stu-id="ae152-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="ae152-292">Denne ændring påvirker ikke reservationer eller åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="ae152-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="ae152-293">Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes åbne udgående lagertransaktioner med afgangsstatus *I bestilling*, *Reserveret bestilt* eller *Reserveret fysisk* for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.</span><span class="sxs-lookup"><span data-stu-id="ae152-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="ae152-294">Selvom afkrydsningsfeltet **Tillad reservation ved behovsordre** er markeret for niveauet **Id**, er det stadig muligt *ikke* at reservere et bestemt id i ordren.</span><span class="sxs-lookup"><span data-stu-id="ae152-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="ae152-295">I dette tilfælde gælder den standardlagerlogik for lagerstedsoperationer, der er gyldig for reservationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ae152-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="ae152-296">Hvis du vil reservere et bestemt id, skal du bruge en [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md)-proces. I programmet kan du foretage reservationen direkte fra en salgsordre ved at bruge indstillingen **Ordrebekræftede reservationer pr. id** for kommandoen **Åbn i Excel**.</span><span class="sxs-lookup"><span data-stu-id="ae152-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="ae152-297">I de enhedsdata, der åbnes i tilføjelsesprogrammet til Excel, skal du angive følgende reservationsrelaterede data og derefter vælge **Publicer** for at sende dataene tilbage til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="ae152-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="ae152-298">Reference (kun *Salgsordre*-værdien understøttes).</span><span class="sxs-lookup"><span data-stu-id="ae152-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="ae152-299">Ordrenummer (værdien kan afledes af partiet).</span><span class="sxs-lookup"><span data-stu-id="ae152-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="ae152-300">Parti-id</span><span class="sxs-lookup"><span data-stu-id="ae152-300">Lot ID</span></span>
- <span data-ttu-id="ae152-301">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="ae152-301">License plate</span></span>
- <span data-ttu-id="ae152-302">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="ae152-302">Quantity</span></span>

<span data-ttu-id="ae152-303">Hvis du skal reservere et bestemt id for en vare med en batchsporing, skal du bruge siden **Batchreservation** som beskrevet i afsnittet [Angive oplysninger om salgsordre](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="ae152-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="ae152-304">Når den salgsordrelinje, der bruger en ordrebekræftet reservation af id, behandles af lagerstedshandlinger, bruges lokationsdirektiver ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="ae152-305">Hvis et lagersteds arbejdselement består af linjer, der svarer til en hel palle og har id-bekræftede antal, kan du optimere plukprocessen ved hjælp af et menupunkt i en mobilenhed, hvor indstillingen **Håndter efter id** er angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ae152-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="ae152-306">En lagermedarbejder kan derefter scanne et id for at fuldføre et pluk i stedet for at skulle scanne varerne fra arbejdet én efter én.</span><span class="sxs-lookup"><span data-stu-id="ae152-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Menupunktet i mobilenheden, hvor indstillingen Håndter efter id er angivet til Ja](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="ae152-308">Da funktionen **Håndter efter id** ikke understøtter arbejde, der dækker flere paller, er det bedre at have et separat arbejdselement til forskellige id'er.</span><span class="sxs-lookup"><span data-stu-id="ae152-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="ae152-309">Hvis du vil bruge denne fremgangsmåde, skal du tilføje feltet **Ordre bekræftet id** som en arbejdshovedpause på siden **Arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="ae152-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-310">For den ordrebekræftede arbejdsoprettelsesproces tildeles en værdi for "ordrebekræftet lagerdimension" til pluklinjerne, og der vil ikke være mulighed for at få vist id-værdien direkte.</span><span class="sxs-lookup"><span data-stu-id="ae152-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="ae152-311">Kun *Brugerstyret*-proces understøttes, når du konfigurerer et menupunkt i mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="ae152-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="ae152-312">Eksempel på scenario: oprette og behandle en ordrebekræftet id-reservation</span><span class="sxs-lookup"><span data-stu-id="ae152-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="ae152-313">Dette scenario viser, hvordan du kan oprette og behandle en ordrebekræftet id-reservation.</span><span class="sxs-lookup"><span data-stu-id="ae152-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ae152-314">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="ae152-314">Make demo data available</span></span>

<span data-ttu-id="ae152-315">Dette scenario indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er leveret til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae152-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="ae152-316">Hvis du vil arbejde gennem scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et miljø, hvor standarddemodata er installeret.</span><span class="sxs-lookup"><span data-stu-id="ae152-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="ae152-317">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="ae152-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="ae152-318">Oprette et hierarki for lagerreservationer, der giver mulighed for reservation af id</span><span class="sxs-lookup"><span data-stu-id="ae152-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="ae152-319">Gå til **Lokationsstyring \> Konfiguration \> Lager \> Reservationshierarki**.</span><span class="sxs-lookup"><span data-stu-id="ae152-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="ae152-320">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ae152-320">Select **New**.</span></span>
1. <span data-ttu-id="ae152-321">Angiv en værdi i feltet **Navn** (f.eks. *FleksibeltID*).</span><span class="sxs-lookup"><span data-stu-id="ae152-321">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="ae152-322">Indtast en beskrivelse i feltet **Beskrivelse** (f.eks. *Fleksibel id-reservation*).</span><span class="sxs-lookup"><span data-stu-id="ae152-322">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="ae152-323">Vælg **Batchnummer**, **Serienummer** og **Ejer** på listen **Valgte**.</span><span class="sxs-lookup"><span data-stu-id="ae152-323">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="ae152-324">Vælg knappen **Fjern** ![bagudrettet pil](media/backward-button.png) for at flytte de valgte poster til listen **Tilgængelige**.</span><span class="sxs-lookup"><span data-stu-id="ae152-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="ae152-325">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae152-325">Select **OK**.</span></span>
1. <span data-ttu-id="ae152-326">I rækken med dimensionsniveau for **Id** skal du markere afkrydsningsfeltet **Tillad reservation i behovsordre**.</span><span class="sxs-lookup"><span data-stu-id="ae152-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="ae152-327">Niveauet **Lokation** vælges automatisk, og du kan ikke fjerne markeringerne i afkrydsningsfeltet for det.</span><span class="sxs-lookup"><span data-stu-id="ae152-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="ae152-328">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ae152-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="ae152-329">Oprette to frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="ae152-329">Create two released products</span></span>

1. <span data-ttu-id="ae152-330">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="ae152-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ae152-331">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ae152-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ae152-332">Angiv følgende værdier i dialogboksen **Nyt frigivet produkt**:</span><span class="sxs-lookup"><span data-stu-id="ae152-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ae152-333">**Produktnummer:** *Vare1*</span><span class="sxs-lookup"><span data-stu-id="ae152-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="ae152-334">**Varenummer:** *Vare1*</span><span class="sxs-lookup"><span data-stu-id="ae152-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="ae152-335">**Varemodelgruppe:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="ae152-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="ae152-336">**Varegruppe:** *Lyd*</span><span class="sxs-lookup"><span data-stu-id="ae152-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="ae152-337">**Lagringsdimensionsgruppe:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="ae152-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="ae152-338">**Sporingsdimensionsgruppe:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="ae152-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="ae152-339">**Reservationshierarki:** *FleksibeltID*</span><span class="sxs-lookup"><span data-stu-id="ae152-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="ae152-340">Vælg **OK** for at oprette produktet og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ae152-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="ae152-341">Det nye produkt åbnes.</span><span class="sxs-lookup"><span data-stu-id="ae152-341">The new product is opened.</span></span> <span data-ttu-id="ae152-342">I oversigtspanelet **Lager** skal du i feltet **Enhedsseriegruppe-id** angive *ea*.</span><span class="sxs-lookup"><span data-stu-id="ae152-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="ae152-343">Gentag de forrige trin for at oprette et andet produkt, der har de samme indstillinger, men angiv felterne **Produktnummer** og **Varenummer** til *Vare2*.</span><span class="sxs-lookup"><span data-stu-id="ae152-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="ae152-344">I handlingsruden skal du under fanen **Styr lager** i gruppen **Vis** vælge **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="ae152-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="ae152-345">Vælg derefter **Justering af antal**.</span><span class="sxs-lookup"><span data-stu-id="ae152-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="ae152-346">Juster den disponible lagerbeholdning af de nye varer som angivet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ae152-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="ae152-347">Post</span><span class="sxs-lookup"><span data-stu-id="ae152-347">Item</span></span>  | <span data-ttu-id="ae152-348">Lagersted</span><span class="sxs-lookup"><span data-stu-id="ae152-348">Warehouse</span></span> | <span data-ttu-id="ae152-349">Placering</span><span class="sxs-lookup"><span data-stu-id="ae152-349">Location</span></span> | <span data-ttu-id="ae152-350">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="ae152-350">License plate</span></span> | <span data-ttu-id="ae152-351">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="ae152-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="ae152-352">Vare1</span><span class="sxs-lookup"><span data-stu-id="ae152-352">Item1</span></span> | <span data-ttu-id="ae152-353">24</span><span class="sxs-lookup"><span data-stu-id="ae152-353">24</span></span>        | <span data-ttu-id="ae152-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="ae152-354">FL-010</span></span>   | <span data-ttu-id="ae152-355">LP01</span><span class="sxs-lookup"><span data-stu-id="ae152-355">LP01</span></span>          | <span data-ttu-id="ae152-356">10</span><span class="sxs-lookup"><span data-stu-id="ae152-356">10</span></span>       |
    | <span data-ttu-id="ae152-357">Vare1</span><span class="sxs-lookup"><span data-stu-id="ae152-357">Item1</span></span> | <span data-ttu-id="ae152-358">24</span><span class="sxs-lookup"><span data-stu-id="ae152-358">24</span></span>        | <span data-ttu-id="ae152-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="ae152-359">FL-011</span></span>   | <span data-ttu-id="ae152-360">LP02</span><span class="sxs-lookup"><span data-stu-id="ae152-360">LP02</span></span>          | <span data-ttu-id="ae152-361">10</span><span class="sxs-lookup"><span data-stu-id="ae152-361">10</span></span>       |
    | <span data-ttu-id="ae152-362">Vare2</span><span class="sxs-lookup"><span data-stu-id="ae152-362">Item2</span></span> | <span data-ttu-id="ae152-363">24</span><span class="sxs-lookup"><span data-stu-id="ae152-363">24</span></span>        | <span data-ttu-id="ae152-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="ae152-364">FL-010</span></span>   | <span data-ttu-id="ae152-365">LP01</span><span class="sxs-lookup"><span data-stu-id="ae152-365">LP01</span></span>          | <span data-ttu-id="ae152-366">5</span><span class="sxs-lookup"><span data-stu-id="ae152-366">5</span></span>        |
    | <span data-ttu-id="ae152-367">Vare2</span><span class="sxs-lookup"><span data-stu-id="ae152-367">Item2</span></span> | <span data-ttu-id="ae152-368">24</span><span class="sxs-lookup"><span data-stu-id="ae152-368">24</span></span>        | <span data-ttu-id="ae152-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="ae152-369">FL-011</span></span>   | <span data-ttu-id="ae152-370">LP02</span><span class="sxs-lookup"><span data-stu-id="ae152-370">LP02</span></span>          | <span data-ttu-id="ae152-371">5</span><span class="sxs-lookup"><span data-stu-id="ae152-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="ae152-372">Du skal oprette de to id'er og bruge lokationer, der giver mulighed for blandede varer, f.eks. *FL-010* og *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="ae152-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="ae152-373">Oprette en salgsordre og reservere et bestemt id</span><span class="sxs-lookup"><span data-stu-id="ae152-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="ae152-374">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ae152-375">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ae152-375">Select **New**.</span></span>
1. <span data-ttu-id="ae152-376">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="ae152-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ae152-377">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ae152-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ae152-378">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="ae152-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="ae152-379">Vælg **OK** for at lukke dialogboksen **Opret salgsordrer** og åbne den nye salgsordre.</span><span class="sxs-lookup"><span data-stu-id="ae152-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="ae152-380">I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="ae152-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="ae152-381">**Varenummer:** *Vare1*</span><span class="sxs-lookup"><span data-stu-id="ae152-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="ae152-382">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="ae152-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="ae152-383">Tilføj en anden salgsordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="ae152-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="ae152-384">**Varenummer:** *Vare2*</span><span class="sxs-lookup"><span data-stu-id="ae152-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="ae152-385">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="ae152-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ae152-386">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ae152-386">Select **Save**.</span></span>
1. <span data-ttu-id="ae152-387">I oversigtspanelet **Linjedetaljer** skal du under fanen **Konfiguration** notere dig **Parti-id**-værdien for hver linje.</span><span class="sxs-lookup"><span data-stu-id="ae152-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="ae152-388">Disse værdier skal angives under reservation af bestemte id'er.</span><span class="sxs-lookup"><span data-stu-id="ae152-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-389">Hvis du vil reservere et bestemt id, skal du bruge dataenheden **Ordrebekræftede reservationer pr. id**.</span><span class="sxs-lookup"><span data-stu-id="ae152-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="ae152-390">Hvis du vil reservere et bestemt id for en vare med batchsporing, skal du bruge siden **Batchreservation** som beskrevet i afsnittet [Angive oplysninger om salgsordre](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="ae152-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="ae152-391">Hvis du angiver id'et direkte på salgsordrelinjen og bekræfter det på systemet, bruges behandlingen af lagerstyring ikke for linjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="ae152-392">Vælg **Åbn i Microsoft Office**, vælg **Ordrebekræftede reservationer pr. id**, og download filen.</span><span class="sxs-lookup"><span data-stu-id="ae152-392">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="ae152-393">Åbn den downloadede fil i Excel, og vælg **Aktivér redigering** for at aktivere Excel-tilføjelsesprogrammet til at køre.</span><span class="sxs-lookup"><span data-stu-id="ae152-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="ae152-394">Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du vælge **Har tillid til dette tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="ae152-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="ae152-395">Hvis du bliver bedt om at logge på, skal du vælge **Log på** og derefter logge på ved hjælp af de samme legitimationsoplysninger, du brugte til at logge på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae152-395">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="ae152-396">Hvis du vil reservere en vare på et bestemt id, skal du vælge **Ny** i Excel-tilføjelsesprogrammet for at tilføje en reservationslinje og derefter angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ae152-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="ae152-397">**Parti-id:** Angiv den **Parti-id**-værdi, du har fundet for salgsordrelinjen til *Vare1*.</span><span class="sxs-lookup"><span data-stu-id="ae152-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="ae152-398">**Id:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="ae152-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="ae152-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="ae152-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="ae152-400">Vælg **Ny** for at tilføje en anden reservationslinje, og angiv følgende værdier på den:</span><span class="sxs-lookup"><span data-stu-id="ae152-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="ae152-401">**Parti-id:** Angiv den **Parti-id**-værdi, du har fundet for salgsordrelinjen til *Vare2*.</span><span class="sxs-lookup"><span data-stu-id="ae152-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="ae152-402">**Id:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="ae152-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="ae152-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="ae152-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="ae152-404">Vælg **Publicer** i Excel-tilføjelsesprogrammet for at sende dataene tilbage til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae152-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-405">Reservationslinjen vises kun i systemet, hvis publiceringen er fuldført uden fejl.</span><span class="sxs-lookup"><span data-stu-id="ae152-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="ae152-406">Gå tilbage til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae152-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="ae152-407">Hvis du vil gennemse varens reservation, skal du i oversigtspanelet **Salgsordrelinjer** i menuen **Lager** vælge **Vedligehold \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="ae152-408">Bemærk, at for salgsordrelinjen til *Vare1* er lager *10* reserveret, og for salgsordrelinjen til *Vare2* er lager *5* reserveret.</span><span class="sxs-lookup"><span data-stu-id="ae152-408">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="ae152-409">Hvis du vil gennemse lagertransaktioner, der er relateret til reservationen af salgsordrelinjen, skal du i oversigtspanelet **Salgsordrelinjer** i menuen **Lager** vælge **Vis \> Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="ae152-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="ae152-410">Bemærk, at der er to transaktioner, der er relateret til reservationen: en, hvor **Reference**-feltet er angivet til *Salgsordre*, og en, hvor **Reference**-feltet er angivet til *Ordrebekræftet reservation*.</span><span class="sxs-lookup"><span data-stu-id="ae152-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-411">En transaktion, hvor feltet **Reference** er angivet til *Salgsordre* repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation** (sted, lagersted og lagerstatus).</span><span class="sxs-lookup"><span data-stu-id="ae152-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="ae152-412">En transaktion, hvor **Reference**-feltet er angivet til *Ordrebekræftet reservation*, repræsenterer ordrelinjereservationen for det specifikke id og den specifikke lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="ae152-413">Frigiv salgsordren ved i handlingsruden at bruge fanen **Lager**, gruppen **Handlinger** og indstillingen **Frigiv til lagersted**.</span><span class="sxs-lookup"><span data-stu-id="ae152-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="ae152-414">Gennemgå og behandle lagerstedsarbejde med ordrebekræftede id'er, der er tildelt</span><span class="sxs-lookup"><span data-stu-id="ae152-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="ae152-415">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Arbejdsdetaljer** i menuen **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="ae152-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="ae152-416">Når der foretages reservation for et bestemt batch, bruger systemet ikke lokationsdirektiver, når det opretter arbejdet for salgsordren, der bruger id-reservation.</span><span class="sxs-lookup"><span data-stu-id="ae152-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="ae152-417">Da den ordrebekræftede reservation angiver alle lagerdimensioner, herunder lokationen, skal du ikke bruge lokationsdirektiver, da disse lagerdimensioner kun er angivet i arbejdet.</span><span class="sxs-lookup"><span data-stu-id="ae152-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="ae152-418">De vises i afsnittet **Fra lagerdimensioner** på siden **Arbejdslagertransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="ae152-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-419">Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til *Ordrebekræftet reservation*.</span><span class="sxs-lookup"><span data-stu-id="ae152-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="ae152-420">Lagertransaktionen, hvor feltet **Reference** er angivet til *Arbejde*, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.</span><span class="sxs-lookup"><span data-stu-id="ae152-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="ae152-421">På mobilenheden skal du afslutte plukning og placere arbejdet ved hjælp af et menupunkt, hvor afkrydsningsfeltet **Håndter efter id** er markeret.</span><span class="sxs-lookup"><span data-stu-id="ae152-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae152-422">Med funktionen **Håndter efter id** kan du behandle hele id'et.</span><span class="sxs-lookup"><span data-stu-id="ae152-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="ae152-423">Hvis du skal behandle en del af id'et, kan du ikke bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="ae152-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="ae152-424">Det anbefales, at du har genereret et separat arbejde for hvert enkelt id.</span><span class="sxs-lookup"><span data-stu-id="ae152-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="ae152-425">Du kan opnå dette resultat ved at bruge funktionen **Opgaveoverskriften skifter** på siden **Arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="ae152-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="ae152-426">Id *LP02* plukkes nu til salgsordrelinjer og placeres på lokationen *Lagerport*.</span><span class="sxs-lookup"><span data-stu-id="ae152-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="ae152-427">På dette tidspunkt er det klar til at blive læsset og sendt til kundens adresse.</span><span class="sxs-lookup"><span data-stu-id="ae152-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="ae152-428">Undtagelseshåndtering af lagerstedsarbejde, der har ordrebekræftede batchnumre</span><span class="sxs-lookup"><span data-stu-id="ae152-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="ae152-429">Lagerstedsarbejde for plukning af ordrebekræftede batchnumre er underlagt samme standardhåndtering af undtagelser for lagersted og handlinger som almindeligt arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="ae152-430">Generelt kan det åbne arbejde eller den åbne arbejdslinje annulleres, den kan afbrydes, fordi en brugerlokation er fuld, den kan være kort plukket, og den kan opdateres på grund af en bevægelse.</span><span class="sxs-lookup"><span data-stu-id="ae152-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="ae152-431">På samme måde kan den plukkede mængde arbejde, der allerede er udført, reduceres, eller arbejdet kan tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="ae152-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="ae152-432">Følgende nøgleregel anvendes til alle disse handlinger af typen undtagelseshåndtering: Det batchnummer, der er reserveret til kunden, kan aldrig erstattes med et andet batchnummer, men lagerdimensionerne (lokation og id) kan ændres via enten en manuel opdatering fra brugerens side eller en automatisk opdatering udført af systemet.</span><span class="sxs-lookup"><span data-stu-id="ae152-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="ae152-433">Den automatiske opdatering er baseret på den samme tilfældige tildeling af lagringsdimensioner, der anvendes, når en bestemt batch blev reserveret automatisk, men der ikke blev angivet nogen lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="ae152-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="ae152-434">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="ae152-434">Example scenario</span></span>

<span data-ttu-id="ae152-435">Et eksempel på dette scenario er en situation, hvor tidligere udført arbejde ikke kan plukkes ved hjælp af funktionen **Reducer det antal, der er plukket**.</span><span class="sxs-lookup"><span data-stu-id="ae152-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="ae152-436">I dette eksempel antages det, at du allerede har udført de trin, der er beskrevet i [Eksempel på scenario: batchnummertildeling](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="ae152-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="ae152-437">Det er en fortsættelse af dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="ae152-437">It continues from that example.</span></span>

1. <span data-ttu-id="ae152-438">Gå til **Lokationsstyring** \> **Laster** \> **Aktive laster**.</span><span class="sxs-lookup"><span data-stu-id="ae152-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="ae152-439">Vælg den last, der blev oprettet i forbindelse med forsendelsen af salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ae152-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="ae152-440">Vælg **Reducer det antal, der er plukket** i oversigtspanelet **Indlæs ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="ae152-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="ae152-441">Vælg **FL-001** i feltet **Flyt til lokation** på siden **Reducer det antal, der er plukket**.</span><span class="sxs-lookup"><span data-stu-id="ae152-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="ae152-442">Vælg **LP33** i feltet **Flyt til nummerplade**.</span><span class="sxs-lookup"><span data-stu-id="ae152-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="ae152-443">Angiv **10** i feltet **Lagerantal, hvor plukning skal fortrydes**.</span><span class="sxs-lookup"><span data-stu-id="ae152-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="ae152-444">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae152-444">Select **OK**.</span></span>

<span data-ttu-id="ae152-445">Følgende er resultatet af handlingen til fortrydelse af plukning:</span><span class="sxs-lookup"><span data-stu-id="ae152-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="ae152-446">Status for det tidligere lukkede arbejde angives til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="ae152-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="ae152-447">Der oprettes nyt arbejde af typen **Lagerbevægelser** for det ikke-plukkede antal på **10** for batchnummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="ae152-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="ae152-448">Dette arbejde repræsenterer bevægelsen fra lokationen **Baydoor** til id **LP33** på lokation **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="ae152-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="ae152-449">Status er angivet til **Lukket**.</span><span class="sxs-lookup"><span data-stu-id="ae152-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="ae152-450">Systemet reserverer igen det batchnummer, der oprindeligt blev bestilt, og tildeler lokation og id'er.</span><span class="sxs-lookup"><span data-stu-id="ae152-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="ae152-451">(Denne proces svarer til at køre funktionen **Reserver linje** for ordrelinjen for et bestemt batchnummer).</span><span class="sxs-lookup"><span data-stu-id="ae152-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="ae152-452">Derfor vises **B11** som bekræftet i oversigtspanelet **Batchnumre bundet til kildelinje** på siden **Batchreservation**, og feltet **Reservation** indeholder antallet **10** for batchnummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="ae152-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="ae152-453">Desuden angives feltet **Lokation** til **FL-001**, og feltet **Nummerplade** angives til **LP11**.</span><span class="sxs-lookup"><span data-stu-id="ae152-453">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="ae152-454">(Du kan føje disse felter til gitteret, hvis de ikke er synlige).</span><span class="sxs-lookup"><span data-stu-id="ae152-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="ae152-455">Følgende tabeller indeholder en oversigt, der viser, hvordan systemet håndterer ordrebekræftet batchreservation for specifikke lagerstedshandlinger.</span><span class="sxs-lookup"><span data-stu-id="ae152-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="ae152-456">Hvis du vil fortolke indholdet i tabellerne, skal du antage, at hver lagerstedshandling køres i konteksten af det eksisterende lagerarbejde, der stammer fra en ordrebekræftet batchreservation, eller at udførelsen af de enkelte lagerhandlinger påvirker arbejde af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="ae152-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-457">I disse tabeller angiver kolonnen "Batchantal er tilgængeligt", om der findes et tilgængeligt batchantal ud over det antal, der enten allerede er reserveret for de aktuelle ordrebekræftede reservationer, eller som allerede er reserveret af det lagerstedsarbejde, der stammer fra reservationer af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="ae152-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="ae152-458">Tilsidesæt pluklokationen for det åbne arbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-459">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-460">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-461">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-461">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-462">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-462">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-463">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-464">Indstillingen <strong>Tillad tilsidesættelse af pluklokation</strong> er aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ae152-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ae152-465">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-466">Vælg menupunktet <strong>Tilsidesæt lokation</strong> på lagerstedsappen, når du starter pluk af arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="ae152-467">Vælg <strong>Foreslå</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="ae152-468">Bekræft den nye lokation, der foreslås, på basis af tilgængeligheden af batchantal.</span><span class="sxs-lookup"><span data-stu-id="ae152-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-469">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="ae152-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ae152-470">Lokationen på pluklinjen opdateres til den nye lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="ae152-471">(Hvis lokaliteten er id-styret, tildeles et tilfældigt id til lagerbeholdningstransaktionen, og arbejderen kan plukke fra et hvilken som helst id, der har tilgængeligt antal).</span><span class="sxs-lookup"><span data-stu-id="ae152-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="ae152-472">Hvis antallet findes på mere end ét id på den nye lokation, opdeles den oprindelige pluklinje i flere linjer, så den svarer til hvert enkelt id.</span><span class="sxs-lookup"><span data-stu-id="ae152-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-473">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-474">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae152-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-475">Vælg menupunktet <strong>Tilsidesæt lokation</strong> på lagerstedsappen, når du starter pluk af arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="ae152-476">Angiv en lokation manuelt.</span><span class="sxs-lookup"><span data-stu-id="ae152-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-477">Handlingen <strong>Tilsidesæt lokation</strong> er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="ae152-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="ae152-478">Det mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="ae152-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="ae152-479">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="ae152-480">Knappen Fuld – opdel en arbejdslinje på grund af overløb på brugerens lokation</span><span class="sxs-lookup"><span data-stu-id="ae152-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-481">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-482">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-483">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-483">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-484">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-484">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-485">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ae152-486">Indstillingen <strong>Tillad opdeling af arbejde</strong> er aktiveret for menupunktet mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="ae152-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="ae152-487">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-488">Vælg menupunktet <strong>Fuld</strong> på lagerstedsapp, når du behandler plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="ae152-489">I feltet <strong>Plukantal</strong> skal du angive en del af antallet af det krævede pluk for at angive den fulde kapacitet.</span><span class="sxs-lookup"><span data-stu-id="ae152-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-490">I det aktuelle arbejde opdateres antallet med det resterende antal, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="ae152-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="ae152-491">Nyt arbejde for det plukkede antal oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="ae152-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="ae152-492">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="ae152-493">Reducer det plukkede antal af fuldført arbejde (fra en last)</span><span class="sxs-lookup"><span data-stu-id="ae152-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-494">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-495">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-496">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-496">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-497">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-497">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-498">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-499">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-499">Not applicable</span></span></td>
<td><span data-ttu-id="ae152-500">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-501">Åbn siden <strong>Reducer det antal, der er plukket</strong> antal fra lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="ae152-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="ae152-502">Angiv hele antallet, plukning skal fortrydes for.</span><span class="sxs-lookup"><span data-stu-id="ae152-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="ae152-503">Vælg en "flyt til"-lokation/id.</span><span class="sxs-lookup"><span data-stu-id="ae152-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="ae152-504">Arbejde, der er tilknyttet lastlinjen, annulleres.</span><span class="sxs-lookup"><span data-stu-id="ae152-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="ae152-505">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="ae152-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-506">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-507">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-508">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-508">No</span></span></td>
<td><span data-ttu-id="ae152-509">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-509">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-510">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-510">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-511">Antallet reserveres igen for samme batch og for samme lokation og id (hvis lokationen er id-styret), der blev angivet under annullering af pluk.</span><span class="sxs-lookup"><span data-stu-id="ae152-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="ae152-512">Flyt en vare inden for et lagersted</span><span class="sxs-lookup"><span data-stu-id="ae152-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-513">Denne lagerstedshandling gælder kun for flytning af typen **Arbejdsoprettelsesproces**, ikke for bevægelse efter skabelon.</span><span class="sxs-lookup"><span data-stu-id="ae152-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-514">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-515">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-516">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-516">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-517">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-517">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-518">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-519">Indstillingen <strong>Tillad flytning af lager med tilknyttet arbejde</strong> er aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ae152-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ae152-520">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-521">Start en bevægelse på lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="ae152-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="ae152-522">Angiv "fra"- og "til"-lokationer.</span><span class="sxs-lookup"><span data-stu-id="ae152-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="ae152-523">I alt eksisterende arbejde, der påvirkes af flytningen, opdateres plukpladsen til den nye "til"-lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="ae152-524">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="ae152-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-525">Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-526">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-527">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-527">No</span></span></td>
<td><span data-ttu-id="ae152-528">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-528">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-529">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-529">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-530">Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for den samme batch og for den nye "til"-lokation og det nye id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="ae152-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="ae152-531">Tilbagefør det plukkede antal af fuldført arbejde (fra en belastning eller en bølge)</span><span class="sxs-lookup"><span data-stu-id="ae152-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-532">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-533">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-534">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-534">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-535">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-535">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-536">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="ae152-537">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-537">Not applicable</span></span></td>
<td><span data-ttu-id="ae152-538">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-539">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ae152-540">Vælg indstillingen <strong>Efterlad varer på aktuel lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="ae152-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-541">Alt arbejde, der er tilknyttet lasten, annulleres.</span><span class="sxs-lookup"><span data-stu-id="ae152-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="ae152-542">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-543">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-544">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-544">No</span></span></td>
<td><span data-ttu-id="ae152-545">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-545">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-546">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-546">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-547">Antallet reserveres igen for den samme batch og for den lokation og det id, hvor antallet blev placeret ved tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="ae152-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-548">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-549">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ae152-550">Vælg indstillingen <strong>Tildel varer til denne lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="ae152-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-551">Det aktuelle arbejde er annulleret.</span><span class="sxs-lookup"><span data-stu-id="ae152-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="ae152-552">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="ae152-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-553">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-554">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-555">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-555">No</span></span></td>
<td><span data-ttu-id="ae152-556">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-556">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-557">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-557">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-558">Antallet reserveres igen for den samme batch og for den lokation og det id, som antallet blev tildelt ved tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="ae152-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-559">Ja/nej</span><span class="sxs-lookup"><span data-stu-id="ae152-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-560">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ae152-561">Vælg indstillingen <strong>Flyt varer til denne lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="ae152-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-562">Tilbageførsel understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="ae152-563">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-564">Ja/nej</span><span class="sxs-lookup"><span data-stu-id="ae152-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-565">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ae152-566">Vælg indstillingen <strong>Flyt varer på basis af lokationsvejledninger</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="ae152-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-567">Tilbageførsel understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="ae152-568">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="ae152-569">Kort pluk et antal – Registrer antallet som fysisk ikke fundet ved lokationen/id'et, når du udfører plukarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-570">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-571">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-572">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-572">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-573">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-573">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-574">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-575">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="ae152-576">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-577">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-578">Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-579">I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-580">Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ae152-581">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="ae152-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-582">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-583">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-584">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-584">No</span></span></td>
<td><span data-ttu-id="ae152-585">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ae152-586">Handlingen kort pluk mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="ae152-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="ae152-587">Det aktuelle arbejde forbliver åbent.</span><span class="sxs-lookup"><span data-stu-id="ae152-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-588">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-589">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="ae152-590">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-591">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-592">Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-593">I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-594">Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ae152-595">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="ae152-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-596">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-597">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-598">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-598">No</span></span></td>
<td><span data-ttu-id="ae152-599">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-599">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-600">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-600">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-601">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, fjernes.</span><span class="sxs-lookup"><span data-stu-id="ae152-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-602">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej/Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="ae152-603">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ae152-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ae152-604">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-605">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-606">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-607">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="ae152-608">Vælg lokationen/id'et på listen.</span><span class="sxs-lookup"><span data-stu-id="ae152-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-609">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="ae152-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ae152-610">Pluklinjen er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ae152-611">Læg på lager-linjen annulleres.</span><span class="sxs-lookup"><span data-stu-id="ae152-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="ae152-612">Der oprettes en ny pluklinje.</span><span class="sxs-lookup"><span data-stu-id="ae152-612">A new pick line is created.</span></span> <span data-ttu-id="ae152-613">Den bruger den lokation/det ud, som brugeren har valgt.</span><span class="sxs-lookup"><span data-stu-id="ae152-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="ae152-614">Der oprettes en ny læg på lager-linje.</span><span class="sxs-lookup"><span data-stu-id="ae152-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ae152-615">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="ae152-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-616">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-617">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="ae152-618">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ae152-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ae152-619">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae152-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-620">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-621">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-622">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-623">Handlingen kort pluk mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="ae152-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="ae152-624">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-625">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="ae152-626">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ae152-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ae152-627">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae152-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-628">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-629">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-630">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="ae152-631">Vælg lokationen/id'et på listen.</span><span class="sxs-lookup"><span data-stu-id="ae152-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ae152-632">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="ae152-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ae152-633">Pluklinjen er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ae152-634">Læg på lager-linjen annulleres.</span><span class="sxs-lookup"><span data-stu-id="ae152-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ae152-635">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="ae152-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ae152-636">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation/id, fjernes.</span><span class="sxs-lookup"><span data-stu-id="ae152-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-637">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Automatisk</strong>, <strong>Reguler lager</strong> = <strong>Ja/Nej</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja/Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="ae152-638">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="ae152-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-639">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="ae152-640">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="ae152-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ae152-641">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med automatisk omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-642">Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="ae152-643">Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="ae152-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="ae152-644">Skift status for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="ae152-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="ae152-645">Lagerstedshandlingen kan udføres fra flere indgangspunkter.</span><span class="sxs-lookup"><span data-stu-id="ae152-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="ae152-646">Det eksempel, der vises her, bruger handlingen **Ændring af lagerstatus** på siden **Disponibel efter lokation**.</span><span class="sxs-lookup"><span data-stu-id="ae152-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ae152-647">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="ae152-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="ae152-648">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="ae152-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ae152-649">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="ae152-649">Key user steps</span></span></th>
<th><span data-ttu-id="ae152-650">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="ae152-650">Warehouse work</span></span></th>
<th><span data-ttu-id="ae152-651">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="ae152-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-652">Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Reservationer</strong> eller <strong>Afmærkninger og reservationer</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="ae152-653">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-654">Vælg en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="ae152-655">Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="ae152-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="ae152-656">Vælg <strong>Ændring af lagerstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="ae152-657">Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-658">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ae152-659">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-660">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="ae152-661">To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ae152-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="ae152-662">Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</span><span class="sxs-lookup"><span data-stu-id="ae152-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ae152-663">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-663">No</span></span></td>
<td><span data-ttu-id="ae152-664">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-664">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-665">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ae152-666">Reservationen fjernes.</span><span class="sxs-lookup"><span data-stu-id="ae152-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="ae152-667">To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ae152-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="ae152-668">Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</span><span class="sxs-lookup"><span data-stu-id="ae152-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="ae152-669">Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Ingen</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="ae152-670">Ja</span><span class="sxs-lookup"><span data-stu-id="ae152-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ae152-671">Vælg en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="ae152-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="ae152-672">Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="ae152-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="ae152-673">Vælg <strong>Ændring af lagerstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="ae152-674">Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae152-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ae152-675">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="ae152-676">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="ae152-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ae152-677">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="ae152-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae152-678">Nr.</span><span class="sxs-lookup"><span data-stu-id="ae152-678">No</span></span></td>
<td><span data-ttu-id="ae152-679">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="ae152-679">See the previous row.</span></span></td>
<td><span data-ttu-id="ae152-680">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="ae152-681">Ændringer i lagerstatus er ikke tilladt.</span><span class="sxs-lookup"><span data-stu-id="ae152-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="ae152-682">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="ae152-682">Limitations</span></span>

- <span data-ttu-id="ae152-683">Reservationsfunktionaliteten for fleksibel dimension for lagerstedsniveau understøtter ikke følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="ae152-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="ae152-684">Styring af fastvægt</span><span class="sxs-lookup"><span data-stu-id="ae152-684">Catch weight management</span></span>
    - <span data-ttu-id="ae152-685">Fysisk negativt lager</span><span class="sxs-lookup"><span data-stu-id="ae152-685">Physical negative inventory</span></span>
    - <span data-ttu-id="ae152-686">Reservation i forhold til bestilt forsyning</span><span class="sxs-lookup"><span data-stu-id="ae152-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="ae152-687">Flytteordrer og pluk af råvarer</span><span class="sxs-lookup"><span data-stu-id="ae152-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="ae152-688">Der er begrænsninger for containerkonsolideringsreglen for pakning efter vejledningsenhed.</span><span class="sxs-lookup"><span data-stu-id="ae152-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="ae152-689">I forbindelse med ordrebekræftede reservationer anbefales det, at du ikke bruger skabeloner til containerbuild, hvor feltet **Pakning efter vejledningsenhed** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ae152-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="ae152-690">I det aktuelle design bruges lokationsvejledninger ikke, når der oprettes lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="ae152-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="ae152-691">Derfor er det kun den laveste enhed i enhedsseriegruppen (lagerenheden), der anvendes under containeriseringsbølgetrinnet.</span><span class="sxs-lookup"><span data-stu-id="ae152-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]