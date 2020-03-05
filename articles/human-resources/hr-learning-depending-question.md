---
title: Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål
description: Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e49814212b69a618fc3d855b7e290e6b6ff303
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008563"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="e4904-103">Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e4904-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="e4904-104">Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4904-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="e4904-105">For eksempel, hvis du spørger "Foretrækker du kaffe eller te", bestemmes et logisk opfølgende spørgsmål afhængigt af om svarpersonen vælger kaffe eller te som deres svar.</span><span class="sxs-lookup"><span data-stu-id="e4904-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="e4904-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="e4904-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="e4904-107">Find det eksisterende spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e4904-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="e4904-108">Gå til Spørgeskema > Design > Spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="e4904-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="e4904-109">Markér WorkFH-spørgeskemaet på listen.</span><span class="sxs-lookup"><span data-stu-id="e4904-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="e4904-110">Føj alle spørgsmål og underspørgsmål til spørgeskemaet</span><span class="sxs-lookup"><span data-stu-id="e4904-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="e4904-111">Klik på Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4904-111">Click Questions.</span></span>
2. <span data-ttu-id="e4904-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e4904-112">Click New.</span></span>
3. <span data-ttu-id="e4904-113">Vælg spørgsmålsnummer 00016 i feltet Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4904-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="e4904-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e4904-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e4904-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e4904-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e4904-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4904-116">Click Save.</span></span>
7. <span data-ttu-id="e4904-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e4904-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="e4904-118">Angive Spørgeskemasekvensen til Betinget, og gør spørgsmålet afhængigt af det relevante spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e4904-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="e4904-119">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="e4904-119">Click Edit.</span></span>
2. <span data-ttu-id="e4904-120">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e4904-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="e4904-121">Vælg "Betinget" i feltet Spørgsmålsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e4904-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="e4904-122">Klik på Betinget spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4904-122">Click Conditional question.</span></span>
5. <span data-ttu-id="e4904-123">Vælg "Questions\Explain hvorfor du besvarede det forrige spørgsmål som du gjorde?" i træet.</span><span class="sxs-lookup"><span data-stu-id="e4904-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="e4904-124">Vælg spørgsmål 00009 i feltet Overordnet spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4904-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="e4904-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e4904-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e4904-126">Angiv det svarsekvens-id for den svarmulighed, du vil gøre spørgsmålet afhængigt af, i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="e4904-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="e4904-127">Angiv for eksempel 1 til den første Smart-indstilling.</span><span class="sxs-lookup"><span data-stu-id="e4904-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="e4904-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4904-128">Click Save.</span></span>
10. <span data-ttu-id="e4904-129">Vælg '"Spørgsmål\Jeg betales rimeligt for det arbejde, jeg udfører.".</span><span class="sxs-lookup"><span data-stu-id="e4904-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="e4904-130">Bemærk, at spørgsmålstræet opdateres for at vise afhængigheden.</span><span class="sxs-lookup"><span data-stu-id="e4904-130">Note that the question tree updated to show the dependency.</span></span>  
