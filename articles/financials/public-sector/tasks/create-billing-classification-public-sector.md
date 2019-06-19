---
title: Oprette en faktureringsklassifikation i den offentlige sektor
description: Offentlige institutioner kan bruge faktureringsklassifikationer til at administrere fritekstfakturaer.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillingClassification
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09b075391f73c68e5311379babf0642dea8c0635
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557234"
---
# <a name="create-a-billing-classification-in-the-public-sector"></a><span data-ttu-id="53cce-103">Oprette en faktureringsklassifikation i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="53cce-103">Create a billing classification in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53cce-104">Offentlige institutioner kan bruge faktureringsklassifikationer til at administrere fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="53cce-104">Public-sector organizations can use billing classifications to help manage free text invoices.</span></span> <span data-ttu-id="53cce-105">Faktureringsklassifikationer bruges til at gruppere ensartede fritekstfakturaer til behandling og visning.</span><span class="sxs-lookup"><span data-stu-id="53cce-105">Billing classifications are used to group similar free text invoices for processing and viewing.</span></span> <span data-ttu-id="53cce-106">Før du bruger denne procedure, skal du kontrollere, at der findes en faktureringskode, der kan tildeles til en faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="53cce-106">Before using this procedure, verify that a billing code exists that can be assigned to a billing classification.</span></span> <span data-ttu-id="53cce-107">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="53cce-107">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="53cce-108">Gå til Debitor > Opsætning > Faktureringsklassifikationer.</span><span class="sxs-lookup"><span data-stu-id="53cce-108">Go to Accounts receivable > Setup > Billing classifications.</span></span>
2. <span data-ttu-id="53cce-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53cce-109">Click New.</span></span>
3. <span data-ttu-id="53cce-110">Angiv en værdi i feltet Faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="53cce-110">In the Billing classification field, type a value.</span></span>
4. <span data-ttu-id="53cce-111">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="53cce-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="53cce-112">Klik på rullelisten i feltet Betalingsbetingelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53cce-112">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="53cce-113">Klik på betalingsbetingelseskoden for denne faktureringsklassifikation på listen.</span><span class="sxs-lookup"><span data-stu-id="53cce-113">In the list, click the terms of payment for this billing classification.</span></span>
    * <span data-ttu-id="53cce-114">Når du accepterer standardindstillingerne for renter og rykkere, beregnes der ikke rente for fakturaer, der bruger denne faktureringsklassifikation, og der sendes ikke rykkere.</span><span class="sxs-lookup"><span data-stu-id="53cce-114">When you accept the default settings for interest and collection letters, interest won't be calculated for invoices that use this billing classification, and collection letters won't be sent.</span></span> <span data-ttu-id="53cce-115">Hvis du vil ændre disse indstillinger, skal du låse opgaveguiden op ved at klikke på ikonet til oplåsning øverst på skærmen.</span><span class="sxs-lookup"><span data-stu-id="53cce-115">To change these settings, unlock the task guide by clicking the Unlock icon at the top of the screen.</span></span>  
7. <span data-ttu-id="53cce-116">Udvid eller skjul sektionen Faktureringskoder.</span><span class="sxs-lookup"><span data-stu-id="53cce-116">Expand or collapse the Billing codes section.</span></span>
8. <span data-ttu-id="53cce-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="53cce-117">Click Add.</span></span>
9. <span data-ttu-id="53cce-118">Klik på rullelisten i feltet Faktureringskode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53cce-118">In the Billing code field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="53cce-119">På listen skal du klikke på en faktureringskode, der skal føjes til denne faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="53cce-119">In the list, click a billing code to add to this billing classification.</span></span>
11. <span data-ttu-id="53cce-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="53cce-120">Click Save.</span></span>

