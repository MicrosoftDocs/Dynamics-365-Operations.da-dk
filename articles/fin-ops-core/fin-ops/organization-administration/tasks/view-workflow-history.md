---
title: Vise arbejdsgangshistorik
description: Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351f9c80eab8e9810fa6a4538f003eaef1a4a4fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747219"
---
# <a name="view-workflow-history"></a><span data-ttu-id="38c53-103">Vise arbejdsgangshistorik</span><span class="sxs-lookup"><span data-stu-id="38c53-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38c53-104">Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38c53-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="38c53-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="38c53-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="38c53-106">Gå til **Navigationsrude > Moduler > Almindelig > Forespørgsler > Arbejdsgang > Arbejdsgangshistorik**.</span><span class="sxs-lookup"><span data-stu-id="38c53-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="38c53-107">Brug denne formular til at få vist status for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38c53-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="38c53-108">**Forekomst-ID'et** er identifikationskoden for den arbejdsgangsforekomst, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38c53-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="38c53-109">**Status** for arbejdsgangen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="38c53-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="38c53-110">**Arbejdsgang-ID'et** er identifikationskoden for den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38c53-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="38c53-111">**Dokumentet** er identifikationskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38c53-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="38c53-112">**Dokumenttypen** er typen af dokument, der er sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="38c53-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="38c53-113">**Arbejdsgangen** er navnet på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38c53-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="38c53-114">**Version** er versionsnummeret på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38c53-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="38c53-115">**Oprettelsesdatoen og klokkeslættet** er datoen og klokkeslættet, hvor dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="38c53-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="38c53-116">Den **Medgået tid** er den tid, der er gået, siden dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="38c53-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="38c53-117">Knappen **Genoptag** giver dig mulighed at genoptage arbejdsgangsprocessen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="38c53-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="38c53-118">Knappen **Tilbagekald** gør det muligt at tilbagekalde det valgte dokument, så det ikke bliver behandlet.</span><span class="sxs-lookup"><span data-stu-id="38c53-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="38c53-119">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="38c53-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="38c53-120">Sørg for, at afsnittet **Arbejdselementer** er udvidet.</span><span class="sxs-lookup"><span data-stu-id="38c53-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="38c53-121">I dette afsnit kan du få vist de arbejdselementer, der er knyttet til det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="38c53-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="38c53-122">For eksempel skal en opgave måske fuldføres, eller dokumentet skal muligvis godkendes.</span><span class="sxs-lookup"><span data-stu-id="38c53-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="38c53-123">Knappen **Tildel igen** åbner en dialogboks, hvor du igen kan tildele et arbejdselement til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="38c53-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="38c53-124">Sørg for, at sektionen **Sporingsdetaljer** er udvidet.</span><span class="sxs-lookup"><span data-stu-id="38c53-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="38c53-125">I denne sektion kan du få vist arbejdsgangshistorikken for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="38c53-125">In this section you can view the workflow history of the selected document.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]