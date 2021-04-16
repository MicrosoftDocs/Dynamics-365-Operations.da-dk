---
title: Reparationsstyring
description: Du kan gruppere problemer systematisk, så det bliver muligt at foreslå løsninger, der tidligere har vist sig at fungere.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d0c6ee65713af86378ada79075f969a41f1c0ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836008"
---
# <a name="repair-management"></a><span data-ttu-id="ca446-103">Reparationsstyring</span><span class="sxs-lookup"><span data-stu-id="ca446-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ca446-104">I forbindelse med reparationsstyring kan du gruppere problemer systematisk.</span><span class="sxs-lookup"><span data-stu-id="ca446-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="ca446-105">På denne måde er det nemmere at foreslå løsninger, der tidligere har vist sig at fungere.</span><span class="sxs-lookup"><span data-stu-id="ca446-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="ca446-106">Du kan angive indstillinger for symptomer, diagnoser og løsninger.</span><span class="sxs-lookup"><span data-stu-id="ca446-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="ca446-107">Du kan så bruge disse senere, når du modtager en lignende vare til reparation.</span><span class="sxs-lookup"><span data-stu-id="ca446-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="ca446-108">Du kan også oprette reparationsstadier, der følger hvad der sker med en bestemt reparation.</span><span class="sxs-lookup"><span data-stu-id="ca446-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="ca446-109">Konfigurere reparationsstyring</span><span class="sxs-lookup"><span data-stu-id="ca446-109">Setting up repair management</span></span>

<span data-ttu-id="ca446-110">Brug følgende forms til at angive oplysninger, der skal bruges til at angive symptomer, diagnose og løsning i forbindelse med en reparation.</span><span class="sxs-lookup"><span data-stu-id="ca446-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="ca446-111">**Servicestyring** \> **Opsætning** \> **Reparation** \> **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="ca446-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="ca446-112">**Servicestyring** \> **Opsætning** \> **Reparation** \> **Symptomområder**.</span><span class="sxs-lookup"><span data-stu-id="ca446-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="ca446-113">**Servicestyring** \> **Opsætning** \> **Reparation** \> **Diagnoseområder**.</span><span class="sxs-lookup"><span data-stu-id="ca446-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="ca446-114">**Servicestyring** \> **Opsætning** \> **Reparation** \> **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="ca446-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="ca446-115">**Servicestyring** \> **Opsætning** \> **Reparation** \> **Reparationsstadier**.</span><span class="sxs-lookup"><span data-stu-id="ca446-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="ca446-116">Symptomer og betingelser</span><span class="sxs-lookup"><span data-stu-id="ca446-116">Symptoms and conditions</span></span>

<span data-ttu-id="ca446-117">Symptomer er den måde, som kunden beskriver problemet.</span><span class="sxs-lookup"><span data-stu-id="ca446-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="ca446-118">Symptomer omfatter kundens observationer, der henleder til behovet for reparation.</span><span class="sxs-lookup"><span data-stu-id="ca446-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="ca446-119">Du kan bruge symptomområder, -koder og -betingelser.</span><span class="sxs-lookup"><span data-stu-id="ca446-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="ca446-120">Symptomområdet er området for funktionsfejl, og symptomkoden dækker fejlsymptomet.</span><span class="sxs-lookup"><span data-stu-id="ca446-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="ca446-121">Betingelsen beskriver den situation, hvori problemet udløses.</span><span class="sxs-lookup"><span data-stu-id="ca446-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="ca446-122">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="ca446-122">**Example**</span></span>

<span data-ttu-id="ca446-123">En computer sendes til reparation, fordi der opstår fejl på harddisken efter længere tids brug.</span><span class="sxs-lookup"><span data-stu-id="ca446-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="ca446-124">Harddiskfejlen forårsager blå skærm.</span><span class="sxs-lookup"><span data-stu-id="ca446-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="ca446-125">Den tekniker, der modtager computeren, angiver følgende symptomer og betingelser:</span><span class="sxs-lookup"><span data-stu-id="ca446-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="ca446-126">Symptomområdet er harddisken.</span><span class="sxs-lookup"><span data-stu-id="ca446-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="ca446-127">Symptomkoden er fejlen med blå skærm.</span><span class="sxs-lookup"><span data-stu-id="ca446-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="ca446-128">Betingelsen er, at der opstår fejl på harddisken efter længere tids brug.</span><span class="sxs-lookup"><span data-stu-id="ca446-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="ca446-129">Diagnose og løsninger</span><span class="sxs-lookup"><span data-stu-id="ca446-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="ca446-130">Felterne til diagnose og løsning afspejler reparationen.</span><span class="sxs-lookup"><span data-stu-id="ca446-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="ca446-131">Det er det, en tekniker har gjort for at finde årsagen til problemet.</span><span class="sxs-lookup"><span data-stu-id="ca446-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="ca446-132">Diagnoseområdet omfatter, det der skal udføres for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="ca446-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="ca446-133">Diagnosekoden er, hvordan problemet er blevet håndteret, og løsningskoden kan være, at varen er repareret, udskiftet, eller at kunden har annulleret ordren.</span><span class="sxs-lookup"><span data-stu-id="ca446-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="ca446-134">Hvis computeren f.eks. er blevet repareret, kan diagnoseområdet værd 'defekt del', diagnosekoden kan være 'nyt skærmkort installeret', og løsningskoden kan være 'udskiftet'.</span><span class="sxs-lookup"><span data-stu-id="ca446-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="ca446-135">Reparationsstadier</span><span class="sxs-lookup"><span data-stu-id="ca446-135">Repair stages</span></span>

