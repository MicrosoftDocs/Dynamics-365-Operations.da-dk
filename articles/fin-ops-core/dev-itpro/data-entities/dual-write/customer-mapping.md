---
title: Integreret debitormaster
description: I dette emne beskrives integrationen af debitordata mellem Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124583"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="a1d12-103">Integreret kundemaster</span><span class="sxs-lookup"><span data-stu-id="a1d12-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a1d12-104">Det er typisk, at debitorposter styres i mere end ét program.</span><span class="sxs-lookup"><span data-stu-id="a1d12-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="a1d12-105">F.eks. kan salgsaktivitet indlæse kommercielle debitorposter via et Sales-program, og e-handel eller detailsalg kan indlæse debitorposter via et Finance and Operations-program.</span><span class="sxs-lookup"><span data-stu-id="a1d12-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="a1d12-106">Uanset hvor debitorposten stammer fra, er den integreret i baggrunden på tværs af applikationsgrænser og infrastrukturforskelle.</span><span class="sxs-lookup"><span data-stu-id="a1d12-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="a1d12-107">Integreret debitor-mastering hjælper med at håndtere multi-mastering-scenarier og giver en omfattende visning af debitoren i Dynamics 365-programpakken.</span><span class="sxs-lookup"><span data-stu-id="a1d12-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="a1d12-108">Debitordataflow</span><span class="sxs-lookup"><span data-stu-id="a1d12-108">Customer data flow</span></span>

<span data-ttu-id="a1d12-109">*Debitor* er et veldefineret begreb i programmer.</span><span class="sxs-lookup"><span data-stu-id="a1d12-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="a1d12-110">Derfor involverer integrationen af debitordata blot en harmonisering af debitorkonceptet mellem de to programmer.</span><span class="sxs-lookup"><span data-stu-id="a1d12-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="a1d12-111">Følgende illustration viser debitordataflowet.</span><span class="sxs-lookup"><span data-stu-id="a1d12-111">The following illustration shows the customer data flow.</span></span>

![Debitordataflow](media/dual-write-customer-data-flow.png)

<span data-ttu-id="a1d12-113">Debitorer kan groft inddeles i to typer: kommercielle/organisatoriske debitorer og forbrugere/slutbrugere.</span><span class="sxs-lookup"><span data-stu-id="a1d12-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="a1d12-114">Disse to typer af debitorer lagres og håndteres forskelligt i Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a1d12-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="a1d12-115">I Finance and Operations styres både kommercielle/organisatoriske debitorer og forbrugere/slutbrugere i en enkelt tabel med navnet **CustTable** (CustomerCustomerV3Entity), og de klassificeres ud fra attributten **Type**.</span><span class="sxs-lookup"><span data-stu-id="a1d12-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="a1d12-116">(Hvis **Type** er angivet til **Organisation**, er debitoren en kommerciel/organisatorisk kunde, og hvis **Type** er angivet til **Person**, er debitoren en forbruger/slutbruger). Oplysningerne om den primære kontaktperson håndteres via enheden SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="a1d12-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="a1d12-117">I Common Data Service bliver kommercielle/organisatoriske kunder styret i kontoenheden og identificeres som debitorer, når attributten **RelationshipType** er angivet til **Debitor.**</span><span class="sxs-lookup"><span data-stu-id="a1d12-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="a1d12-118">Både forbrugere/slutbrugere og kontaktpersonen repræsenteres af kontaktenheden.</span><span class="sxs-lookup"><span data-stu-id="a1d12-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="a1d12-119">Hvis du vil have en klar adskillelse mellem en forbruger/slutbruger og en kontaktperson, har enheden **Kontakt** et boolesk flag med navnet **Salgbar**.</span><span class="sxs-lookup"><span data-stu-id="a1d12-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="a1d12-120">Når **Salgbar** er **Sand**, er kontakten en forbruger/slutbruger, og der kan oprettes tilbud og ordrer for den pågældende kontakt.</span><span class="sxs-lookup"><span data-stu-id="a1d12-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="a1d12-121">Når **Salgbar** er **Falsk**, er kontakten kun en primær kontaktperson for en kunde.</span><span class="sxs-lookup"><span data-stu-id="a1d12-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="a1d12-122">Når en kontakt, der ikke er salgbar, deltager i et tilbud eller en ordreproces, angives **Salgbar** til **Sand** for at markere kontakten som en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="a1d12-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="a1d12-123">En kontakt, der er blevet en salgbar kontakt, forbliver en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="a1d12-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="a1d12-124">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="a1d12-124">Templates</span></span>

