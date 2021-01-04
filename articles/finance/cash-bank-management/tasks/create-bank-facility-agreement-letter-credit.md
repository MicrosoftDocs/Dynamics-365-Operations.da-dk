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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb624700e0b052de977fabecf9670b3515d32ab7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441546"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="47f8f-103">Oprette en bankfacilitetsaftale for en remburs</span><span class="sxs-lookup"><span data-stu-id="47f8f-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47f8f-104">Denne opgave fører dig gennem oprettelse af en bankfacilitetsaftale til behandling af en remburs.</span><span class="sxs-lookup"><span data-stu-id="47f8f-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="47f8f-105">Du vil konfigurere bankfaciliteter og posteringsprofiler før denne opgave.</span><span class="sxs-lookup"><span data-stu-id="47f8f-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="47f8f-106">Denne opgave bruger demofirmaet "USMF".</span><span class="sxs-lookup"><span data-stu-id="47f8f-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="47f8f-107">Oprette bankfacilitetsaftale</span><span class="sxs-lookup"><span data-stu-id="47f8f-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="47f8f-108">Gå til Kontant- og bankstyring > Remburser > Bankfacilitetsaftaler.</span><span class="sxs-lookup"><span data-stu-id="47f8f-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="47f8f-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="47f8f-109">Click New.</span></span>
3. <span data-ttu-id="47f8f-110">Indtast aftalenummeret i henhold til aftalen med banken i feltet Aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="47f8f-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="47f8f-111">Angiv kontonummeret i den udstedende bank i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="47f8f-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="47f8f-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="47f8f-113">Angiv en dato og et klokkeslæt i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="47f8f-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="47f8f-114">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="47f8f-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="47f8f-115">Udvis eller skjul sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="47f8f-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="47f8f-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="47f8f-116">Click Add line.</span></span>
10. <span data-ttu-id="47f8f-117">Klik på rullelisten i feltet Facilitetstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="47f8f-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="47f8f-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="47f8f-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="47f8f-120">Angiv det facilitetsbeløb, der er forhandlet med banken, i feltet Grænse.</span><span class="sxs-lookup"><span data-stu-id="47f8f-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="47f8f-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47f8f-121">Click Save.</span></span>
15. <span data-ttu-id="47f8f-122">Klik på Udvid for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="47f8f-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="47f8f-123">Skriv en værdi i feltet Nyt aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="47f8f-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="47f8f-124">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="47f8f-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="47f8f-125">Klik på Forlæng.</span><span class="sxs-lookup"><span data-stu-id="47f8f-125">Click Extend.</span></span>
19. <span data-ttu-id="47f8f-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47f8f-126">Close the page.</span></span>

