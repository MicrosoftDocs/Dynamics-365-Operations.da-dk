---
title: Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner
description: Dette emne beskriver, hvordan du redigerer og overvåger onlineordre- og asynkrone kundeordretransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458726"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="351da-103">Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="351da-104">Dette emne beskriver, hvordan du redigerer og overvåger onlineordre- og asynkrone kundeordretransaktioner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="351da-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="351da-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="351da-105">Overview</span></span>

<span data-ttu-id="351da-106">Fra Commerce-version 10.0.5 til 10.0.6 er der tilføjet understøttelse for redigering af cash and carry-transaktioner (f.eks. salg og returneringer) og kassestyringstransaktioner (f.eks. kassebeholdning og fjernelse af betalingsmiddel).</span><span class="sxs-lookup"><span data-stu-id="351da-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="351da-107">I Commerce version 10.0.7 blev der tilføjet understøttelse for redigering af onlineordretransaktioner og asynkrone kundeordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="351da-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="351da-108">Redigere og overvåge ordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-108">Edit and audit order transactions</span></span>

<span data-ttu-id="351da-109">Hvis du vil redigere og overvåge ordretransaktioner i hovedkontoret Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="351da-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="351da-110">Installér [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="351da-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="351da-111">På siden **Detailparametre** på fanen **Kundeordrer** i oversigtspanelet **Ordre** skal du angive en holdkode for **Holdkode for ordresynkroniseringsfejl**.</span><span class="sxs-lookup"><span data-stu-id="351da-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="351da-112">Åbn arbejdsområdet **Butiksregnskab**.</span><span class="sxs-lookup"><span data-stu-id="351da-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="351da-113">Felterne **Onlineordresynkroniseringsfejl** og **Kundeordresynkronisering** indeholder en forudfiltreret visning af detailtransaktionssiden.</span><span class="sxs-lookup"><span data-stu-id="351da-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="351da-114">Hver enkelt viser de transaktionsposter, hvor synkroniseringen mislykkedes for den tilsvarende ordretype.</span><span class="sxs-lookup"><span data-stu-id="351da-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="351da-115">Åbn enten siden **Onlineordresynkroniseringsfejl** eller siden **Kundeordresynkroniseringsfejl**.</span><span class="sxs-lookup"><span data-stu-id="351da-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="351da-116">Vælg en post for at få vist oplysninger om synkroniseringsfejlen.</span><span class="sxs-lookup"><span data-stu-id="351da-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="351da-117">Oversigtspanelet **Synkroniseringsstatus** viser følgende fejloplysninger:</span><span class="sxs-lookup"><span data-stu-id="351da-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="351da-118">Ventende ordrestatus</span><span class="sxs-lookup"><span data-stu-id="351da-118">Pending order status</span></span>
    - <span data-ttu-id="351da-119">Oplysninger om ordrefejl</span><span class="sxs-lookup"><span data-stu-id="351da-119">Order error details</span></span>
    - <span data-ttu-id="351da-120">Dato og klokkeslæt for ændring</span><span class="sxs-lookup"><span data-stu-id="351da-120">Modified date and time</span></span>
    - <span data-ttu-id="351da-121">Antal forsøg</span><span class="sxs-lookup"><span data-stu-id="351da-121">Retry count</span></span>

