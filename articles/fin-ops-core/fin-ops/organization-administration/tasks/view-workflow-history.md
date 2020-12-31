---
title: Vise arbejdsgangshistorik
description: Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d7118e85ff56f8c935c24a91dc84c6cc09641e0
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694305"
---
# <a name="view-workflow-history"></a><span data-ttu-id="3239a-103">Vise arbejdsgangshistorik</span><span class="sxs-lookup"><span data-stu-id="3239a-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3239a-104">Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="3239a-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="3239a-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="3239a-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3239a-106">Gå til **Navigationsrude > Moduler > Almindelig > Forespørgsler > Arbejdsgang > Arbejdsgangshistorik**.</span><span class="sxs-lookup"><span data-stu-id="3239a-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="3239a-107">Brug denne formular til at få vist status for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="3239a-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="3239a-108">**Forekomst-ID'et** er identifikationskoden for den arbejdsgangsforekomst, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3239a-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3239a-109">**Status** for arbejdsgangen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="3239a-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="3239a-110">**Arbejdsgang-ID'et** er identifikationskoden for den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3239a-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3239a-111">**Dokumentet** er identifikationskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3239a-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="3239a-112">**Dokumenttypen** er typen af dokument, der er sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="3239a-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="3239a-113">**Arbejdsgangen** er navnet på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3239a-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3239a-114">**Version** er versionsnummeret på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3239a-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3239a-115">**Oprettelsesdatoen og klokkeslættet** er datoen og klokkeslættet, hvor dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="3239a-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="3239a-116">Den **Medgået tid** er den tid, der er gået, siden dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="3239a-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="3239a-117">Knappen **Genoptag** giver dig mulighed at genoptage arbejdsgangsprocessen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="3239a-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="3239a-118">Knappen **Tilbagekald** gør det muligt at tilbagekalde det valgte dokument, så det ikke bliver behandlet.</span><span class="sxs-lookup"><span data-stu-id="3239a-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="3239a-119">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="3239a-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="3239a-120">Sørg for, at afsnittet **Arbejdselementer** er udvidet.</span><span class="sxs-lookup"><span data-stu-id="3239a-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="3239a-121">I dette afsnit kan du få vist de arbejdselementer, der er knyttet til det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="3239a-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="3239a-122">For eksempel skal en opgave måske fuldføres, eller dokumentet skal muligvis godkendes.</span><span class="sxs-lookup"><span data-stu-id="3239a-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="3239a-123">Knappen **Tildel igen** åbner en dialogboks, hvor du igen kan tildele et arbejdselement til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="3239a-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="3239a-124">Sørg for, at sektionen **Sporingsdetaljer** er udvidet.</span><span class="sxs-lookup"><span data-stu-id="3239a-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="3239a-125">I denne sektion kan du få vist arbejdsgangshistorikken for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="3239a-125">In this section you can view the workflow history of the selected document.</span></span>  

