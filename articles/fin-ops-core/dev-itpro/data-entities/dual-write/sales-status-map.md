---
title: Konfigurere tilknytningen af statusfelter for salgsordre
description: Dette emne forklarer, hvordan du kan konfigurere statusfelterne for salgsordre til dobbeltskrivning.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
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
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829279"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="33c11-103">Konfigurere tilknytningen af statusfelter for salgsordre</span><span class="sxs-lookup"><span data-stu-id="33c11-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33c11-104">De felter, der angiver status for salgsordrer, har forskellige fasttekstværdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="33c11-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="33c11-105">Der kræves yderligere opsætning for at knytte disse felter til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="33c11-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="33c11-106">Felter i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33c11-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="33c11-107">I Supply Chain Management afspejler to felter status for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="33c11-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="33c11-108">De felter, du skal tilknytte, er **Status** og **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="33c11-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="33c11-109">Fastteksten **Status** angiver ordrens overordnede status.</span><span class="sxs-lookup"><span data-stu-id="33c11-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="33c11-110">Denne status vises i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="33c11-110">This status is shown on the order header.</span></span>

<span data-ttu-id="33c11-111">Fastteksten **Status** har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="33c11-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="33c11-112">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-112">Open Order</span></span>
- <span data-ttu-id="33c11-113">Leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-113">Delivered</span></span>
- <span data-ttu-id="33c11-114">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-114">Invoiced</span></span>
- <span data-ttu-id="33c11-115">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-115">Cancelled</span></span>

<span data-ttu-id="33c11-116">Fastteksten **Dokumentstatus** angiver det seneste dokument, der blev genereret til ordren.</span><span class="sxs-lookup"><span data-stu-id="33c11-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="33c11-117">Hvis ordren f.eks. er bekræftet, er dette dokument en salgsordrebekræftelse.</span><span class="sxs-lookup"><span data-stu-id="33c11-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="33c11-118">Hvis en salgsordre er delvist faktureret, og den resterende linje er bekræftet, forbliver dokumentstatussen **Faktura**, fordi fakturaen genereres senere i processen.</span><span class="sxs-lookup"><span data-stu-id="33c11-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="33c11-119">Fastteksten **Dokumentstatus** har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="33c11-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="33c11-120">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="33c11-120">Confirmation</span></span>
- <span data-ttu-id="33c11-121">Plukliste</span><span class="sxs-lookup"><span data-stu-id="33c11-121">Picking List</span></span>
- <span data-ttu-id="33c11-122">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="33c11-122">Packing Slip</span></span>
- <span data-ttu-id="33c11-123">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="33c11-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="33c11-124">Felter i Salg</span><span class="sxs-lookup"><span data-stu-id="33c11-124">Fields in Sales</span></span>

<span data-ttu-id="33c11-125">I Salg angiver to felter status for ordren.</span><span class="sxs-lookup"><span data-stu-id="33c11-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="33c11-126">De felter, du skal tilknytte, er **Status** og **Behandlingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="33c11-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="33c11-127">Fastteksten **Status** angiver ordrens overordnede status.</span><span class="sxs-lookup"><span data-stu-id="33c11-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="33c11-128">Den har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="33c11-128">It has the following values:</span></span>

- <span data-ttu-id="33c11-129">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-129">Active</span></span>
- <span data-ttu-id="33c11-130">Sendt</span><span class="sxs-lookup"><span data-stu-id="33c11-130">Submitted</span></span>
- <span data-ttu-id="33c11-131">Opfyldt</span><span class="sxs-lookup"><span data-stu-id="33c11-131">Fulfilled</span></span>
- <span data-ttu-id="33c11-132">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-132">Invoiced</span></span>
- <span data-ttu-id="33c11-133">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-133">Cancelled</span></span>

