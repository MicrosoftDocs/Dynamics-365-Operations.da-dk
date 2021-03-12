---
title: Afbryde og genoptage en transaktion i POS
description: Dette emne forklarer, hvordan brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat ved hjælp af Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 823d538bea481aef4f3657fe0ae1ebb3b0cf759c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972524"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="851ba-103">Afbryde og genoptage en transaktion i POS</span><span class="sxs-lookup"><span data-stu-id="851ba-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="851ba-104">POS-brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="851ba-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="851ba-105">Transaktioner afbrydes ofte for hurtigt at frigøre et kasseapparat til en anden opgave uden at tage tid fra den aktuelle transaktion.</span><span class="sxs-lookup"><span data-stu-id="851ba-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="851ba-106">En butiksansat begynder f.eks. at behandle en debitorpostering på en mobilenhed, men skal afslutte den på et kasseapparat, der har en pengeskuffe.</span><span class="sxs-lookup"><span data-stu-id="851ba-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="851ba-107">Den butiksansatte kan afbryde transaktionen på mobilenheden og derefter hente den frem og genoptage den på et kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="851ba-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="851ba-108">Konfigurere afbryde- og genoptage-funktionalitet</span><span class="sxs-lookup"><span data-stu-id="851ba-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="851ba-109">POS-handlinger</span><span class="sxs-lookup"><span data-stu-id="851ba-109">POS operations</span></span>

<span data-ttu-id="851ba-110">Afbrydelse og genoptagelse understøttes af to [POS-handlinger](pos-operations.md).</span><span class="sxs-lookup"><span data-stu-id="851ba-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="851ba-111">Du kan tildele disse handlinger til [knapmatrixer](pos-screen-layouts.md) på transaktionssiden eller velkomstsiden.</span><span class="sxs-lookup"><span data-stu-id="851ba-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="851ba-112">503: Udsæt transaktion</span><span class="sxs-lookup"><span data-stu-id="851ba-112">503: Suspend transaction</span></span>
- <span data-ttu-id="851ba-113">504: Hent transaktion igen</span><span class="sxs-lookup"><span data-stu-id="851ba-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="851ba-114">Skabelon for modtagelse</span><span class="sxs-lookup"><span data-stu-id="851ba-114">Receipt template</span></span>

<span data-ttu-id="851ba-115">POS kan konfigureres til at generere en udskrevet følgeseddel, når en transaktion afbrydes.</span><span class="sxs-lookup"><span data-stu-id="851ba-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="851ba-116">Dette bilag kan derefter bruges til hurtigt at identificere og genkalde transaktionen senere.</span><span class="sxs-lookup"><span data-stu-id="851ba-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="851ba-117">Hvis du vil indstille POS til at udskrive en følgeseddel, skal du tilføje kvitteringsformatet **Udsat transaktion** i butikkens kvitteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="851ba-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="851ba-118">Du kan designe kvitteringsformatet, så bestemte oplysninger om posteringen medtages eller udelukkes.</span><span class="sxs-lookup"><span data-stu-id="851ba-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="851ba-119">Formatet kan f.eks. omfatte en stregkode for at understøtte scanning.</span><span class="sxs-lookup"><span data-stu-id="851ba-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="851ba-120">Kvitteringsnummerering</span><span class="sxs-lookup"><span data-stu-id="851ba-120">Receipt numbering</span></span>

<span data-ttu-id="851ba-121">Hvad angår andre POS-transaktionstyper, der genererer en udskrevet kvittering, kan du definere en nummerserie for udsatte transaktioner i sektionen **Kvitteringsnummerering** af butikkens funktionalitetsprofilen.</span><span class="sxs-lookup"><span data-stu-id="851ba-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="851ba-122">Erklær som ugyldig, når skiftet lukkes</span><span class="sxs-lookup"><span data-stu-id="851ba-122">Void when closing shift</span></span>

