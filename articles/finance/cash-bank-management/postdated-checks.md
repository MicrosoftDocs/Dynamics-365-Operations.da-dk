---
title: Fremdaterede checks
description: Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks i Microsoft Dynamics 365 Finance. Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Derfor kan checken ikke indløses før den angivne dato.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441713"
---
# <a name="postdated-checks"></a><span data-ttu-id="cb704-105">Fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="cb704-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb704-106">Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="cb704-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="cb704-107">Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="cb704-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="cb704-108">Derfor kan checken ikke indløses før den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="cb704-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="cb704-109">Dynamics 365 Finance understøtter hele administrationscyklussen for fremdaterede checks i både Debitor og Kreditor som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="cb704-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb704-110">Scenarie</span><span class="sxs-lookup"><span data-stu-id="cb704-110">Scenario</span></span></th>
<th><span data-ttu-id="cb704-111">Oplysninger</span><span class="sxs-lookup"><span data-stu-id="cb704-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb704-112">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="cb704-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="cb704-113">Du skal oprette en ny betalingsmetode og angive betalingsrutine for clearingkonti til udstedte checks, modtagne checks og A-skat.</span><span class="sxs-lookup"><span data-stu-id="cb704-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb704-114">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="cb704-115">Registrer detaljerne omkring en fremdateret check, før du udsteder til en kreditor.</span><span class="sxs-lookup"><span data-stu-id="cb704-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="cb704-116">Når betalingen bogføres, genkendes kreditorens gæld, men bankkontoen er endnu ikke kredit.</span><span class="sxs-lookup"><span data-stu-id="cb704-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="cb704-117">I stedet bruges en clearingkonto til dette formål.</span><span class="sxs-lookup"><span data-stu-id="cb704-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb704-118">Registrere og bogføre en fremdateret check til en debitor</span><span class="sxs-lookup"><span data-stu-id="cb704-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="cb704-119">Registrer oplysninger om en fremdateret check, du har modtaget fra en debitor.</span><span class="sxs-lookup"><span data-stu-id="cb704-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="cb704-120">Når betalingen bogføres, er debitoren kredit, men bankkontoen er endnu ikke debet.</span><span class="sxs-lookup"><span data-stu-id="cb704-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="cb704-121">I stedet bruges en clearingkonto til dette formål.</span><span class="sxs-lookup"><span data-stu-id="cb704-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb704-122">Registrer og bogfør en fremdateret erstatningscheck for en debitor eller kreditor.</span><span class="sxs-lookup"><span data-stu-id="cb704-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="cb704-123">Hvis din oprindelige check til en kreditor eller fra en debitor går tabt eller beskadiges, kan du udstede en fremdateret erstatningscheck til.</span><span class="sxs-lookup"><span data-stu-id="cb704-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="cb704-124">Når du registrerer checkoplysningerne, skal du angive en reference til den oprindelige check og angive, at den nye check er en erstatning for den oprindelige.</span><span class="sxs-lookup"><span data-stu-id="cb704-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="cb704-125">Du kan også bogføre erstatningschecken.</span><span class="sxs-lookup"><span data-stu-id="cb704-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb704-126">Overføre en fremdateret debitorcheck til en kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="cb704-127">Når du modtager en fremdateret check fra en debitor, kan du overføre den pågældende check til en kreditor som betaling.</span><span class="sxs-lookup"><span data-stu-id="cb704-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb704-128">Udligne en fremdateret check for en debitor eller kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="cb704-129">Du kan udligne en fremdateret check, der er bogført på en mellemkonto, for en debitor eller en kreditor, når checken forfalder.</span><span class="sxs-lookup"><span data-stu-id="cb704-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="cb704-130">Når checken er udlignet, er banken endelig debet eller kredit mod den clearingkonto, der blev brugt tidligere.</span><span class="sxs-lookup"><span data-stu-id="cb704-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb704-131">Annullere en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="cb704-132">Du kan annullere en bogført, fremdateret check i disse situationer: - Checken returneres af banken.</span><span class="sxs-lookup"><span data-stu-id="cb704-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="cb704-133">- Checken anvendes til en forkert faktura.</span><span class="sxs-lookup"><span data-stu-id="cb704-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="cb704-134">- Der modtages et kontantbeløb til dækning af checkbeløbet.</span><span class="sxs-lookup"><span data-stu-id="cb704-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="cb704-135">Stands betaling af en fremdateret check.</span><span class="sxs-lookup"><span data-stu-id="cb704-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="cb704-136">Du kan standse betalingen af en fremdateret check, der er udstedt til en leverandør, af forskellige årsager, f.eks. hvis du mangler midler at betale med, hvis aftalen med leverandøren er ændret, hvis leverandøren leverer defekte varer, eller hvis du har returneret varer til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="cb704-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="cb704-137">Du kan kun standse betalingen, hvis checken ikke allerede er clearet.</span><span class="sxs-lookup"><span data-stu-id="cb704-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="cb704-138">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="cb704-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="cb704-139">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="cb704-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="cb704-140">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="cb704-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="cb704-141">Udligne en fremdateret check fra en debitor</span><span class="sxs-lookup"><span data-stu-id="cb704-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="cb704-142">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="cb704-143">Udligne en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="cb704-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



