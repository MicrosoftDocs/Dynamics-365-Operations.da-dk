---
title: Behandling af udgiftskvittering
description: Dette emne indeholder oplysninger om behandling af kvitteringer med brug af optisk tegngenkendelse (OCR). Denne funktion er beregnet til at forbedre brugeroplevelsen, når der oprettes udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154034"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="69d4f-104">Behandling af udgiftskvittering</span><span class="sxs-lookup"><span data-stu-id="69d4f-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="69d4f-105">Udgiftsregistrering er blevet forbedret via indførelsen af OCR-behandling (optisk tegngenkendelse) af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="69d4f-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="69d4f-106">Denne funktion er beregnet til at forbedre brugeroplevelsen, når der oprettes udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="69d4f-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="69d4f-107">Hovedfunktioner</span><span class="sxs-lookup"><span data-stu-id="69d4f-107">Key features</span></span>

- <span data-ttu-id="69d4f-108">Forhandlerens navn, dato og det samlede beløb udtrækkes fra kvitteringerne.</span><span class="sxs-lookup"><span data-stu-id="69d4f-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="69d4f-109">Funktionen forsøger at afstemme ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="69d4f-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="69d4f-110">Brugerne kan oprette manuelt indtastede udgiftstransaktioner fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="69d4f-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="69d4f-111">Eksempler på anvendelse</span><span class="sxs-lookup"><span data-stu-id="69d4f-111">Usage examples</span></span>

- <span data-ttu-id="69d4f-112">**Tilknyt automatisk kvitteringer, der indeholder kreditkorttransaktioner, når der oprettes en udgiftsrapport.**</span><span class="sxs-lookup"><span data-stu-id="69d4f-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="69d4f-113">Åbn arbejdsområdet **Udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="69d4f-114">Kontroller under fanen **Kvitteringer**, at der findes ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="69d4f-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="69d4f-115">Du kan også overføre kvitteringer under fanen **Kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="69d4f-116">Under fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter.</span><span class="sxs-lookup"><span data-stu-id="69d4f-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="69d4f-117">Udgiftsadministratoren importerer typisk disse udgifter fra udbyderen af kreditkortet.</span><span class="sxs-lookup"><span data-stu-id="69d4f-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="69d4f-118">Vælg **Ny udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-118">Select **New expense report**.</span></span> <span data-ttu-id="69d4f-119">Bemærk, at du nu også kan medtage udgifter og kvitteringer, når du opretter en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="69d4f-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="69d4f-120">Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer med udgifter.</span><span class="sxs-lookup"><span data-stu-id="69d4f-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="69d4f-121">**Opret en udgift, eller afstem en udgift fra en kvittering.**</span><span class="sxs-lookup"><span data-stu-id="69d4f-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="69d4f-122">I en udgiftsrapport skal du under fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="69d4f-123">Bemærk indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="69d4f-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="69d4f-124">Vælg **Opret** for at oprette en manuelt indtaste udgiftstransaktion, og indsæt de værdier, der er udtrukket fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="69d4f-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="69d4f-125">Hvis du vælger **Afstem**, forsøger systemet at afstemme en eksisterende udgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="69d4f-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="69d4f-126">Installation</span><span class="sxs-lookup"><span data-stu-id="69d4f-126">Installation</span></span>

<span data-ttu-id="69d4f-127">Denne funktion fungerer sammen med funktionen **Udgiftsrapporter nyfortolkede** for at gøre udgiftsangivelsesoplevelsen mere enkel.</span><span class="sxs-lookup"><span data-stu-id="69d4f-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="69d4f-128">Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til Udgiftsstyring-tjeneste til Microsoft Dynamics 365 Finance, og aktivere funktionerne i din forekomst.</span><span class="sxs-lookup"><span data-stu-id="69d4f-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="69d4f-129">Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="69d4f-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="69d4f-130">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="69d4f-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="69d4f-131">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="69d4f-132">Vælg **Vedligehold**, eller rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="69d4f-133">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="69d4f-134">Vælg **Udgiftsstyring-tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="69d4f-135">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="69d4f-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="69d4f-136">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-136">Select **Install**.</span></span>

<span data-ttu-id="69d4f-137">I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="69d4f-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="69d4f-138">Udgiftsrapporter nyfortolkede</span><span class="sxs-lookup"><span data-stu-id="69d4f-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="69d4f-139">Match og opret udgift automatisk fra tilgang</span><span class="sxs-lookup"><span data-stu-id="69d4f-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="69d4f-140">Når du aktiverer disse funktioner, udføres følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="69d4f-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="69d4f-141">Det eksisterende arbejdsområde **Udgiftsstyring** erstattes med det nye arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="69d4f-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="69d4f-142">Der tilføjes et nyt menupunkt for synlighed af udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="69d4f-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="69d4f-143">Du kan stadig åbne den tidligere side **Udgiftsrapporter** ved at gå til **Udgiftsstyring > Mine udgifter > Udgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="69d4f-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="69d4f-144">Arbejdsgange og eventuelle godkendelser fører stadig til den eksisterende side med udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="69d4f-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="69d4f-145">Kvitteringer vil blive behandlet via Microsoft Azure Cognitive Services, og metadata vil blive udtrukket og tilføjet.</span><span class="sxs-lookup"><span data-stu-id="69d4f-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="69d4f-146">Der tilføjes en indstilling, du kan bruge til at oprette en udgiftsrapport, der indeholder afstemte ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="69d4f-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="69d4f-147">En indstilling, der føjes til udgiftsrapporter, giver dig mulighed for at oprette en udgiftslinje ud fra en kvittering eller forsøge at afstemme en eksisterende kvittering med en eksisterende udgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="69d4f-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="69d4f-148">Yderligere oplysninger om den nyfortolkede funktion til udgiftsrapporter finder du i [Udgiftsrapporter i nyfortolkning](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="69d4f-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="69d4f-149">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="69d4f-149">Frequently asked questions</span></span>

<span data-ttu-id="69d4f-150">**Bruger Microsoft mine data til sine modeller?**</span><span class="sxs-lookup"><span data-stu-id="69d4f-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="69d4f-151">Nej, Microsoft har udviklet en generel model til maskinel indlæring til tjenesten til behandling af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="69d4f-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="69d4f-152">Denne model er ikke baseret på de kvitteringer, du overfører.</span><span class="sxs-lookup"><span data-stu-id="69d4f-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="69d4f-153">**Hvor er denne funktion tilgængelig, og hvor behandles den?**</span><span class="sxs-lookup"><span data-stu-id="69d4f-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="69d4f-154">I øjeblikket understøttes USA.</span><span class="sxs-lookup"><span data-stu-id="69d4f-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="69d4f-155">**Hvor sendes mine kvitteringer hen?**</span><span class="sxs-lookup"><span data-stu-id="69d4f-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="69d4f-156">Finance kontakter Cognitive Services for at udtrække feltdata.</span><span class="sxs-lookup"><span data-stu-id="69d4f-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="69d4f-157">Cognitive Services bevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår.</span><span class="sxs-lookup"><span data-stu-id="69d4f-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="69d4f-158">Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="69d4f-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="69d4f-159">Kvitteringer gemmes stadig i Finance.</span><span class="sxs-lookup"><span data-stu-id="69d4f-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="69d4f-160">Du kan finde flere oplysninger [Få forståelse af kvitteringer med ny funktion i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="69d4f-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
