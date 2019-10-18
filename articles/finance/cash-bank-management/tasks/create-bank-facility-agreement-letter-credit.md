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
ms.openlocfilehash: 9e63e0ffa4ddafd38595d7e9d84ffa2399a9f67b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188205"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="761c2-103">Oprette en bankfacilitetsaftale for en remburs</span><span class="sxs-lookup"><span data-stu-id="761c2-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="761c2-104">Denne opgave fører dig gennem oprettelse af en bankfacilitetsaftale til behandling af en remburs.</span><span class="sxs-lookup"><span data-stu-id="761c2-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="761c2-105">Du vil konfigurere bankfaciliteter og posteringsprofiler før denne opgave.</span><span class="sxs-lookup"><span data-stu-id="761c2-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="761c2-106">Denne opgave bruger demofirmaet "USMF".</span><span class="sxs-lookup"><span data-stu-id="761c2-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="761c2-107">Oprette bankfacilitetsaftale</span><span class="sxs-lookup"><span data-stu-id="761c2-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="761c2-108">Gå til Kontant- og bankstyring > Remburser > Bankfacilitetsaftaler.</span><span class="sxs-lookup"><span data-stu-id="761c2-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="761c2-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="761c2-109">Click New.</span></span>
3. <span data-ttu-id="761c2-110">Indtast aftalenummeret i henhold til aftalen med banken i feltet Aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="761c2-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="761c2-111">Angiv kontonummeret i den udstedende bank i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="761c2-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="761c2-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="761c2-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="761c2-113">Angiv en dato og et klokkeslæt i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="761c2-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="761c2-114">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="761c2-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="761c2-115">Udvis eller skjul sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="761c2-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="761c2-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="761c2-116">Click Add line.</span></span>
10. <span data-ttu-id="761c2-117">Klik på rullelisten i feltet Facilitetstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="761c2-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="761c2-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="761c2-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="761c2-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="761c2-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="761c2-120">Angiv det facilitetsbeløb, der er forhandlet med banken, i feltet Grænse.</span><span class="sxs-lookup"><span data-stu-id="761c2-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="761c2-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="761c2-121">Click Save.</span></span>
15. <span data-ttu-id="761c2-122">Klik på Udvid for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="761c2-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="761c2-123">Skriv en værdi i feltet Nyt aftalenummer.</span><span class="sxs-lookup"><span data-stu-id="761c2-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="761c2-124">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="761c2-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="761c2-125">Klik på Forlæng.</span><span class="sxs-lookup"><span data-stu-id="761c2-125">Click Extend.</span></span>
19. <span data-ttu-id="761c2-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="761c2-126">Close the page.</span></span>

