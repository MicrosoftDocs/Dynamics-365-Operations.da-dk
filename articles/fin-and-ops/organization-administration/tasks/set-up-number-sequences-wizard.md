--- 
title: Opret nummerserier vha. en guide
description: "Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er."
author: sericks007
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1aaea94678e9ddfa771c21063f53aefa172b5e97
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="f4c72-103">Opret nummerserier vha. en guide</span><span class="sxs-lookup"><span data-stu-id="f4c72-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c72-104">Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er.</span><span class="sxs-lookup"><span data-stu-id="f4c72-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="f4c72-105">En masterdata- eller transaktionspost, der kræver et id, kaldes en reference.</span><span class="sxs-lookup"><span data-stu-id="f4c72-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="f4c72-106">Før du kan oprette nye poster for en reference, skal du konfigurere en nummerserie og knytte den til referencen.</span><span class="sxs-lookup"><span data-stu-id="f4c72-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="f4c72-107">Denne fremgangsmåde forklarer, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="f4c72-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="f4c72-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f4c72-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f4c72-109">Gå til Virksomhedsadministration > Nummerserier > Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="f4c72-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="f4c72-110">Klik på Generer.</span><span class="sxs-lookup"><span data-stu-id="f4c72-110">Click Generate.</span></span>
3. <span data-ttu-id="f4c72-111">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="f4c72-111">Click Next.</span></span>
    * <span data-ttu-id="f4c72-112">På denne side kan du redigere identifikationskoden, den laveste værdi og den højeste værdi.</span><span class="sxs-lookup"><span data-stu-id="f4c72-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="f4c72-113">Du kan også angive, om nummerserien skal være fortløbende.</span><span class="sxs-lookup"><span data-stu-id="f4c72-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="f4c72-114">Du skal ikke markere indstillingen Fortløbende, hvis du skal forudallokere numre til nummerserien.</span><span class="sxs-lookup"><span data-stu-id="f4c72-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="f4c72-115">Hvis du vil føje et områdesegment til en nummerseries format, skal du vælge formatet på listen og derefter klikke på Medtager område i format.</span><span class="sxs-lookup"><span data-stu-id="f4c72-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="f4c72-116">Hvis du vil fjerne et områdesegment fra en nummerseries format, skal du vælge formatet på listen og derefter klikke på Fjerner område fra format.</span><span class="sxs-lookup"><span data-stu-id="f4c72-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="f4c72-117">Hvis du vil udelukke en nummerserie fra automatisk generering, skal du vælge nummerserien på listen og derefter klikke på Slet.</span><span class="sxs-lookup"><span data-stu-id="f4c72-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="f4c72-118">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="f4c72-118">Click Next.</span></span>
5. <span data-ttu-id="f4c72-119">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="f4c72-119">Click Finish.</span></span>


