---
title: Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger
description: Dette emne forklarer, hvordan du opretter en arbejdsordre ud fra en vedligeholdelsesanmodning i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c42f259a57675c3dbac829d6d671e91982ef9011
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571685"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="13ad7-103">Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="13ad7-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="13ad7-104">Når du har oprettet vedligeholdelsesanmodninger, kan du nemt konvertere dem til arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="13ad7-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="13ad7-105">I dette emne beskrives den hurtigste metode til at arbejde med vedligeholdelsesanmodninger på, opdatere flere vedligeholdelsesanmodninger på samme tid og derefter oprette en arbejdsordre for flere vedligeholdelsesanmodninger på samme tid.</span><span class="sxs-lookup"><span data-stu-id="13ad7-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="13ad7-106">På siden **Aktive vedligeholdelsesanmodninger** og **Vedligeholdelsesanmodninger for mine arbejdssteder** kan du også arbejde med én vedligeholdelsesanmodning ad gangen og konvertere én vedligeholdelsesanmodning til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="13ad7-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="13ad7-107">Enhver vedligeholdelsesanmodning kan kun relateres til én arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="13ad7-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="13ad7-108">Flere vedligeholdelsesanmodninger kan dog inkluderes i én arbejdsordre, selvom vedligeholdelsesanmodningerne har forskellige aktiver.</span><span class="sxs-lookup"><span data-stu-id="13ad7-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="13ad7-109">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="13ad7-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="13ad7-110">Før du kan oprette en arbejdsordre ud fra vedligeholdelsesanmodninger, skal du som minimum vælge en vedligeholdelsesjobtype for vedligeholdelsesanmodningerne og også en variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante.</span><span class="sxs-lookup"><span data-stu-id="13ad7-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="13ad7-111">I gittervisningen kan du nemt opdatere oplysninger for en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="13ad7-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="13ad7-112">Når du er klar til at oprette en arbejdsordre, skal du vælge de vedligeholdelsesanmodninger, der skal medtages i den.</span><span class="sxs-lookup"><span data-stu-id="13ad7-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="13ad7-113">Hvis du vælger flere vedligeholdelsesanmodninger, der skal konverteres til en arbejdsordre, skal både feltet **Aktiv** og feltet **Vedligeholdelsesjobtype** angives, før du opretter arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="13ad7-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="13ad7-114">Hvis du vælger én vedligeholdelsesanmodning, der skal konverteres til en arbejdsordre, er det kun feltet **Aktiv**, der skal angives, før du opretter arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="13ad7-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="13ad7-115">Men når du opretter arbejdsordren, kan du vælge en vedligeholdelsesjobtype (og en relateret variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante) i dialogboksen **Opret arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="13ad7-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="13ad7-116">Vælg **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="13ad7-116">Select **Work order**.</span></span>
5. <span data-ttu-id="13ad7-117">Angiv felterne i dialogboksen **Opret arbejdsordre**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="13ad7-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="13ad7-118">En meddelelseslinje kan give dig besked om, at der er oprettet en ny arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="13ad7-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="13ad7-119">Når du opretter en arbejdsordre, der er baseret på en vedligeholdelsesanmodning, og det aktiv, der er relateret til vedligeholdelsesanmodningen, er inkluderet i en garantiaftale, giver en meddelelseslinje dig desuden besked om garantiaftalen.</span><span class="sxs-lookup"><span data-stu-id="13ad7-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="13ad7-120">Vælg **Styring af aktiver** \> **Almindeligt** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, og åbn derefter den nye arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="13ad7-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Åbne ny arbejdsordre](media/05-manage-maintenance-requests.png)

