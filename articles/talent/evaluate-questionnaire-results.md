---
title: Få vist og evaluere resultaterne af spørgeskemaer
description: I dette emne forklares det, hvordan du kan få vist og evaluere resultaterne af de spørgeskemaer, som svarpersonerne har udfyldt.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 38b694b6dd4b1b9a198452e409bd64d7934b4685
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517650"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="51238-103">Få vist og evaluere resultaterne af spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="51238-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51238-104">I dette emne forklares det, hvordan du kan få vist og evaluere resultaterne af de spørgeskemaer, som svarpersonerne har udfyldt.</span><span class="sxs-lookup"><span data-stu-id="51238-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="51238-105">Når svarpersonerne har udfyldt et spørgeskema, kan du få vist og evaluere spørgeskemaresultaterne på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="51238-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="51238-106">**Fuldførte besvarelser** – Få vist oplysninger om de spørgeskemaer, som svarpersonernes har udfyldte, og generér rapporter for at opsummere svar og eventuelle point, der blev opnået.</span><span class="sxs-lookup"><span data-stu-id="51238-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="51238-107">**Resultatgrupper** – Få vist oplysninger om resultatgrupper og statistikker for spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="51238-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="51238-108">Statistikker for resultatgrupper kan genereres enten for en enkelt besvarelse af et spørgeskema eller for alle besvarelser.</span><span class="sxs-lookup"><span data-stu-id="51238-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="51238-109">**Spørgeskemastatistik** – Angiv kriterier for at beregne statistik for en bestemt gruppe svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="51238-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="51238-110">Du kan også generere forskellige rapporter til visning af resultater, der sorteres efter person, besvarelse eller resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="51238-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="51238-111">Der er følgende tilgængelige rapporter vedrørende udfyldte spørgeskemaer:</span><span class="sxs-lookup"><span data-stu-id="51238-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="51238-112">Besvarelser</span><span class="sxs-lookup"><span data-stu-id="51238-112">Answers</span></span>
-   <span data-ttu-id="51238-113">Besvarelser pr. spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="51238-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="51238-114">Besvarelser pr. person.</span><span class="sxs-lookup"><span data-stu-id="51238-114">Answers per person</span></span>
-   <span data-ttu-id="51238-115">Feedbackanalyse</span><span class="sxs-lookup"><span data-stu-id="51238-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="51238-116">Resultater af besvarelser</span><span class="sxs-lookup"><span data-stu-id="51238-116">Answer session results</span></span>
<span data-ttu-id="51238-117">Når svarpersoner udfylder et spørgeskema, kan du se resultaterne af de fuldførte besvarelser.</span><span class="sxs-lookup"><span data-stu-id="51238-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="51238-118">En svarsession er en brugers svar på et spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="51238-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="51238-119">Du kan få vist detaljer om fuldførte besvarelser på siden **Svar**.</span><span class="sxs-lookup"><span data-stu-id="51238-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="51238-120">Besvarelser, der findes på siden **Svar**, er filtreret på forskellige måder, afhængigt af hvordan du åbner siden:</span><span class="sxs-lookup"><span data-stu-id="51238-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="51238-121">Alle spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="51238-121">All questionnaires</span></span>
-   <span data-ttu-id="51238-122">Et bestemt spørgeskema</span><span class="sxs-lookup"><span data-stu-id="51238-122">A specific questionnaire</span></span>
-   <span data-ttu-id="51238-123">En bestemt person</span><span class="sxs-lookup"><span data-stu-id="51238-123">A specific person</span></span>

<span data-ttu-id="51238-124">Fra siden **Svar** kan du se oplysninger om svar, opnåede point, svarpersonens svar i hver resultatgruppe og det spørgsmålshierarki, der blev brugt til det valgte spørgeskema, hvis der blev brugt spørgsmålshierarki.</span><span class="sxs-lookup"><span data-stu-id="51238-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="51238-125">Du kan også generere og udskrive følgende rapporter:</span><span class="sxs-lookup"><span data-stu-id="51238-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="51238-126">**Resultatrapport** – denne rapport viser en grafisk repræsentation af de point, der blev opnået pr. resultatgruppe for den valgte besvarelse.</span><span class="sxs-lookup"><span data-stu-id="51238-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="51238-127">**Svarrapport** – denne rapport viser de svar, som svarpersonen valgte for hver enkelt spørgsmål i spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="51238-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="51238-128">**Forkerte svar** – denne rapport indeholder oplysninger, der er relateret til de forkerte svar, som svarpersonen valgte.</span><span class="sxs-lookup"><span data-stu-id="51238-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="51238-129">**Bemærk!** Rapporten **Resultater** er kun tilgængelig, hvis du bruger resultatgrupper på spørgeskemaet, og hvis du har valgt **Resultatside** på siden **Spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="51238-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="51238-130">Rapporten **Smart** og rapporten **Forkerte svar** er kun tilgængelige, hvis du har valgt **Svarrapport** på siden **Spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="51238-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="51238-131">Spørgeskemastatistik</span><span class="sxs-lookup"><span data-stu-id="51238-131">Questionnaire statistics</span></span>
<span data-ttu-id="51238-132">Du kan bruge spørgeskemastatistik til at analysere resultaterne af et udfyldt spørgeskema baseret på beregninger, som du definerer.</span><span class="sxs-lookup"><span data-stu-id="51238-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="51238-133">Når du skal definere beregninger, skal du udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="51238-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="51238-134">Vælg kriterier til at beregne og få vist statistikken.</span><span class="sxs-lookup"><span data-stu-id="51238-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="51238-135">Du kan få vist statistik efter spørgeskema, spørgsmål, spørgsmålsrækker eller grupper af resultater.</span><span class="sxs-lookup"><span data-stu-id="51238-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="51238-136">Vælg den type diagram, der skal bruges, når du får vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="51238-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="51238-137">Vælg persontyper fra netværket, f.eks. medarbejder, kontakter eller ansøger, som du vil medtage svar fra.</span><span class="sxs-lookup"><span data-stu-id="51238-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="51238-138">Du kan også medtage svar fra spørgeskemaer, der blev fuldført anonymt.</span><span class="sxs-lookup"><span data-stu-id="51238-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="51238-139">Definer intervaller, der er baseret på alder eller anciennitet for at analysere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="51238-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="51238-140">Vælg eller kontrollér indstillinger, der afgrænser emnet i statistikken.</span><span class="sxs-lookup"><span data-stu-id="51238-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="51238-141">Ved at vælge et postnummer kan du f.eks. analysere resultater fra alle svarpersoner i et specifikt geografisk område.</span><span class="sxs-lookup"><span data-stu-id="51238-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="51238-142">Vælg eller bekræft kriterier til at analysere resultaterne efter svarperson eller spørgeskemakarakteristika.</span><span class="sxs-lookup"><span data-stu-id="51238-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="51238-143">Hvis du vælger **Postnummer**, kan du f.eks. analysere korrelationen mellem en svarpersons placering og korrekte svar.</span><span class="sxs-lookup"><span data-stu-id="51238-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="51238-144">De indstillinger, du definerer, gemmes og kan bruges til at genberegne resultater med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="51238-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="51238-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="51238-145">Additional resources</span></span>
--------

[<span data-ttu-id="51238-146">Udforme spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="51238-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="51238-147">Brug af spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="51238-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="51238-148">Distribution og udfyldning af et spørgeskema</span><span class="sxs-lookup"><span data-stu-id="51238-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

