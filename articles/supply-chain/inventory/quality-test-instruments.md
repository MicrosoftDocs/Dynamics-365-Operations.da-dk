---
title: Testinstrumenter for kvalitetsstyring
description: I dette emne beskrives, hvordan du opretter testinstrumenter, som kan bruges til test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021726"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="ac357-103">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ac357-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac357-104">I dette emne beskrives, hvordan du opretter testinstrumenter, som kan bruges til test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ac357-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ac357-105">Du kan bruge siden **Testinstrumenter** til at definere og få vist detaljer om de enheder, der bruges til at udføre test for kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="ac357-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="ac357-106">Testinstrumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ac357-106">Test instruments are optional.</span></span> <span data-ttu-id="ac357-107">De kan dog hjælpe kvalitetsmedarbejdere med at finde ud af, hvilken enhed eller hvilket værktøj de skal bruge til at udføre en bestemt test.</span><span class="sxs-lookup"><span data-stu-id="ac357-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="ac357-108">Eksempel på testinstrument</span><span class="sxs-lookup"><span data-stu-id="ac357-108">Test instrument example</span></span>

<span data-ttu-id="ac357-109">Du udfører forskellige test af elektroniske komponenter.</span><span class="sxs-lookup"><span data-stu-id="ac357-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="ac357-110">Nogle test angår strømspændingen for komponenter, én test angår deres temperatur, og én test angår deres vægt.</span><span class="sxs-lookup"><span data-stu-id="ac357-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="ac357-111">Der bruges forskellige værktøjer, enheder eller udstyr til at udføre hver test.</span><span class="sxs-lookup"><span data-stu-id="ac357-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="ac357-112">En strømspændingsmåler kan f.eks. bruges til at måle spændingen, et termometer kan bruges til at måle temperaturen, og en vægt kan bruges til at måle vægt.</span><span class="sxs-lookup"><span data-stu-id="ac357-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="ac357-113">Du kan konfigurere hver af disse enheder som et testinstrument og angive den måleenhed, som testresultaterne skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="ac357-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="ac357-114">Resultaterne fra strømspændingsmåleren registreres f.eks. i volt, resultaterne fra termometeret registreres i grader såsom Fahrenheit eller Celsius, og resultaterne fra vægten registreres i pund eller kilo.</span><span class="sxs-lookup"><span data-stu-id="ac357-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="ac357-115">Oprette et testinstrument</span><span class="sxs-lookup"><span data-stu-id="ac357-115">Create a test instrument</span></span>

1. <span data-ttu-id="ac357-116">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testinstrumenter**.</span><span class="sxs-lookup"><span data-stu-id="ac357-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="ac357-117">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="ac357-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac357-118">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="ac357-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ac357-119">**Testinstrument** – Angiv et entydigt id eller navn til testinstrumentet.</span><span class="sxs-lookup"><span data-stu-id="ac357-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="ac357-120">**Beskrivelse** – Indtast en detaljeret beskrivelse af testinstrumentet.</span><span class="sxs-lookup"><span data-stu-id="ac357-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="ac357-121">**Enhed** – Vælg den enhed, som instrumentet måler resultater i.</span><span class="sxs-lookup"><span data-stu-id="ac357-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="ac357-122">Feltet **Præcision** angives automatisk ud fra den enhed, du vælger.</span><span class="sxs-lookup"><span data-stu-id="ac357-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="ac357-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ac357-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac357-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ac357-124">Additional resources</span></span>

- [<span data-ttu-id="ac357-125">Test for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ac357-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="ac357-126">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ac357-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
