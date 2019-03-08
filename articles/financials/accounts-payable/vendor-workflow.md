---
title: Arbejdsgang for kreditorer
description: Rediger leverandøroplysninger, og brug arbejdsgange til at godkende dem.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "329683"
---
# <a name="vendor-workflow"></a><span data-ttu-id="a1ab2-103">Arbejdsgang for kreditorer</span><span class="sxs-lookup"><span data-stu-id="a1ab2-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1ab2-104">Når arbejdsgangen for kreditorer bruges, sendes ændringer, der er foretaget af bestemte felter, til arbejdsgangen til godkendelse, inden de føjes til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="a1ab2-105">Konfigurere kreditorarbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="a1ab2-105">Set up the vendor workflow</span></span>

<span data-ttu-id="a1ab2-106">Du skal aktivere arbejdsgangfunktionen, før du kan bruge den.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="a1ab2-107">Gå til **Kreditor \> Opsætning \> Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="a1ab2-108">Under fanen **Generelt** på oversigtspanelet **Kreditorgodkendelse** skal du vælge **Ja** i indstillingen **Aktivér kreditorgodkendelser**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="a1ab2-109">I feltet **Dataenheds funktionalitet** skal du vælge den funktionalitet, der skal bruges, når data importeres:</span><span class="sxs-lookup"><span data-stu-id="a1ab2-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="a1ab2-110">**Tillade ændringer uden godkendelse** – Dataenheden kan opdatere kreditorposten uden at behandle den via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="a1ab2-111">**Afvis ændringer** – Der kan ikke foretages ændringer af kreditorposten.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="a1ab2-112">For de felter, der er aktiveret for arbejdsgangen, mislykkes importen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="a1ab2-113">**Opret forslag til ændring** – Alle felter ændres undtagen de felter, der er aktiveret til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="a1ab2-114">De nye værdier for disse felter bliver føjet til kreditoren som foreslåede ændringer, og arbejdsprocessen startes automatisk.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="a1ab2-115">På listen over kreditorfelter skal du markere afkrydsningsfeltet **Aktivér** for hvert felt, der skal godkendes, før ændringerne kan udføres.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="a1ab2-116">Gå til **Kreditor \> Opsætning \> Kreditorarbejdsgange**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="a1ab2-117">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-117">Select **New**.</span></span>
7. <span data-ttu-id="a1ab2-118">Vælg **Arbejdsgang for forslag til ændring af kreditor**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="a1ab2-119">Konfigurer arbejdsgangen, så den passer til godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="a1ab2-120">Elementet til godkendelse af arbejdsgangen **Arbejdsgangsgodkendelse af forslag til ændring af kreditor** anvender ændringerne på kreditoren.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="a1ab2-121">Ændre kreditoroplysninger og sende ændringerne til arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="a1ab2-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="a1ab2-122">Når du ændrer et felt, der er aktiveret for arbejdsgangen, vises siden **Foreslåede ændringer**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="a1ab2-123">Denne side viser den oprindelige værdi i feltet og den nye værdi, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="a1ab2-124">Det felt, du har ændret, vender tilbage til den oprindelige værdi.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="a1ab2-125">En statusmeddelelse fortæller dig også, at ændringerne ikke er sendt.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="a1ab2-126">Hver gang du ændrer et felt, der er aktiveret for arbejdsgangen, føjes dette felt til listen på siden **Foreslåede ændringer**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="a1ab2-127">For at slette den foreslåede værdi for et felt kan du bruge knappen **Slet** ud for feltet på listen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="a1ab2-128">Hvis du vil slette alle ændringer, skal du bruge knappen **Udelad alle ændringer** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="a1ab2-129">Vælg **OK** for at lukke siden.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="a1ab2-130">Når du har mindst én foreslåede ændring, vises der to ekstra faner i handlingsruden: **Foreslåede ændringer** og **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="a1ab2-131">Vælg **Foreslåede ændringer** for at åbne siden **Foreslåede ændringer** og se dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="a1ab2-132">Vælg **Arbejdsgang \> Send for at sende ændringerne til arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="a1ab2-133">Status på siden ændres til **Ændringer, der afventer godkendelse**.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="a1ab2-134">Arbejdsgangen følger standardarbejdsgangsprocessen i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a1ab2-135">Godkenderen sendes til siden **Kreditor**, hvor han eller hun kan gennemgå ændringerne på siden **Foreslåede ændringer** og derefter vælge **Arbejdsgang \> Godkend** for at godkende arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="a1ab2-136">Når alle godkendelser er fuldført, opdateres felterne med de værdier, du foreslog.</span><span class="sxs-lookup"><span data-stu-id="a1ab2-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
