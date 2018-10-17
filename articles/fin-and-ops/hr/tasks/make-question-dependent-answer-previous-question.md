--- 
title: "Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål"
description: "Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: deb79398f5a0ebdbdb774c106c90ca50a69c275e
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="4dff8-103">Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål</span><span class="sxs-lookup"><span data-stu-id="4dff8-103">Make a question dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dff8-104">Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="4dff8-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="4dff8-105">For eksempel, hvis du spørger "Foretrækker du kaffe eller te", bestemmes et logisk opfølgende spørgsmål afhængigt af om svarpersonen vælger kaffe eller te som deres svar.</span><span class="sxs-lookup"><span data-stu-id="4dff8-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="4dff8-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="4dff8-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="4dff8-107">Find det eksisterende spørgeskema</span><span class="sxs-lookup"><span data-stu-id="4dff8-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="4dff8-108">Gå til Spørgeskema > Design > Spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="4dff8-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="4dff8-109">Markér WorkFH-spørgeskemaet på listen.</span><span class="sxs-lookup"><span data-stu-id="4dff8-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="4dff8-110">Føj alle spørgsmål og underspørgsmål til spørgeskemaet</span><span class="sxs-lookup"><span data-stu-id="4dff8-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="4dff8-111">Klik på Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="4dff8-111">Click Questions.</span></span>
2. <span data-ttu-id="4dff8-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4dff8-112">Click New.</span></span>
3. <span data-ttu-id="4dff8-113">Vælg spørgsmålsnummer 00016 i feltet Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="4dff8-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="4dff8-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4dff8-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4dff8-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4dff8-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4dff8-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4dff8-116">Click Save.</span></span>
7. <span data-ttu-id="4dff8-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4dff8-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="4dff8-118">Angive Spørgeskemasekvensen til Betinget, og gør spørgsmålet afhængigt af det relevante spørgsmål</span><span class="sxs-lookup"><span data-stu-id="4dff8-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="4dff8-119">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="4dff8-119">Click Edit.</span></span>
2. <span data-ttu-id="4dff8-120">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4dff8-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="4dff8-121">Vælg "Betinget" i feltet Spørgsmålsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="4dff8-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="4dff8-122">Klik på Betinget spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="4dff8-122">Click Conditional question.</span></span>
5. <span data-ttu-id="4dff8-123">Vælg "Questions\Explain hvorfor du besvarede det forrige spørgsmål som du gjorde?" i træet.</span><span class="sxs-lookup"><span data-stu-id="4dff8-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="4dff8-124">Vælg spørgsmål 00009 i feltet Overordnet spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="4dff8-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="4dff8-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4dff8-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4dff8-126">Angiv det svarsekvens-id for den svarmulighed, du vil gøre spørgsmålet afhængigt af, i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="4dff8-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="4dff8-127">Angiv for eksempel 1 til den første Smart-indstilling.</span><span class="sxs-lookup"><span data-stu-id="4dff8-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="4dff8-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4dff8-128">Click Save.</span></span>
10. <span data-ttu-id="4dff8-129">Vælg '"Spørgsmål\Jeg betales rimeligt for det arbejde, jeg udfører.".</span><span class="sxs-lookup"><span data-stu-id="4dff8-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="4dff8-130">Bemærk, at spørgsmålstræet opdateres for at vise afhængigheden.</span><span class="sxs-lookup"><span data-stu-id="4dff8-130">Note that the question tree updated to show the dependency.</span></span>  