<span data-ttu-id="a1d12-125">Debitordata indeholder alle oplysninger om debitoren, f.eks debitorens gruppe, adresser, kontaktoplysninger, betalingsprofil, fakturaprofil og fordelskundestatus.</span><span class="sxs-lookup"><span data-stu-id="a1d12-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="a1d12-126">En samling af enhedstilknytninger fungerer sammen under interaktion med debitordata, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a1d12-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a1d12-127">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="a1d12-127">Finance and Operations apps</span></span> | <span data-ttu-id="a1d12-128">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="a1d12-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="a1d12-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a1d12-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="a1d12-130">CDS kontakter V2</span><span class="sxs-lookup"><span data-stu-id="a1d12-130">CDS Contacts V2</span></span>             | <span data-ttu-id="a1d12-131">kontakter</span><span class="sxs-lookup"><span data-stu-id="a1d12-131">contacts</span></span>                        | <span data-ttu-id="a1d12-132">Denne skabelon synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-133">Debitorgrupper</span><span class="sxs-lookup"><span data-stu-id="a1d12-133">Customer groups</span></span>             | <span data-ttu-id="a1d12-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="a1d12-134">msdyn_customergroups</span></span>            | <span data-ttu-id="a1d12-135">Denne skabelon synkroniserer kundegruppeoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a1d12-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="a1d12-136">Debitorbetalingsmetode</span><span class="sxs-lookup"><span data-stu-id="a1d12-136">Customer payment method</span></span>     | <span data-ttu-id="a1d12-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="a1d12-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="a1d12-138">Denne skabelon synkroniserer kundebetalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a1d12-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="a1d12-139">Debitorer V3</span><span class="sxs-lookup"><span data-stu-id="a1d12-139">Customers V3</span></span>                | <span data-ttu-id="a1d12-140">konti</span><span class="sxs-lookup"><span data-stu-id="a1d12-140">accounts</span></span>                        | <span data-ttu-id="a1d12-141">Denne skabelon synkroniserer kundemasteroplysninger for kommercielle og organisatoriske kunder.</span><span class="sxs-lookup"><span data-stu-id="a1d12-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="a1d12-142">Debitorer V3</span><span class="sxs-lookup"><span data-stu-id="a1d12-142">Customers V3</span></span>                | <span data-ttu-id="a1d12-143">kontakter</span><span class="sxs-lookup"><span data-stu-id="a1d12-143">contacts</span></span>                        | <span data-ttu-id="a1d12-144">Denne skabelon synkroniserer kundemasterdata for forbrugere og slutbrugere.</span><span class="sxs-lookup"><span data-stu-id="a1d12-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="a1d12-145">Fordelskundekort</span><span class="sxs-lookup"><span data-stu-id="a1d12-145">Loyalty card</span></span>                | <span data-ttu-id="a1d12-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="a1d12-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="a1d12-147">Denne skabelon synkroniserer oplysninger om fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="a1d12-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="a1d12-148">Foranstillede navne</span><span class="sxs-lookup"><span data-stu-id="a1d12-148">Name affixes</span></span>                | <span data-ttu-id="a1d12-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="a1d12-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="a1d12-150">Denne skabelon synkroniserer referencedata for foranstillede navne for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-151">Betalingsdagslinjer CDS V2</span><span class="sxs-lookup"><span data-stu-id="a1d12-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="a1d12-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="a1d12-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="a1d12-153">Denne skabelon synkroniserer betalingsdagslinjers referencedata for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-154">Betalingsdage CDS</span><span class="sxs-lookup"><span data-stu-id="a1d12-154">Payment days CDS</span></span>            | <span data-ttu-id="a1d12-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="a1d12-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="a1d12-156">Denne skabelon synkroniserer referencedata for linjer for betalingsdage for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-157">Betalingsplanlinjer</span><span class="sxs-lookup"><span data-stu-id="a1d12-157">Payment schedule lines</span></span>      | <span data-ttu-id="a1d12-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="a1d12-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="a1d12-159">Synkroniserer betalingsdagsskemalinjers referencedata for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-160">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="a1d12-160">Payment schedule</span></span>            | <span data-ttu-id="a1d12-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="a1d12-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="a1d12-162">Denne skabelon synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1d12-163">Betalingsbetingelse</span><span class="sxs-lookup"><span data-stu-id="a1d12-163">Terms of payment</span></span>            | <span data-ttu-id="a1d12-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="a1d12-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="a1d12-165">Denne skabelon synkroniserer referencedata for betalingsbetingelser (betalingsvilkår) for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1d12-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
