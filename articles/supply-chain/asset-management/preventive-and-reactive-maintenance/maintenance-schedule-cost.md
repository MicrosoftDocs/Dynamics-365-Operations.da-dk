---
title: Omkostning til vedligeholdelsestidsplan
description: I dette emne beskrives omkostning til vedligeholdelsestidsplaner i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91c5b2e70ee083bf2741e245f1ca840ab939ad3f
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3382969"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="f5320-103">Omkostning til vedligeholdelsestidsplan</span><span class="sxs-lookup"><span data-stu-id="f5320-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f5320-104">I Styring af aktiver kan du beregne budgetomkostninger på vedligeholdelsestidsplanslinjer.</span><span class="sxs-lookup"><span data-stu-id="f5320-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="f5320-105">Dette er nyttigt, hvis du vil have en oversigt over forventede omkostninger, f.eks. omkostninger i forbindelse med planlagte forebyggende vedligeholdelsesjob for det næste år.</span><span class="sxs-lookup"><span data-stu-id="f5320-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="f5320-106">Beregningerne er baseret på eksisterende vedligeholdelsestidsplanslinjer af typen "Vedligeholdelsesplaner", "Vedligeholdelsesrunder" og "Vedligeholdelsesanmodninger".</span><span class="sxs-lookup"><span data-stu-id="f5320-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="f5320-107">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Omkostning til vedligeholdelsestidsplan**.</span><span class="sxs-lookup"><span data-stu-id="f5320-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="f5320-108">I dialogboksen **Omkostning til vedligeholdelsestidsplan** kan du vælge en **Økonomisk dimensionsopsætning**, hvis du vil have vist omkostninger, der er grupperet i økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f5320-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="f5320-109">Økonomiske dimensionsopsætninger oprettes i **Finans** > **Kontoplan** > **Dimensioner** > **Økonomiske dimensionsopsætninger**.</span><span class="sxs-lookup"><span data-stu-id="f5320-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="f5320-110">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede vedligeholdelsestidsplanslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="f5320-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="f5320-111">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="f5320-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="f5320-112">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="f5320-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="f5320-113">Hvis du vil foretage en beregning for bestemte aktiver, skal du klikke på **Filter** i oversigtspanelet **Poster, der skal indgå** og vælge de relevante aktiver.</span><span class="sxs-lookup"><span data-stu-id="f5320-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="f5320-114">Hvis det er nødvendigt, kan du også angive en **Forventet startdato** for omkostningsberegningen eller vælge en anden **Status** for omkostningsberegningen</span><span class="sxs-lookup"><span data-stu-id="f5320-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="f5320-115">Klik på **OK** for at starte omkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="f5320-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="f5320-116">Under fanen **Omkostning til vedligeholdelsestidsplan** i **Gruppér efter...**-handlingsrudegrupper skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i omkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="f5320-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="f5320-117">De valgte gruppeknapper i handlingsruden er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="f5320-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="f5320-118">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="f5320-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="f5320-119">Klik på knappen **Beregn omkostninger**, hvis du vil foretage en ny omkostningsberegning.</span><span class="sxs-lookup"><span data-stu-id="f5320-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="f5320-120">I illustrationen herunder vises resultaterne af en omkostningsberegning for en vedligeholdelsestidsplan.</span><span class="sxs-lookup"><span data-stu-id="f5320-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Figur 1](media/17-preventive-maintenance.png)

