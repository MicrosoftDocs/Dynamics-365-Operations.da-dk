---
title: Test for kvalitetsstyring
description: I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021678"
---
# <a name="quality-management-tests"></a><span data-ttu-id="7b229-103">Test for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="7b229-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b229-104">I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b229-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7b229-105">Du kan bruge siden **Test** til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne.</span><span class="sxs-lookup"><span data-stu-id="7b229-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="7b229-106">Du kan tildele en eller flere individuelle test til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="7b229-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="7b229-107">Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="7b229-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="7b229-108">Måleværdier bruges til kvantitative test.</span><span class="sxs-lookup"><span data-stu-id="7b229-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="7b229-109">Til kvalitative test bruges testvariabler.</span><span class="sxs-lookup"><span data-stu-id="7b229-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="7b229-110">For kvantitativ test er feltet **Type** angivet til *Heltal* eller *Del*.</span><span class="sxs-lookup"><span data-stu-id="7b229-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="7b229-111">Der er også angivet en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="7b229-111">A unit of measure is also specified.</span></span> <span data-ttu-id="7b229-112">Kvalitetsspecifikationer og testresultater er udtrykt som tal.</span><span class="sxs-lookup"><span data-stu-id="7b229-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="7b229-113">For kvalitative test er feltet **Type** angivet til *Indstilling*.</span><span class="sxs-lookup"><span data-stu-id="7b229-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="7b229-114">Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger.</span><span class="sxs-lookup"><span data-stu-id="7b229-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="7b229-115">Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</span><span class="sxs-lookup"><span data-stu-id="7b229-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="7b229-116">Du kan også vælge at tildele et testinstrument til en test.</span><span class="sxs-lookup"><span data-stu-id="7b229-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="7b229-117">Testinstrumenter er dog ikke påkrævede for at oprette og bruge test sammen med kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="7b229-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="7b229-118">Du kan finde flere oplysninger under [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="7b229-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="7b229-119">Du kan også vælge at angive en enhed for en test for at angive den måleenhed, som testresultaterne skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="7b229-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="7b229-120">En test for temperatur kan f.eks. omfatte en enhed på grader Fahrenheit eller grader Celsius.</span><span class="sxs-lookup"><span data-stu-id="7b229-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="7b229-121">Eksempel på en test</span><span class="sxs-lookup"><span data-stu-id="7b229-121">Example of a test</span></span>

<span data-ttu-id="7b229-122">Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitativ test for skader på emballagen.</span><span class="sxs-lookup"><span data-stu-id="7b229-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="7b229-123">Virksomheden angiver yderligere oplysninger om den kvalitative test for at definere testvariablen (f.eks. beskadiget emballage) og udfaldet.</span><span class="sxs-lookup"><span data-stu-id="7b229-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="7b229-124">Firmaet bruger siden **Testgrupper** til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="7b229-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="7b229-125">Testgruppen tildeles en kvalitetsordre, så virksomheden kan rapportere testresultater for de to test.</span><span class="sxs-lookup"><span data-stu-id="7b229-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="7b229-126">Oprette en test</span><span class="sxs-lookup"><span data-stu-id="7b229-126">Create a test</span></span>

<span data-ttu-id="7b229-127">Benyt denne fremgangsmåde for at oprette en test.</span><span class="sxs-lookup"><span data-stu-id="7b229-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="7b229-128">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Test**.</span><span class="sxs-lookup"><span data-stu-id="7b229-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="7b229-129">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="7b229-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7b229-130">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="7b229-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7b229-131">**Test** – Angiv et entydigt id eller navn til testen.</span><span class="sxs-lookup"><span data-stu-id="7b229-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="7b229-132">**Beskrivelse** – Indtast en detaljeret beskrivelse af testen.</span><span class="sxs-lookup"><span data-stu-id="7b229-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="7b229-133">**Type** – Vælg den resultattype, som testen giver.</span><span class="sxs-lookup"><span data-stu-id="7b229-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="7b229-134">For kvantitative test skal du vælge *Del* eller *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="7b229-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="7b229-135">Vælg *Indstilling* for kvalitative test.</span><span class="sxs-lookup"><span data-stu-id="7b229-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="7b229-136">**Testinstrument** – Vælg et [testinstrument](quality-test-instruments.md), der skal bruges til testen.</span><span class="sxs-lookup"><span data-stu-id="7b229-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="7b229-137">**Enhed** – Hvis du har valgt *Del* eller *Heltal* i feltet **Type** (dvs. hvis testen er en kvantitativ test), skal du vælge den måleenhed, som testresultaterne skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="7b229-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="7b229-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7b229-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="7b229-139">Når du har gemt en test, kan du ikke længere redigere feltet **Type** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="7b229-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="7b229-140">Hvis du skal ændre typen af de testresultater, der registreres for en test, skal du vælge **Skift kvalitetstesttype** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7b229-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="7b229-141">I dialogboksen **Skift kvalitetstesttype** skal du angive feltet **Ny type** til den ønskede type og derefter vælge **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="7b229-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b229-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7b229-142">Additional resources</span></span>

- [<span data-ttu-id="7b229-143">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="7b229-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="7b229-144">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="7b229-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="7b229-145">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="7b229-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="7b229-146">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="7b229-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
