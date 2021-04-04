---
title: Konfigurere tilknytning af kolonnerne for salgsordrestatus
description: Dette emne forklarer, hvordan du kan konfigurere statuskolonnerne for salgsordre til dobbeltskrivning.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
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
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: ecf26a2a697fa4d0485c1904041692a6c10ce9c3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560403"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="45ce8-103">Konfigurere tilknytning af kolonnerne for salgsordrestatus</span><span class="sxs-lookup"><span data-stu-id="45ce8-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45ce8-104">De kolonner, der angiver status for salgsordrer, har forskellige fasttekstværdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="45ce8-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="45ce8-105">Der kræves yderligere opsætning for at knytte disse kolonner til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="45ce8-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="45ce8-106">kolonner i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45ce8-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="45ce8-107">I Supply Chain Management afspejler to kolonner status for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="45ce8-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="45ce8-108">De kolonner, du skal tilknytte, er **Status** og **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="45ce8-109">Fastteksten **Status** angiver ordrens overordnede status.</span><span class="sxs-lookup"><span data-stu-id="45ce8-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="45ce8-110">Denne status vises i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="45ce8-110">This status is shown on the order header.</span></span>

<span data-ttu-id="45ce8-111">Fastteksten **Status** har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="45ce8-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="45ce8-112">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-112">Open Order</span></span>
- <span data-ttu-id="45ce8-113">Leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-113">Delivered</span></span>
- <span data-ttu-id="45ce8-114">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-114">Invoiced</span></span>
- <span data-ttu-id="45ce8-115">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-115">Cancelled</span></span>

<span data-ttu-id="45ce8-116">Fastteksten **Dokumentstatus** angiver det seneste dokument, der blev genereret til ordren.</span><span class="sxs-lookup"><span data-stu-id="45ce8-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="45ce8-117">Hvis ordren f.eks. er bekræftet, er dette dokument en salgsordrebekræftelse.</span><span class="sxs-lookup"><span data-stu-id="45ce8-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="45ce8-118">Hvis en salgsordre er delvist faktureret, og den resterende linje er bekræftet, forbliver dokumentstatussen **Faktura**, fordi fakturaen genereres senere i processen.</span><span class="sxs-lookup"><span data-stu-id="45ce8-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="45ce8-119">Fastteksten **Dokumentstatus** har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="45ce8-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="45ce8-120">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="45ce8-120">Confirmation</span></span>
- <span data-ttu-id="45ce8-121">Plukliste</span><span class="sxs-lookup"><span data-stu-id="45ce8-121">Picking List</span></span>
- <span data-ttu-id="45ce8-122">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="45ce8-122">Packing Slip</span></span>
- <span data-ttu-id="45ce8-123">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="45ce8-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="45ce8-124">kolonner i Salg</span><span class="sxs-lookup"><span data-stu-id="45ce8-124">columns in Sales</span></span>

<span data-ttu-id="45ce8-125">I Salg angiver to kolonner status for ordren.</span><span class="sxs-lookup"><span data-stu-id="45ce8-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="45ce8-126">De kolonner, du skal tilknytte, er **Status** og **Behandlingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="45ce8-127">Fastteksten **Status** angiver ordrens overordnede status.</span><span class="sxs-lookup"><span data-stu-id="45ce8-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="45ce8-128">Den har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="45ce8-128">It has the following values:</span></span>

- <span data-ttu-id="45ce8-129">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-129">Active</span></span>
- <span data-ttu-id="45ce8-130">Sendt</span><span class="sxs-lookup"><span data-stu-id="45ce8-130">Submitted</span></span>
- <span data-ttu-id="45ce8-131">Opfyldt</span><span class="sxs-lookup"><span data-stu-id="45ce8-131">Fulfilled</span></span>
- <span data-ttu-id="45ce8-132">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-132">Invoiced</span></span>
- <span data-ttu-id="45ce8-133">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-133">Cancelled</span></span>

