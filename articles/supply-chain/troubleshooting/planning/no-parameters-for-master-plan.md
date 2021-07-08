---
title: Der findes ikke parametre for behovsplanen
description: Når du forsøger at autorisere et ordreforslag, modtager du en fejlmeddelelse om, at der ikke findes parametre for behovsplanen.
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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294040"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="a1681-103">Der findes ikke parametre for behovsplanen</span><span class="sxs-lookup"><span data-stu-id="a1681-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="a1681-104">Fejlkode: SYS25368</span><span class="sxs-lookup"><span data-stu-id="a1681-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1681-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a1681-105">Symptoms</span></span>

<span data-ttu-id="a1681-106">Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="a1681-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="a1681-107">Parametre for behovsplan %1 findes ikke.</span><span class="sxs-lookup"><span data-stu-id="a1681-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="a1681-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="a1681-108">Cause</span></span>

<span data-ttu-id="a1681-109">På grund af konfigurationsproblemer kan systemet ikke finde indstillingerne for den angivne plan.</span><span class="sxs-lookup"><span data-stu-id="a1681-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1681-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="a1681-110">Resolution</span></span>

- <span data-ttu-id="a1681-111">Gå til **Varedisponering \> Konfiguration \> Planer \> Behovsplaner**, og kontrollér, at der findes en plan med det angivne navn.</span><span class="sxs-lookup"><span data-stu-id="a1681-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
