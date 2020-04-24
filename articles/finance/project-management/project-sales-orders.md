---
title: Projektsalgsordre for tids- og materialeprojekter
description: Dette emne beskriver, hvordan du opretter projektbaserede salgsordre for tids- og materialeprojekter.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249087"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="7f2b8-103">Projektsalgsordre for tids- og materialeprojekter</span><span class="sxs-lookup"><span data-stu-id="7f2b8-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f2b8-104">Dette emne beskriver, hvordan du opretter en ny salgsordre for et projekt.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="7f2b8-105">Salgsordre kan alene oprettes for projekter af typen **tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="7f2b8-106">Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du slå parametret **Tillad salgsordre for projekter med flere finansieringskilder** til på siden **Projektstyring og regnskabsparametre**.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="7f2b8-107">Understøttelse til projektsalgsordre med flere finansieringskilder bliver tilgængelig i forbindelse med programfrigivelse 10.0.2 og senere versioner.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="7f2b8-108">Parametret for at aktivere understøttelse af projektsalgsordre med flere finansieringskilder bliver fjernet i forbindelse med frigivelsesbølgen i april 2020, hvorefter funktionen altid vil være slået til.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="7f2b8-109">Du kan oprette projektbaserede salgsordre på to måder:</span><span class="sxs-lookup"><span data-stu-id="7f2b8-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="7f2b8-110">Gå til selve projektet.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-110">Go to the project itself.</span></span> <span data-ttu-id="7f2b8-111">I handlingsruden skal du på vælge **Administrer > Opgaveelementer > Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="7f2b8-112">Projektoplysningerne er angivet i henhold til standarderne for projektets salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="7f2b8-113">Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge finansieringskilden for at konfigurere kunden til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="7f2b8-114">Hvis projektet alene har én finansieringskilde, bliver kunden automatisk konfigureret.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="7f2b8-115">Gå til listesiden **Alle salgsordrer**, og opret en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="7f2b8-116">Du skal vælge projektet for slagsordren.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="7f2b8-117">Når du har valgt projektet, bliver kunden konfigureret på grundlag af finansieringskilden, ellers, hvis projektkontrakten har flere finansieringskilder, skal du vælge finansieringskilden.</span><span class="sxs-lookup"><span data-stu-id="7f2b8-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

