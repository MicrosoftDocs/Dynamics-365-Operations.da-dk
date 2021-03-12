---
title: Godkend ordreforslag
description: I dette emne beskrives godkendelse af ordreforslag, der understøttes i planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983563"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="dfd0c-103">Godkend ordreforslag</span><span class="sxs-lookup"><span data-stu-id="dfd0c-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfd0c-104">Dette emne beskriver, hvordan status for ordreforslag opdateres i planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="dfd0c-105">Bemærk, at godkendelse af ordreforslag er et valgfrit trin, når du skal oprette en autoriseret ordre fra et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="dfd0c-106">Det anbefales at godkende ændrede ordreforslag, for ellers ignoreres ændringerne, som overskrives af næste planlægningskørsel.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Ordreforslagsflow](media/approved-planned-orders-1.png)

<span data-ttu-id="dfd0c-108">Feltet **Status** hjælper dig med at spore status ved hjælp af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dfd0c-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="dfd0c-109">**Ubehandlet:** Når varedisponering opretter ordreforslag, har ordreforslagene statussen *Ubehandlet*.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="dfd0c-110">Ordreforslag med denne status vil blive slettet under næste planlægningskørsel.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="dfd0c-111">**Fuldført:** Hvis du ikke vil autorisere et ordreforslag, kan du ændre status til *Fuldført* for at angive, at du har afsluttet evalueringen af ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="dfd0c-112">Bemærk, at status som *Ubehandlet* og *Fuldført* håndteres på samme måde af systemet.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="dfd0c-113">**Godkendt:** Hvis du vil beholde redigeringer eller planlægger at autorisere et ordreforslag, skal du ændre status til *Godkendt*.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="dfd0c-114">Ordreforslag med statussen *Godkendt* regnes for fastlagte og forventede forsyninger i varedisponeringen, så de ikke ændres eller slettes, når varedisponeringen køres.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="dfd0c-115">For at opnå dette kopierer planlægningslogikken de *Godkendte* planlagte ordre fra den gamle planversion til den nye planversion under varedisponering.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="dfd0c-116">Bemærk, at *Godkendte* ordreforslag kun betragtes som forsyning inden for den specifikke behovsplan.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="dfd0c-117">Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**.</span><span class="sxs-lookup"><span data-stu-id="dfd0c-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
