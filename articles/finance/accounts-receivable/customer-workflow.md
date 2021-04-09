---
title: Arbejdsgang for kunde
description: Dette emne indeholder oplysninger om arbejdsgangen for kunden. Du kan ændre bestemte felter for en kunde og derefter sende ændringerne til godkendelse ved hjælp af arbejdsgangen, inden de føjes til kunden.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c769d225ee0f7b35719c37d9b9bc690a20060911
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817263"
---
# <a name="customer-workflow"></a><span data-ttu-id="68cdc-104">Arbejdsgang for kunde</span><span class="sxs-lookup"><span data-stu-id="68cdc-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68cdc-105">Arbejdsgangen for kunde er føjet til version 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="68cdc-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="68cdc-106">Du kan ændre specifikke felter for en kunde, og derefter sende disse ændringer til godkendelse ved hjælp af arbejdsgangen, før de tilføjes til kunden.</span><span class="sxs-lookup"><span data-stu-id="68cdc-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="68cdc-107">Konfigurer kundens arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="68cdc-107">Set up the customer workflow</span></span>

<span data-ttu-id="68cdc-108">Før du kan bruge funktionen for kundens arbejdsgang, skal du aktivere den.</span><span class="sxs-lookup"><span data-stu-id="68cdc-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="68cdc-109">Gå til **Debitor \> Opsætning \> Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="68cdc-110">På fanen **Generelt** i oversigtspanelet **Kundegodkendelse** skal du angive indstillingen **Aktivér kundegodkendelser** til **Ja** for at aktivere funktionen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="68cdc-111">I feltet **Dataenheds funktionalitet**, skal du vælge den funktionalitet, som dataenhederne skal bruge, når data importeres:</span><span class="sxs-lookup"><span data-stu-id="68cdc-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="68cdc-112">**Tillad ændringer uden godkendelse** – En enhed kan opdatere kundeposten uden at behandle den via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="68cdc-113">**Afvis ændringer** – Ændringerne kan ikke foretage ændringer i kundeposten.</span><span class="sxs-lookup"><span data-stu-id="68cdc-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="68cdc-114">Importen vil mislykkes for de felter, der er aktiveret for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="68cdc-115">**Opret forslag til ændring** – Alle felter ændres, undtagen de felter, der er aktiveret for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="68cdc-116">De nye værdier for disse felter vil blive føjet til kunden som forslag til ændringer, og arbejdsgangen startes automatisk.</span><span class="sxs-lookup"><span data-stu-id="68cdc-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="68cdc-117">På listen over felter for kunden, skal du derefter vælge afkrydsningsfeltet **Aktivér** for hvert felt, der skal godkendes, før ændringerne kan foretages.</span><span class="sxs-lookup"><span data-stu-id="68cdc-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="68cdc-118">Gå til **Debitor \> Opsætning \> Debitorarbejdsgange**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="68cdc-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-119">Select **New**.</span></span>
7. <span data-ttu-id="68cdc-120">Vælg **Arbejdsgang for forslag til ændring af kunde**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="68cdc-121">Konfigurer arbejdsgangen, så den passer til din godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="68cdc-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="68cdc-122">Elementet for godkendelsen af arbejdsgangen **Arbejdsgangsgodkendelse af forslag til ændring af kunde** aktiverer ændringerne for kunden.</span><span class="sxs-lookup"><span data-stu-id="68cdc-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="68cdc-123">Rediger kundeoplysninger, og send ændringerne af arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="68cdc-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="68cdc-124">Når du ændrer et felt, der er aktiveret for arbejdsgangen, vises siden **Forslag til ændringer**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="68cdc-125">Denne side viser den oprindelige værdi i feltet og den nye værdi, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="68cdc-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="68cdc-126">Det felt, du ændrede, vender tilbage til den oprindelige værdi.</span><span class="sxs-lookup"><span data-stu-id="68cdc-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="68cdc-127">En statusmeddelelse på siden fortæller dig, at dine ændringer ikke er blevet sendt.</span><span class="sxs-lookup"><span data-stu-id="68cdc-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="68cdc-128">Hver gang du ændrer et felt, der er aktiveret for arbejdsgangen, føjes feltet til listen over foreslåede ændringer.</span><span class="sxs-lookup"><span data-stu-id="68cdc-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="68cdc-129">Hvis du vil udelade den foreslåede værdi for et felt, kan du bruge knappen **Udelad** ved siden af feltet på listen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="68cdc-130">Hvis du vil udelade alle ændringer, skal du bruge knappen **Udelad alle ændringer** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="68cdc-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="68cdc-131">Vælg **OK** for at lukke siden.</span><span class="sxs-lookup"><span data-stu-id="68cdc-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="68cdc-132">Når du har mindst én foreslået ændring, vises der yderligere to menuer i handlingsruden: **Forslag til ændringer** og **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="68cdc-133">Vælg **Forslag til ændringer** for at åbne siden **Forslag til ændringer** og gennemse dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="68cdc-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="68cdc-134">Vælg **Arbejdsgang \> Send** for at sende ændringerne af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="68cdc-135">Status på siden ændres til **Ændringer, der afventer godkendelse**.</span><span class="sxs-lookup"><span data-stu-id="68cdc-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="68cdc-136">Arbejdsgangen følger standardprocessen for arbejdsgang i ansøgningen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="68cdc-137">Godkenderen dirigeres til siden **Kunde**, hvor ændringerne kan gennemgås på siden **Forslag til ændringer**. Vælg derefter **Arbejdsgang \> Godkend** for at godkende arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="68cdc-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="68cdc-138">Når alle godkendelser er fuldført, opdateres felterne med de værdier, du foreslog.</span><span class="sxs-lookup"><span data-stu-id="68cdc-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]