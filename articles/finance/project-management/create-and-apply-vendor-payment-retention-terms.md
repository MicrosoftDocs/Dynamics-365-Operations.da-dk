---
title: Oprette og anvende betingelser for tilbageholdelse af kreditorbetaling
description: Dette afsnit indeholder oplysninger om konfiguration og vedligeholdelse af betingelserne for tilbageholdelse af kreditorbetalinger.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410205"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="3d134-103">Oprette og anvende betingelser for tilbageholdelse af kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="3d134-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="3d134-104">Opsætning af betingelser for tilbageholdelse af kreditorbetalinger for et projekt er nyttig, når organisationen vil tilbageholde en del af de betalinger, der foretages til en kreditor.</span><span class="sxs-lookup"><span data-stu-id="3d134-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="3d134-105">Når du f.eks. ønsker at tilbageholde betalingen til en leverandør, indtil de leverede produkter opfylder dine forventninger.</span><span class="sxs-lookup"><span data-stu-id="3d134-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="3d134-106">Betingelserne for tilbageholdelse af kreditorbetalinger kan specificeres, når du forhandler en kreditorkontrakt.</span><span class="sxs-lookup"><span data-stu-id="3d134-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="3d134-107">Oprette tilbageholdelsesbetingelser for kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="3d134-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="3d134-108">Du kan angive en procentdel af en kreditorbetaling, som du vil tilbageholde, og den procentdel af tidligere tilbageholdte beløb, som du vil frigive.</span><span class="sxs-lookup"><span data-stu-id="3d134-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="3d134-109">Der tilbageholdes automatisk beløb for kreditorfakturaer, indtil kontrakten har nået det angivne færdiggørelsesniveau.</span><span class="sxs-lookup"><span data-stu-id="3d134-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="3d134-110">Når du har konfigureret tilbageholdelsesbetingelserne, kan du anvende dem på ethvert af projekterne for den pågældende kreditor.</span><span class="sxs-lookup"><span data-stu-id="3d134-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="3d134-111">Brug følgende trin til at konfigurere og vedligeholde tilbageholdelsesbetingelser for kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="3d134-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="3d134-112">Gå til **Projektstyring og regnskab** > **Tilbageholdelse** > **Tilbageholdelsesbetingelser for kreditorbetaling**.</span><span class="sxs-lookup"><span data-stu-id="3d134-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="3d134-113">Vælg **Ny** for at tilføje en ny kreditortilbageholdelsesbetingelse.</span><span class="sxs-lookup"><span data-stu-id="3d134-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="3d134-114">Værdien for **Regel-id** for den nye betingelse angives automatisk.</span><span class="sxs-lookup"><span data-stu-id="3d134-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="3d134-115">Angiv en kort beskrivelse i feltet **Beskrivelse**, og vælg **Betingelser** i oversigtspanelet. Vælg **Tilføj linje** for at angive betingelsesværdier for følgende:</span><span class="sxs-lookup"><span data-stu-id="3d134-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="3d134-116">**Procentdel af leverede enheder**: Angiv en færdiggørelsesprocent for betingelsen.</span><span class="sxs-lookup"><span data-stu-id="3d134-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="3d134-117">Beløb tilbageholdes automatisk for kreditorfakturaer, indtil projektstadiet for færdiggørelse er lig med den specificerede procentdel.</span><span class="sxs-lookup"><span data-stu-id="3d134-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="3d134-118">Hvis du f.eks. skriver 50,00, tilbageholdes beløb, indtil 50 % af projektet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3d134-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="3d134-119">**Procentdel, der skal tilbageholdes**: Angiv den procentdel af beløbet på en kreditorfaktura, der skal tilbageholdes.</span><span class="sxs-lookup"><span data-stu-id="3d134-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="3d134-120">Hvis du f.eks. skriver 10,00, tilbageholdes 10 procent af beløbet på en kreditorfaktura, indtil projektet når den færdiggørelsesgrad, der er indstillet i feltet **Procentdel af leverede enheder**.</span><span class="sxs-lookup"><span data-stu-id="3d134-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="3d134-121">**Procentdel, der skal frigives**: Vælg **Tilføj linje** for at angive en procentdel af eventuelle tidligere tilbageholdte beløb, der skal frigives på det valgte færdiggørelsesniveau for projektet.</span><span class="sxs-lookup"><span data-stu-id="3d134-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="3d134-122">Hvis du har mere end én milepæl for forskellige niveauer af projektfærdiggørelse, skal du angive en særskilt kreditortilbagholdelsesbetingelseslinje for hver tilbageholdelsesregel.</span><span class="sxs-lookup"><span data-stu-id="3d134-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="3d134-123">Hver linje kan angive en særskilt tilbageholdelsesprocentdel og en særskilt frigivelsesprocentdel for hvert angivet niveau af projektfærdiggørelse.</span><span class="sxs-lookup"><span data-stu-id="3d134-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="3d134-124">Når du har oprettet tilbageholdelsesbetingelser for en kreditor, kan du anvende betingelserne på et projekt.</span><span class="sxs-lookup"><span data-stu-id="3d134-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="3d134-125">Anvende kreditortilbageholdelsesbetingelser på et projekt</span><span class="sxs-lookup"><span data-stu-id="3d134-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="3d134-126">Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**, og åbn et projekt på siden projektliste.</span><span class="sxs-lookup"><span data-stu-id="3d134-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="3d134-127">I oversigtpanelet **Kreditoraftaler** skal du vælge **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="3d134-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="3d134-128">Vælg én af følgende indstillinger i feltet **Kontokode**:</span><span class="sxs-lookup"><span data-stu-id="3d134-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="3d134-129">**Tabel**: Kreditortilbageholdelsesbetingelserne gælder for en enkelt kreditor.</span><span class="sxs-lookup"><span data-stu-id="3d134-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="3d134-130">**Gruppe**: Kreditortilbageholdelsesbetingelserne gælder for alle kreditorer i en kreditorgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d134-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="3d134-131">**Alle**; Kreditortilbageholdelsesbetingelserne gælder for alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="3d134-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="3d134-132">I feltet **Kreditor/Kreditorgruppe** skal du vælge den kreditor eller kreditorgruppe, som kreditortilbageholdelsesbetingelserne gælder for.</span><span class="sxs-lookup"><span data-stu-id="3d134-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="3d134-133">Hvis du har valgt **Alle** i det foregående trin, er dette felt ikke tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="3d134-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="3d134-134">I feltet **Kreditortilbageholdelsesbetingelser** skal du vælge den tilbageholdelsesbetingelse, som du oprettede under den forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="3d134-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="3d134-135">Hvis projektet også har betingelser for betal ved betaling konfigureret for kreditoren, skal du angive grænseprocenten for projektet i feltet **Grænseværdi for Betal ved betaling i procent**.</span><span class="sxs-lookup"><span data-stu-id="3d134-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="3d134-136">Betingelser for tilbageholdelse af kreditorbetaling vises også på indkøbsordrer, som du opretter for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="3d134-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
