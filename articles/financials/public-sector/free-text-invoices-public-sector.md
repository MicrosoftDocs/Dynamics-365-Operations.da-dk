---
title: Fritekstfakturaer i den offentlige sektor
description: I dette emne beskrives funktionen til fritekstfakturaer, som er tilgængelig for den offentlige sektor, samt besvares almindelige spørgsmål om brugen af faktureringsklassifikationer og faktureringskoder til fritekstfakturaer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillingClassification, CustBillingCode, CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25821
ms.assetid: 483e2726-ec48-4d1f-82f5-bffddea301ce
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f458e52ac77496682018e496dcedce358549ad3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845823"
---
# <a name="free-text-invoices-in-the-public-sector"></a><span data-ttu-id="2ad6a-103">Fritekstfakturaer i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="2ad6a-103">Free text invoices in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad6a-104">I dette emne beskrives funktionen til fritekstfakturaer, som er tilgængelig for den offentlige sektor, samt besvares almindelige spørgsmål om brugen af faktureringsklassifikationer og faktureringskoder til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-104">This topic describes the free text invoice functionality that is available for public sector as well as answers common questions about using billing classifications and billing codes with free text invoices.</span></span>

<a name="do-i-have-to-select-a-billing-classification-for-every-free-text-invoice"></a><span data-ttu-id="2ad6a-105">Skal jeg vælge en faktureringsklassifikation for hver fritekstfaktura?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-105">Do I have to select a billing classification for every free text invoice?</span></span>
-------------------------------------------------------------------------

<span data-ttu-id="2ad6a-106">Ja, når faktureringsklassifikationer er aktiveret, er det nødvendigt at angive en faktureringsklassifikation for hver fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-106">Yes, when billing classifications are enabled, you have to enter a billing classification for every free text invoice.</span></span> <span data-ttu-id="2ad6a-107">Faktureringsklassifikationen styrer, hvilke faktureringskoder der kan angives på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-107">The billing classification controls which billing codes that you can enter on the invoice.</span></span> <span data-ttu-id="2ad6a-108">Den styrer også betalingsvilkår og -betingelser, nummerserier og behandlingen af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-108">It also governs payment terms and conditions, number sequences, and the processing of the invoice.</span></span> <span data-ttu-id="2ad6a-109">Du kan få flere oplysninger om faktureringsklassifikationer i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="2ad6a-109">To learn more about billing classifications, see [Billing classifications and billing codes in the public sector](billing-classifications-billing-codes-public-sector.md).</span></span>

## <a name="what-happens-if-ive-already-created-free-text-invoices-when-i-enable-billing-classifications"></a><span data-ttu-id="2ad6a-110">Hvad sker der, hvis jeg allerede har oprettet fritekstfakturaer, når jeg aktiverer faktureringsklassifikationer?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-110">What happens if I’ve already created free text invoices when I enable billing classifications?</span></span>
<span data-ttu-id="2ad6a-111">Hvis en faktura ikke er bogført endnu, når du har aktiveret faktureringsklassifikationer, skal du tildele en faktureringsklassifikation til fakturaen, før du kan bogføre den.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-111">If an invoice was not yet posted when you enabled billing classifications, you have to assign a billing classification to the invoice before you can post it.</span></span> <span data-ttu-id="2ad6a-112">Når du åbner siden for at få vist fakturaen, får du en meddelelse om, at faktureringsklassifikationen er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-112">When you open the page to view the invoice, you'll get a message telling you that the billing classification is required.</span></span>

## <a name="why-should-i-use-billing-codes-when-i-create-free-text-invoices"></a><span data-ttu-id="2ad6a-113">Hvorfor skal jeg bruge faktureringskoder, når jeg opretter fritekstfakturaer?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-113">Why should I use billing codes when I create free text invoices?</span></span>
<span data-ttu-id="2ad6a-114">Når du vælger en faktureringskode, angives der automatisk standardværdier på mange felter på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-114">When you select a billing code, default values are automatically entered in many fields on the invoice line.</span></span> <span data-ttu-id="2ad6a-115">Dette gør dataindtastningen hurtigere og mere nøjagtig.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-115">This makes data entry faster and more accurate.</span></span> <span data-ttu-id="2ad6a-116">Faktureringskoder bruges også med bogføringsdefinitioner til at styre, hvordan debitorposteringer bogføres i Finans.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-116">Billing codes are also used with posting definitions to control how Accounts receivable transactions are posted to the ledger.</span></span>

