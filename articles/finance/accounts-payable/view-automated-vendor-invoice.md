---
title: Se automatiseringsresultater for kreditorfaktura (prøveversion)
description: Dette emne forklarer, hvordan du kan få vist status for kreditorfakturaer i den automatiske send-til-arbejdsgang-proces.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec49a621e24b6373532497b499e8b9d45c9bed14
ms.sourcegitcommit: 30c541426cf2037b768e3556e1b170a64991f64a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/17/2020
ms.locfileid: "4441731"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="0b0cc-103">Få vist resultater af automatisering af kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="0b0cc-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b0cc-104">Dette emne forklarer, hvordan du kan få vist status for kreditorfakturaer i den automatiske send-til-arbejdsgang-proces.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="0b0cc-105">Detaljerede oplysninger om automatiseringshistorikken opretholdes for hver af de importerede kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="0b0cc-106">Afhængigt af de forretningsprocesser, du har automatiseret, viser siden **Ventende kreditorfakturaer** **Status for automatisk kvitteringsafstemning** og **Status for automatisk afsendelse til arbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="0b0cc-107">Du kan få vist detaljerne og oprette en plan for at fokusere på de fakturaer, der ikke kunne udføres i et automatiseret trin.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="0b0cc-108">Derefter kan du genoptage den automatiserede proces for den importerede faktura, når du har løst problemet.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="0b0cc-109">Før du kan redigere en faktura, der er sendt, skal du afbryde den automatiserede behandling midlertidigt.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="0b0cc-110">Hvis en faktura i den automatiske afsendelse til arbejdsgang-proces skal afbrydes midlertidigt, skal du angive indstillingen **Medtag i automatisk behandling** til **Nej** på siden **Kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="0b0cc-111">Automatisering kører derefter ikke, før **Medtag i automatisk behandling** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="0b0cc-112">En faktura kan afbrydes midlertidigt fra yderligere automatisering, hvis den endnu ikke er i arbejdsprocessystemet, og den ikke bruges af den automatiserede proces.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="0b0cc-113">Hvis en importeret faktura er underlagt afsendelse til arbejdsgang-processen, kan du få vist værdien af dens **Status for automatisering** på siden **Kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="0b0cc-114">Følgende statusangivelser registreres:</span><span class="sxs-lookup"><span data-stu-id="0b0cc-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="0b0cc-115">**Medtages** – De automatiserede processer, der er defineret på siden **Kreditorparametre**, kører korrekt, men er endnu ikke fuldført.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="0b0cc-116">**Midlertidigt afbrudt** – De automatiserede processer, der er defineret på siden **Kreditorparametre**, er kørt, men mindst ét trin i processen mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="0b0cc-117">Statussen **Afbrudt midlertidigt** anvendes også, hvis feltet **Medtag i automatisk behandling** er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="0b0cc-118">Du kan få vist fejlene ved at vælge **Vis seneste resultater**.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="0b0cc-119">**I arbejdsgang** – Den importerede faktura er sendt til arbejdsgangssystemet enten af den automatiske afsendelse til arbejdsgang eller manuelt.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="0b0cc-120">**Fuldført arbejdsgang** – Arbejdsgangsprocessen er fuldført for den importerede faktura.</span><span class="sxs-lookup"><span data-stu-id="0b0cc-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
