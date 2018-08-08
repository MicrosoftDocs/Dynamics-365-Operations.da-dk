--- 
title: Oprette en bankkonto for kreditor
description: "Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 636bbafc87835f1cfe5de0301e3f020a8ac01a56
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="b59ea-103">Oprette en bankkonto for kreditor</span><span class="sxs-lookup"><span data-stu-id="b59ea-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b59ea-104">Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør.</span><span class="sxs-lookup"><span data-stu-id="b59ea-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="b59ea-105">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b59ea-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="b59ea-106">Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="b59ea-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="b59ea-107">Vælg den kreditor, du vil oprette en bankkonto for, og klik derefter på linket på kreditors konto-id.</span><span class="sxs-lookup"><span data-stu-id="b59ea-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="b59ea-108">Klik på Kreditor i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b59ea-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="b59ea-109">Klik på Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="b59ea-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="b59ea-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b59ea-110">Click New.</span></span>
6. <span data-ttu-id="b59ea-111">Skriv en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b59ea-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="b59ea-112">Dette id bruges til at identificere bankkontoen på kreditorposten.</span><span class="sxs-lookup"><span data-stu-id="b59ea-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="b59ea-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="b59ea-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b59ea-114">Indtast eller vælg en værdi i feltet Bankgrupper.</span><span class="sxs-lookup"><span data-stu-id="b59ea-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="b59ea-115">I feltet Registreringsnummertype skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="b59ea-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="b59ea-116">Det er den registreringsnummertype, der anvendes til internationale betalinger.</span><span class="sxs-lookup"><span data-stu-id="b59ea-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="b59ea-117">Skriv en værdi i feltet Bankkontonummer.</span><span class="sxs-lookup"><span data-stu-id="b59ea-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="b59ea-118">Indtast en værdi i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="b59ea-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="b59ea-119">Skriv en værdi i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="b59ea-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="b59ea-120">IBAN-nummeret skal være i det korrekte format.</span><span class="sxs-lookup"><span data-stu-id="b59ea-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="b59ea-121">Du kan f.eks. bruge DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="b59ea-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="b59ea-122">Status for bankkontoen er Aktiv, hvis aktiv-datoen er nået, og udløbsdatoen ikke er overskredet.</span><span class="sxs-lookup"><span data-stu-id="b59ea-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="b59ea-123">Den er også aktiv, hvis både feltet Aktiv-dato og feltet Udløbsdato er tomt.</span><span class="sxs-lookup"><span data-stu-id="b59ea-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="b59ea-124">Hvis datoerne i både feltet Aktiv-dato og feltet Udløbsdato ligger i fremtiden, er elektroniske betalinger ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="b59ea-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="b59ea-125">Andre betalingstyper er tilgængelige, og bankkontoen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="b59ea-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="b59ea-126">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b59ea-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="b59ea-127">Indtast en værdi i feltet Tekstkode.</span><span class="sxs-lookup"><span data-stu-id="b59ea-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="b59ea-128">Dette felt angiver en kode, der vises på modtagerens bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="b59ea-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="b59ea-129">Skriv en værdi i feltet Meddelelse til bank.</span><span class="sxs-lookup"><span data-stu-id="b59ea-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="b59ea-130">Skriv en værdi i feltet Kursreference.</span><span class="sxs-lookup"><span data-stu-id="b59ea-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="b59ea-131">Det er referencenummeret til evt. termins- eller aftalekurs.</span><span class="sxs-lookup"><span data-stu-id="b59ea-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="b59ea-132">Indtast eller vælg en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="b59ea-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="b59ea-133">Når der udstedes adviseringer, indeholder dette afsnit en oversigt over deres status (ventende eller godkendt).</span><span class="sxs-lookup"><span data-stu-id="b59ea-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="b59ea-134">Udvid sektionen Adresse.</span><span class="sxs-lookup"><span data-stu-id="b59ea-134">Expand the Address section.</span></span>
19. <span data-ttu-id="b59ea-135">Udvid afsnittet Adviseringer.</span><span class="sxs-lookup"><span data-stu-id="b59ea-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="b59ea-136">Udvid eller skjul sektionen Kontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b59ea-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="b59ea-137">Indtast en værdi i feltet Telefon.</span><span class="sxs-lookup"><span data-stu-id="b59ea-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="b59ea-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b59ea-138">Close the page.</span></span>
23. <span data-ttu-id="b59ea-139">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b59ea-139">Click Edit.</span></span>
24. <span data-ttu-id="b59ea-140">Vis sektionen Betaling.</span><span class="sxs-lookup"><span data-stu-id="b59ea-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="b59ea-141">Vælg den konto, du lige har oprettet, i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b59ea-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="b59ea-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b59ea-142">Click Save.</span></span>
    * <span data-ttu-id="b59ea-143">Adressen kan være nedarvet fra bankgruppen, hvis der er angivet en, eller du kan tilføje den her.</span><span class="sxs-lookup"><span data-stu-id="b59ea-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


