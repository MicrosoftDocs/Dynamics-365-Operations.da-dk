---
title: Metode for halvårligt afskrivningsprincip
description: I dette emne beskrives den metode, som anlægsaktiver bruger til at beregne afskrivning ved hjælp af halvårsprincippet, der beregner seks måneders afskrivning i et aktivs første og sidste år i brug.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 578f812a0426566c6bc2b943a6b2b7b6c01b94de
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761437"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="2a988-103">Metode for halvårligt afskrivningsprincip</span><span class="sxs-lookup"><span data-stu-id="2a988-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2a988-104">I dette emne beskrives den metode, der bruges i anlægsaktiver til at beregne afskrivninger ved hjælp af halvårsprincippet.</span><span class="sxs-lookup"><span data-stu-id="2a988-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="2a988-105">Det halvårlige princip beregner seks afskrivningsmåneder under et anlægs første og sidste år i brug.</span><span class="sxs-lookup"><span data-stu-id="2a988-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="2a988-106">Du kan finde flere oplysninger om afskrivningsprincipper under [Afskrivningsmetoder og -principper](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="2a988-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="2a988-107">Når du bruger afskrivningsprincippet på seks måneder, bruger systemet anskaffelsesåret eller det år, hvor anlægsaktivet blev taget i brug, og beregner derefter fem års afskrivning fra det pågældende år og tilføjer derefter seks måneder.</span><span class="sxs-lookup"><span data-stu-id="2a988-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="2a988-108">For at illustrere denne proces skal du forestille dig et aktiv, der er anskaffet til en pris af 50.000 og taget i brug i april 2020.</span><span class="sxs-lookup"><span data-stu-id="2a988-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="2a988-109">Det antages også, at aktivet har en levetid på fem år.</span><span class="sxs-lookup"><span data-stu-id="2a988-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="2a988-110">Det første år, det er i brug, afsluttes i december 2020, hvilket betyder, at anlægsaktivets fem års levetid vil ophøre i december 2024.</span><span class="sxs-lookup"><span data-stu-id="2a988-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="2a988-111">I det halvårlige afskrivningsprincip lægges der seks måneder til aktivets levetid, hvilket betyder, at levetiden slutter i juni 2025.</span><span class="sxs-lookup"><span data-stu-id="2a988-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="2a988-112">Årlig afskrivning 50.000/5 = 10.000 månedlig afskrivning 10.000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="2a988-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="2a988-113">Første års afskrivning 10.000/2 = 5.000 og den efterfølgende månedlige afskrivning 5.000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="2a988-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="2a988-114">[![Afskrivningsplan for halvårligt afskrivningsprincip](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="2a988-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="2a988-115">De udvidede afskrivningsperioder, der tilføjes af halvårsprincippet, giver en mere præcis afskrivningsfordeling.</span><span class="sxs-lookup"><span data-stu-id="2a988-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="2a988-116">Seks måneders princippet fordeler afskrivningsudgifter mere ligeligt, hvilket er nyttigt ved rapportering til driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="2a988-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
