---
title: Integreret debitormaster
description: I dette emne beskrives integrationen af debitordata mellem Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 402342b459c366d0e198e3d0e946deb1f9e81739
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568120"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="1411c-103">Integreret kundemaster</span><span class="sxs-lookup"><span data-stu-id="1411c-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="1411c-104">Debitordata kan styres i mere end ét Dynamics 365-program.</span><span class="sxs-lookup"><span data-stu-id="1411c-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="1411c-105">En debitorrække kan f.eks. stamme fra en salgsaktivitet i Dynamics 365 Sales (en modelbaseret app i Dynamics 365), eller en række kan stamme fra detailaktivitet i Dynamics 365 Commerce (en Finance and Operations-app).</span><span class="sxs-lookup"><span data-stu-id="1411c-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="1411c-106">Uanset hvor debitordataene stammer fra, integreres de i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="1411c-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="1411c-107">Integreret kundemaster giver dig fleksibiliteten til at administrere debitordata i ethvert Dynamics 365-program og giver en omfattende oversigt over kunden på tværs af Dynamics 365-programpakken.</span><span class="sxs-lookup"><span data-stu-id="1411c-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="1411c-108">Debitordataflow</span><span class="sxs-lookup"><span data-stu-id="1411c-108">Customer data flow</span></span>

<span data-ttu-id="1411c-109">*Debitor* er et veldefineret begreb i programmer.</span><span class="sxs-lookup"><span data-stu-id="1411c-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="1411c-110">Derfor involverer integrationen af debitordata blot en harmonisering af debitorkonceptet mellem de to programmer.</span><span class="sxs-lookup"><span data-stu-id="1411c-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="1411c-111">Følgende illustration viser debitordataflowet.</span><span class="sxs-lookup"><span data-stu-id="1411c-111">The following illustration shows the customer data flow.</span></span>

![Debitordataflow](media/dual-write-customer-data-flow.png)

<span data-ttu-id="1411c-113">Debitorer kan groft inddeles i to typer: kommercielle/organisatoriske debitorer og forbrugere/slutbrugere.</span><span class="sxs-lookup"><span data-stu-id="1411c-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="1411c-114">Disse to typer af debitorer lagres og håndteres forskelligt i Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1411c-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="1411c-115">I Finance and Operations  styres både kommercielle/organisatoriske debitorer og forbrugere/slutbrugere i en enkelt tabel med navnet **CustTable** (CustCustomerV3Entity), og de klassificeres ud fra attributten **Type**.</span><span class="sxs-lookup"><span data-stu-id="1411c-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="1411c-116">(Hvis **Type** er angivet til **Organisation**, er debitoren en kommerciel/organisatorisk kunde, og hvis **Type** er angivet til **Person**, er debitoren en forbruger/slutbruger). Oplysningerne om den primære kontaktperson håndteres via tabellen SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="1411c-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="1411c-117">I Dataverse bliver kommercielle/organisatoriske kunder styret i kontotabellen og identificeres som debitorer, når attributten **RelationshipType** er angivet til **Debitor.**</span><span class="sxs-lookup"><span data-stu-id="1411c-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="1411c-118">Både forbrugere/slutbrugere og kontaktpersonen repræsenteres af kontakttabellen.</span><span class="sxs-lookup"><span data-stu-id="1411c-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="1411c-119">Hvis du vil have en klar adskillelse mellem en forbruger/slutbruger og en kontaktperson, har tabellen **Kontakt** et boolesk flag med navnet **Salgbar**.</span><span class="sxs-lookup"><span data-stu-id="1411c-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="1411c-120">Når **Salgbar** er **Sand**, er kontakten en forbruger/slutbruger, og der kan oprettes tilbud og ordrer for den pågældende kontakt.</span><span class="sxs-lookup"><span data-stu-id="1411c-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="1411c-121">Når **Salgbar** er **Falsk**, er kontakten kun en primær kontaktperson for en kunde.</span><span class="sxs-lookup"><span data-stu-id="1411c-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="1411c-122">Når en kontakt, der ikke er salgbar, deltager i et tilbud eller en ordreproces, angives **Salgbar** til **Sand** for at markere kontakten som en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="1411c-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="1411c-123">En kontakt, der er blevet en salgbar kontakt, forbliver en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="1411c-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="1411c-124">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="1411c-124">Templates</span></span>

