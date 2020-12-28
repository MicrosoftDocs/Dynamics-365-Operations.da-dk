---
title: Importere konfigurationer for elektronisk OIOUBL-fakturering
description: Denne procedure viser, hvordan du importerer elektroniske OIOUBL-fakturakonfigurationer.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c8cd44d574787eef79c162c8ec8ce14f09abeb3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407688"
---
# <a name="import-oioubl-electronic-invoicing-configurations"></a><span data-ttu-id="c4255-103">Importere konfigurationer for elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="c4255-103">Import OIOUBL electronic invoicing configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4255-104">Denne procedure viser, hvordan du importerer elektroniske OIOUBL-fakturakonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="c4255-104">This procedure shows how to import OIOUBL electronic invoice configurations.</span></span> 



<span data-ttu-id="c4255-105">Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.</span><span class="sxs-lookup"><span data-stu-id="c4255-105">This task was created using the demo data company USMF with the country/region of legal entity primary address updated to Denmark.</span></span>



<span data-ttu-id="c4255-106">Det er den første af seks opgaver, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="c4255-106">This is the first of six tasks that demonstrate the process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="c4255-107">Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="c4255-107">This task uses the OIOUBL e-invoice example, which is common for Denmark, Austria, and Norway.</span></span>

1. <span data-ttu-id="c4255-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="c4255-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c4255-109">Vælg Microsoft på listen over konfigurationsudbydere.</span><span class="sxs-lookup"><span data-stu-id="c4255-109">In the list of Configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="c4255-110">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="c4255-110">Click Set active.</span></span>
4. <span data-ttu-id="c4255-111">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="c4255-111">Click Repositories.</span></span>
5. <span data-ttu-id="c4255-112">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="c4255-112">Click Open.</span></span>
6. <span data-ttu-id="c4255-113">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="c4255-113">Click Show filters.</span></span>
7. <span data-ttu-id="c4255-114">Anvend følgende filtre: Angiv filterværdien "OIOUBL salgsfaktura" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"</span><span class="sxs-lookup"><span data-stu-id="c4255-114">Apply the following filters: Enter a filter value of "OIOUBL Sales invoice" on the "Configuration name" field using the "begins with" filter operator</span></span>
8. <span data-ttu-id="c4255-115">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="c4255-115">Click Import.</span></span>
9. <span data-ttu-id="c4255-116">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="c4255-116">Click Yes.</span></span>
10. <span data-ttu-id="c4255-117">Anvend følgende filtre: Angiv filterværdien "OIOUBL kreditnota" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"</span><span class="sxs-lookup"><span data-stu-id="c4255-117">Apply the following filters: Enter a filter value of "OIOUBL Sales credit note" on the "Configuration name" field using the "begins with" filter operator</span></span>
11. <span data-ttu-id="c4255-118">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="c4255-118">Click Import.</span></span>
12. <span data-ttu-id="c4255-119">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="c4255-119">Click Yes.</span></span>
13. <span data-ttu-id="c4255-120">Anvend følgende filtre: Angiv filterværdien "OIOUBL projektfaktura" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"</span><span class="sxs-lookup"><span data-stu-id="c4255-120">Apply the following filters: Enter a filter value of "OIOUBL Project invoice" on the "Configuration name" field using the "begins with" filter operator</span></span>
14. <span data-ttu-id="c4255-121">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="c4255-121">Click Import.</span></span>
15. <span data-ttu-id="c4255-122">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="c4255-122">Click Yes.</span></span>
16. <span data-ttu-id="c4255-123">Anvend følgende filtre: Angiv filterværdien "OIOUBL projektkreditnota" i feltet "Konfigurationsnavn" ved hjælp af filteroperatoren "starter med"</span><span class="sxs-lookup"><span data-stu-id="c4255-123">Apply the following filters: Enter a filter value of "OIOUBL Project credit note" on the "Configuration name" field using the "begins with" filter operator</span></span>
17. <span data-ttu-id="c4255-124">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="c4255-124">Click Import.</span></span>
18. <span data-ttu-id="c4255-125">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="c4255-125">Click Yes.</span></span>

