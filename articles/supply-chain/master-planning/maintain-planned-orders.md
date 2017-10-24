---
title: Vedligehold ordreforslag
description: Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ec45e7426f65827f161245870f9114e52e035ab
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="a3963-104">Vedligehold ordreforslag</span><span class="sxs-lookup"><span data-stu-id="a3963-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a3963-105">Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="a3963-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="a3963-106">Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="a3963-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="a3963-107">Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**.</span><span class="sxs-lookup"><span data-stu-id="a3963-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="a3963-108">Du kan bruge feltet **Status** til at registrere status.</span><span class="sxs-lookup"><span data-stu-id="a3963-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="a3963-109">Følgende værdier bruges:</span><span class="sxs-lookup"><span data-stu-id="a3963-109">The following values are used:</span></span>

-   <span data-ttu-id="a3963-110">Når varedisponering opretter ordreforslag, har ordreforslagene statussen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="a3963-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="a3963-111">Hvis du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="a3963-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="a3963-112">Når du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Godkendt**.</span><span class="sxs-lookup"><span data-stu-id="a3963-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="a3963-113">Denne status angiver, at du godkender autorisation af ordreforslaget, men det er ikke autoriseret endnu.</span><span class="sxs-lookup"><span data-stu-id="a3963-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="a3963-114">**Bemærk!** Et godkendt ordreforslag overføres i den aktuelle tilstand til næste beregning af varedisponering.</span><span class="sxs-lookup"><span data-stu-id="a3963-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="a3963-115">Du kan autorisere ordreforslag ved at klikke på **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="a3963-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="a3963-116">Du kan autorisere følgende ordreforslag:</span><span class="sxs-lookup"><span data-stu-id="a3963-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="a3963-117">Det ordreforslag, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="a3963-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="a3963-118">Flere ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="a3963-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="a3963-119">Ordreforslag oprettes via en udfoldning fra siden **Udfoldning**.</span><span class="sxs-lookup"><span data-stu-id="a3963-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="a3963-120">Klik på **Ordreforslag**, vælg ordreforslaget, og klik derefter på **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="a3963-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="a3963-121">Når et ordreforslag er autoriseret, flyttes det til ordresektionen i det relevante modul.</span><span class="sxs-lookup"><span data-stu-id="a3963-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="a3963-122">**Bemærk!** Du kan højreklikke på et ordreforslag, der har en bestemt status, og filtrere efter andre ordreforslag med samme status.</span><span class="sxs-lookup"><span data-stu-id="a3963-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="a3963-123">Denne funktionalitet kan f.eks. være nyttig, hvis du vil filtrere efter alle ordreforslag, der har statussen **Godkendt**, så du kan autorisere dem.</span><span class="sxs-lookup"><span data-stu-id="a3963-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="a3963-124">Se også</span><span class="sxs-lookup"><span data-stu-id="a3963-124">See also</span></span>
--------

[<span data-ttu-id="a3963-125">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="a3963-125">Master plans</span></span>](master-plans.md)




