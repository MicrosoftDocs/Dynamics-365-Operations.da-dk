---
title: Vis arbejdsgangshistorik
description: Brug disse trin for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560446"
---
# <a name="view-workflow-history"></a><span data-ttu-id="97e6f-103">Vis arbejdsgangshistorik</span><span class="sxs-lookup"><span data-stu-id="97e6f-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97e6f-104">Brug disse trin for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="97e6f-104">Use these steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="97e6f-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="97e6f-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="97e6f-106">Gå til Generelt > Forespørgsler > Arbejdsgang > Arbejdsgangshistorik.</span><span class="sxs-lookup"><span data-stu-id="97e6f-106">Go to Common > Inquiries > Workflow > Workflow history.</span></span>
    * <span data-ttu-id="97e6f-107">Brug denne formular til at få vist status for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="97e6f-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    * <span data-ttu-id="97e6f-108">Forekomst-id'et er identifikationskoden for den arbejdsgangsforekomst, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-108">The Instance ID is      the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="97e6f-109">Status for arbejdsgangen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="97e6f-109">The Status is the workflow status of the document.</span></span>  
    * <span data-ttu-id="97e6f-110">Arbejdsgang-id'et er identifikationskoden for den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-110">The Workflow ID is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="97e6f-111">Dokumentet er identifikationskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-111">The Document is the identification code of the document.</span></span>  
    * <span data-ttu-id="97e6f-112">Dokumenttypen er typen af dokument, der er sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="97e6f-112">The Document type is the type of document that was submitted for processing.</span></span>  
    * <span data-ttu-id="97e6f-113">Arbejdsgangen er navnet på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-113">The Workflow is the name of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="97e6f-114">Versionsnummeret er versionsnummeret på den arbejdsgang, der behandler eller har behandlet dokumentet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-114">The Version is the version number of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="97e6f-115">Oprettelsesdatoen og klokkeslættet er datoen og klokkeslættet, hvor dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="97e6f-115">The Created date and time is the date and time that the document was submitted.</span></span>  
    * <span data-ttu-id="97e6f-116">Den medgåede tid er den tid, der er gået, siden dokumentet blev sendt.</span><span class="sxs-lookup"><span data-stu-id="97e6f-116">The Elapsed time is the time that has passed since the document was submitted.</span></span>  
    * <span data-ttu-id="97e6f-117">Knappen Genoptag giver dig mulighed at genoptage arbejdsgangsprocessen for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="97e6f-117">The Resume button allows you to resume the workflow process for the selected document.</span></span>  
    * <span data-ttu-id="97e6f-118">Knappen Tilbagekald gør det muligt at tilbagekalde det valgte dokument, så det ikke bliver behandlet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-118">The Recall button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="97e6f-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="97e6f-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="97e6f-120">Sørg for, at afsnittet Arbejdselementer er udvidet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-120">Make sure the Work items section is expanded.</span></span>    <span data-ttu-id="97e6f-121">I dette afsnit kan du få vist de arbejdselementer, der er knyttet til det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="97e6f-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="97e6f-122">For eksempel skal en opgave måske fuldføres, eller dokumentet skal muligvis godkendes.</span><span class="sxs-lookup"><span data-stu-id="97e6f-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    * <span data-ttu-id="97e6f-123">Knappen Tildel igen åbner en dialogboks, hvor du igen kan tildele et arbejdselement til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="97e6f-123">The Reassign button will open a dialog box where you can reassign a work item to another user.</span></span>  
    * <span data-ttu-id="97e6f-124">Sørg for, at sektionen Sporingsdetaljer er udvidet.</span><span class="sxs-lookup"><span data-stu-id="97e6f-124">Make sure the Tracking details section is expanded.</span></span>    <span data-ttu-id="97e6f-125">I denne sektion kan du få vist arbejdsgangshistorikken for det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="97e6f-125">In this section you can view the workflow history of the selected document.</span></span>  

