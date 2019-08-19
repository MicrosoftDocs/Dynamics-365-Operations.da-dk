---
title: EU-posteringscertifikater
description: Denne artikel indeholder oplysninger om postcertifikater i den Europæiske Union (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46a4180163adea72e7d8712ed5ce6a3306e477c5
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852282"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="03b18-103">EU-postcertifikater</span><span class="sxs-lookup"><span data-stu-id="03b18-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03b18-104">Denne artikel indeholder oplysninger om postcertifikater i den Europæiske Union (EU).</span><span class="sxs-lookup"><span data-stu-id="03b18-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="03b18-105">Du kan udføre følgende opgaver for et EU-posteringscertifikat:</span><span class="sxs-lookup"><span data-stu-id="03b18-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="03b18-106">Oprette og udstede et EU-posteringscertifikat sammen med en følgeseddel eller debitorfaktura for levering af varer eller tjenester til EU-lande/-regioner.</span><span class="sxs-lookup"><span data-stu-id="03b18-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="03b18-107">Modtage EU-posteringscertifikatet, der er signeret af en EU-kunde.</span><span class="sxs-lookup"><span data-stu-id="03b18-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="03b18-108">Overføre det signerede EU-posteringscertifikat, der er modtaget enten fra kunden eller fra en tredjepart, der er ansvarlig for levering af varer til kunden.</span><span class="sxs-lookup"><span data-stu-id="03b18-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="03b18-109">Tilknytte det overførte EU-posteringscertifikat med en debitorfaktura.</span><span class="sxs-lookup"><span data-stu-id="03b18-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="03b18-110">Opdatere status for det overførte EU-posteringscertifikat.</span><span class="sxs-lookup"><span data-stu-id="03b18-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03b18-111">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="03b18-111">Prerequisites</span></span>
<span data-ttu-id="03b18-112">Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.</span><span class="sxs-lookup"><span data-stu-id="03b18-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b18-113">Kategori</span><span class="sxs-lookup"><span data-stu-id="03b18-113">Category</span></span></th>
<th><span data-ttu-id="03b18-114">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="03b18-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03b18-115">Land/område</span><span class="sxs-lookup"><span data-stu-id="03b18-115">Country/region</span></span></td>
<td><span data-ttu-id="03b18-116">Den primære adresse for den juridiske skal enhed være i et EU-medlemsland.</span><span class="sxs-lookup"><span data-stu-id="03b18-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03b18-117">Relaterede opsætningsopgaver</span><span class="sxs-lookup"><span data-stu-id="03b18-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="03b18-118">På siden <strong>Kreditorparametre</strong> skal du vælge indstillingerne <strong>Aktivér administration af indførselscertifikater</strong> og <strong>Aktivér udstedelse af indførselscertifikater</strong>.</span><span class="sxs-lookup"><span data-stu-id="03b18-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="03b18-119">På siden <strong>Kunder</strong> på oversigtspanelet <strong>Faktura og levering</strong> skal du vælge indstillingen <strong>Postcertifikat er påkrævet</strong> for at angive, at et EU-indførselscertifikat er obligatorisk for kunden.</span><span class="sxs-lookup"><span data-stu-id="03b18-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="03b18-120">Vælg indstillingen <strong>Udsted indførselscertifikat</strong> for at udstede et EU-indførselscertifikat for den juridiske enhed for kunden.</span><span class="sxs-lookup"><span data-stu-id="03b18-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="03b18-121">På siden <strong>Debitorparametre</strong> skal du vælge en nummerseriekode for referencen <strong>Postcertifikat</strong>.</span><span class="sxs-lookup"><span data-stu-id="03b18-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03b18-122">Relaterede transaktioner</span><span class="sxs-lookup"><span data-stu-id="03b18-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="03b18-123">Opret en debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="03b18-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="03b18-124">Opret en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="03b18-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="03b18-125">Oprettelse, registrering og overførsel af et EU-indførselscertifikat</span><span class="sxs-lookup"><span data-stu-id="03b18-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="03b18-126">Du kan oprette et EU-posteringscertifikat automatisk eller manuelt.</span><span class="sxs-lookup"><span data-stu-id="03b18-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="03b18-127">Et EU-posteringscertifikat oprettes og udskrives automatisk, når du bogfører en følgeseddel eller en faktura for en kunde ved hjælp af siden **Bogføring af følgeseddel** eller **Bogføring af faktura**.</span><span class="sxs-lookup"><span data-stu-id="03b18-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="03b18-128">Hvis du manuelt vil oprette eller udskrive et EU-indførselscertifikat til en debitorfaktura igen, skal du bruge siden **Fakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="03b18-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="03b18-129">Derudover kan du bruge siden **Postcertifikatkladde** til at angive oplysninger om et EU-indførselscertifikat, der er udstedt af en tredjepart.</span><span class="sxs-lookup"><span data-stu-id="03b18-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="03b18-130">Oprette et EU-indførselscertifikat automatisk eller manuelt</span><span class="sxs-lookup"><span data-stu-id="03b18-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="03b18-131">Kan du automatisk oprette et EU-indførselscertifikat ved hjælp af en følgeseddel på siden **Alle salgsordrer** eller ved hjælp af en faktura på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="03b18-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="03b18-132">Hvis du vil oprette et EU-indførselscertifikat manuelt, kan du bruge en faktura på siden **Fakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="03b18-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="03b18-133">Før du manuelt opretter et EU-indførselscertifikat, skal du dog ændre status for certificering af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="03b18-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="03b18-134">Registrere et EU-indførselscertifikat</span><span class="sxs-lookup"><span data-stu-id="03b18-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="03b18-135">Hvis registrering er påkrævet, kan du bruge siden **Postcertifikatkladde** til at registrere et EU-indførselscertifikat, der er udstedt af en tredjepart.</span><span class="sxs-lookup"><span data-stu-id="03b18-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="03b18-136">Overføre et modtaget EU-indførselscertifikat</span><span class="sxs-lookup"><span data-stu-id="03b18-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="03b18-137">Brug siden **Bilag** til at overføre et modtaget EU-indførselscertifikatet, der er signeret af en EU-kunde.</span><span class="sxs-lookup"><span data-stu-id="03b18-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="03b18-138">Når certifikatet er overført, kan du knytte det til en faktura som bevis for, at varer er leveret.</span><span class="sxs-lookup"><span data-stu-id="03b18-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="03b18-139">Denne dokumentation er påkrævet, hvis du skal udstede en faktura, der ikke indeholder moms, og den bruges også under revision.</span><span class="sxs-lookup"><span data-stu-id="03b18-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="03b18-140">Valgfrit: Opdatere status for certificering og udskrive status for en faktura</span><span class="sxs-lookup"><span data-stu-id="03b18-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="03b18-141">Du kan opdatere status for indførselscertificering og udskriftstatus for en debitorfaktura ved hjælp af siden **Fakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="03b18-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="03b18-142">Tekniske oplysninger til systemadministratorer</span><span class="sxs-lookup"><span data-stu-id="03b18-142">Technical information for system administrators</span></span>
<span data-ttu-id="03b18-143">Hvis du ikke har adgang til de sider, der bruges til at fuldføre denne opgave, skal du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="03b18-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b18-144">Kategori</span><span class="sxs-lookup"><span data-stu-id="03b18-144">Category</span></span></th>
<th><span data-ttu-id="03b18-145">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="03b18-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03b18-146">Sikkerhedsroller og programadgangsrettigheder</span><span class="sxs-lookup"><span data-stu-id="03b18-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="03b18-147">Når du vil angive og oprette EU-posteringscertifikater for varer eller tjenester, skal du være medlem af en sikkerhedsrolle, der omfatter følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="03b18-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="03b18-148"><strong>Debitorassistent</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="03b18-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="03b18-149"><strong>Kundeservicerepræsentant</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="03b18-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="03b18-150"><strong>Salgsassistent</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="03b18-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="03b18-151"><strong>Shippingmedarbejder</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="03b18-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





