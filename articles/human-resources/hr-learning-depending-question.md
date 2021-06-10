---
title: Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål
description: Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39da0418f60273a82cb51e5cf3aad60e4efdb234
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056654"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="d82ef-103">Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål</span><span class="sxs-lookup"><span data-stu-id="d82ef-103">Make a question dependent on the answer of the previous question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="d82ef-104">Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="d82ef-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="d82ef-105">For eksempel, hvis du spørger "Foretrækker du kaffe eller te", bestemmes et logisk opfølgende spørgsmål afhængigt af om svarpersonen vælger kaffe eller te som deres svar.</span><span class="sxs-lookup"><span data-stu-id="d82ef-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="d82ef-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="d82ef-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="d82ef-107">Find det eksisterende spørgeskema</span><span class="sxs-lookup"><span data-stu-id="d82ef-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="d82ef-108">Gå til Spørgeskema > Design > Spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="d82ef-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="d82ef-109">Markér WorkFH-spørgeskemaet på listen.</span><span class="sxs-lookup"><span data-stu-id="d82ef-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="d82ef-110">Føj alle spørgsmål og underspørgsmål til spørgeskemaet</span><span class="sxs-lookup"><span data-stu-id="d82ef-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="d82ef-111">Klik på Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="d82ef-111">Click Questions.</span></span>
2. <span data-ttu-id="d82ef-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d82ef-112">Click New.</span></span>
3. <span data-ttu-id="d82ef-113">Vælg spørgsmålsnummer 00016 i feltet Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="d82ef-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="d82ef-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d82ef-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d82ef-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d82ef-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d82ef-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d82ef-116">Click Save.</span></span>
7. <span data-ttu-id="d82ef-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d82ef-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="d82ef-118">Angive Spørgeskemasekvensen til Betinget, og gør spørgsmålet afhængigt af det relevante spørgsmål</span><span class="sxs-lookup"><span data-stu-id="d82ef-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="d82ef-119">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d82ef-119">Click Edit.</span></span>
2. <span data-ttu-id="d82ef-120">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d82ef-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="d82ef-121">Vælg "Betinget" i feltet Spørgsmålsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="d82ef-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="d82ef-122">Klik på Betinget spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="d82ef-122">Click Conditional question.</span></span>
5. <span data-ttu-id="d82ef-123">Vælg "Questions\Explain hvorfor du besvarede det forrige spørgsmål som du gjorde?" i træet.</span><span class="sxs-lookup"><span data-stu-id="d82ef-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="d82ef-124">Vælg spørgsmål 00009 i feltet Overordnet spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="d82ef-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="d82ef-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d82ef-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d82ef-126">Angiv det svarsekvens-id for den svarmulighed, du vil gøre spørgsmålet afhængigt af, i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="d82ef-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="d82ef-127">Angiv for eksempel 1 til den første Smart-indstilling.</span><span class="sxs-lookup"><span data-stu-id="d82ef-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="d82ef-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d82ef-128">Click Save.</span></span>
10. <span data-ttu-id="d82ef-129">Vælg '"Spørgsmål\Jeg betales rimeligt for det arbejde, jeg udfører.".</span><span class="sxs-lookup"><span data-stu-id="d82ef-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="d82ef-130">Bemærk, at spørgsmålstræet opdateres for at vise afhængigheden.</span><span class="sxs-lookup"><span data-stu-id="d82ef-130">Note that the question tree updated to show the dependency.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]