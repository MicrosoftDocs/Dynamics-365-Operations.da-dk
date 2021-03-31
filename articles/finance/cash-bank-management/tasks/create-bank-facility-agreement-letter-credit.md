---
title: Oprette en bankfacilitetsaftale for en remburs
description: Denne opgave fører dig gennem oprettelse af en bankfacilitetsaftale til behandling af en remburs.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40d13e996b08efecb19be961c592230567656a4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225483"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="b71da-103">Oprette en bankfacilitetsaftale for en remburs</span><span class="sxs-lookup"><span data-stu-id="b71da-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b71da-104">Denne opgave fører dig gennem oprettelse af en bankfacilitetsaftale til behandling af en remburs.</span><span class="sxs-lookup"><span data-stu-id="b71da-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="b71da-105">Du vil konfigurere bankfaciliteter og posteringsprofiler før denne opgave.</span><span class="sxs-lookup"><span data-stu-id="b71da-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="b71da-106">Denne opgave bruger demofirmaet "USMF".</span><span class="sxs-lookup"><span data-stu-id="b71da-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="b71da-107">Oprette bankfacilitetsaftale</span><span class="sxs-lookup"><span data-stu-id="b71da-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="b71da-108">Gå til Kontant- og bankstyring > Remburser > Bankfacilitetsaftaler.</span><span class="sxs-lookup"><span data-stu-id="b71da-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="b71da-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b71da-109">Click New.</span></span>
3. <span data-ttu-id="b71da-110">Indtast aftalenummeret i henhold til aftalen med banken i feltet Aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="b71da-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="b71da-111">Angiv kontonummeret i den udstedende bank i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b71da-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="b71da-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b71da-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b71da-113">Angiv en dato og et klokkeslæt i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="b71da-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="b71da-114">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="b71da-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="b71da-115">Udvis eller skjul sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b71da-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="b71da-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="b71da-116">Click Add line.</span></span>
10. <span data-ttu-id="b71da-117">Klik på rullelisten i feltet Facilitetstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b71da-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b71da-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b71da-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b71da-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b71da-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b71da-120">Angiv det facilitetsbeløb, der er forhandlet med banken, i feltet Grænse.</span><span class="sxs-lookup"><span data-stu-id="b71da-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="b71da-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b71da-121">Click Save.</span></span>
15. <span data-ttu-id="b71da-122">Klik på Udvid for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="b71da-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="b71da-123">Skriv en værdi i feltet Nyt aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="b71da-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="b71da-124">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="b71da-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="b71da-125">Klik på Forlæng.</span><span class="sxs-lookup"><span data-stu-id="b71da-125">Click Extend.</span></span>
19. <span data-ttu-id="b71da-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b71da-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]