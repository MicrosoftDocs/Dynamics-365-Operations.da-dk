---
title: Fastlægge betalingsmåde for debitor
description: I dette emne forklares, hvordan du kan oprette betalingsmåde til debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188803"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="35573-103">Fastlægge betalingsmåde for debitor</span><span class="sxs-lookup"><span data-stu-id="35573-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35573-104">I dette emne forklares, hvordan du kan oprette betalingsmåde til debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="35573-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="35573-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="35573-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="35573-106">I navigationsruden skal du gå til **Moduler > Debitor > Betalingsopsætning > Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="35573-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="35573-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="35573-107">Select **New**.</span></span>
3. <span data-ttu-id="35573-108">Angiv et id for betalingsmåden i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="35573-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="35573-109">Metoden for betalings-id vises på fakturaer og betalinger, så udform beskrivelsen på en måde, så læseren ved, hvilken type betaling der registreres og for hvilken bankkonto.</span><span class="sxs-lookup"><span data-stu-id="35573-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="35573-110">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="35573-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="35573-111">Vælg, hvilken betalingsstatus der kræves, for at betalinger kan bogføres.</span><span class="sxs-lookup"><span data-stu-id="35573-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="35573-112">Når du opretter en kundebetaling, kan den kun bogføres, når betalingsstatus svarer den betalingsstatus, som du angiver her.</span><span class="sxs-lookup"><span data-stu-id="35573-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="35573-113">Vælg, hvordan debitorbetalinger skal oprettes for fakturaer.</span><span class="sxs-lookup"><span data-stu-id="35573-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="35573-114">Denne indstilling bruges kun, når du kører et betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="35573-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="35573-115">Der kunne bruges et betalingsforslag til debitorbetalinger, når der udføres direkte debiteringer og trækkes midler fra kundernes bankkonti.</span><span class="sxs-lookup"><span data-stu-id="35573-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="35573-116">Vælg betalingstype.</span><span class="sxs-lookup"><span data-stu-id="35573-116">Select the type of payment.</span></span> <span data-ttu-id="35573-117">Betalingstypen hjælper med at afgøre, om der udføres en form for validering eller ej af betalingen.</span><span class="sxs-lookup"><span data-stu-id="35573-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="35573-118">Vælg den kontotype, betalinger bogføres på.</span><span class="sxs-lookup"><span data-stu-id="35573-118">Select what account type payments will post to.</span></span> <span data-ttu-id="35573-119">Bank vil normalt blive valgt for denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="35573-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="35573-120">Vælg den bankkonto, som betalingen vil blive registreret på.</span><span class="sxs-lookup"><span data-stu-id="35573-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="35573-121">Angiv den banktransaktionstype, der identificerer den type betaling, der bruges af din bank.</span><span class="sxs-lookup"><span data-stu-id="35573-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="35573-122">Banktransaktionstypen bruges under bankafstemningsprocessen og kan gøre afstemningen nemmere.</span><span class="sxs-lookup"><span data-stu-id="35573-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="35573-123">Vælg, om denne betaling midlertidigt skal bogføres på en mellemkonto.</span><span class="sxs-lookup"><span data-stu-id="35573-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="35573-124">Hvis du vil prøve variabeltid for en betaling for at cleare banken, kan du bruge funktionen Mellemkontering.</span><span class="sxs-lookup"><span data-stu-id="35573-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="35573-125">Betalingen bogføres midlertidigt på en finanskonto, indtil banken er clearet, hvorefter betalingen flyttes til den bankkonto, du her defineret her.</span><span class="sxs-lookup"><span data-stu-id="35573-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="35573-126">Angiv den hovedkonto, der er brugt til mellemkonteringen.</span><span class="sxs-lookup"><span data-stu-id="35573-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="35573-127">Dette er den hovedkonto, som betalingen skal bogføres på midlertidigt, hvis der anvendes mellemkonto.</span><span class="sxs-lookup"><span data-stu-id="35573-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="35573-128">Brug fanen **Filformat** til at definere indstillingen for elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="35573-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="35573-129">Brug fanen **Betalingskontrol** til at definere felter, der er obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="35573-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="35573-130">Hvis du f.eks. har brug for, at alle betalinger med denne betalingsmåde skal indbetales, kan du vælge denne indstilling under denne fane.</span><span class="sxs-lookup"><span data-stu-id="35573-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="35573-131">Brug fanen **Betalingsattributter** til at definere, hvilke betalingsattributter du vil bruge til denne betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="35573-131">Use the **Payment atrributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="35573-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="35573-132">Select **Save**.</span></span>

