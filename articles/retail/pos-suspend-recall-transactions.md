---
title: Afbryde og genoptage en transaktion i POS
description: Dette emne forklarer, hvordan brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat ved hjælp af Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569538"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="fb661-103">Afbryde og genoptage transaktioner i POS</span><span class="sxs-lookup"><span data-stu-id="fb661-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fb661-104">POS-brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="fb661-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="fb661-105">Transaktioner afbrydes ofte for hurtigt at frigøre et kasseapparat til en anden opgave uden at tage tid fra den aktuelle transaktion.</span><span class="sxs-lookup"><span data-stu-id="fb661-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="fb661-106">En butiksansat begynder f.eks. at behandle en debitorpostering på en mobilenhed, men skal afslutte den på et kasseapparat, der har en pengeskuffe.</span><span class="sxs-lookup"><span data-stu-id="fb661-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="fb661-107">Den butiksansatte kan afbryde transaktionen på mobilenheden og derefter hente den frem og genoptage den på et kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="fb661-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="fb661-108">Konfigurere afbryde- og genoptage-funktionalitet</span><span class="sxs-lookup"><span data-stu-id="fb661-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="fb661-109">POS-handlinger</span><span class="sxs-lookup"><span data-stu-id="fb661-109">POS operations</span></span>

<span data-ttu-id="fb661-110">Afbrydelse og genoptagelse understøttes af to [POS-handlinger](pos-operations.md).</span><span class="sxs-lookup"><span data-stu-id="fb661-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="fb661-111">Du kan tildele disse handlinger til [knapmatrixer](pos-screen-layouts.md) på transaktionssiden eller velkomstsiden.</span><span class="sxs-lookup"><span data-stu-id="fb661-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="fb661-112">503: Udsæt transaktion</span><span class="sxs-lookup"><span data-stu-id="fb661-112">503: Suspend transaction</span></span>
- <span data-ttu-id="fb661-113">504: Hent transaktion igen</span><span class="sxs-lookup"><span data-stu-id="fb661-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="fb661-114">Skabelon for modtagelse</span><span class="sxs-lookup"><span data-stu-id="fb661-114">Receipt template</span></span>

<span data-ttu-id="fb661-115">POS kan konfigureres til at generere en udskrevet følgeseddel, når en transaktion afbrydes.</span><span class="sxs-lookup"><span data-stu-id="fb661-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="fb661-116">Dette bilag kan derefter bruges til hurtigt at identificere og genkalde transaktionen senere.</span><span class="sxs-lookup"><span data-stu-id="fb661-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="fb661-117">Hvis du vil indstille POS til at udskrive en følgeseddel, skal du tilføje kvitteringsformatet **Udsat transaktion** i butikkens kvitteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="fb661-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="fb661-118">Du kan designe kvitteringsformatet, så bestemte oplysninger om posteringen medtages eller udelukkes.</span><span class="sxs-lookup"><span data-stu-id="fb661-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="fb661-119">Formatet kan f.eks. omfatte en stregkode for at understøtte scanning.</span><span class="sxs-lookup"><span data-stu-id="fb661-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="fb661-120">Kvitteringsnummerering</span><span class="sxs-lookup"><span data-stu-id="fb661-120">Receipt numbering</span></span>

<span data-ttu-id="fb661-121">Hvad angår andre POS-transaktionstyper, der genererer en udskrevet kvittering, kan du definere en nummerserie for udsatte transaktioner i sektionen **Kvitteringsnummerering** af butikkens funktionalitetsprofilen.</span><span class="sxs-lookup"><span data-stu-id="fb661-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="fb661-122">Erklær som ugyldig, når skiftet lukkes</span><span class="sxs-lookup"><span data-stu-id="fb661-122">Void when closing shift</span></span>