<span data-ttu-id="ca446-136">Reparationsstadier angiver, hvordan reparationsprocessen skrider frem.</span><span class="sxs-lookup"><span data-stu-id="ca446-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="ca446-137">Reparationsstadiet har en afmeldingsparameter, **Fuldført**, der viser, at en reparationslinje er fuldført, og at der er registreret en dato og et tidspunkt for færdiggørelsen.</span><span class="sxs-lookup"><span data-stu-id="ca446-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="ca446-138">Anvende reparationsstyring</span><span class="sxs-lookup"><span data-stu-id="ca446-138">Applying repair management</span></span>

<span data-ttu-id="ca446-139">Hvis du vil anvende reparationsstyring på en vare, skal varen være oprettet med en serviceobjektrelation på en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="ca446-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="ca446-140">Fra serviceordren kan du derefter oprette en reparationslinje med oplysninger om det aktuelle problem.</span><span class="sxs-lookup"><span data-stu-id="ca446-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="ca446-141">På reparationslinjen angiver du det serviceobjekt, der skal repareres, sammen med oplysninger om symptomer, diagnose og udførelse.</span><span class="sxs-lookup"><span data-stu-id="ca446-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="ca446-142">Du kan også oprette en bemærkning til reparationslinjen.</span><span class="sxs-lookup"><span data-stu-id="ca446-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="ca446-143">Du kan oprette reparationslinjer for hvert trin i reparationsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ca446-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="ca446-144">Oprette en reparationslinje på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="ca446-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="ca446-145">Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="ca446-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ca446-146">Vælg serviceordren med det serviceobjekt, der skal repareres.</span><span class="sxs-lookup"><span data-stu-id="ca446-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="ca446-147">Vælg **Reparation** \> **Reparationslinjer** for at åbne formularen **Reparationslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ca446-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="ca446-148">Vælg **Ny** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="ca446-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="ca446-149">Vælg et serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="ca446-149">Select a service object.</span></span> <span data-ttu-id="ca446-150">Du kan vælge et hvilket som helst serviceobjekt, der er oprettet med en objektrelation på serviceordren.</span><span class="sxs-lookup"><span data-stu-id="ca446-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="ca446-151">Vælg en eller flere af de foruddefinerede værdier for symptomer, diagnoser og udførelser, der er relevante på reparationslinjen, og vælg om nødvendigt fanen **Bemærkning** for at oprette en bemærkning på reparationslinjen.</span><span class="sxs-lookup"><span data-stu-id="ca446-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="ca446-152">Vælg **Gem** for at gemme den nye reparationslinje.</span><span class="sxs-lookup"><span data-stu-id="ca446-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="ca446-153">Feltet **Dato og klokkeslæt for oprettelse** under fanen **Generelt** i formularen **Reparationslinjer** opdateres med tidspunktet for lagring.</span><span class="sxs-lookup"><span data-stu-id="ca446-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="ca446-154">Spore og afslutte et reparationsforløb</span><span class="sxs-lookup"><span data-stu-id="ca446-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="ca446-155">Du kan angive reparationsstadierne til en reparationslinje, så du kan spore reparationsforløbet.</span><span class="sxs-lookup"><span data-stu-id="ca446-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="ca446-156">Når et reparationsproblem er blevet løst, kan du lukke reparationslinjen.</span><span class="sxs-lookup"><span data-stu-id="ca446-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="ca446-157">Indstil reparationsstatus med egenskaben **Fuldført** aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ca446-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="ca446-158">Dato og klokkeslæt registreres som afslutningstidspunkt på linjen.</span><span class="sxs-lookup"><span data-stu-id="ca446-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="ca446-159">Afslutte en reparationslinje, når et problem er løst</span><span class="sxs-lookup"><span data-stu-id="ca446-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="ca446-160">Åbn formularen **Reparationslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ca446-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="ca446-161">Følg fremgangsmåden tidligere i dette emne for at oprette en reparationslinje.</span><span class="sxs-lookup"><span data-stu-id="ca446-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="ca446-162">Vælg reparationslinjen med det reparationsproblem, du vil afslutte.</span><span class="sxs-lookup"><span data-stu-id="ca446-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="ca446-163">I feltet **Reparationsstadie** skal du vælge et stadie, hvor egenskaben **Fuldført** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ca446-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]