---
title: Produktionsordreforslag skal planlægges, før det kan autoriseres
description: Når du forsøger at autorisere et ordreforslag, får du vist en fejlmeddelelse om, at ordren skal planlægges, før den kan autoriseres.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294042"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="97263-103">Produktionsordreforslag skal planlægges, før det kan autoriseres</span><span class="sxs-lookup"><span data-stu-id="97263-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="97263-104">Fejlkode: SYS309802</span><span class="sxs-lookup"><span data-stu-id="97263-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="97263-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="97263-105">Symptoms</span></span>

<span data-ttu-id="97263-106">Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="97263-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="97263-107">Den planlagte produktionsordre skal planlægges, inden den kan autoriseres.</span><span class="sxs-lookup"><span data-stu-id="97263-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="97263-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="97263-108">Cause</span></span>

<span data-ttu-id="97263-109">De planlagte start- og slutdatoer må ikke være tomme.</span><span class="sxs-lookup"><span data-stu-id="97263-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="97263-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="97263-110">Resolution</span></span>

<span data-ttu-id="97263-111">Benyt følgende fremgangsmåde for at angive start- og slutdatoer for ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="97263-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="97263-112">Gå til **Varedisponering \> Varedisponering \> Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="97263-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="97263-113">Åbn det relevante ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="97263-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="97263-114">Angiv datoer i felterne **Startdato** og **Slutdato** i sektionen **Planlagt** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="97263-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
