---
title: Oprette en Excel-projektmappe for at redigere detailtransaktioner
description: Dette emne beskriver, hvordan du opretter en Excel-projektmappe, så du kan redigere detailtransaktioner i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458728"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="5489c-103">Oprette en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="5489c-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5489c-104">Dette emne beskriver, hvordan du opretter en Excel-projektmappe, så du kan redigere detailtransaktioner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5489c-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5489c-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="5489c-105">Overview</span></span>

<span data-ttu-id="5489c-106">Der er en foruddefineret Excel-skabelon, som kunder kan få adgang til fra forskellige dele af systemet og bruge til at redigere og overvåge detailtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5489c-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="5489c-107">Kunder kan også oprette en brugerdefineret Excel-projektmappe til dette formål.</span><span class="sxs-lookup"><span data-stu-id="5489c-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="5489c-108">Oprette og konfigurere en Excel-projektmappe</span><span class="sxs-lookup"><span data-stu-id="5489c-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="5489c-109">Hvis du vil oprette og konfigurere en Excel-projektmappe, så du kan redigere detailtransaktioner, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5489c-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="5489c-110">Åbn Excel, og opret en tom projektmappe.</span><span class="sxs-lookup"><span data-stu-id="5489c-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="5489c-111">Vælg **Mine tilføjelsesprogrammer** på fanen **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="5489c-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="5489c-112">Vælg linket **Tilføj serveroplysninger** i højre rude.</span><span class="sxs-lookup"><span data-stu-id="5489c-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="5489c-113">Angiv URL-adressen til serveren, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5489c-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="5489c-114">Hvis du modtager fejlmeddelelsen "Der blev ikke fundet nogen applet-registreringer", skal du følge disse trin for at løse problemet:</span><span class="sxs-lookup"><span data-stu-id="5489c-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="5489c-115">I Commerce skal du gå til **Systemadministration \> Opsætning \> Parametre for Office-apps**.</span><span class="sxs-lookup"><span data-stu-id="5489c-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="5489c-116">Vælg **Initialiser app-parametre** på oversigtspanelet **App-parametre**.</span><span class="sxs-lookup"><span data-stu-id="5489c-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="5489c-117">Vælg **OK** i boksen med bekræftelsesmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="5489c-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="5489c-118">Vælg **Initialiser applet-registrering** på oversigtspanelet **Registrerede applets**.</span><span class="sxs-lookup"><span data-stu-id="5489c-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="5489c-119">Gentag de forrige tre trin efter behov.</span><span class="sxs-lookup"><span data-stu-id="5489c-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="5489c-120">Vælg **Design**, og vælg derefter **Tilføj tabel**.</span><span class="sxs-lookup"><span data-stu-id="5489c-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="5489c-121">På baggrund af de data, der skal ændres, skal du vælge de enheder, der skal føjes til Excel-projektmappen til redigering.</span><span class="sxs-lookup"><span data-stu-id="5489c-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="5489c-122">Brug følgende tabel som reference.</span><span class="sxs-lookup"><span data-stu-id="5489c-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="5489c-123">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="5489c-123">Transaction type</span></span> | <span data-ttu-id="5489c-124">Dataenheder, der skal bruges</span><span class="sxs-lookup"><span data-stu-id="5489c-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="5489c-125">Cash and carry-transaktioner, onlineordrer, asynkrone kundeordrer, asynkrone kundetilbud</span><span class="sxs-lookup"><span data-stu-id="5489c-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="5489c-126">Transaktion (reviderbar), salgstransaktion (reviderbar), betalingstransaktioner (reviderbare), momstransaktioner (reviderbare), rabattransaktioner (reviderbare), gebyrtransaktioner (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="5489c-127">Indsættelse i banken</span><span class="sxs-lookup"><span data-stu-id="5489c-127">Bank drop</span></span> | <span data-ttu-id="5489c-128">Transaktion (reviderbar), betalingsmiddeltransaktioner i banken (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5489c-129">Deponering til pengeskab</span><span class="sxs-lookup"><span data-stu-id="5489c-129">Safe drop</span></span> | <span data-ttu-id="5489c-130">Transaktion (reviderbar), betalingsmiddeltransaktioner lagt i pengeskab (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5489c-131">Kasseoptælling</span><span class="sxs-lookup"><span data-stu-id="5489c-131">Tender declaration</span></span> | <span data-ttu-id="5489c-132">Transaktion (reviderbar), betalingsmiddeltransaktioner med kasseoptælling (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="5489c-133">Indtægt, udgift</span><span class="sxs-lookup"><span data-stu-id="5489c-133">Income, Expense</span></span> | <span data-ttu-id="5489c-134">Transaktioner (reviderbare), indkomst-/udgiftstransaktioner (reviderbare), betalingstransaktioner (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="5489c-135">Angive startbeløb, fjernelse af betalingsmiddel, kassebeholdning, betalingsmiddel for byttepenge, fakturabetaling, kundeindbetalinger</span><span class="sxs-lookup"><span data-stu-id="5489c-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="5489c-136">Transaktion (reviderbar), betalingstransaktioner (reviderbare)</span><span class="sxs-lookup"><span data-stu-id="5489c-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="5489c-137">Det er vigtigt, at du kun føjer én dataenhed til hver enkelt Excel-projektmappe.</span><span class="sxs-lookup"><span data-stu-id="5489c-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="5489c-138">Desuden skal alle felter, der er markeret med et nøglesymbol, føjes til den relevante projektmappe.</span><span class="sxs-lookup"><span data-stu-id="5489c-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="5489c-139">Når projektmappen er konfigureret, skal du anvende de påkrævede filtre.</span><span class="sxs-lookup"><span data-stu-id="5489c-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="5489c-140">Sørg for at anvende de samme filtre på alle regneark i filen.</span><span class="sxs-lookup"><span data-stu-id="5489c-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="5489c-141">Undgå at indlæse meget store datamængder i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="5489c-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="5489c-142">Ellers kan ydeevnen påvirkes, og Excel og dit system kan blive langsommere.</span><span class="sxs-lookup"><span data-stu-id="5489c-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="5489c-143">Det anbefales, at du altid bruger "Firma" og enten "Opgørelsesnummer" eller "Transaktionsnummer" som filtre til filen.</span><span class="sxs-lookup"><span data-stu-id="5489c-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="5489c-144">Når filtrene er konfigureret, skal du vælge **Opdater** for at indlæse dataene.</span><span class="sxs-lookup"><span data-stu-id="5489c-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="5489c-145">Rediger de nødvendige data, og publicer dem derefter.</span><span class="sxs-lookup"><span data-stu-id="5489c-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="5489c-146">Hvis knappen **Publicer** ikke er tilgængelig, er nogle nøglefelter sandsynligvis ikke føjet til Excel-projektmappen.</span><span class="sxs-lookup"><span data-stu-id="5489c-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5489c-147">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5489c-147">Additional resources</span></span>

[<span data-ttu-id="5489c-148">Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="5489c-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="5489c-149">Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="5489c-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="5489c-150">Redigere økonomiske dimensioner for detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="5489c-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="5489c-151">Føje felter til en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="5489c-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
