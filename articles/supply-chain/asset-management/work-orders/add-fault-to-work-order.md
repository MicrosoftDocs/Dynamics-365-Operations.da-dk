---
title: Føje fejl til arbejdsordre
description: Dette emne indeholder en beskrivelse af, hvordan du kan føje fejlregistreringer til arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a79986e3b477865bc1816a1d28c1b7094ae3974
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809800"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="e30e0-103">Tilføje fejl til arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="e30e0-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e30e0-104">Du kan føje fejl, der er defineret i fejldesigneren, til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="e30e0-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="e30e0-105">En eller flere fejlposter skal være tilknyttet de aktivtyper, der bruges for det aktiv, som er valgt i arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="e30e0-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="e30e0-106">Yderligere oplysninger om den opsætningen finder du i [Fejlhåndtering](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="e30e0-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="e30e0-107">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e30e0-108">Vælg den arbejdsordre, der skal foretages en fejlregistrering for, og vælg fanen **Arbejdsordre** i handlingsruden, og vælg **Aktivfejl** i gruppen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="e30e0-109">Vælg **Tilføj linje** i oversigtspanelet **Symptomer**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="e30e0-110">Et fejlserienummer indsættes automatisk i feltet **Fejl**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="e30e0-111">Vælg det relevante symptom i feltet **Fejlsymptom**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="e30e0-112">Vælg de relevante værdier i felterne **Fejlområde** og **Fejltype**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="e30e0-113">Feltet **Fejldato** indeholder automatisk dags dato.</span><span class="sxs-lookup"><span data-stu-id="e30e0-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="e30e0-114">Vælg en anden dato efter behov.</span><span class="sxs-lookup"><span data-stu-id="e30e0-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="e30e0-115">I oversigtspanelet **Årsager til valgt symptom** kan du tilføje en linje, der beskriver årsagen til problemet.</span><span class="sxs-lookup"><span data-stu-id="e30e0-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="e30e0-116">I oversigtspanelet **Løsninger til valgt symptom** kan du tilføje en linje, der beskriver en mulig løsning på problemet.</span><span class="sxs-lookup"><span data-stu-id="e30e0-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="e30e0-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-117">Select **Save**.</span></span>

<span data-ttu-id="e30e0-118">Følgende illustration viser et eksempel på en fejlregistrering.</span><span class="sxs-lookup"><span data-stu-id="e30e0-118">The illustration below shows an example of a fault registration.</span></span>

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="e30e0-120">Se aktivfejl</span><span class="sxs-lookup"><span data-stu-id="e30e0-120">View asset faults</span></span>

<span data-ttu-id="e30e0-121">På listen **Aktivfejl** kan du få en oversigt over alle fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="e30e0-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="e30e0-122">På listesiden **Aktivfejl** kan du se en oversigt over alle fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="e30e0-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="e30e0-123">Vælg **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl** for at åbne siden.</span><span class="sxs-lookup"><span data-stu-id="e30e0-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="e30e0-124">Udskrive aktivfejlrapport</span><span class="sxs-lookup"><span data-stu-id="e30e0-124">Print asset fault report</span></span>

<span data-ttu-id="e30e0-125">På listesiden **Alle aktiver** kan du udskrive en fejlrapport for aktiver, der viser alle fejlregistreringer og en grafisk oversigt over fejlstatistik.</span><span class="sxs-lookup"><span data-stu-id="e30e0-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="e30e0-126">Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e30e0-127">Vælg det aktiv, fejlrapporten skal udskrives for.</span><span class="sxs-lookup"><span data-stu-id="e30e0-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="e30e0-128">I handlingsruden under fanen **Generelt** i gruppen **Rapporter** skal du vælge **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="e30e0-129">Indsæt en bestemt periode, eller vælg en fejltype.</span><span class="sxs-lookup"><span data-stu-id="e30e0-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="e30e0-130">Vælg **OK** for at udskrive rapporten.</span><span class="sxs-lookup"><span data-stu-id="e30e0-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="e30e0-131">Du kan udskrive en fejlrapport for flere aktiver eller aktivtyper ved at vælge **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="e30e0-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]