---
title: Reservationspolitik for fleksibel dimension for lagerstedsniveau
description: I dette emne beskrives politikken for lagerreservation, hvor virksomheder, der sælger batchsporede produkter og kører deres logistik som WMS-aktiverede operationer, kan reservere bestemte batches for kundesalgsordrer, selvom det reservationshierarki, der er tilknyttet produkterne, ikke tillader reservation af bestemte batches.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec80346126713cc604b00e6ca7f6e8f4c242dc6f
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530299"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="9723f-103">Reservationspolitik for fleksibel dimension for lagerstedsniveau</span><span class="sxs-lookup"><span data-stu-id="9723f-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9723f-104">Når et lagerreservationshierarki af typen "Batch under\[lokation\]" er knyttet til produkter, kan virksomheder, der sælger batchsporede produkter og kører logistik som handlinger, der er aktiveret for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere bestemte batches af de pågældende produkter til kundesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="9723f-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="9723f-105">Dette emne beskriver den politik for lagerreservation, der giver disse virksomheder mulighed for at reservere bestemte batches, selv når produkterne er knyttet til et reservationshierarki af typen "batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="9723f-106">Lagerreservationshierarki</span><span class="sxs-lookup"><span data-stu-id="9723f-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="9723f-107">I dette afsnit opsummeres det eksisterende lagerreservationshierarki.</span><span class="sxs-lookup"><span data-stu-id="9723f-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="9723f-108">Der fokuseres på den måde, batchsporede og seriesporede varer håndteres på.</span><span class="sxs-lookup"><span data-stu-id="9723f-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="9723f-109">Lagerreservationshierarkiet bestemmer, at med hensyn til lagringsdimensioner er det behovsordren, der har de obligatoriske dimensioner for websted, lagersted og lagerstatus, hvorimod lagerstedets logik er ansvarlig for at tildele en lokation til de ønskede antal og reserve lokationen.</span><span class="sxs-lookup"><span data-stu-id="9723f-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="9723f-110">I interaktionerne mellem behovsordren og lagerstedsoperationerne forventes det med andre ord, at behovsordren angiver, hvor ordren skal afsendes fra (dvs. hvilket sted og lagersted).</span><span class="sxs-lookup"><span data-stu-id="9723f-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="9723f-111">Lagerstedet er derefter afhængig af logikken for at finde det påkrævede antal på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="9723f-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="9723f-112">For at afspejle den operationelle model for virksomheden er sporingsdimensionerne (batch- og serienumre) dog underlagt større fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="9723f-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="9723f-113">Et lagerreservationshierarki kan tage højde for scenarier, hvor følgende betingelser gælder:</span><span class="sxs-lookup"><span data-stu-id="9723f-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="9723f-114">Virksomheden er afhængig af sin lagerdrift for at administrere plukning af antal, der har batch- eller serienumre, efter at antallene er fundet på lagerpladsen i lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="9723f-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="9723f-115">Denne model kaldes ofte *Batch-under\[lokation\]*.</span><span class="sxs-lookup"><span data-stu-id="9723f-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="9723f-116">Den bruges typisk, når et produkts batch- eller serienummeridentifikation ikke er vigtig for de kunder, der placerer efterspørgslen hos den sælgende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="9723f-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="9723f-117">Hvis batch- eller serienumre er en del af en kundes ordrespecifikation, og de registreres i behovsordren, er den lagerdrift, der finder antal på lagerstedet, begrænset af de specifikt ønskede numre, og de kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="9723f-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="9723f-118">Denne model kaldes ofte *Batch-over\[lokation\]*.</span><span class="sxs-lookup"><span data-stu-id="9723f-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="9723f-119">I disse scenarier er udfordringen, at der kun kan tildeles ét lagerreservationshierarki til hvert frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="9723f-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="9723f-120">For at WMS kan håndtere sporede varer, efter at hierarkitildelingen bestemmer, hvornår batch- eller serienummeret skal reserveres (enten når behovsordren udtages eller under pluk på lagerstedet), kan denne tidsindstilling ikke ændres på ad hoc-basis.</span><span class="sxs-lookup"><span data-stu-id="9723f-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="9723f-121">Fleksibel reservation for batchsporede varer</span><span class="sxs-lookup"><span data-stu-id="9723f-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="9723f-122">Forretningsscenarie</span><span class="sxs-lookup"><span data-stu-id="9723f-122">Business scenario</span></span>

