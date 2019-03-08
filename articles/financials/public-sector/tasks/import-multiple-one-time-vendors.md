---
title: Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor
description: Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssige relationer med, samtidig med at du opretter en post for kreditoren.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendImportOneTimeVendFileUpload_PSN
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 650215df59018d6a930e432483f5bc3d73fef692
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370261"
---
# <a name="import-and-create-multiple-one-time-vendors-and-invoices-in-the-public-sector"></a><span data-ttu-id="722e6-103">Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="722e6-103">Import and create multiple one-time vendors and invoices in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="722e6-104">Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssige relationer med, samtidig med at du opretter en post for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="722e6-104">When approval or a contract in the form of a purchase order is not required, you can create an invoice for a new vendor with whom you have no regular relationship, at the same time as creating a record for the vendor.</span></span> <span data-ttu-id="722e6-105">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="722e6-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="722e6-106">Gå til Kreditor > Periodiske opgaver > Importer engangskreditorer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="722e6-106">Go to Accounts payable > Periodic tasks > Import one-time vendors and invoices.</span></span>
2. <span data-ttu-id="722e6-107">Søg efter og vælg den csv-fil, der indeholder leverandøroplysninger.</span><span class="sxs-lookup"><span data-stu-id="722e6-107">Browse for and select the CSV file that contains vendor information.</span></span>
3. <span data-ttu-id="722e6-108">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="722e6-108">In the Account structure field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="722e6-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="722e6-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="722e6-110">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="722e6-110">Click OK.</span></span>
    * <span data-ttu-id="722e6-111">Kreditor- og fakturaoplysningerne er importeret.</span><span class="sxs-lookup"><span data-stu-id="722e6-111">The vendor and invoice information is imported.</span></span> <span data-ttu-id="722e6-112">Hvis der er fejl, bliver der udskrevet en rapport, og du skal rette alle de angivne poster i importfilen og derefter importere filen igen.</span><span class="sxs-lookup"><span data-stu-id="722e6-112">If there are errors, a report will be printed, and you should correct any listed entries in the import file and then reimport the file.</span></span>  
6. <span data-ttu-id="722e6-113">Gå til Kreditor > Periodiske opgaver > Behandl engangskreditorer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="722e6-113">Go to Accounts payable > Periodic tasks > Process one-time vendors and invoices.</span></span>
    * <span data-ttu-id="722e6-114">Der søges efter dublerede kreditornavne eller Federal Tax Id.</span><span class="sxs-lookup"><span data-stu-id="722e6-114">Duplicate vendor names or Federal tax IDs will be looked for.</span></span>  <span data-ttu-id="722e6-115">Vigtigt! Hvis du vælger ikke at behandle dublerede kreditorer, behandles de relaterede fakturaer heller ikke.</span><span class="sxs-lookup"><span data-stu-id="722e6-115">Important: If you choose not to process duplicate vendors, the related invoices won’t be processed either.</span></span> <span data-ttu-id="722e6-116">Du kan manuelt oprette en faktura ved hjælp af oplysningerne i CSV-filen.</span><span class="sxs-lookup"><span data-stu-id="722e6-116">You can manually create an invoice by using the information in the CSV file.</span></span>    
7. <span data-ttu-id="722e6-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="722e6-117">Click OK.</span></span>

