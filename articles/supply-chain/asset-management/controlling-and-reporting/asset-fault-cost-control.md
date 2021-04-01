---
title: Omkostningsstyring for aktivfejl
description: I dette emne beskrives omkostningsstyring af aktivfejl i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253824"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="19b14-103">Omkostningsstyring for aktivfejl</span><span class="sxs-lookup"><span data-stu-id="19b14-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="19b14-104">I Styring af aktiver kan du beregne omkostninger for registreringer af aktivfejl for at få vist en oversigt over faktiske omkostninger sammenlignet med budgetomkostninger.</span><span class="sxs-lookup"><span data-stu-id="19b14-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="19b14-105">De faktiske omkostninger er baseret på bogførte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="19b14-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="19b14-106">Datoen er den fejldato, hvor symptomet blev registreret.</span><span class="sxs-lookup"><span data-stu-id="19b14-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="19b14-107">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Omkostningsstyring af aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="19b14-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="19b14-108">Vælg en økonomisk dimension, der skal inkluderes i beregningen, hvis det er nødvendigt, i dialogboksen **Omkostningsstyring for aktiver**.</span><span class="sxs-lookup"><span data-stu-id="19b14-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="19b14-109">Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater med en omkostning på nul.</span><span class="sxs-lookup"><span data-stu-id="19b14-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="19b14-110">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede omkostningsstyringslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="19b14-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="19b14-111">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktivfejls omkostningsstyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="19b14-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="19b14-112">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle aktivfejls omkostningsstyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="19b14-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="19b14-113">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver, fejldatoer og fejlårsager i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="19b14-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="19b14-114">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="19b14-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="19b14-115">Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="19b14-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="19b14-116">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="19b14-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="19b14-117">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="19b14-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="19b14-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="19b14-118">Example</span></span>

<span data-ttu-id="19b14-119">I dette eksempel vises beregning af omkostningskontrol for aktivfejl.</span><span class="sxs-lookup"><span data-stu-id="19b14-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="19b14-120">I feltet **Oprindeligt budget** vises budgetomkostninger fra arbejdsordrebudgettet.</span><span class="sxs-lookup"><span data-stu-id="19b14-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="19b14-121">I feltet **Faktiske omkostninger** vises bogførte omkostninger på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="19b14-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="19b14-122">I feltet **Bindende omkostning** vises de samlede omkostninger, som dit firma er bundet til i forbindelse med arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="19b14-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Figur 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="19b14-124">Se emnet [Fejlstyring](../setup-for-work-orders/fault-management.md), hvis du vil have oplysninger om, hvordan du definerer fejl.</span><span class="sxs-lookup"><span data-stu-id="19b14-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]