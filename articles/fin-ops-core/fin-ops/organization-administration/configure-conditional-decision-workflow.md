---
title: Konfigurere betingede beslutninger i en arbejdsgang
description: Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a953d4e781db42834f0bc8daf80040c39ea5b5c
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698114"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="1856e-103">Konfigurere betingede beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1856e-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1856e-104">Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning.</span><span class="sxs-lookup"><span data-stu-id="1856e-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="1856e-105">En betinget beslutning er et punkt, hvor en arbejdsgang opdeles i to forgreninger.</span><span class="sxs-lookup"><span data-stu-id="1856e-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="1856e-106">Hvis du vil konfigurere en betinget beslutning i arbejdsgangseditoren, skal du højreklikke på den betingede beslutning og derefter klikke på **Egenskaber** for at åbne formen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="1856e-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="1856e-107">Navngive en beslutning</span><span class="sxs-lookup"><span data-stu-id="1856e-107">Name a decision</span></span>

<span data-ttu-id="1856e-108">Benyt denne fremgangsmåde til at angive et navn på den betingede beslutning.</span><span class="sxs-lookup"><span data-stu-id="1856e-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="1856e-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1856e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1856e-110">Angiv et entydigt navn på den betingede beslutning i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1856e-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="1856e-111">Angive betingelser</span><span class="sxs-lookup"><span data-stu-id="1856e-111">Set conditions</span></span>

<span data-ttu-id="1856e-112">Systemet bestemmer, hvilken forgrening der skal bruges, ved at evaluere det sendte dokument for at afgøre, om det opfylder bestemte betingelser.</span><span class="sxs-lookup"><span data-stu-id="1856e-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="1856e-113">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1856e-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1856e-114">Klik på **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="1856e-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="1856e-115">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="1856e-115">Enter a condition.</span></span>
4. <span data-ttu-id="1856e-116">Angiv supplerende betingelser, hvis det er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="1856e-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="1856e-117">Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="1856e-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="1856e-118">Klik på **Test** for at åbne formen **Test betingelse for arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="1856e-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="1856e-119">Vælg en post i området **Valider betingelse** i formen.</span><span class="sxs-lookup"><span data-stu-id="1856e-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="1856e-120">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="1856e-120">Click **Test**.</span></span> <span data-ttu-id="1856e-121">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="1856e-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="1856e-122">Klik på **OK** eller **Annuller** for at vende tilbage til formen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="1856e-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