<span data-ttu-id="45ce8-134">Fastteksten **Behandlingsstatus** blev introduceret, så statussen kan tilknyttes mere præcist ved hjælp af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45ce8-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="45ce8-135">Følgende tabel viser tilknytningen af **Behandlingsstatus** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45ce8-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="45ce8-136">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="45ce8-136">Processing Status</span></span>   | <span data-ttu-id="45ce8-137">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45ce8-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="45ce8-138">Dokumentstatus i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45ce8-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="45ce8-139">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-139">Active</span></span>              | <span data-ttu-id="45ce8-140">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-140">Open Order</span></span>                        | <span data-ttu-id="45ce8-141">None</span><span class="sxs-lookup"><span data-stu-id="45ce8-141">None</span></span>                                       |
| <span data-ttu-id="45ce8-142">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="45ce8-142">Confirmed</span></span>           | <span data-ttu-id="45ce8-143">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-143">Open Order</span></span>                        | <span data-ttu-id="45ce8-144">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="45ce8-144">Confirmation</span></span>                               |
| <span data-ttu-id="45ce8-145">Plukket</span><span class="sxs-lookup"><span data-stu-id="45ce8-145">Picked</span></span>              | <span data-ttu-id="45ce8-146">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-146">Open Order</span></span>                        | <span data-ttu-id="45ce8-147">Plukliste</span><span class="sxs-lookup"><span data-stu-id="45ce8-147">Picking List</span></span>                               |
| <span data-ttu-id="45ce8-148">Delvist leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-148">Partially Delivered</span></span> | <span data-ttu-id="45ce8-149">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-149">Open Order</span></span>                        | <span data-ttu-id="45ce8-150">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="45ce8-150">Packing Slip</span></span>                               |
| <span data-ttu-id="45ce8-151">Leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-151">Delivered</span></span>           | <span data-ttu-id="45ce8-152">Leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-152">Delivered</span></span>                         | <span data-ttu-id="45ce8-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="45ce8-153">Packing Slip</span></span>                               |
| <span data-ttu-id="45ce8-154">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-154">Partially Invoiced</span></span>  | <span data-ttu-id="45ce8-155">Leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-155">Delivered</span></span>                         | <span data-ttu-id="45ce8-156">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="45ce8-156">Invoice</span></span>                                    |
| <span data-ttu-id="45ce8-157">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-157">Invoiced</span></span>            | <span data-ttu-id="45ce8-158">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-158">Invoiced</span></span>                          | <span data-ttu-id="45ce8-159">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="45ce8-159">Invoice</span></span>                                    |
| <span data-ttu-id="45ce8-160">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-160">Cancelled</span></span>           | <span data-ttu-id="45ce8-161">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-161">Cancelled</span></span>                         | <span data-ttu-id="45ce8-162">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="45ce8-162">Not applicable</span></span>                             |

<span data-ttu-id="45ce8-163">Følgende tabel viser tilknytningen af **Behandlingsstatus** mellem Salg og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45ce8-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="45ce8-164">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="45ce8-164">Processing Status</span></span>   | <span data-ttu-id="45ce8-165">Status i Salg</span><span class="sxs-lookup"><span data-stu-id="45ce8-165">Status in Sales</span></span> | <span data-ttu-id="45ce8-166">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45ce8-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="45ce8-167">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-167">Active</span></span>              | <span data-ttu-id="45ce8-168">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-168">Active</span></span>          | <span data-ttu-id="45ce8-169">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-169">Open Order</span></span>                        |
| <span data-ttu-id="45ce8-170">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="45ce8-170">Confirmed</span></span>           | <span data-ttu-id="45ce8-171">Sendt</span><span class="sxs-lookup"><span data-stu-id="45ce8-171">Submitted</span></span>       | <span data-ttu-id="45ce8-172">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-172">Open Order</span></span>                        |
| <span data-ttu-id="45ce8-173">Plukket</span><span class="sxs-lookup"><span data-stu-id="45ce8-173">Picked</span></span>              | <span data-ttu-id="45ce8-174">Sendt</span><span class="sxs-lookup"><span data-stu-id="45ce8-174">Submitted</span></span>       | <span data-ttu-id="45ce8-175">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-175">Open Order</span></span>                        |
| <span data-ttu-id="45ce8-176">Delvist leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-176">Partially Delivered</span></span> | <span data-ttu-id="45ce8-177">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-177">Active</span></span>          | <span data-ttu-id="45ce8-178">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-178">Open Order</span></span>                        |
| <span data-ttu-id="45ce8-179">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-179">Partially Invoiced</span></span>  | <span data-ttu-id="45ce8-180">Aktive</span><span class="sxs-lookup"><span data-stu-id="45ce8-180">Active</span></span>          | <span data-ttu-id="45ce8-181">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="45ce8-181">Open Order</span></span>                        |
| <span data-ttu-id="45ce8-182">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-182">Partially Invoiced</span></span>  | <span data-ttu-id="45ce8-183">Opfyldt</span><span class="sxs-lookup"><span data-stu-id="45ce8-183">Fulfilled</span></span>       | <span data-ttu-id="45ce8-184">Leveret</span><span class="sxs-lookup"><span data-stu-id="45ce8-184">Delivered</span></span>                         |
| <span data-ttu-id="45ce8-185">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-185">Invoiced</span></span>            | <span data-ttu-id="45ce8-186">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-186">Invoiced</span></span>        | <span data-ttu-id="45ce8-187">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="45ce8-187">Invoiced</span></span>                          |
| <span data-ttu-id="45ce8-188">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-188">Cancelled</span></span>           | <span data-ttu-id="45ce8-189">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-189">Cancelled</span></span>       | <span data-ttu-id="45ce8-190">Annulleret</span><span class="sxs-lookup"><span data-stu-id="45ce8-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="45ce8-191">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="45ce8-191">Setup</span></span>

