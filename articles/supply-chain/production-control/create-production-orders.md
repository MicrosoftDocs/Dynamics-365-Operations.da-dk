---
title: Oversigt over produktionsordres livscyklus
description: Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare. Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato. Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424773"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="d8cde-105">Oversigt over produktionsordres livscyklus</span><span class="sxs-lookup"><span data-stu-id="d8cde-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8cde-106">Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare.</span><span class="sxs-lookup"><span data-stu-id="d8cde-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="d8cde-107">Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato.</span><span class="sxs-lookup"><span data-stu-id="d8cde-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="d8cde-108">Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen.</span><span class="sxs-lookup"><span data-stu-id="d8cde-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="d8cde-109">En produktionsordre gennemgår trin i produktionslevetiden.</span><span class="sxs-lookup"><span data-stu-id="d8cde-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="d8cde-110">Når en ordre oprettes, får den statusangivelsen **Oprettet**.</span><span class="sxs-lookup"><span data-stu-id="d8cde-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="d8cde-111">Når en ordre er afsluttet, får den statusangivelsen **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="d8cde-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="d8cde-112">En parameterindstilling i hver fase gør det muligt for en bruger at konfigurere de enkelte trin.</span><span class="sxs-lookup"><span data-stu-id="d8cde-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="d8cde-113">Indstillingen kan konfigureres til en enkelt bruger eller til alle brugere.</span><span class="sxs-lookup"><span data-stu-id="d8cde-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="d8cde-114">Produktionsstyklisten og produktionsruten er de vigtigste enheder i produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="d8cde-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="d8cde-115">De kopieres til produktionsordren baseret på den valgte vare og mængde, der skal produceres.</span><span class="sxs-lookup"><span data-stu-id="d8cde-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="d8cde-116">Før produktionsordren startes, kan produktionsstyklisten og ruten redigeres.</span><span class="sxs-lookup"><span data-stu-id="d8cde-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="d8cde-117">En produktionsordre kan oprettes i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="d8cde-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="d8cde-118">Oprettes af varedisponeringsudførelse baseret på materialebehov.</span><span class="sxs-lookup"><span data-stu-id="d8cde-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="d8cde-119">Oprettes direkte fra en salgsordrelinje, eller når en produktionsordre på højere niveau oprettes og forkalkuleres (sporet forsyning).</span><span class="sxs-lookup"><span data-stu-id="d8cde-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="d8cde-120">Oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="d8cde-120">Created manually.</span></span>




