---
title: Føje fejl til arbejdsordre
description: Dette emne indeholder en beskrivelse af, hvordan du kan føje fejlregistreringer til arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875572"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="1b177-103">Føje fejl til arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="1b177-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="1b177-104">Du kan føje fejl, der er defineret i fejldesigneren, til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="1b177-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="1b177-105">Det valgte aktiv i arbejdsordren skal indeholde aktivtyper, der har en eller flere fejlposter tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="1b177-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="1b177-106">Læs mere om opsætning i afsnittet [Fejlstyring](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="1b177-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="1b177-107">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1b177-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1b177-108">Vælg den arbejdsordre, du vil foretage en fejlregistrering for, på listen, og klik på **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="1b177-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="1b177-109">Klik på **Tilføj linje** i oversigtspanelet **Symptomer**.</span><span class="sxs-lookup"><span data-stu-id="1b177-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="1b177-110">Et fejlserienummer indsættes automatisk i feltet **Fejl**.</span><span class="sxs-lookup"><span data-stu-id="1b177-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="1b177-111">Vælg det relevante symptom i feltet **Fejlsymptom**.</span><span class="sxs-lookup"><span data-stu-id="1b177-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="1b177-112">Vælg **Fejlområde** og **Fejltype**.</span><span class="sxs-lookup"><span data-stu-id="1b177-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="1b177-113">Feltet **Fejldato** indeholder automatisk dags dato.</span><span class="sxs-lookup"><span data-stu-id="1b177-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="1b177-114">Hvis det er nødvendigt, kan du vælge en anden dato.</span><span class="sxs-lookup"><span data-stu-id="1b177-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="1b177-115">I oversigtspanelet **Årsager til valgt symptom** kan du tilføje en linje, der beskriver årsagen til problemet.</span><span class="sxs-lookup"><span data-stu-id="1b177-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="1b177-116">I oversigtspanelet **Løsninger til valgt symptom** kan du tilføje en linje, der beskriver en mulig løsning på problemet.</span><span class="sxs-lookup"><span data-stu-id="1b177-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="1b177-117">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1b177-117">Click **Save**.</span></span>

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="1b177-119">Se aktivfejl</span><span class="sxs-lookup"><span data-stu-id="1b177-119">View asset faults</span></span>

<span data-ttu-id="1b177-120">På listen **Aktivfejl** kan du få en oversigt over alle fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="1b177-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="1b177-121">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl** for at åbne listen.</span><span class="sxs-lookup"><span data-stu-id="1b177-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="1b177-122">Udskrive aktivfejlrapport</span><span class="sxs-lookup"><span data-stu-id="1b177-122">Print asset fault report</span></span>

<span data-ttu-id="1b177-123">På listesiden **Alle aktiver** kan du udskrive en fejlrapport for aktiver, der viser alle fejlregistreringer og en grafisk oversigt over fejlstatistik.</span><span class="sxs-lookup"><span data-stu-id="1b177-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="1b177-124">Klik på **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="1b177-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="1b177-125">På listen **Aktiver** skal du vælge det aktiv, du vil udskrive en fejlrapport for.</span><span class="sxs-lookup"><span data-stu-id="1b177-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="1b177-126">Klik på **Aktivfejl** i sektionen **Rapporter** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1b177-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="1b177-127">Indsæt en bestemt periode, eller vælg en fejltype.</span><span class="sxs-lookup"><span data-stu-id="1b177-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="1b177-128">Klik på **OK** for at udskrive rapporten.</span><span class="sxs-lookup"><span data-stu-id="1b177-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="1b177-129">Du kan også udskrive en fejlrapport for flere aktiver eller aktivtyper ved at klikke på **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="1b177-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

