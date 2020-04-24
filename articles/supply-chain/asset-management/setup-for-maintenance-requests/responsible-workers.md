---
title: Ansvarlige vedligeholdelsesarbejdere
description: Dette emne beskriver, hvordan du konfigurerer ansvarlige vedligeholdelsesarbejdere i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208932"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="48d3b-103">Ansvarlige vedligeholdelsesarbejdere</span><span class="sxs-lookup"><span data-stu-id="48d3b-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="48d3b-104">Ansvarlige vedligeholdelsesarbejdere kan relateres til aktivtyper, aktiver, arbejdssteder, kategorier af vedligeholdelsesjobtyper, vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper og handler.</span><span class="sxs-lookup"><span data-stu-id="48d3b-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="48d3b-105">De kan bruges på arbejdsordrer og vedligeholdelsesanmodninger til at indikere en præference for de vedligeholdelsesarbejdere, der skal være ansvarlige for en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="48d3b-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="48d3b-106">(Disse vedligeholdelsesarbejdere er dog ikke nødvendigvis de samme arbejdere, der er planlagt til at skulle udføre arbejdsordren.) Du kan frit vælge, om du ønsker at bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="48d3b-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="48d3b-107">Den kan eksempelvis bruges til at vælge ansvarlige arbejdere eller arbejdergrupper til bestemte arbejdstyper eller arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="48d3b-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="48d3b-108">I løbet af en arbejdsordres livscyklus eller en vedligeholdelsesanmodnings livscyklus kan ansvarlige vedligeholdelsesarbejdere ændres eller opdateres.</span><span class="sxs-lookup"><span data-stu-id="48d3b-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="48d3b-109">Denne ændring eller opdatering kan være relateret til eksempelvis en ændring i tilstanden for vedligeholdelsesanmodnings livscyklus eller tilstanden for arbejdsordrens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="48d3b-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="48d3b-110">Opsætningen på siden **Ansvarlig vedligeholdelsesarbejder** bruges *ikke* under planlægningen af arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="48d3b-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="48d3b-111">I Styring af aktiver kan du også konfigurere *foretrukne* vedligeholdelsesarbejdere, der kan allokeres til arbejdsordrer i forbindelse med arbejdsordrens planlægning.</span><span class="sxs-lookup"><span data-stu-id="48d3b-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="48d3b-112">Før du kan konfigurere ansvarlige vedligeholdelsesarbejdere, skal du konfigurere de arbejdere og vedligeholdelsesarbejdergrupper, der skal være tilgængelige for udvælgelse.</span><span class="sxs-lookup"><span data-stu-id="48d3b-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="48d3b-113">Du finder oplysninger om, hvordan du konfigurerer arbejdere og vedligeholdelsesarbejdergrupper, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="48d3b-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="48d3b-114">Konfigurer ansvarlige vedligeholdelsesarbejdere</span><span class="sxs-lookup"><span data-stu-id="48d3b-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="48d3b-115">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Ansvarlige vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="48d3b-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="48d3b-116">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="48d3b-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="48d3b-117">Opret først en standard ansvarlig vedligeholdelsesarbejder eller konfigurer en ansvarlig vedligeholdelsesarbejdergruppe, hvor du kun konfigurer feltet **Ansvarlig vedligeholdelsesarbejdergruppe** og/eller feltet **Ansvarlig arbejder**.</span><span class="sxs-lookup"><span data-stu-id="48d3b-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="48d3b-118">Lad de resterende felter være tomme.</span><span class="sxs-lookup"><span data-stu-id="48d3b-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="48d3b-119">Denne standardopsætning bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="48d3b-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48d3b-120">Ved oprettelse af en vedligeholdelsesanmodning, når en ansvarlig vedligeholdelsesarbejder eller ansvarlig vedligeholdelsesarbejdergruppe stilles til rådighed for udvælgelse på siden **Alle vedligeholdelsesanmodninger**, gennemgår Styring af aktiver alle ansvarlige vedligeholdelsesarbejderposter for at kontrollere, om der er et mulig match.</span><span class="sxs-lookup"><span data-stu-id="48d3b-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="48d3b-121">Den kontrollerer altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="48d3b-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="48d3b-122">Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Handel**.</span><span class="sxs-lookup"><span data-stu-id="48d3b-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="48d3b-123">Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Vedligeholdelsesjobtypevariant**.</span><span class="sxs-lookup"><span data-stu-id="48d3b-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="48d3b-124">Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Vedligeholdelsesjobtype** osv.</span><span class="sxs-lookup"><span data-stu-id="48d3b-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="48d3b-125">Som du kan se på sidens layout, betyder denne adfærd, at Styring af aktiver kontrollerer hver post fra højre mod venstre for et match (i rækkefølgen **Handel**, **Vedligeholdelsesjobtypevariant**, **Vedligeholdelsejobtype**, **Vedligeholdelsejobtypekategori**, **Arbejdssteder**, **Aktiv** og til sidst **Aktivtype**) for at finde den mest specifikke kombination.</span><span class="sxs-lookup"><span data-stu-id="48d3b-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="48d3b-126">Hvis der ikke findes et match, bruges standardposten, som ikke har nogen markeringer i de syv felter.</span><span class="sxs-lookup"><span data-stu-id="48d3b-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="48d3b-127">I følgende illustration vises et eksempel på listesiden **Ansvarlige vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="48d3b-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Siden Ansvarlige vedligeholdelsesarbejdere](media/08-setup-for-requests.png)