<span data-ttu-id="fb661-123">Du kan bruge indstillingen **Erklær som ugyldig, når skiftet lukkes** til at kræve, at brugerne enten fuldfører eller annullerer en afbrudt transaktion, før de afslutter deres skift.</span><span class="sxs-lookup"><span data-stu-id="fb661-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="fb661-124">Når der udføres et **Luk skift**, beder POS brugerne om enten at vise eller annullere alle udestående, afbrudte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="fb661-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="fb661-125">Afbryde og genoptage en transaktion</span><span class="sxs-lookup"><span data-stu-id="fb661-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="fb661-126">Afbryde en transaktion</span><span class="sxs-lookup"><span data-stu-id="fb661-126">Suspend a transaction</span></span>

<span data-ttu-id="fb661-127">Brugere, der har de nødvendige rettigheder, og som har et skærmlayout, der omfatter handlingen **Udsæt transaktion**, kan afbryde en transaktion, så den kan hentes frem senere eller på et andet kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="fb661-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="fb661-128">Transaktioner kan kun afbrydes, hvis de **ikke** indeholde følgende typer linjer:</span><span class="sxs-lookup"><span data-stu-id="fb661-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="fb661-129">Aktive betalingslinjer</span><span class="sxs-lookup"><span data-stu-id="fb661-129">Active payment lines</span></span>
- <span data-ttu-id="fb661-130">Gavekortlinjer (enten til udstedelse af et gavekort eller til tilføjelse af saldoen for gavekortet)</span><span class="sxs-lookup"><span data-stu-id="fb661-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="fb661-131">En afbrudt transaktion påvirker ikke salgsoplysninger eller oplysninger om disponibel lagerbeholdning for butikken.</span><span class="sxs-lookup"><span data-stu-id="fb661-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="fb661-132">Genoptage en afbrudt transaktion</span><span class="sxs-lookup"><span data-stu-id="fb661-132">Resume a suspended transaction</span></span>

<span data-ttu-id="fb661-133">Afbrudte transaktioner kan hentes frem og genoptages i den samme butik af alle brugere, der har de fornødne rettigheder, og som også har et layout, der omfatter handlingen **Hent transaktion igen**.</span><span class="sxs-lookup"><span data-stu-id="fb661-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="fb661-134">Du kan hurtigt og nemt kalde en afbrudt transaktion frem igen ved at scanne stregkoden på udskrevne følgeseddel, mens du ser på listen over transaktioner fra handlingen **Hent transaktion igen**.</span><span class="sxs-lookup"><span data-stu-id="fb661-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="fb661-135">Overvejelser om offlinetilstand</span><span class="sxs-lookup"><span data-stu-id="fb661-135">Considerations for offline mode</span></span>

- <span data-ttu-id="fb661-136">Ingen transaktioner, der afbrydes, mens POS i onlinetilstand, kan fortsætte i offlinetilstand, fordi dataene ikke er synkroniseret med offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="fb661-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="fb661-137">Hvis du afbryder en transaktion, mens POS er offline, kan du genkalde den i offlinetilstand, forudsat at POS ikke på noget tidspunkt, siden du afbrød transaktionen, er blevet skiftet tilbage til onlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="fb661-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="fb661-138">Når POS skiftes tilbage til onlinetilstand, flyttes data om afbrudte transaktioner til onlinedatabasen og fjernes fra offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="fb661-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="fb661-139">Derfor kan transaktionerne kun genoptages i onlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="fb661-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="fb661-140">Hvis du skifter POS tilbage til offlinetilstand, kan du ikke genoptage de afbrudte transaktioner, fordi de allerede er blevet fjernet fra offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="fb661-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="fb661-141">Annullere en afbrudt transaktion</span><span class="sxs-lookup"><span data-stu-id="fb661-141">Void a suspended transaction</span></span>

<span data-ttu-id="fb661-142">Du kan annullere afbrudte transaktioner enten ved at genkalde transaktionen og derefter udføre handlingen **Afvis transaktion** eller ved at markere transaktionen på listen **Hent transaktion igen** og vælge **Afvist** på applinjen.</span><span class="sxs-lookup"><span data-stu-id="fb661-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="fb661-143">Butikken kan også konfigureres til at bede brugerne om at annullere afbrudte transaktioner, når de afslutter deres skift.</span><span class="sxs-lookup"><span data-stu-id="fb661-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
