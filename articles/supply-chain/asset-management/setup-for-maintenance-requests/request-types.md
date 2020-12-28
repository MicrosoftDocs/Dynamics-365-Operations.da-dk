---
title: Typer af vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer typer af vedligeholdelsesanmodninger i Styring af aktiver.
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
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424740"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="8b27d-103">Typer af vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="8b27d-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8b27d-104">Vedligeholdelsesanmodningstyper bruges til at kategorisere vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="8b27d-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="8b27d-105">Du kan for eksempel have vedligeholdelsesanmodningstyper, der er relateret til forebyggende vedligeholdelse og korrigerende vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="8b27d-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="8b27d-106">Eller du kan have en særlig vedligeholdelsesanmodningstype, der bruges til at administrere reparationer af aktiver (depotreparation).</span><span class="sxs-lookup"><span data-stu-id="8b27d-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="8b27d-107">En vedligeholdelsesanmodningstype definerer tilknytningen til en vedligeholdelsesanmodnings livscyklustilstandsgruppe (vedligeholdelseslivscyklusmodel).</span><span class="sxs-lookup"><span data-stu-id="8b27d-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="8b27d-108">Livscyklusmodeller for vedligeholdelsesanmodninger definerer de livscyklustilstande, der kan angives for en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="8b27d-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="8b27d-109">(Eksempler på livscyklustilstande for vedligeholdelsesanmodninger omfatter **Oprettet**, **Aktive** og **Afsluttede**.)</span><span class="sxs-lookup"><span data-stu-id="8b27d-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="8b27d-110">Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Vedligeholdelsesanmodningstyper**.</span><span class="sxs-lookup"><span data-stu-id="8b27d-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="8b27d-111">Vælg **Ny** for at oprette en vedligeholdelsesanmodningstype.</span><span class="sxs-lookup"><span data-stu-id="8b27d-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="8b27d-112">I feltet **Vedligeholdelsesanmodningstype** skal du angive et ID for vedligeholdelsesanmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="8b27d-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="8b27d-113">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8b27d-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="8b27d-114">I oversigtspanelet **Generelt** skal du i feltet **Vedligeholdelsesanmodningens livscyklusmodel** vælge en livscyklusmodel for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="8b27d-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="8b27d-115">I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="8b27d-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="8b27d-116">Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, får arbejdsordren automatisk den arbejdsordretype, der er relateret til vedligeholdelsesanmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="8b27d-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="8b27d-117">I følgende illustration vises et eksempel på listesiden **Vedligeholdelsesanmodningstype**.</span><span class="sxs-lookup"><span data-stu-id="8b27d-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Siden Vedligeholdelsesanmodningstyper](media/07-setup-for-requests.png)
