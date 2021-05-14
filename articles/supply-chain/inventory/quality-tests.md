---
title: Test for kvalitetsstyring
description: I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956593"
---
# <a name="quality-management-tests"></a><span data-ttu-id="ed44c-103">Test for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ed44c-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed44c-104">I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed44c-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ed44c-105">Du kan bruge siden **Test** til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne.</span><span class="sxs-lookup"><span data-stu-id="ed44c-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="ed44c-106">Du kan tildele en eller flere individuelle test til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="ed44c-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="ed44c-107">Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="ed44c-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="ed44c-108">Måleværdier bruges til kvantitative test.</span><span class="sxs-lookup"><span data-stu-id="ed44c-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="ed44c-109">Til kvalitative test bruges testvariabler.</span><span class="sxs-lookup"><span data-stu-id="ed44c-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="ed44c-110">For kvantitativ test er feltet **Type** angivet til *Heltal* eller *Del*.</span><span class="sxs-lookup"><span data-stu-id="ed44c-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="ed44c-111">Der er også angivet en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="ed44c-111">A unit of measure is also specified.</span></span> <span data-ttu-id="ed44c-112">Kvalitetsspecifikationer og testresultater er udtrykt som tal.</span><span class="sxs-lookup"><span data-stu-id="ed44c-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="ed44c-113">For kvalitative test er feltet **Type** angivet til *Indstilling*.</span><span class="sxs-lookup"><span data-stu-id="ed44c-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="ed44c-114">Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger.</span><span class="sxs-lookup"><span data-stu-id="ed44c-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="ed44c-115">Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</span><span class="sxs-lookup"><span data-stu-id="ed44c-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="ed44c-116">Du kan også vælge at tildele et testinstrument til en test.</span><span class="sxs-lookup"><span data-stu-id="ed44c-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="ed44c-117">Testinstrumenter er dog ikke påkrævede for at oprette og bruge test sammen med kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="ed44c-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="ed44c-118">Du kan finde flere oplysninger under [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="ed44c-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="ed44c-119">Du kan også vælge at angive en enhed for en test for at angive den måleenhed, som testresultaterne skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="ed44c-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="ed44c-120">En test for temperatur kan f.eks. omfatte en enhed på grader Fahrenheit eller grader Celsius.</span><span class="sxs-lookup"><span data-stu-id="ed44c-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="ed44c-121">Eksempel på en test</span><span class="sxs-lookup"><span data-stu-id="ed44c-121">Example of a test</span></span>

<span data-ttu-id="ed44c-122">Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitativ test for skader på emballagen.</span><span class="sxs-lookup"><span data-stu-id="ed44c-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="ed44c-123">Virksomheden angiver yderligere oplysninger om den kvalitative test for at definere testvariablen (f.eks. beskadiget emballage) og udfaldet.</span><span class="sxs-lookup"><span data-stu-id="ed44c-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="ed44c-124">Firmaet bruger siden **Testgrupper** til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="ed44c-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="ed44c-125">Testgruppen tildeles en kvalitetsordre, så virksomheden kan rapportere testresultater for de to test.</span><span class="sxs-lookup"><span data-stu-id="ed44c-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="ed44c-126">Oprette en test</span><span class="sxs-lookup"><span data-stu-id="ed44c-126">Create a test</span></span>

<span data-ttu-id="ed44c-127">Benyt denne fremgangsmåde for at oprette en test.</span><span class="sxs-lookup"><span data-stu-id="ed44c-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="ed44c-128">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Test**.</span><span class="sxs-lookup"><span data-stu-id="ed44c-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="ed44c-129">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="ed44c-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ed44c-130">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="ed44c-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ed44c-131">**Test** – Angiv et entydigt id eller navn til testen.</span><span class="sxs-lookup"><span data-stu-id="ed44c-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="ed44c-132">**Beskrivelse** – Indtast en detaljeret beskrivelse af testen.</span><span class="sxs-lookup"><span data-stu-id="ed44c-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="ed44c-133">**Type** – Vælg den resultattype, som testen giver.</span><span class="sxs-lookup"><span data-stu-id="ed44c-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="ed44c-134">For kvantitative test skal du vælge *Del* eller *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="ed44c-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="ed44c-135">Vælg *Indstilling* for kvalitative test.</span><span class="sxs-lookup"><span data-stu-id="ed44c-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="ed44c-136">**Testinstrument** – Vælg et [testinstrument](quality-test-instruments.md), der skal bruges til testen.</span><span class="sxs-lookup"><span data-stu-id="ed44c-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="ed44c-137">**Enhed** – Hvis du har valgt *Del* eller *Heltal* i feltet **Type** (dvs. hvis testen er en kvantitativ test), skal du vælge den måleenhed, som testresultaterne skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="ed44c-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="ed44c-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ed44c-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="ed44c-139">Når du har gemt en test, kan du ikke længere redigere feltet **Type** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="ed44c-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="ed44c-140">Hvis du skal ændre typen af de testresultater, der registreres for en test, skal du vælge **Skift kvalitetstesttype** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ed44c-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="ed44c-141">I dialogboksen **Skift kvalitetstesttype** skal du angive feltet **Ny type** til den ønskede type og derefter vælge **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ed44c-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed44c-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ed44c-142">Additional resources</span></span>

- [<span data-ttu-id="ed44c-143">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ed44c-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="ed44c-144">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ed44c-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="ed44c-145">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ed44c-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="ed44c-146">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="ed44c-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