<span data-ttu-id="9723f-123">I dette scenario bruger et firma en lagerstrategi, hvor færdigvarer spores efter batchnumre.</span><span class="sxs-lookup"><span data-stu-id="9723f-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="9723f-124">Dette firma bruger også WMS-arbejdsbyrden.</span><span class="sxs-lookup"><span data-stu-id="9723f-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="9723f-125">Da denne arbejdsbyrde har en veludviklet logik til planlægning og kørsel af lagerstedspluk- og forsendelsesoperationer for batchaktiverede varer, er de fleste af de færdige varer knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="9723f-126">Fordelen ved denne type driftsopsætning er, at beslutninger (der rent faktisk er reservationsbeslutninger) om, hvilke batches der skal plukkes, og hvor de skal placeres på lagerstedet, udskydes, indtil lagerstedsplukoperationerne er startet.</span><span class="sxs-lookup"><span data-stu-id="9723f-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="9723f-127">De foretages ikke, når kundeordren afgives.</span><span class="sxs-lookup"><span data-stu-id="9723f-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="9723f-128">Selvom reservationshierarkiet "Batch-under\[lokation\]" fungerer godt for firmaets forretningsmål, kræver mange af firmaets etablerede kunder samme batch, som de tidligere har købt, når de genbestiller produkter.</span><span class="sxs-lookup"><span data-stu-id="9723f-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="9723f-129">Derfor vil firmaet søge efter fleksibilitet i den måde, som reglerne for batchreservation håndteres på, så der sker følgende, afhængigt af kundernes behov for den samme vare:</span><span class="sxs-lookup"><span data-stu-id="9723f-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="9723f-130">Et batchnummer kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres under lagerdrift og/eller udtages af andre behov.</span><span class="sxs-lookup"><span data-stu-id="9723f-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="9723f-131">Denne funktionsmåde er en hjælp til at sikre, at det batchnummer, der blev bestilt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="9723f-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="9723f-132">Hvis batchnummeret ikke er vigtigt for kunden, kan lagerdriften bestemme et batchnummer under pluk, efter salgsordreregistrering og reservation er udført.</span><span class="sxs-lookup"><span data-stu-id="9723f-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="9723f-133">Tilladelse af reservation af en bestemt batch i salgsordren</span><span class="sxs-lookup"><span data-stu-id="9723f-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="9723f-134">For at give plads til den ønskede fleksibilitet i batchreservationens funktionsmåde for varer, der er knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]", skal lagerstyringen markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Batchnummer** på siden **Lagerreservationshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="9723f-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Angivelse af fleksibelt lagerreservationshierarki](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="9723f-136">Når niveauet **Batchnummer** i hierarkiet vælges, vil alle dimensioner over dette niveau og op gennem niveauet **Lokation** automatisk blive valgt.</span><span class="sxs-lookup"><span data-stu-id="9723f-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="9723f-137">(Som standard er alle dimensioner over niveauet **Lokation** niveauet forudvalgt). Denne funktionsmåde afspejler den logik, hvor alle dimensioner i intervallet mellem batchnummeret og lokationen også reserveres automatisk, når du reserverer et bestemt batchnummer på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9723f-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="9723f-138">Afkrydsningsfeltet **Tillad reservation i behovsordre** gælder kun for reservationshierarkiniveauer, der er ligger under lagerstedets lokationsdimension.</span><span class="sxs-lookup"><span data-stu-id="9723f-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="9723f-139">**Batchnummer** er det eneste niveau i hierarkiet, der er åbent for den fleksible reservationspolitik.</span><span class="sxs-lookup"><span data-stu-id="9723f-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="9723f-140">Du kan med andre ord ikke markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Lokation**, **Nummerplade** eller **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="9723f-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="9723f-141">Hvis reservationshierarkiet indeholder serienummerdimensionen (der altid skal være under niveauet **Batchnummer**), og hvis du har aktiveret batchspecifik reservation for batchnummeret, fortsætter systemet med at håndtere serienummerreservation og plukoperationer baseret på de regler, der gælder for reservationspolitikken "Serie-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="9723f-142">Du kan på et hvilket som helst tidspunkt tillade batchspecifik reservation for et eksisterende reservationshierarki af typen "Batch-under\[lokation\]" i din installation.</span><span class="sxs-lookup"><span data-stu-id="9723f-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="9723f-143">Denne ændring påvirker ikke reservationer og åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="9723f-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="9723f-144">Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes lagertransaktioner af afgangstypen **Reserveret bestilt**, **Reserveret fysisk** eller **Bestilt** for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.</span><span class="sxs-lookup"><span data-stu-id="9723f-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="9723f-145">Hvis en vares eksisterende reservationshierarki ikke tillader batchspecifikation i ordren, kan du igen tildele det til et reservationshierarki, der tillader batchspecifikation, forudsat at strukturen i hierarkiniveauet er den samme i begge hierarkier.</span><span class="sxs-lookup"><span data-stu-id="9723f-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="9723f-146">Brug funktionen **Skift reservationshierarki til varer** til at udføre omfordelingen.</span><span class="sxs-lookup"><span data-stu-id="9723f-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="9723f-147">Denne ændring kan være relevant, når du vil forhindre fleksibel batchreservation af et undersæt af batchsporede varer, men tillade den for resten af produktsortimentet.</span><span class="sxs-lookup"><span data-stu-id="9723f-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="9723f-148">Hvis du ikke vil reservere et bestemt batchnummer for varen på en ordrelinje, så gælder standardlogikken for lagerdrift, der er gældende for et reservationshierarki af typen "Batch-under\[lokation\]", stadig, uanset om du har markeret afkrydsningsfeltet **Tillad reservation i behovsordre**.</span><span class="sxs-lookup"><span data-stu-id="9723f-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="9723f-149">Reservere et bestemt batchnummer til en kundeordre</span><span class="sxs-lookup"><span data-stu-id="9723f-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="9723f-150">Efter en batchsporet vares lagerreservationshierarki af typen "Batch-under\[lokation\]" er konfigureret til at tillade reservation af bestemte batchnumre i salgsordrer, kan salgsordrebehandlere udtage kundeordrer på samme vare på en af følgende måder afhængigt af kundens anmodning:</span><span class="sxs-lookup"><span data-stu-id="9723f-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="9723f-151">**Angiv ordredetaljer uden at angive et batchnummer** – denne tilgang skal bruges, når produktets batchspecifikation ikke er vigtig for kunden.</span><span class="sxs-lookup"><span data-stu-id="9723f-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="9723f-152">Alle eksisterende processer, der er knyttet til håndtering af en ordre af denne type i systemet, ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="9723f-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="9723f-153">Der kræves ingen yderligere overvejelser fra brugernes side.</span><span class="sxs-lookup"><span data-stu-id="9723f-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="9723f-154">**Angiv ordredetaljer, og reservér et bestemt batchnummer** – denne tilgang skal bruges, når kunden anmoder om en bestemt batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="9723f-155">Kunderne anmoder typisk om en bestemt batch, når de genbestiller et produkt, som de tidligere har købt.</span><span class="sxs-lookup"><span data-stu-id="9723f-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="9723f-156">Denne type batchspecifik reservation er en såkaldt *ordrebekræftet reservation*.</span><span class="sxs-lookup"><span data-stu-id="9723f-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="9723f-157">Følgende regelsæt er gældende, når antal behandles, og et batchnummer bekræftes for en bestemt ordre:</span><span class="sxs-lookup"><span data-stu-id="9723f-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="9723f-158">Hvis der skal kunne foretages reservation af et bestemt batchnummer for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet reservere alle dimensioner til og med lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="9723f-159">Dette område omfatter typisk id-dimensionen.</span><span class="sxs-lookup"><span data-stu-id="9723f-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="9723f-160">Lokationsvejledninger bruges ikke, når der oprettes plukarbejde for en salgslinje, hvor der bruges ordrebekræftet batchreservation.</span><span class="sxs-lookup"><span data-stu-id="9723f-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="9723f-161">Hverken brugeren eller systemet må ændre batchnummeret under lagerstedsbehandling af arbejde for ordrebekræftede batches.</span><span class="sxs-lookup"><span data-stu-id="9723f-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="9723f-162">(Denne behandling omfatter undtagelseshåndtering).</span><span class="sxs-lookup"><span data-stu-id="9723f-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="9723f-163">I følgende eksempel vises slutpunkt-til-slutpunkt-flowet.</span><span class="sxs-lookup"><span data-stu-id="9723f-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9723f-164">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="9723f-164">Example scenario</span></span>

<span data-ttu-id="9723f-165">I dette eksempel skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9723f-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="9723f-166">Opret et lagerreservationshierarki for at tillade batchspecifik reservation</span><span class="sxs-lookup"><span data-stu-id="9723f-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="9723f-167">Gå til **Lokationsstyring** \> **Opsætning** \> **Lager \> Reservationshierarki**.</span><span class="sxs-lookup"><span data-stu-id="9723f-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="9723f-168">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9723f-168">Select **New**.</span></span>
3. <span data-ttu-id="9723f-169">Angiv et navn i feltet **Navn** (f.eks. **Batchfleks**).</span><span class="sxs-lookup"><span data-stu-id="9723f-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="9723f-170">Indtast en beskrivelse i feltet **Beskrivelse** (f.eks. **Batch under fleksibel**).</span><span class="sxs-lookup"><span data-stu-id="9723f-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="9723f-171">I feltet **Valgt** skal du vælge **Serienummer** og **Ejer** og derefter vælge den venstre pileknap for at flytte dem til feltet **Tilgængelig**.</span><span class="sxs-lookup"><span data-stu-id="9723f-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="9723f-172">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9723f-172">Select **OK**.</span></span>
7. <span data-ttu-id="9723f-173">I rækken med dimensionsniveau for **Batchnummer** skal du markere afkrydsningsfeltet **Tillad reservation i behovsordre**.</span><span class="sxs-lookup"><span data-stu-id="9723f-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="9723f-174">Niveauerne **Nummerplade** og **Lokation** vælges automatisk, og du kan ikke fjerne markeringerne i afkrydsningsfelterne for dem.</span><span class="sxs-lookup"><span data-stu-id="9723f-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="9723f-175">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9723f-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="9723f-176">Opret et nyt frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="9723f-176">Create a new released product</span></span>

1. <span data-ttu-id="9723f-177">Angiv produktets tre masterdataparametre ved hjælp af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="9723f-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="9723f-178">Vælg **Artikler** i feltet **Lagringsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9723f-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="9723f-179">Vælg **Batch-fy** i feltet **Sporingsdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9723f-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="9723f-180">I feltet **Reservationshierarki** skal du vælge **Batchfleks**.</span><span class="sxs-lookup"><span data-stu-id="9723f-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="9723f-181">Opret to batchnumre f.eks. **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="9723f-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="9723f-182">Føj vareantal til disponibel lagerbeholdning ved hjælp af følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="9723f-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="9723f-183">Lagersted</span><span class="sxs-lookup"><span data-stu-id="9723f-183">Warehouse</span></span> | <span data-ttu-id="9723f-184">Batchnummer</span><span class="sxs-lookup"><span data-stu-id="9723f-184">Batch number</span></span> | <span data-ttu-id="9723f-185">Adresse</span><span class="sxs-lookup"><span data-stu-id="9723f-185">Location</span></span> | <span data-ttu-id="9723f-186">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="9723f-186">License plate</span></span> | <span data-ttu-id="9723f-187">Mængde</span><span class="sxs-lookup"><span data-stu-id="9723f-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="9723f-188">24</span><span class="sxs-lookup"><span data-stu-id="9723f-188">24</span></span>        | <span data-ttu-id="9723f-189">B11</span><span class="sxs-lookup"><span data-stu-id="9723f-189">B11</span></span>          | <span data-ttu-id="9723f-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="9723f-190">BULK-001</span></span> | <span data-ttu-id="9723f-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="9723f-191">None</span></span>          | <span data-ttu-id="9723f-192">10</span><span class="sxs-lookup"><span data-stu-id="9723f-192">10</span></span>       |
    | <span data-ttu-id="9723f-193">24</span><span class="sxs-lookup"><span data-stu-id="9723f-193">24</span></span>        | <span data-ttu-id="9723f-194">B11</span><span class="sxs-lookup"><span data-stu-id="9723f-194">B11</span></span>          | <span data-ttu-id="9723f-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="9723f-195">FL-001</span></span>   | <span data-ttu-id="9723f-196">LP11</span><span class="sxs-lookup"><span data-stu-id="9723f-196">LP11</span></span>          | <span data-ttu-id="9723f-197">10</span><span class="sxs-lookup"><span data-stu-id="9723f-197">10</span></span>       |
    | <span data-ttu-id="9723f-198">24</span><span class="sxs-lookup"><span data-stu-id="9723f-198">24</span></span>        | <span data-ttu-id="9723f-199">B22</span><span class="sxs-lookup"><span data-stu-id="9723f-199">B22</span></span>          | <span data-ttu-id="9723f-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="9723f-200">FL-002</span></span>   | <span data-ttu-id="9723f-201">LP22</span><span class="sxs-lookup"><span data-stu-id="9723f-201">LP22</span></span>          | <span data-ttu-id="9723f-202">10</span><span class="sxs-lookup"><span data-stu-id="9723f-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="9723f-203">Indtast oplysninger om salgsordrer</span><span class="sxs-lookup"><span data-stu-id="9723f-203">Enter sales order details</span></span>

1. <span data-ttu-id="9723f-204">Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9723f-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="9723f-205">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9723f-205">Select **New**.</span></span>
3. <span data-ttu-id="9723f-206">Angiv **US-003** i feltet **Debitorkonto** i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="9723f-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="9723f-207">Tilføj en linje for den nye vare, og angiv **10** som antal.</span><span class="sxs-lookup"><span data-stu-id="9723f-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="9723f-208">Sørg for, at feltet **Lagersted** er angivet til **24**.</span><span class="sxs-lookup"><span data-stu-id="9723f-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="9723f-209">Vælg **Lager** i oversigtspanelet **Salgsordrelinjer**, og vælg derefter **Batchreservation** i gruppen **Vedligehold**.</span><span class="sxs-lookup"><span data-stu-id="9723f-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="9723f-210">På siden **Batchreservation** vises en liste over batches, der er tilgængelige til reservation for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9723f-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="9723f-211">I dette eksempel vises antallet **20** for batchnummer **B11** og antallet **10** for batchnummer **B22**.</span><span class="sxs-lookup"><span data-stu-id="9723f-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="9723f-212">Bemærk, at der ikke kan opnås adgang til siden **Batchreservation** fra en linje, hvis varen på linjen er tilknyttet reservationshierarkiet "Batch-under\[lokation\]", medmindre den er konfigureret til at tillade batchspecifik reservation.</span><span class="sxs-lookup"><span data-stu-id="9723f-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9723f-213">Hvis du vil reservere et bestemt batch til en salgsordre, skal du bruge siden **Batchreservation**.</span><span class="sxs-lookup"><span data-stu-id="9723f-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="9723f-214">Hvis du angiver batchnummeret direkte på salgsordrelinjen, fungerer systemet, som om du har angivet en bestemt batchværdi for en vare, der er underlagt reservationspolitikken "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="9723f-215">Når du gemmer linjen, vil du modtage en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="9723f-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="9723f-216">Hvis du bekræfter, at batchnummeret skal angives direkte på ordrelinjen, håndteres linjen ikke af den almindelige lokationsstyringslogik.</span><span class="sxs-lookup"><span data-stu-id="9723f-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="9723f-217">Hvis du reserverer antallet fra siden **Reservation**, reserveres der ikke noget bestemt batch, og udførelsen af lagerdrift for linjen følger de regler, der gælder i henhold til reservationspolitikken "Batch-under\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="9723f-218">Generelt er funktionen og interaktionen med denne side meget lig den måde, der arbejdes og interageres med varer, som har et tilknyttet reservationshierarki af typen "Batch-over\[lokation\]".</span><span class="sxs-lookup"><span data-stu-id="9723f-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="9723f-219">Der gælder dog følgende undtagelser:</span><span class="sxs-lookup"><span data-stu-id="9723f-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="9723f-220">Oversigtspanelet **Batchnumre bundet til kildelinje** viser de batchnumre, der er reserveret til ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9723f-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="9723f-221">Batchværdierne i gitteret vises under hele udførelsescyklussen for ordrelinjen, herunder lagerstedets behandlingsstadier.</span><span class="sxs-lookup"><span data-stu-id="9723f-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="9723f-222">Derimod vises der i oversigtspanelet **Oversigt** en almindelig ordrelinjereservation (dvs. reservation, der udføres for dimensionerne over niveauet **Lokation**) i gitteret op til det punkt, hvor der oprettes lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="9723f-223">Arbejdsenheden overtager derefter linjereservationen, og linjereservationen vises ikke længere på siden.</span><span class="sxs-lookup"><span data-stu-id="9723f-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="9723f-224">Oversigtspanelet **Batchnumre bundet til kildelinje** sikrer, at salgsordrebehandleren kan få vist de batchnumre, der er bundet til kundens ordre på et tidspunkt i løbet livscyklussen op til og med fakturering.</span><span class="sxs-lookup"><span data-stu-id="9723f-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="9723f-225">Ud over at reservere en bestemt batch kan en bruger manuelt vælge batchens specifikke lokation og id i stedet for at lade systemet vælge dem automatisk.</span><span class="sxs-lookup"><span data-stu-id="9723f-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="9723f-226">Denne funktion er relateret til designet af den ordrebekræftede batchreservationsmekanisme.</span><span class="sxs-lookup"><span data-stu-id="9723f-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="9723f-227">Når et batchnummer reserveres for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet som tidligere nævnt reservere alle dimensioner til og med lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="9723f-228">Lagerstedsarbejdet vil derfor indeholde de samme lagringsdimensioner, der blev reserveret af de brugere, der har arbejdet med ordrerne, og de repræsenterer muligvis ikke altid den varelagringsplacering, der er praktisk eller endda mulig for plukoperationer.</span><span class="sxs-lookup"><span data-stu-id="9723f-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="9723f-229">Hvis ordrebehandlere er opmærksomme på lagerbegrænsningerne, kan det være en god ide manuelt at vælge de specifikke lokationer og id'er, når de reserverer en batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="9723f-230">I dette tilfælde skal brugeren bruge funktionen **Vis dimensioner** i sidehovedet og tilføje lokationen og id'et i gitteret i oversigtspanelet **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="9723f-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="9723f-231">På siden **Batchreservation** skal du vælge linjen for batch **B11** og derefter vælge **Reserver linje**.</span><span class="sxs-lookup"><span data-stu-id="9723f-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="9723f-232">Der er ingen foruddefineret logik ved tildeling af lokationer og id'er under automatisk reservation.</span><span class="sxs-lookup"><span data-stu-id="9723f-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="9723f-233">Du kan angive antallet manuelt i feltet **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="9723f-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="9723f-234">Bemærk, at oversigtspanelet **Batchnumre bundet til kildelinje**, batch **B11** er vist som **Bindende**.</span><span class="sxs-lookup"><span data-stu-id="9723f-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tilknytning af et bestemt batchnummer til en salgsordrelinje på siden Batchreservation](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="9723f-236">Reservation af antallet i en salgsordrelinje kan udføres på tværs af flere batches.</span><span class="sxs-lookup"><span data-stu-id="9723f-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="9723f-237">På samme måde kan reservation af samme batch udføres mod flere lokationer og id'er (hvis der er aktiveret id'er for lokationerne).</span><span class="sxs-lookup"><span data-stu-id="9723f-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="9723f-238">Reservation af en bestemt batch for antallet på en salgsordrelinje kan også være delvis.</span><span class="sxs-lookup"><span data-stu-id="9723f-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="9723f-239">Det samlede antal på 100 enheder kan f.eks. reserveres, så en bestemt batch bekræftes til 20 enheder, hvorimod 80 enheder er reserveret på lokations- og lagerstedsniveauer for alle tilgængelige batches.</span><span class="sxs-lookup"><span data-stu-id="9723f-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="9723f-240">I dette tilfælde vil WMS håndtere plukoperationer ved hjælp af to separate arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="9723f-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="9723f-241">Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="9723f-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="9723f-242">Vælg din vare, og vælg derefter **Styr lager** \> **Vis** \> **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9723f-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Ordrebekræftet reservation som en lagertransaktionstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="9723f-244">Gennemse varens lagertransaktioner, der er relateret til reservationen af salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9723f-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="9723f-245">En transaktion, hvor feltet **Reference** er angivet til **Salgsordre**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="9723f-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="9723f-246">Ifølge varens lagerreservationshierarki er disse dimensioner lokation, lagersted og lagerstatus.</span><span class="sxs-lookup"><span data-stu-id="9723f-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="9723f-247">En transaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for den specifikke batch og alle lagerdimensionerne over den.</span><span class="sxs-lookup"><span data-stu-id="9723f-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="9723f-248">Ifølge varens lagerreservationshierarki er disse dimensioner batchnummer og lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="9723f-249">I dette eksempel er lokationen **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="9723f-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="9723f-250">Vælg **Lagersted** \> **Handlinger** \> **Frigiv til lagersted** i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="9723f-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="9723f-251">Ordrelinjen er nu i bølge, og der oprettes en belastning og et arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="9723f-252">Gennemse og behandl lagerstedsarbejde, der har ordrebekræftede batchnumre</span><span class="sxs-lookup"><span data-stu-id="9723f-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="9723f-253">I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted** \> **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9723f-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="9723f-254">Det arbejde, der håndterer plukoperationen for batchantal, der er bundet til salgsordrelinjen, har følgende karakteristika:</span><span class="sxs-lookup"><span data-stu-id="9723f-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="9723f-255">For at kunne oprette arbejde bruger systemet arbejdsskabeloner, men ikke lokationsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="9723f-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="9723f-256">Alle de standardindstillinger, der er defineret for arbejdsskabeloner, f.eks. det maksimale antal pluklinjer eller en bestemt måleenhed, vil blive anvendt til at bestemme, hvornår der skal oprettes nyt arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="9723f-257">De regler, der er knyttet til lokationsvejledninger til identifikation af pluklokationer, tages dog ikke i betragtning, fordi den ordrebekræftede reservation allerede angiver alle lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="9723f-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="9723f-258">Disse lagerdimensioner omfatter dimensionerne på lagerstedets lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="9723f-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="9723f-259">Derfor arver arbejdet disse dimensioner, uden at lokationsvejledninger skal benyttes.</span><span class="sxs-lookup"><span data-stu-id="9723f-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="9723f-260">Batchnummeret vises ikke på pluklinjen (som det er tilfældet for den arbejdslinje, der er oprettet for en vare, der har et tilknyttet reservationshierarki for "Batch-over\[lokation\]"). I stedet vises batchnummeret "fra" og alle andre lagringsdimensioner i arbejdslinjens lagertransaktion, der refereres til fra de tilknyttede lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="9723f-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Lagersteds lagertransaktion for arbejde, der stammer fra ordrebekræftet reservation](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="9723f-262">Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**.</span><span class="sxs-lookup"><span data-stu-id="9723f-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="9723f-263">Lagertransaktionen, hvor feltet **Reference** er angivet til **Arbejde**, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.</span><span class="sxs-lookup"><span data-stu-id="9723f-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="9723f-264">Lagerdrift kan fortsætte med at håndtere udførelsen af arbejdet på sædvanlig vis.</span><span class="sxs-lookup"><span data-stu-id="9723f-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="9723f-265">Vejledningen på mobilenheden giver dog arbejderen besked på at vælge et bestemt batchnummer.</span><span class="sxs-lookup"><span data-stu-id="9723f-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="9723f-266">I lagermiljøer med id-styrede lokationer kan en arbejder, når vedkommende når en lokation, der gemmer samme batch med flere id'er, plukke fra et hvilket som helst id, der ikke allerede er reserveret (f.eks. af en anden ordrebekræftet reservation eller arbejde, der stammer fra en reservation af den pågældende type).</span><span class="sxs-lookup"><span data-stu-id="9723f-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="9723f-267">Hvis det bliver for upraktisk at plukke fra den lokation, der er angivet på arbejdslinjen, kan lageroperatøren bruge en af følgende handlinger til at omdirigere plukning af den specifikke batch fra en mere praktisk lokation:</span><span class="sxs-lookup"><span data-stu-id="9723f-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="9723f-268">Standardhandlingen **Tilsidesæt lokation** på en mobilenhed (hvis lagermedarbejderens indstilling **Tillad tilsidesættelse af pluklokation** er aktiveret)</span><span class="sxs-lookup"><span data-stu-id="9723f-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="9723f-269">Handlingen **Skift lokation** på siden **Arbejdslistedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9723f-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="9723f-270">Udfør plukning og placering af arbejdet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="9723f-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="9723f-271">Antallet **10** for batchnummer **B11** plukkes nu for salgsordrelinjen og placeres på lokationen **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="9723f-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="9723f-272">På dette tidspunkt er det klar til at blive læsset på lastbilen og sendt til kundens adresse.</span><span class="sxs-lookup"><span data-stu-id="9723f-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="9723f-273">Undtagelseshåndtering af lagerstedsarbejde, der har ordrebekræftede batchnumre</span><span class="sxs-lookup"><span data-stu-id="9723f-273">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="9723f-274">Lagerstedsarbejde for plukning af ordrebekræftede batchnumre er underlagt samme standardhåndtering af undtagelser for lagersted og handlinger som almindeligt arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="9723f-275">Generelt kan det åbne arbejde eller den åbne arbejdslinje annulleres, den kan afbrydes, fordi en brugerlokation er fuld, den kan være kort plukket, og den kan opdateres på grund af en bevægelse.</span><span class="sxs-lookup"><span data-stu-id="9723f-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="9723f-276">På samme måde kan den plukkede mængde arbejde, der allerede er udført, reduceres, eller arbejdet kan tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="9723f-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="9723f-277">Følgende nøgleregel anvendes til alle disse handlinger af typen undtagelseshåndtering: Det batchnummer, der er reserveret til kunden, kan aldrig erstattes med et andet batchnummer, men lagerdimensionerne (lokation og id) kan ændres via enten en manuel opdatering fra brugerens side eller en automatisk opdatering udført af systemet.</span><span class="sxs-lookup"><span data-stu-id="9723f-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="9723f-278">Den automatiske opdatering er baseret på den samme tilfældige tildeling af lagringsdimensioner, der anvendes, når en bestemt batch blev reserveret automatisk, men der ikke blev angivet nogen lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="9723f-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="9723f-279">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="9723f-279">Example scenario</span></span>

<span data-ttu-id="9723f-280">Et eksempel på dette scenario er en situation, hvor tidligere udført arbejde ikke kan plukkes ved hjælp af funktionen **Reducer det antal, der er plukket**.</span><span class="sxs-lookup"><span data-stu-id="9723f-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="9723f-281">I dette eksempel fortsættes det foregående eksempel i dette emne.</span><span class="sxs-lookup"><span data-stu-id="9723f-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="9723f-282">Gå til **Lokationsstyring** \> **Laster** \> **Aktive laster**.</span><span class="sxs-lookup"><span data-stu-id="9723f-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="9723f-283">Vælg den last, der blev oprettet i forbindelse med forsendelsen af salgsordren.</span><span class="sxs-lookup"><span data-stu-id="9723f-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="9723f-284">Vælg **Reducer det antal, der er plukket** i oversigtspanelet **Indlæs ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="9723f-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="9723f-285">Vælg **FL-001** i feltet **Flyt til lokation** på siden **Reducer det antal, der er plukket**.</span><span class="sxs-lookup"><span data-stu-id="9723f-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="9723f-286">Vælg **LP33** i feltet **Flyt til nummerplade**.</span><span class="sxs-lookup"><span data-stu-id="9723f-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="9723f-287">Angiv **10** i feltet **Lagerantal, hvor plukning skal fortrydes**.</span><span class="sxs-lookup"><span data-stu-id="9723f-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="9723f-288">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9723f-288">Select **OK**.</span></span>

<span data-ttu-id="9723f-289">Følgende er resultatet af handlingen til fortrydelse af plukning:</span><span class="sxs-lookup"><span data-stu-id="9723f-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="9723f-290">Status for det tidligere lukkede arbejde angives til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="9723f-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="9723f-291">Der oprettes nyt arbejde af typen **Lagerbevægelser** for det ikke-plukkede antal på **10** for batchnummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="9723f-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="9723f-292">Dette arbejde repræsenterer bevægelsen fra lokationen **Baydoor** til id **LP33** på lokation **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="9723f-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="9723f-293">Status er angivet til **Lukket**.</span><span class="sxs-lookup"><span data-stu-id="9723f-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="9723f-294">Systemet reserverer igen det batchnummer, der oprindeligt blev bestilt, og tildeler lokation og id'er.</span><span class="sxs-lookup"><span data-stu-id="9723f-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="9723f-295">(Denne proces svarer til at køre funktionen **Reserver linje** for ordrelinjen for et bestemt batchnummer).</span><span class="sxs-lookup"><span data-stu-id="9723f-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="9723f-296">Derfor vises **B11** som bekræftet i oversigtspanelet **Batchnumre bundet til kildelinje** på siden **Batchreservation**, og feltet **Reservation** indeholder antallet **10** for batchnummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="9723f-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="9723f-297">Desuden angives feltet **Lokation** til **FL-001**, og feltet **Nummerplade** angives til **LP11**.</span><span class="sxs-lookup"><span data-stu-id="9723f-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="9723f-298">(Du kan føje disse felter til gitteret, hvis de ikke er synlige).</span><span class="sxs-lookup"><span data-stu-id="9723f-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="9723f-299">Følgende tabeller indeholder en oversigt, der viser, hvordan systemet håndterer ordrebekræftet batchreservation for specifikke lagerstedshandlinger.</span><span class="sxs-lookup"><span data-stu-id="9723f-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="9723f-300">Hvis du vil fortolke indholdet i tabellerne, skal du antage, at hver lagerstedshandling køres i konteksten af det eksisterende lagerarbejde, der stammer fra en ordrebekræftet batchreservation, eller at udførelsen af de enkelte lagerhandlinger påvirker arbejde af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="9723f-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="9723f-301">I disse tabeller angiver kolonnen "Batchantal er tilgængeligt", om der findes et tilgængeligt batchantal ud over det antal, der enten allerede er reserveret for de aktuelle ordrebekræftede reservationer, eller som allerede er reserveret af det lagerstedsarbejde, der stammer fra reservationer af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="9723f-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="9723f-302">Tilsidesæt pluklokationen for det åbne arbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-303">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-304">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-305">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-305">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-306">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-306">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-307">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-308">Indstillingen <strong>Tillad tilsidesættelse af pluklokation</strong> er aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9723f-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9723f-309">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-310">Vælg menupunktet <strong>Tilsidesæt lokation</strong> på lagerstedsappen, når du starter pluk af arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-310">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="9723f-311">Vælg <strong>Foreslå</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="9723f-312">Bekræft den nye lokation, der foreslås, på basis af tilgængeligheden af batchantal.</span><span class="sxs-lookup"><span data-stu-id="9723f-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-313">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="9723f-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9723f-314">Lokationen på pluklinjen opdateres til den nye lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="9723f-315">(Hvis lokaliteten er id-styret, tildeles et tilfældigt id til lagerbeholdningstransaktionen, og arbejderen kan plukke fra et hvilken som helst id, der har tilgængeligt antal).</span><span class="sxs-lookup"><span data-stu-id="9723f-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="9723f-316">Hvis antallet findes på mere end ét id på den nye lokation, opdeles den oprindelige pluklinje i flere linjer, så den svarer til hvert enkelt id.</span><span class="sxs-lookup"><span data-stu-id="9723f-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-317">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-318">Ingen</span><span class="sxs-lookup"><span data-stu-id="9723f-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-319">Vælg menupunktet <strong>Tilsidesæt lokation</strong> på lagerstedsappen, når du starter pluk af arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-319">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="9723f-320">Angiv en lokation manuelt.</span><span class="sxs-lookup"><span data-stu-id="9723f-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-321">Handlingen <strong>Tilsidesæt lokation</strong> er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="9723f-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="9723f-322">Det mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="9723f-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="9723f-323">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="9723f-324">Knappen Fuld – opdel en arbejdslinje på grund af overløb på brugerens lokation</span><span class="sxs-lookup"><span data-stu-id="9723f-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-325">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-326">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-327">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-327">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-328">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-328">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-329">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9723f-330">Indstillingen <strong>Tillad opdeling af arbejde</strong> er aktiveret for menupunktet mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="9723f-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="9723f-331">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-332">Vælg menupunktet <strong>Fuld</strong> på lagerstedsapp, når du behandler plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-332">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="9723f-333">I feltet <strong>Plukantal</strong> skal du angive en del af antallet af det krævede pluk for at angive den fulde kapacitet.</span><span class="sxs-lookup"><span data-stu-id="9723f-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-334">I det aktuelle arbejde opdateres antallet med det resterende antal, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="9723f-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="9723f-335">Nyt arbejde for det plukkede antal oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="9723f-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="9723f-336">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="9723f-337">Reducer det plukkede antal af fuldført arbejde (fra en last)</span><span class="sxs-lookup"><span data-stu-id="9723f-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-338">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-339">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-340">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-340">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-341">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-341">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-342">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-343">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-343">Not applicable</span></span></td>
<td><span data-ttu-id="9723f-344">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-345">Åbn siden <strong>Reducer det antal, der er plukket</strong> antal fra lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="9723f-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="9723f-346">Angiv hele antallet, plukning skal fortrydes for.</span><span class="sxs-lookup"><span data-stu-id="9723f-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="9723f-347">Vælg en "flyt til"-lokation/id.</span><span class="sxs-lookup"><span data-stu-id="9723f-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="9723f-348">Arbejde, der er tilknyttet lastlinjen, annulleres.</span><span class="sxs-lookup"><span data-stu-id="9723f-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="9723f-349">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="9723f-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-350">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-351">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-352">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-352">No</span></span></td>
<td><span data-ttu-id="9723f-353">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-353">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-354">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-354">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-355">Antallet reserveres igen for samme batch og for samme lokation og id (hvis lokationen er id-styret), der blev angivet under annullering af pluk.</span><span class="sxs-lookup"><span data-stu-id="9723f-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="9723f-356">Flyt en vare inden for et lagersted</span><span class="sxs-lookup"><span data-stu-id="9723f-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="9723f-357">Denne lagerstedshandling gælder kun for flytning af typen **Arbejdsoprettelsesproces**, ikke for bevægelse efter skabelon.</span><span class="sxs-lookup"><span data-stu-id="9723f-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-358">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-359">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-360">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-360">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-361">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-361">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-362">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-363">Indstillingen <strong>Tillad flytning af lager med tilknyttet arbejde</strong> er aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9723f-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9723f-364">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-365">Start en bevægelse på lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="9723f-365">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="9723f-366">Angiv "fra"- og "til"-lokationer.</span><span class="sxs-lookup"><span data-stu-id="9723f-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="9723f-367">I alt eksisterende arbejde, der påvirkes af flytningen, opdateres plukpladsen til den nye "til"-lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="9723f-368">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="9723f-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-369">Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-370">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-371">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-371">No</span></span></td>
<td><span data-ttu-id="9723f-372">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-372">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-373">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-373">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-374">Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for den samme batch og for den nye "til"-lokation og det nye id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="9723f-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="9723f-375">Tilbagefør det plukkede antal af fuldført arbejde (fra en belastning eller en bølge)</span><span class="sxs-lookup"><span data-stu-id="9723f-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-376">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-377">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-378">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-378">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-379">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-379">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-380">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="9723f-381">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-381">Not applicable</span></span></td>
<td><span data-ttu-id="9723f-382">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-383">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9723f-384">Vælg indstillingen <strong>Efterlad varer på aktuel lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="9723f-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-385">Alt arbejde, der er tilknyttet lasten, annulleres.</span><span class="sxs-lookup"><span data-stu-id="9723f-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="9723f-386">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-387">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-388">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-388">No</span></span></td>
<td><span data-ttu-id="9723f-389">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-389">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-390">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-390">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-391">Antallet reserveres igen for den samme batch og for den lokation og det id, hvor antallet blev placeret ved tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="9723f-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-392">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-393">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9723f-394">Vælg indstillingen <strong>Tildel varer til denne lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="9723f-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-395">Det aktuelle arbejde er annulleret.</span><span class="sxs-lookup"><span data-stu-id="9723f-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="9723f-396">Nyt arbejde for lagerbevægelsen oprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="9723f-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-397">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-398">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-399">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-399">No</span></span></td>
<td><span data-ttu-id="9723f-400">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-400">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-401">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-401">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-402">Antallet reserveres igen for den samme batch og for den lokation og det id, som antallet blev tildelt ved tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="9723f-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-403">Ja/nej</span><span class="sxs-lookup"><span data-stu-id="9723f-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-404">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9723f-405">Vælg indstillingen <strong>Flyt varer til denne lokation</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="9723f-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-406">Tilbageførsel understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="9723f-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="9723f-407">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-408">Ja/nej</span><span class="sxs-lookup"><span data-stu-id="9723f-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-409">Åbn siden <strong>Tilbagefør arbejde</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9723f-410">Vælg indstillingen <strong>Flyt varer på basis af lokationsvejledninger</strong> på siden med anmodning.</span><span class="sxs-lookup"><span data-stu-id="9723f-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-411">Tilbageførsel understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="9723f-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="9723f-412">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="9723f-413">Kort pluk et antal – Registrer antallet som fysisk ikke fundet ved lokationen/id'et, når du udfører plukarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-414">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-415">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-416">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-416">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-417">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-417">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-418">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-419">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="9723f-420">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-421">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-421">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-422">Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-423">I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-424">Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9723f-425">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="9723f-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-426">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-427">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-428">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-428">No</span></span></td>
<td><span data-ttu-id="9723f-429">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9723f-430">Handlingen kort pluk mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="9723f-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="9723f-431">Det aktuelle arbejde forbliver åbent.</span><span class="sxs-lookup"><span data-stu-id="9723f-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-432">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-433">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="9723f-434">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-435">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-435">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-436">Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-437">I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-438">Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9723f-439">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="9723f-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-440">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-441">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-442">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-442">No</span></span></td>
<td><span data-ttu-id="9723f-443">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-443">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-444">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-444">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-445">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, fjernes.</span><span class="sxs-lookup"><span data-stu-id="9723f-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-446">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej/Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="9723f-447">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9723f-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9723f-448">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-449">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-449">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-450">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-451">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="9723f-452">Vælg lokationen/id'et på listen.</span><span class="sxs-lookup"><span data-stu-id="9723f-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-453">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="9723f-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9723f-454">Pluklinjen er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9723f-455">Læg på lager-linjen annulleres.</span><span class="sxs-lookup"><span data-stu-id="9723f-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="9723f-456">Der oprettes en ny pluklinje.</span><span class="sxs-lookup"><span data-stu-id="9723f-456">A new pick line is created.</span></span> <span data-ttu-id="9723f-457">Den bruger den lokation/det ud, som brugeren har valgt.</span><span class="sxs-lookup"><span data-stu-id="9723f-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="9723f-458">Der oprettes en ny læg på lager-linje.</span><span class="sxs-lookup"><span data-stu-id="9723f-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9723f-459">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="9723f-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-460">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-461">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="9723f-462">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9723f-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9723f-463">Ingen</span><span class="sxs-lookup"><span data-stu-id="9723f-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-464">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-464">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-465">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-466">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-467">Handlingen kort pluk mislykkes, og der udløses en fejl.</span><span class="sxs-lookup"><span data-stu-id="9723f-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="9723f-468">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-469">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="9723f-470">Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9723f-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9723f-471">Ingen</span><span class="sxs-lookup"><span data-stu-id="9723f-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-472">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-472">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-473">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-474">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="9723f-475">Vælg lokationen/id'et på listen.</span><span class="sxs-lookup"><span data-stu-id="9723f-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9723f-476">Følgende handlinger finder sted i det aktuelle arbejde:</span><span class="sxs-lookup"><span data-stu-id="9723f-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9723f-477">Pluklinjen er lukket, og det plukkede antal er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9723f-478">Læg på lager-linjen annulleres.</span><span class="sxs-lookup"><span data-stu-id="9723f-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9723f-479">Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="9723f-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9723f-480">Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation/id, fjernes.</span><span class="sxs-lookup"><span data-stu-id="9723f-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-481">En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Automatisk</strong>, <strong>Reguler lager</strong> = <strong>Ja/Nej</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja/Nej</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="9723f-482">Ikke relevant</span><span class="sxs-lookup"><span data-stu-id="9723f-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-483">Vælg menupunktet <strong>Kort pluk</strong> på lagerstedsappen, når du kører plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-483">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="9723f-484">Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</span><span class="sxs-lookup"><span data-stu-id="9723f-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9723f-485">I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med automatisk omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-486">Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="9723f-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="9723f-487">Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="9723f-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="9723f-488">Skift status for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="9723f-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="9723f-489">Lagerstedshandlingen kan udføres fra flere indgangspunkter.</span><span class="sxs-lookup"><span data-stu-id="9723f-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="9723f-490">Det eksempel, der vises her, bruger handlingen **Ændring af lagerstatus** på siden **Disponibel efter lokation**.</span><span class="sxs-lookup"><span data-stu-id="9723f-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9723f-491">Vigtig opsætningsparameter</span><span class="sxs-lookup"><span data-stu-id="9723f-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="9723f-492">Batchantal er tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="9723f-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9723f-493">Vigtige brugertrin</span><span class="sxs-lookup"><span data-stu-id="9723f-493">Key user steps</span></span></th>
<th><span data-ttu-id="9723f-494">Lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="9723f-494">Warehouse work</span></span></th>
<th><span data-ttu-id="9723f-495">Ordrebekræftet batchreservation</span><span class="sxs-lookup"><span data-stu-id="9723f-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-496">Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Reservationer</strong> eller <strong>Afmærkninger og reservationer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="9723f-497">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-498">Vælg en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="9723f-499">Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="9723f-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="9723f-500">Vælg <strong>Ændring af lagerstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="9723f-501">Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-502">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9723f-503">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-504">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="9723f-505">To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</span><span class="sxs-lookup"><span data-stu-id="9723f-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="9723f-506">Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</span><span class="sxs-lookup"><span data-stu-id="9723f-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="9723f-507">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-507">No</span></span></td>
<td><span data-ttu-id="9723f-508">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-508">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-509">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9723f-510">Reservationen fjernes.</span><span class="sxs-lookup"><span data-stu-id="9723f-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="9723f-511">To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</span><span class="sxs-lookup"><span data-stu-id="9723f-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="9723f-512">Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</span><span class="sxs-lookup"><span data-stu-id="9723f-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="9723f-513">Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Ingen</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="9723f-514">Ja</span><span class="sxs-lookup"><span data-stu-id="9723f-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9723f-515">Vælg en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="9723f-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="9723f-516">Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</span><span class="sxs-lookup"><span data-stu-id="9723f-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="9723f-517">Vælg <strong>Ændring af lagerstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="9723f-518">Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</span><span class="sxs-lookup"><span data-stu-id="9723f-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9723f-519">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="9723f-520">Antallet reserveres igen for samme batch.</span><span class="sxs-lookup"><span data-stu-id="9723f-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9723f-521">Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="9723f-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9723f-522">Nr.</span><span class="sxs-lookup"><span data-stu-id="9723f-522">No</span></span></td>
<td><span data-ttu-id="9723f-523">Se den forrige række.</span><span class="sxs-lookup"><span data-stu-id="9723f-523">See the previous row.</span></span></td>
<td><span data-ttu-id="9723f-524">Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="9723f-525">Ændringer i lagerstatus er ikke tilladt.</span><span class="sxs-lookup"><span data-stu-id="9723f-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="9723f-526">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="9723f-526">Limitations</span></span>

- <span data-ttu-id="9723f-527">Reservationsfunktionaliteten for fleksibel dimension for lagerstedsniveau understøtter ikke følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="9723f-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="9723f-528">Styring af fastvægt</span><span class="sxs-lookup"><span data-stu-id="9723f-528">Catch weight management</span></span>
    - <span data-ttu-id="9723f-529">Fysisk negativt lager</span><span class="sxs-lookup"><span data-stu-id="9723f-529">Physical negative inventory</span></span>
    - <span data-ttu-id="9723f-530">Reservation i forhold til bestilt forsyning</span><span class="sxs-lookup"><span data-stu-id="9723f-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="9723f-531">Flytteordrer og pluk af råvarer</span><span class="sxs-lookup"><span data-stu-id="9723f-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="9723f-532">Der er begrænsninger for containerkonsolideringsreglen for pakning efter vejledningsenhed.</span><span class="sxs-lookup"><span data-stu-id="9723f-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="9723f-533">I forbindelse med ordrebekræftede reservationer anbefales det, at du ikke bruger skabeloner til containerbuild, hvor feltet **Pakning efter vejledningsenhed** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="9723f-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="9723f-534">I det aktuelle design bruges lokationsvejledninger ikke, når der oprettes lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="9723f-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="9723f-535">Derfor er det kun den laveste enhed i enhedsseriegruppen (lagerenheden), der anvendes under containeriseringsbølgetrinnet.</span><span class="sxs-lookup"><span data-stu-id="9723f-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