<span data-ttu-id="45ce8-192">Hvis du vil konfigurere tilknytningen af statuskolonnerne for salgsordre, skal du aktivere attributterne **IsSOPIntegrationEnabled** og **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="45ce8-193">Hvis du vil aktivere attributten **IsSOPIntegrationEnabled**, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="45ce8-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="45ce8-194">Åbn en browser, og gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="45ce8-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="45ce8-195">Erstat **\<test-name\>** med dit firmas link til Salg.</span><span class="sxs-lookup"><span data-stu-id="45ce8-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="45ce8-196">På den side, der åbnes, skal du søge efter **organizationid** og notere dig værdien.</span><span class="sxs-lookup"><span data-stu-id="45ce8-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Finde organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="45ce8-198">Åbn browserkonsollen i Salg, og kør følgende script.</span><span class="sxs-lookup"><span data-stu-id="45ce8-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="45ce8-199">Brug værdien af **organizationid** fra trin 2.</span><span class="sxs-lookup"><span data-stu-id="45ce8-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i browserkonsollen](media/sales-map-script.png)

4. <span data-ttu-id="45ce8-201">Kontrollér, at **IsSOPIntegrationEnabled** er angivet til **true**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="45ce8-202">Brug URL-adressen fra trin 1 til at kontrollere værdien.</span><span class="sxs-lookup"><span data-stu-id="45ce8-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled er angivet til true](media/sales-map-integration-enabled.png)

<span data-ttu-id="45ce8-204">Hvis du vil aktivere attributten **isIntegrationUser**, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="45ce8-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="45ce8-205">Gå i Salg til **Indstilling \> Tilpasning \> Tilpas systemet**, vælg **Brugertabel**, og åbn derefter **Formular \> Bruger**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Åbne brugerformularen](media/sales-map-user.png)

2. <span data-ttu-id="45ce8-207">I Feltoversigt skal du finde **Integrationsbrugertilstand** og dobbeltklikke på den for at føje den til formularen.</span><span class="sxs-lookup"><span data-stu-id="45ce8-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="45ce8-208">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="45ce8-208">Save your change.</span></span>

    ![Tilføje kolonnen Integrationsbrugertilstand i formularen](media/sales-map-field-explorer.png)

3. <span data-ttu-id="45ce8-210">Gå i Salg til **Indstilling \> Sikkerhed \> Brugere**, og skift visningen fra **Aktiverede brugere** til **Programbrugere**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Ændre visningen fra Aktiverede brugere til Programbrugere](media/sales-map-enabled-users.png)

4. <span data-ttu-id="45ce8-212">Vælg de to poster for **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste over programbrugere](media/sales-map-user-mode.png)

5. <span data-ttu-id="45ce8-214">Ret værdien i kolonnen **Integrationsbrugertilstand** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="45ce8-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Ændre værdien i kolonnen Integrationsbrugertilstand](media/sales-map-user-mode-yes.png)

<span data-ttu-id="45ce8-216">Dine salgsordrer er nu tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="45ce8-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]