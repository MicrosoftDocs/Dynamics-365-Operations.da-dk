---
title: Konfigurere arbejdsgange for linjeelementer
description: Dette emne forklarer, hvordan du konfigurerer et element i en arbejdsgang for linjeelement.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84da7080542b4cc2ecc487b0a1331482fb69b998
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747899"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="b0821-103">Konfigurere arbejdsgange for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="b0821-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0821-104">Dette emne forklarer, hvordan du konfigurerer et element i en arbejdsgang for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="b0821-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="b0821-105">Hvis du vil konfigurere et element i en arbejdsgang for linjeelementer i arbejdsgangseditoren, skal du højreklikke på elementet og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="b0821-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="b0821-106">Brug derefter nedenstående procedure til at konfigurere egenskaberne for et element i en arbejdsgang for linjeelementer.</span><span class="sxs-lookup"><span data-stu-id="b0821-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="b0821-107">Navngive et element i en arbejdsgang for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="b0821-107">Name the line-item workflow element</span></span>

<span data-ttu-id="b0821-108">Udfør følgende trin for at angive et navn på et element i en arbejdsgang for linjeelementer.</span><span class="sxs-lookup"><span data-stu-id="b0821-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="b0821-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="b0821-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b0821-110">Angiv et entydigt navn på elementet i en arbejdsgang for linjeelementer i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b0821-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="b0821-111">Angive, om samme arbejdsgang bruges til at behandle alle linjeelementer</span><span class="sxs-lookup"><span data-stu-id="b0821-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="b0821-112">Udfør følgende trin for at angive, om samme arbejdsgang bruges til at behandle alle linjeelementer i et dokument.</span><span class="sxs-lookup"><span data-stu-id="b0821-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="b0821-113">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="b0821-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b0821-114">Hvis samme arbejdsgang skal behandle alle linjeelementerne i et dokument, skal du klikke på **Aktivér én arbejdsgang for alle linjeelementer**.</span><span class="sxs-lookup"><span data-stu-id="b0821-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="b0821-115">Vælg derefter den arbejdsgang, der skal bruges til behandling af linjeelementerne.</span><span class="sxs-lookup"><span data-stu-id="b0821-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="b0821-116">Hvis en bestemt arbejdsgang skal behandle de linjeelementer, der opfylder et bestemt sæt betingelser, skal du klikke på **Aktivér en arbejdsgang for hvert linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="b0821-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="b0821-117">Udfør derefter følgende trin for at definere et sæt betingelser:</span><span class="sxs-lookup"><span data-stu-id="b0821-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="b0821-118">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="b0821-118">Click **Add**.</span></span>
    2. <span data-ttu-id="b0821-119">Vælg betingelsen i tabellen.</span><span class="sxs-lookup"><span data-stu-id="b0821-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="b0821-120">Angiv et navn på det sæt betingelser, du definerer, under fanen **Betingelsesnavn**.</span><span class="sxs-lookup"><span data-stu-id="b0821-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="b0821-121">Klik på **Tilføj betingelse** for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="b0821-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="b0821-122">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="b0821-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="b0821-123">Hvis du vil kontrollere, om det sæt betingelser, du har angivet, er konfigureret korrekt, skal du klikke på **Test**.</span><span class="sxs-lookup"><span data-stu-id="b0821-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="b0821-124">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse** skal du vælge en post og derefter klikke på **Test**.</span><span class="sxs-lookup"><span data-stu-id="b0821-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="b0821-125">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="b0821-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="b0821-126">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="b0821-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="b0821-127">Under fanen **Arbejdsgang** skal du vælge den arbejdsgang, der skal bruges til at behandle de linjeelementer, der opfylder et sæt betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="b0821-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]