1. <span data-ttu-id="351da-122">Hvis fejloplysningerne indikerer, at posten skal rettes, skal du vælge **Office-tilføjelsesprogram** og derefter vælge **Rediger den valgte transaktion**.</span><span class="sxs-lookup"><span data-stu-id="351da-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="351da-123">En Excel-fil, der viser oplysningerne om den valgte transaktion, åbnes.</span><span class="sxs-lookup"><span data-stu-id="351da-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="351da-124">Hvis den transaktion, der redigeres, er en onlineordretransaktion, indeholder Excel-filen følgende regneark:</span><span class="sxs-lookup"><span data-stu-id="351da-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="351da-125">**Transaktioner** – dette regneark indeholder oplysningerne for transaktionen på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="351da-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="351da-126">**Salgstransaktioner** – dette regneark indeholder oplysningerne for transaktionen på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="351da-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="351da-127">**Betalingstransaktioner** – dette regneark indeholder oplysningerne om transaktionens betalingslinjer.</span><span class="sxs-lookup"><span data-stu-id="351da-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="351da-128">**Rabattransaktioner** – dette regneark indeholder de rabatrelaterede oplysninger for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="351da-129">**Momstransaktioner** – dette regneark indeholder de momsrelaterede oplysninger for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="351da-130">**Gebyrtransaktioner** – dette regneark indeholder de gebyrrelaterede data for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="351da-131">Hvis den transaktion, der redigeres, er en asynkron kundeordretransaktion, indeholder Excel-filen følgende regneark:</span><span class="sxs-lookup"><span data-stu-id="351da-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="351da-132">**Linjer** – dette regneark indeholder oplysningerne for transaktionen på hoved- og linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="351da-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="351da-133">**Betalinger** – dette regneark indeholder oplysningerne om transaktionens betalingslinjer.</span><span class="sxs-lookup"><span data-stu-id="351da-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="351da-134">**Rabatter** – dette regneark indeholder de rabatrelaterede detaljer for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="351da-135">**Moms** – dette regneark indeholder de momsrelaterede detaljer for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="351da-136">**Gebyrer** – dette regneark indeholder de gebyrrelaterede data for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="351da-137">I Excel-filen i feltet **Ventende ordrestatus** skal du angive **Redigering** og derefter publicere ændringen.</span><span class="sxs-lookup"><span data-stu-id="351da-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="351da-138">På denne måde forhindrer du, at jobbet **Synkroniser ordre**, der kører i batchtilstand, springer denne post over under behandlingen.</span><span class="sxs-lookup"><span data-stu-id="351da-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="351da-139">I Excel-filen redigerer du de relevante felter og overfører derefter dataene tilbage til hovedkontoret Commerce ved hjælp af publiceringsfunktionen i Dynamics Excel-tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="351da-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="351da-140">Når dataene er publiceret, afspejles ændringerne i systemet.</span><span class="sxs-lookup"><span data-stu-id="351da-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="351da-141">Under publiceringen sker der ingen validering for de ændringer, brugerne foretager.</span><span class="sxs-lookup"><span data-stu-id="351da-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="351da-142">Du kan få vist et komplet revisionsspor for ændringerne ved at vælge **Vis revisionsspor** i hovedet på **detailtransaktionen** for ændringerne på hovedniveau og i den relevante sektion og post på den relevante transaktionsside.</span><span class="sxs-lookup"><span data-stu-id="351da-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="351da-143">Alle ændringer, der f.eks. er relateret til salgslinjer, vises på siden **Salgstransaktioner**, og alle ændringer, der er relateret til betalinger, vises på siden **Betalingstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="351da-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="351da-144">Følgende revisionsoplysninger bevares for ændringerne:</span><span class="sxs-lookup"><span data-stu-id="351da-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="351da-145">Dato og klokkeslæt for ændring</span><span class="sxs-lookup"><span data-stu-id="351da-145">Modified date and time</span></span>
    - <span data-ttu-id="351da-146">Felt</span><span class="sxs-lookup"><span data-stu-id="351da-146">Field</span></span>
    - <span data-ttu-id="351da-147">Gammel værdi</span><span class="sxs-lookup"><span data-stu-id="351da-147">Old value</span></span>
    - <span data-ttu-id="351da-148">Ny værdi</span><span class="sxs-lookup"><span data-stu-id="351da-148">New value</span></span>
    - <span data-ttu-id="351da-149">Ændret af</span><span class="sxs-lookup"><span data-stu-id="351da-149">Modified by</span></span>

1. <span data-ttu-id="351da-150">Når du har foretaget og publiceret ændringerne, skal du vælge **Synkroniser ordre** for at starte synkroniseringsprocessen med det samme.</span><span class="sxs-lookup"><span data-stu-id="351da-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="351da-151">Du kan også vente på, at synkroniseringsprocessen, der kører i batchtilstand, behandler transaktionen.</span><span class="sxs-lookup"><span data-stu-id="351da-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="351da-152">Når ordrerne er synkroniseret, sættes de som standard i en holdstatus baseret på den holdkode, der er defineret i Commerce-parametrene.</span><span class="sxs-lookup"><span data-stu-id="351da-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="351da-153">Holdstatussen på ordrerne skal fjernes, før de kan behandles yderligere til opfyldelse eller andre aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="351da-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="351da-154">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="351da-154">Additional resources</span></span>

[<span data-ttu-id="351da-155">Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="351da-156">Redigere økonomiske dimensioner for detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="351da-157">Oprette en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="351da-158">Føje felter til en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="351da-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
