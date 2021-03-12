---
title: Flytning af lager med tilknyttet arbejde i Lokationsstyring
description: I dette emne beskrives, hvordan du kan konfigurere og anvende bekræftelse af stykplukning fra en mobilenhed.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7d0cdace306e6f266dd690db2c9855ea75009e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970325"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="5be0c-103">Flytning af lager med tilknyttet arbejde i Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="5be0c-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5be0c-104">Ved hjælp af lagerbevægelse kan du bestemme, hvilke lagermedarbejdere der skal have tilladelse til at flytte reserveret lager.</span><span class="sxs-lookup"><span data-stu-id="5be0c-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="5be0c-105">Dette giver en fleksibilitet på regulerede lagersteder, hvor du kan vælge, at en arbejder ikke skal kunne vælge en ny pluklokation for plukarbejde, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="5be0c-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="5be0c-106">Det gør det også muligt for lagerstedets chef at styre, hvilke funktioner mindre erfarne arbejdere skal have adgang til.</span><span class="sxs-lookup"><span data-stu-id="5be0c-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="5be0c-107">Muligheden for fleksibel administration af lagermedarbejdernes daglige operationer kan være nyttig i situationer som disse:</span><span class="sxs-lookup"><span data-stu-id="5be0c-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="5be0c-108">Scenario 1</span><span class="sxs-lookup"><span data-stu-id="5be0c-108">Scenario 1</span></span>
<span data-ttu-id="5be0c-109">Et firma har et relativt lille modtagelsesområde, og det er overfyldt med paller og kasser, der venter på at blive lagt på lager.</span><span class="sxs-lookup"><span data-stu-id="5be0c-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="5be0c-110">Der ventes en stor forsendelse på den aktuelle dag, så medarbejderen i modtagelsen beslutter at rydde op i modtagelsesområdet ved at flytte nogle af pallerne til et sekundært, midlertidigt indgående område.</span><span class="sxs-lookup"><span data-stu-id="5be0c-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="5be0c-111">Scenario 2</span><span class="sxs-lookup"><span data-stu-id="5be0c-111">Scenario 2</span></span>
<span data-ttu-id="5be0c-112">En erfaren lagermedarbejderen ser en mulighed for på et lagersted at konsolidere varer på ét sted i stedet for at få dem spredt på 3 steder i nærheden med et lavt antal på hvert sted.</span><span class="sxs-lookup"><span data-stu-id="5be0c-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="5be0c-113">Arbejderen ønsker at konsolidere antallet ved at flytte varer fra hvert af disse steder til det samme sted og på det samme id.</span><span class="sxs-lookup"><span data-stu-id="5be0c-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="5be0c-114">Scenario 3</span><span class="sxs-lookup"><span data-stu-id="5be0c-114">Scenario 3</span></span>
<span data-ttu-id="5be0c-115">En palle afventer forsendelse på et midlertidig sted, f.eks. STAGE01, som er i nærheden af BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="5be0c-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="5be0c-116">På grund af en ændring af planerne ventes lastbilen imidlertid at ankomme til BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="5be0c-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="5be0c-117">Kontorassistenten er opmærksom på dette og skal sikre, at lastbilen ikke behøver at vente på at blive lastet fra STAGE01.</span><span class="sxs-lookup"><span data-stu-id="5be0c-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="5be0c-118">Kontorassistenten beslutter sig for at flytte varerne i forsendelsen fra STAGE01 til STAGE04, som er tættere på den nye destination.</span><span class="sxs-lookup"><span data-stu-id="5be0c-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="5be0c-119">Aktuelle begrænsninger</span><span class="sxs-lookup"><span data-stu-id="5be0c-119">Current limitations</span></span>

<span data-ttu-id="5be0c-120">De arbejdsreservationer, du kan flytte, er begrænset til salgsordre, flytteordreafgang, Flytteordretilgang, indkøbsordre og genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="5be0c-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="5be0c-121">Flytning af varer er begrænset for at forhindre opdeling af arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="5be0c-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="5be0c-122">Det betyder, at hvis du har en arbejdslinje for 100 stk. af vare A fra stedet Loc1, du ikke kan nøjes med at flytte 30 stk. af vare A derfra til et andet sted.</span><span class="sxs-lookup"><span data-stu-id="5be0c-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="5be0c-123">Det ville medføre en opdeling af den eksisterende arbejdslinje i 30 og 70, fordi stederne nu er forskellige.</span><span class="sxs-lookup"><span data-stu-id="5be0c-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="5be0c-124">For midlertidige scenarier, hvor det id, du flytter varerne fra, eller det id, du flytter varerne til, er konfigureret som en mål-LP for en arbejdsordre, er det kun tilladt at flytte hele LP'en for ikke at opdele mål-LP'en.</span><span class="sxs-lookup"><span data-stu-id="5be0c-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="5be0c-125">Kun ad hoc-flytningen understøttes i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="5be0c-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="5be0c-126">Det betyder, at du ikke kan flytte reserveret lager via den flytning, der udføres ved hjælp af menupunkter på mobilenheden i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="5be0c-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="5be0c-127">Konfigurere rettighed til at flytte reserveret lager for individuelle arbejdere</span><span class="sxs-lookup"><span data-stu-id="5be0c-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="5be0c-128">For den medarbejder, der skal have rettighed til at flytte reserveret lager, skal du markere afkrydsningsfeltet **Tillad flytning af lager med tilknyttet arbejde** under **Lokationsstyring** > **Opsætning** > **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="5be0c-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="5be0c-129">Overførsel</span><span class="sxs-lookup"><span data-stu-id="5be0c-129">Backported</span></span>

<span data-ttu-id="5be0c-130">Denne funktion er også blevet overført til Microsoft Dynamics AX 2012 R3 og kan bruges som en del af CU12.</span><span class="sxs-lookup"><span data-stu-id="5be0c-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="5be0c-131">Den kan også hentes særskilt via KB-nummer 3192548.</span><span class="sxs-lookup"><span data-stu-id="5be0c-131">It can also be downloaded individually through KB number 3192548.</span></span> 

