---
title: Føje fejl til arbejdsordre
description: Dette emne indeholder en beskrivelse af, hvordan du kan føje fejlregistreringer til arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215188"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="37462-103">Tilføje fejl til arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="37462-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="37462-104">Du kan føje fejl, der er defineret i fejldesigneren, til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="37462-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="37462-105">En eller flere fejlposter skal være tilknyttet de aktivtyper, der bruges for det aktiv, som er valgt i arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="37462-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="37462-106">Yderligere oplysninger om den opsætningen finder du i [Fejlhåndtering](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="37462-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="37462-107">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="37462-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="37462-108">Vælg den arbejdsordre, der skal foretages en fejlregistrering for, og vælg fanen **Arbejdsordre** i handlingsruden, og vælg **Aktivfejl** i gruppen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="37462-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="37462-109">Vælg **Tilføj linje** i oversigtspanelet **Symptomer**.</span><span class="sxs-lookup"><span data-stu-id="37462-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="37462-110">Et fejlserienummer indsættes automatisk i feltet **Fejl**.</span><span class="sxs-lookup"><span data-stu-id="37462-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="37462-111">Vælg det relevante symptom i feltet **Fejlsymptom**.</span><span class="sxs-lookup"><span data-stu-id="37462-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="37462-112">Vælg de relevante værdier i felterne **Fejlområde** og **Fejltype**.</span><span class="sxs-lookup"><span data-stu-id="37462-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="37462-113">Feltet **Fejldato** indeholder automatisk dags dato.</span><span class="sxs-lookup"><span data-stu-id="37462-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="37462-114">Vælg en anden dato efter behov.</span><span class="sxs-lookup"><span data-stu-id="37462-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="37462-115">I oversigtspanelet **Årsager til valgt symptom** kan du tilføje en linje, der beskriver årsagen til problemet.</span><span class="sxs-lookup"><span data-stu-id="37462-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="37462-116">I oversigtspanelet **Løsninger til valgt symptom** kan du tilføje en linje, der beskriver en mulig løsning på problemet.</span><span class="sxs-lookup"><span data-stu-id="37462-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="37462-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="37462-117">Select **Save**.</span></span>

<span data-ttu-id="37462-118">Følgende illustration viser et eksempel på en fejlregistrering.</span><span class="sxs-lookup"><span data-stu-id="37462-118">The illustration below shows an example of a fault registration.</span></span>

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="37462-120">Se aktivfejl</span><span class="sxs-lookup"><span data-stu-id="37462-120">View asset faults</span></span>

<span data-ttu-id="37462-121">På listen **Aktivfejl** kan du få en oversigt over alle fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="37462-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="37462-122">På listesiden **Aktivfejl** kan du se en oversigt over alle fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="37462-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="37462-123">Vælg **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl** for at åbne siden.</span><span class="sxs-lookup"><span data-stu-id="37462-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="37462-124">Udskrive aktivfejlrapport</span><span class="sxs-lookup"><span data-stu-id="37462-124">Print asset fault report</span></span>

<span data-ttu-id="37462-125">På listesiden **Alle aktiver** kan du udskrive en fejlrapport for aktiver, der viser alle fejlregistreringer og en grafisk oversigt over fejlstatistik.</span><span class="sxs-lookup"><span data-stu-id="37462-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="37462-126">Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="37462-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="37462-127">Vælg det aktiv, fejlrapporten skal udskrives for.</span><span class="sxs-lookup"><span data-stu-id="37462-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="37462-128">I handlingsruden under fanen **Generelt** i gruppen **Rapporter** skal du vælge **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="37462-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="37462-129">Indsæt en bestemt periode, eller vælg en fejltype.</span><span class="sxs-lookup"><span data-stu-id="37462-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="37462-130">Vælg **OK** for at udskrive rapporten.</span><span class="sxs-lookup"><span data-stu-id="37462-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="37462-131">Du kan udskrive en fejlrapport for flere aktiver eller aktivtyper ved at vælge **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="37462-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