## <a name="im-creating-a-free-text-invoice-and-the-billing-code-that-i-want-to-use-isnt-available-what-should-i-do"></a><span data-ttu-id="2ad6a-117">Jeg opretter en fritekstfaktura, og den faktureringskode, der skal bruges, er ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-117">I’m creating a free text invoice, and the billing code that I want to use isn’t available.</span></span> <span data-ttu-id="2ad6a-118">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-118">What should I do?</span></span>
<span data-ttu-id="2ad6a-119">Kontrollér først, at fakturaen bruger den rigtige faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-119">First make sure that the invoice is using the right billing classification.</span></span> <span data-ttu-id="2ad6a-120">Kun visse faktureringskoder kan bruges sammen med hver faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-120">Only certain billing codes can be used with each billing classification.</span></span> <span data-ttu-id="2ad6a-121">Hvis faktureringsklassifikationen er korrekt, skal du derefter vælge en af de faktureringskoder, der er tilgængelige for den fritekstfaktura, du opretter.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-121">If the billing classification is correct, then you should select one of the billing codes that are available for the free text invoice that you are creating.</span></span>

## <a name="i-can-change-some-of-the-fields-on-my-free-text-invoices-all-of-the-time-and-i-can-change-all-of-the-fields-some-of-the-time-but-some-of-the-fields-i-can-only-change-some-of-the-time-whats-up-with-that"></a><span data-ttu-id="2ad6a-122">Jeg kan ændre nogle af felterne på mine fritekstfakturaer hele tiden, og jeg kan ændre alle felterne nogle gange.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-122">I can change some of the fields on my free text invoices all of the time, and I can change all of the fields some of the time.</span></span> <span data-ttu-id="2ad6a-123">Men nogle af felterne kan jeg kun ændre nogle gange.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-123">But some of the fields I can only change some of the time.</span></span> <span data-ttu-id="2ad6a-124">Hvorfor det?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-124">What’s up with that?</span></span>
<span data-ttu-id="2ad6a-125">Indstillinger på faktureringskoden styrer, om du kan ændre bestemte felter.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-125">Settings on the billing code control whether you can change certain fields.</span></span>

-   <span data-ttu-id="2ad6a-126">Hvis faktureringskoden på en fritekstfakturalinje ikke tillader ændringer på fakturaen, kan du ikke ændre beløbet, prisen eller beløbets detaljer på linjen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-126">If the billing code on a free text invoice line doesn’t allow rate changes on the invoice, you can’t change the amount, the unit price, or the amount details on the line.</span></span> 

> [!TIP] 
> <span data-ttu-id="2ad6a-127">Hvis feltet **Faktureringskode** afgør er angivet til salgspris, kan du ikke ændre prisen, men du kan ændre beløbet indirekte ved at ændre antallet.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-127">If the **Billing code determines** field is set to unit price, you can’t change the unit price, but you can change the amount indirectly by changing the quantity.</span></span>

-   <span data-ttu-id="2ad6a-128">Hvis faktureringskoden på en fritekstfakturalinje ikke tillader ændringer til finanskonti, kan du ikke ændre regnskabsfordelinger på linjen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-128">If the billing code on a free text invoice line doesn’t allow changes to the ledger accounts, you can’t change the accounting distributions on the line.</span></span> <span data-ttu-id="2ad6a-129">Du kan ændre den hovedkonto, der vises på fritekstfakturalinjen, men denne ændring påvirker kun, hvad der vises.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-129">You can change the main account that displays on the free text invoice line, but that change affects only what is displayed.</span></span> <span data-ttu-id="2ad6a-130">Ændring af hovedkontoen påvirker ikke fordelingerne.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-130">Changing the main account does not affect the distributions.</span></span>
-   <span data-ttu-id="2ad6a-131">Når der er et projekt, der er tilknyttet fakturalinjen, styrer faktureringskoden, om du kan ændre projekt-id, kategori og finanskonto.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-131">When there’s a project associated with the invoice line, the billing code controls whether you can change the project ID, category, and ledger account.</span></span> 

> [!TIP] 
> <span data-ttu-id="2ad6a-132">Hvis du vil ændre finanskontoen for fakturalinjer, der er relateret til projekter, skal ændringerne tillades, både på selve faktureringskoden og afsnittet Projekter på siden Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-132">To change the ledger account for invoice lines related to projects, changes have to be allowed both on the billing code itself and on the Projects section of the Accounts receivable parameters page.</span></span>

<span data-ttu-id="2ad6a-133">Du kan få flere oplysninger om faktureringskoder i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="2ad6a-133">To learn more about billing codes, see [Billing classifications and billing codes in the public sector](billing-classifications-billing-codes-public-sector.md).</span></span>

## <a name="where-does-the-interest-code-on-a-free-text-invoice-come-from"></a><span data-ttu-id="2ad6a-134">Hvor kommer rentekoden på en fritekstfaktura fra?</span><span class="sxs-lookup"><span data-stu-id="2ad6a-134">Where does the interest code on a free text invoice come from?</span></span>
<span data-ttu-id="2ad6a-135">Rentekoden kan indstilles på faktureringskoden, faktureringsklassifikationen eller posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-135">The interest code can be set on the billing code, the billing classification, or the posting profile.</span></span>