<span data-ttu-id="33c11-134">Fastteksten **Behandlingsstatus** blev introduceret, så statussen kan tilknyttes mere præcist ved hjælp af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33c11-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="33c11-135">Følgende tabel viser tilknytningen af **Behandlingsstatus** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33c11-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="33c11-136">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="33c11-136">Processing Status</span></span>   | <span data-ttu-id="33c11-137">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33c11-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="33c11-138">Dokumentstatus i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33c11-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="33c11-139">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-139">Active</span></span>              | <span data-ttu-id="33c11-140">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-140">Open Order</span></span>                        | <span data-ttu-id="33c11-141">None</span><span class="sxs-lookup"><span data-stu-id="33c11-141">None</span></span>                                       |
| <span data-ttu-id="33c11-142">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="33c11-142">Confirmed</span></span>           | <span data-ttu-id="33c11-143">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-143">Open Order</span></span>                        | <span data-ttu-id="33c11-144">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="33c11-144">Confirmation</span></span>                               |
| <span data-ttu-id="33c11-145">Plukket</span><span class="sxs-lookup"><span data-stu-id="33c11-145">Picked</span></span>              | <span data-ttu-id="33c11-146">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-146">Open Order</span></span>                        | <span data-ttu-id="33c11-147">Plukliste</span><span class="sxs-lookup"><span data-stu-id="33c11-147">Picking List</span></span>                               |
| <span data-ttu-id="33c11-148">Delvist leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-148">Partially Delivered</span></span> | <span data-ttu-id="33c11-149">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-149">Open Order</span></span>                        | <span data-ttu-id="33c11-150">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="33c11-150">Packing Slip</span></span>                               |
| <span data-ttu-id="33c11-151">Leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-151">Delivered</span></span>           | <span data-ttu-id="33c11-152">Leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-152">Delivered</span></span>                         | <span data-ttu-id="33c11-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="33c11-153">Packing Slip</span></span>                               |
| <span data-ttu-id="33c11-154">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-154">Partially Invoiced</span></span>  | <span data-ttu-id="33c11-155">Leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-155">Delivered</span></span>                         | <span data-ttu-id="33c11-156">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="33c11-156">Invoice</span></span>                                    |
| <span data-ttu-id="33c11-157">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-157">Invoiced</span></span>            | <span data-ttu-id="33c11-158">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-158">Invoiced</span></span>                          | <span data-ttu-id="33c11-159">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="33c11-159">Invoice</span></span>                                    |
| <span data-ttu-id="33c11-160">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-160">Cancelled</span></span>           | <span data-ttu-id="33c11-161">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-161">Cancelled</span></span>                         | <span data-ttu-id="33c11-162">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="33c11-162">Not applicable</span></span>                             |

<span data-ttu-id="33c11-163">Følgende tabel viser tilknytningen af **Behandlingsstatus** mellem Salg og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33c11-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="33c11-164">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="33c11-164">Processing Status</span></span>   | <span data-ttu-id="33c11-165">Status i Salg</span><span class="sxs-lookup"><span data-stu-id="33c11-165">Status in Sales</span></span> | <span data-ttu-id="33c11-166">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33c11-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="33c11-167">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-167">Active</span></span>              | <span data-ttu-id="33c11-168">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-168">Active</span></span>          | <span data-ttu-id="33c11-169">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-169">Open Order</span></span>                        |
| <span data-ttu-id="33c11-170">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="33c11-170">Confirmed</span></span>           | <span data-ttu-id="33c11-171">Sendt</span><span class="sxs-lookup"><span data-stu-id="33c11-171">Submitted</span></span>       | <span data-ttu-id="33c11-172">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-172">Open Order</span></span>                        |
| <span data-ttu-id="33c11-173">Plukket</span><span class="sxs-lookup"><span data-stu-id="33c11-173">Picked</span></span>              | <span data-ttu-id="33c11-174">Sendt</span><span class="sxs-lookup"><span data-stu-id="33c11-174">Submitted</span></span>       | <span data-ttu-id="33c11-175">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-175">Open Order</span></span>                        |
| <span data-ttu-id="33c11-176">Delvist leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-176">Partially Delivered</span></span> | <span data-ttu-id="33c11-177">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-177">Active</span></span>          | <span data-ttu-id="33c11-178">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-178">Open Order</span></span>                        |
| <span data-ttu-id="33c11-179">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-179">Partially Invoiced</span></span>  | <span data-ttu-id="33c11-180">Aktive</span><span class="sxs-lookup"><span data-stu-id="33c11-180">Active</span></span>          | <span data-ttu-id="33c11-181">Åben ordre</span><span class="sxs-lookup"><span data-stu-id="33c11-181">Open Order</span></span>                        |
| <span data-ttu-id="33c11-182">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-182">Partially Invoiced</span></span>  | <span data-ttu-id="33c11-183">Opfyldt</span><span class="sxs-lookup"><span data-stu-id="33c11-183">Fulfilled</span></span>       | <span data-ttu-id="33c11-184">Leveret</span><span class="sxs-lookup"><span data-stu-id="33c11-184">Delivered</span></span>                         |
| <span data-ttu-id="33c11-185">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-185">Invoiced</span></span>            | <span data-ttu-id="33c11-186">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-186">Invoiced</span></span>        | <span data-ttu-id="33c11-187">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="33c11-187">Invoiced</span></span>                          |
| <span data-ttu-id="33c11-188">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-188">Cancelled</span></span>           | <span data-ttu-id="33c11-189">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-189">Cancelled</span></span>       | <span data-ttu-id="33c11-190">Annulleret</span><span class="sxs-lookup"><span data-stu-id="33c11-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="33c11-191">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="33c11-191">Setup</span></span>

