---
title: Oprette nummerserier ved hjælp af en guide
description: I dette emne beskrives, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867382"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="2e849-103">Oprette nummerserier ved hjælp af en guide</span><span class="sxs-lookup"><span data-stu-id="2e849-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e849-104">Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er.</span><span class="sxs-lookup"><span data-stu-id="2e849-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="2e849-105">En masterdata- eller transaktionspost, der kræver et id, kaldes en reference.</span><span class="sxs-lookup"><span data-stu-id="2e849-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="2e849-106">Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen.</span><span class="sxs-lookup"><span data-stu-id="2e849-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="2e849-107">I dette emne beskrives, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="2e849-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="2e849-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="2e849-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2e849-109">Gå til **Navigation > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="2e849-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="2e849-110">Vælg **Generer**.</span><span class="sxs-lookup"><span data-stu-id="2e849-110">Select **Generate**.</span></span>
3. <span data-ttu-id="2e849-111">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2e849-111">Select **Next**.</span></span>

   - <span data-ttu-id="2e849-112">På denne side kan du redigere identifikationskoden, den laveste værdi og den højeste værdi.</span><span class="sxs-lookup"><span data-stu-id="2e849-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="2e849-113">Du kan også angive, om nummerserien skal være fortløbende.</span><span class="sxs-lookup"><span data-stu-id="2e849-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="2e849-114">Du skal ikke markere indstillingen **Fortløbende**, hvis du skal forudallokere numre til nummerserien.</span><span class="sxs-lookup"><span data-stu-id="2e849-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="2e849-115">Hvis du vil føje et områdesegment til en nummerseries format, skal du vælge formatet på listen og derefter vælge **Medtager område i format**.</span><span class="sxs-lookup"><span data-stu-id="2e849-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="2e849-116">Hvis du vil fjerne et områdesegment fra en nummerseries format, skal du vælge formatet på listen og derefter vælge **Fjerner område fra format**.</span><span class="sxs-lookup"><span data-stu-id="2e849-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="2e849-117">Hvis du vil udelukke en nummerserie fra automatisk generering, skal du vælge nummerserien på listen og derefter vælge **Slet**.</span><span class="sxs-lookup"><span data-stu-id="2e849-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="2e849-118">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2e849-118">Select **Next**.</span></span>
5. <span data-ttu-id="2e849-119">Vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="2e849-119">Select **Finish**.</span></span>