<span data-ttu-id="851ba-123">Du kan bruge indstillingen **Erklær som ugyldig, når skiftet lukkes** til at kræve, at brugerne enten fuldfører eller annullerer en afbrudt transaktion, før de afslutter deres skift.</span><span class="sxs-lookup"><span data-stu-id="851ba-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="851ba-124">Når der udføres et **Luk skift**, beder POS brugerne om enten at vise eller annullere alle udestående, afbrudte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="851ba-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="851ba-125">Afbryde og genoptage en transaktion</span><span class="sxs-lookup"><span data-stu-id="851ba-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="851ba-126">Afbryde en transaktion</span><span class="sxs-lookup"><span data-stu-id="851ba-126">Suspend a transaction</span></span>

<span data-ttu-id="851ba-127">Brugere, der har de nødvendige rettigheder, og som har et skærmlayout, der omfatter handlingen **Udsæt transaktion**, kan afbryde en transaktion, så den kan hentes frem senere eller på et andet kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="851ba-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="851ba-128">Transaktioner kan kun afbrydes, hvis de **ikke** indeholde følgende typer linjer:</span><span class="sxs-lookup"><span data-stu-id="851ba-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="851ba-129">Aktive betalingslinjer</span><span class="sxs-lookup"><span data-stu-id="851ba-129">Active payment lines</span></span>
- <span data-ttu-id="851ba-130">Gavekortlinjer (enten til udstedelse af et gavekort eller til tilføjelse af saldoen for gavekortet)</span><span class="sxs-lookup"><span data-stu-id="851ba-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="851ba-131">En afbrudt transaktion påvirker ikke salgsoplysninger eller oplysninger om disponibel lagerbeholdning for butikken.</span><span class="sxs-lookup"><span data-stu-id="851ba-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="851ba-132">Genoptage en afbrudt transaktion</span><span class="sxs-lookup"><span data-stu-id="851ba-132">Resume a suspended transaction</span></span>

<span data-ttu-id="851ba-133">Afbrudte transaktioner kan hentes frem og genoptages i den samme butik af alle brugere, der har de fornødne rettigheder, og som også har et layout, der omfatter handlingen **Hent transaktion igen**.</span><span class="sxs-lookup"><span data-stu-id="851ba-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="851ba-134">Du kan hurtigt og nemt kalde en afbrudt transaktion frem igen ved at scanne stregkoden på udskrevne følgeseddel, mens du ser på listen over transaktioner fra handlingen **Hent transaktion igen**.</span><span class="sxs-lookup"><span data-stu-id="851ba-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="851ba-135">Overvejelser om offlinetilstand</span><span class="sxs-lookup"><span data-stu-id="851ba-135">Considerations for offline mode</span></span>

- <span data-ttu-id="851ba-136">Ingen transaktioner, der afbrydes, mens POS i onlinetilstand, kan fortsætte i offlinetilstand, fordi dataene ikke er synkroniseret med offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="851ba-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="851ba-137">Hvis du afbryder en transaktion, mens POS er offline, kan du genkalde den i offlinetilstand, forudsat at POS ikke på noget tidspunkt, siden du afbrød transaktionen, er blevet skiftet tilbage til onlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="851ba-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="851ba-138">Når POS skiftes tilbage til onlinetilstand, flyttes data om afbrudte transaktioner til onlinedatabasen og fjernes fra offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="851ba-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="851ba-139">Derfor kan transaktionerne kun genoptages i onlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="851ba-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="851ba-140">Hvis du skifter POS tilbage til offlinetilstand, kan du ikke genoptage de afbrudte transaktioner, fordi de allerede er blevet fjernet fra offlinedatabasen.</span><span class="sxs-lookup"><span data-stu-id="851ba-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="851ba-141">Annullere en afbrudt transaktion</span><span class="sxs-lookup"><span data-stu-id="851ba-141">Void a suspended transaction</span></span>

<span data-ttu-id="851ba-142">Du kan annullere afbrudte transaktioner enten ved at genkalde transaktionen og derefter udføre handlingen **Afvis transaktion** eller ved at markere transaktionen på listen **Hent transaktion igen** og vælge **Afvist** på applinjen.</span><span class="sxs-lookup"><span data-stu-id="851ba-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="851ba-143">Butikken kan også konfigureres til at bede brugerne om at annullere afbrudte transaktioner, når de afslutter deres skift.</span><span class="sxs-lookup"><span data-stu-id="851ba-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