<span data-ttu-id="33c11-192">Hvis du vil konfigurere tilknytningen af statusfelterne for salgsordre, skal du aktivere attributterne **IsSOPIntegrationEnabled** og **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="33c11-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="33c11-193">Hvis du vil aktivere attributten **IsSOPIntegrationEnabled**, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="33c11-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="33c11-194">Åbn en browser, og gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="33c11-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="33c11-195">Erstat **\<test-name\>** med dit firmas link til Salg.</span><span class="sxs-lookup"><span data-stu-id="33c11-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="33c11-196">På den side, der åbnes, skal du søge efter **organizationid** og notere dig værdien.</span><span class="sxs-lookup"><span data-stu-id="33c11-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Finde organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="33c11-198">Åbn browserkonsollen i Salg, og kør følgende script.</span><span class="sxs-lookup"><span data-stu-id="33c11-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="33c11-199">Brug værdien af **organizationid** fra trin 2.</span><span class="sxs-lookup"><span data-stu-id="33c11-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i browserkonsollen](media/sales-map-script.png)

4. <span data-ttu-id="33c11-201">Kontrollér, at **IsSOPIntegrationEnabled** er angivet til **true**.</span><span class="sxs-lookup"><span data-stu-id="33c11-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="33c11-202">Brug URL-adressen fra trin 1 til at kontrollere værdien.</span><span class="sxs-lookup"><span data-stu-id="33c11-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled er angivet til true](media/sales-map-integration-enabled.png)

<span data-ttu-id="33c11-204">Hvis du vil aktivere attributten **isIntegrationUser**, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="33c11-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="33c11-205">Gå i Salg til **Indstilling \> Tilpasning \> Tilpas systemet**, vælg **Brugerenhed**, og åbn derefter **Formular \> Bruger**.</span><span class="sxs-lookup"><span data-stu-id="33c11-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Åbne brugerformularen](media/sales-map-user.png)

2. <span data-ttu-id="33c11-207">I Feltoversigt skal du finde **Integrationsbrugertilstand** og dobbeltklikke på den for at føje den til formularen.</span><span class="sxs-lookup"><span data-stu-id="33c11-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="33c11-208">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="33c11-208">Save your change.</span></span>

    ![Tilføje feltet Integrationsbrugertilstand i formularen](media/sales-map-field-explorer.png)

3. <span data-ttu-id="33c11-210">Gå i Salg til **Indstilling \> Sikkerhed \> Brugere**, og skift visningen fra **Aktiverede brugere** til **Programbrugere**.</span><span class="sxs-lookup"><span data-stu-id="33c11-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Ændre visningen fra Aktiverede brugere til Programbrugere](media/sales-map-enabled-users.png)

4. <span data-ttu-id="33c11-212">Vælg de to poster for **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="33c11-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste over programbrugere](media/sales-map-user-mode.png)

5. <span data-ttu-id="33c11-214">Ret værdien i feltet **Integrationsbrugertilstand** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="33c11-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Ændre værdien i feltet Integrationsbrugertilstand](media/sales-map-user-mode-yes.png)

<span data-ttu-id="33c11-216">Dine salgsordrer er nu tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="33c11-216">Your sales orders are now mapped.</span></span>