<span data-ttu-id="1411c-125">Debitordata indeholder alle oplysninger om debitoren, f.eks debitorens gruppe, adresser, kontaktoplysninger, betalingsprofil, fakturaprofil og fordelskundestatus.</span><span class="sxs-lookup"><span data-stu-id="1411c-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="1411c-126">En samling af tabeltilknytninger fungerer sammen under interaktion med debitordata, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="1411c-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="1411c-127">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="1411c-127">Finance and Operations apps</span></span> | <span data-ttu-id="1411c-128">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="1411c-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="1411c-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1411c-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="1411c-130">CDS kontakter V2</span><span class="sxs-lookup"><span data-stu-id="1411c-130">CDS Contacts V2</span></span>             | <span data-ttu-id="1411c-131">kontakter</span><span class="sxs-lookup"><span data-stu-id="1411c-131">contacts</span></span>                        | <span data-ttu-id="1411c-132">Denne skabelon synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-133">Debitorgrupper</span><span class="sxs-lookup"><span data-stu-id="1411c-133">Customer groups</span></span>             | <span data-ttu-id="1411c-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="1411c-134">msdyn_customergroups</span></span>            | <span data-ttu-id="1411c-135">Denne skabelon synkroniserer kundegruppeoplysninger.</span><span class="sxs-lookup"><span data-stu-id="1411c-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="1411c-136">Debitorbetalingsmetode</span><span class="sxs-lookup"><span data-stu-id="1411c-136">Customer payment method</span></span>     | <span data-ttu-id="1411c-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="1411c-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="1411c-138">Denne skabelon synkroniserer kundebetalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="1411c-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="1411c-139">Debitorer V3</span><span class="sxs-lookup"><span data-stu-id="1411c-139">Customers V3</span></span>                | <span data-ttu-id="1411c-140">konti</span><span class="sxs-lookup"><span data-stu-id="1411c-140">accounts</span></span>                        | <span data-ttu-id="1411c-141">Denne skabelon synkroniserer kundemasteroplysninger for kommercielle og organisatoriske kunder.</span><span class="sxs-lookup"><span data-stu-id="1411c-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="1411c-142">Debitorer V3</span><span class="sxs-lookup"><span data-stu-id="1411c-142">Customers V3</span></span>                | <span data-ttu-id="1411c-143">kontakter</span><span class="sxs-lookup"><span data-stu-id="1411c-143">contacts</span></span>                        | <span data-ttu-id="1411c-144">Denne skabelon synkroniserer kundemasterdata for forbrugere og slutbrugere.</span><span class="sxs-lookup"><span data-stu-id="1411c-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="1411c-145">Foranstillede navne</span><span class="sxs-lookup"><span data-stu-id="1411c-145">Name affixes</span></span>                | <span data-ttu-id="1411c-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="1411c-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="1411c-147">Denne skabelon synkroniserer referencedata for foranstillede navne for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-148">Betalingsdagslinjer CDS V2</span><span class="sxs-lookup"><span data-stu-id="1411c-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="1411c-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="1411c-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="1411c-150">Denne skabelon synkroniserer betalingsdagslinjers referencedata for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-151">Betalingsdage CDS</span><span class="sxs-lookup"><span data-stu-id="1411c-151">Payment days CDS</span></span>            | <span data-ttu-id="1411c-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="1411c-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="1411c-153">Denne skabelon synkroniserer referencedata for linjer for betalingsdage for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-154">Betalingsplanlinjer</span><span class="sxs-lookup"><span data-stu-id="1411c-154">Payment schedule lines</span></span>      | <span data-ttu-id="1411c-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="1411c-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="1411c-156">Synkroniserer betalingsdagsskemalinjers referencedata for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-157">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="1411c-157">Payment schedule</span></span>            | <span data-ttu-id="1411c-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="1411c-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="1411c-159">Denne skabelon synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1411c-160">Betalingsbetingelse</span><span class="sxs-lookup"><span data-stu-id="1411c-160">Terms of payment</span></span>            | <span data-ttu-id="1411c-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="1411c-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="1411c-162">Denne skabelon synkroniserer referencedata for betalingsbetingelser (betalingsvilkår) for både kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="1411c-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]