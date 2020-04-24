---
title: Beregne kapacitetsbelastning på planlagte arbejdsordrer
description: Dette emne forklarer, hvordan kapacitetsbelastningen beregnes for planlagte arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215349"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="772d4-103">Beregne kapacitetsbelastning på planlagte arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="772d4-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="772d4-104">Du kan beregne kapacitetsbelastningen for planlagte arbejdsordrer for at få overblik over arbejdsbelastningen for ressourcer i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="772d4-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="772d4-105">Der kan foretage beregninger for følgende ressourcer: vedligeholdelsesarbejdere, arbejdergrupper, værktøjer og aktiver.</span><span class="sxs-lookup"><span data-stu-id="772d4-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="772d4-106">Klik på **Styring af aktiver** > **Forespørgsler** > **Plan** > **Kapacitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="772d4-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="772d4-107">I dialogboksen **Beregn kapacitetsbelastning** > feltet **Vis** skal du vælge den belastningstype, du vil beregne: **Kapacitet**, **Reserveret** eller **Rest**.</span><span class="sxs-lookup"><span data-stu-id="772d4-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="772d4-108">Vælg **Ja** på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater, der indeholder nul.</span><span class="sxs-lookup"><span data-stu-id="772d4-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="772d4-109">Vælg de ressourcetyper, som du vil beregne kapacitetsbelastning for, ved at vælge **Ja** i de relevante til/fra-knapper: **Arbejder**, **Vedligeholdelsesarbejdergruppe**, **Værktøj** og **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="772d4-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="772d4-110">Vælg startdatoen for beregningen i feltet **Fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="772d4-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="772d4-111">I feltet **Intervaltype** skal du vælge intervallet for beregningen: **Dag**, **Uge**, **Måned** eller **Kvartal**.</span><span class="sxs-lookup"><span data-stu-id="772d4-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="772d4-112">Indsæt det antal intervaller, du vil beregne, i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="772d4-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="772d4-113">Hvis du f.eks. har valgt **Dag** som intervaltype, og du indsætter tallet "5" i dette felt, foretages der en beregning på fem dage fra startdatoen.</span><span class="sxs-lookup"><span data-stu-id="772d4-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="772d4-114">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="772d4-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="772d4-115">I figuren herunder vises resultatet af en beregning, der dækker tre uger for belastningstypen **Reserveret**.</span><span class="sxs-lookup"><span data-stu-id="772d4-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Figur 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="772d4-117">Hvis du vælger belastningstyperne **Kapacitet** eller **Rest** for beregningen, vises samme resultat, hvis der ikke er foretaget reservationer for ressourcerne i den valgte periode.</span><span class="sxs-lookup"><span data-stu-id="772d4-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="772d4-118">Se [Beregne kapacitetsbelastning](../capacity-planning/calculate-capacity-load.md) for at få oplysninger om, hvordan kapacitetsbelastningen beregnes på vedligeholdelsestidsplanslinjer og ikke planlagte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="772d4-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

