---
title: Bruge stadieårsagskoder
description: Ved at bruge en årsagskode kan du angive, hvorfor en serviceniveauaftale er annulleret, eller hvorfor en serviceniveauaftale har overskredet den tidsgrænse, der er angivet i serviceniveauaftalen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557750"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="74dad-103">Bruge stadieårsagskoder</span><span class="sxs-lookup"><span data-stu-id="74dad-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="74dad-104">Ved at bruge en årsagskode kan du angive, hvorfor en serviceniveauaftale er annulleret, eller hvorfor en serviceniveauaftale har overskredet den tidsgrænse, der er angivet i serviceniveauaftalen.</span><span class="sxs-lookup"><span data-stu-id="74dad-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="74dad-105">Du kan også angive, at en årsagskode er påkrævet, når en serviceniveauaftale annulleres, eller når tidsgrænsen overskrider den tid, der er angivet i serviceniveauaftalen for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="74dad-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="74dad-106">Hvis du har angivet, at der kræves en årsagskode, skal du angive en årsagskode i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="74dad-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="74dad-107">Når en serviceordre overgår til et stadie, hvor tidsregistreringen i forhold til serviceniveauaftalen stoppes for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="74dad-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="74dad-108">Når serviceordren lukkes.</span><span class="sxs-lookup"><span data-stu-id="74dad-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="74dad-109">Når tidsregistreringen stoppes manuelt.</span><span class="sxs-lookup"><span data-stu-id="74dad-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="74dad-110">Definer årsagskoder</span><span class="sxs-lookup"><span data-stu-id="74dad-110">Set up reason codes</span></span>

1.  <span data-ttu-id="74dad-111">Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Stadieårsagskoder**.</span><span class="sxs-lookup"><span data-stu-id="74dad-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="74dad-112">Klik på **Ny** i formularen **Stadieårsagskoder** for at oprette en ny årsagskode.</span><span class="sxs-lookup"><span data-stu-id="74dad-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="74dad-113">Indtast en entydig stadieårsagskode i feltet **Stadieårsagskode**.</span><span class="sxs-lookup"><span data-stu-id="74dad-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="74dad-114">Indtast en beskrivelse af stadieårsagskoden i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="74dad-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="74dad-115">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="74dad-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="74dad-116">Kræve årsagskoder, når en serviceniveauaftale annulleres</span><span class="sxs-lookup"><span data-stu-id="74dad-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="74dad-117">Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.</span><span class="sxs-lookup"><span data-stu-id="74dad-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="74dad-118">I formularen **Parametre for servicestyring** skal du klikke på linket **Generelt** og derefter markere afkrydsningsfeltet **Årsagskode ved annullering**.</span><span class="sxs-lookup"><span data-stu-id="74dad-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="74dad-119">Kræve årsagskoder, når en serviceordre overskrider den tidsgrænse, der er fastsat i serviceniveauaftalen</span><span class="sxs-lookup"><span data-stu-id="74dad-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="74dad-120">Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.</span><span class="sxs-lookup"><span data-stu-id="74dad-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="74dad-121">I formularen **Parametre for servicestyring** skal du klikke på linket **Generelt** og derefter markere afkrydsningsfeltet **Årsagskode ved overskridelse af tid**.</span><span class="sxs-lookup"><span data-stu-id="74dad-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="74dad-122">Se også</span><span class="sxs-lookup"><span data-stu-id="74dad-122">See also</span></span>

[<span data-ttu-id="74dad-123">Starte og stoppe tidsregistrering på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="74dad-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


