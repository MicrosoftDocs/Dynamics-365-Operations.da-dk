---
title: Omkostningsarter, der bruges i Produktionsstyring og Projektstyring og regnskab
description: "Nogle typer produktionsarbejde kan gælde for projekttidsestimater og rapportering. Denne artikel indeholder oplysninger om de omkostningsarter, du skal definere for disse typer produktionsarbejde til produktions- og projektformål."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cab4629740e92f9075b7afc7a5d228b2e01c4664
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="af5c2-104">Omkostningsarter, der bruges i Produktionsstyring og Projektstyring og regnskab</span><span class="sxs-lookup"><span data-stu-id="af5c2-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af5c2-105">Nogle typer produktionsarbejde kan gælde for projekttidsestimater og rapportering.</span><span class="sxs-lookup"><span data-stu-id="af5c2-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="af5c2-106">Denne artikel indeholder oplysninger om de omkostningsarter, du skal definere for disse typer produktionsarbejde til produktions- og projektformål.</span><span class="sxs-lookup"><span data-stu-id="af5c2-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="af5c2-107">Nogle typer produktionsarbejde kan gælde for projekttidsestimater og rapportering.</span><span class="sxs-lookup"><span data-stu-id="af5c2-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="af5c2-108">Hvis det er tilfældet, en der også angives en omkostningsart til produktions- og projektformål.</span><span class="sxs-lookup"><span data-stu-id="af5c2-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="af5c2-109">Når en omkostningsart bruges i produktion og projekter, skal der defineres yderligere projektrelaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="af5c2-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="af5c2-110">Timeomkostninger, der er tilknyttet projekter, kan f.eks. være forskellige fra timeomkostninger, der er tilknyttet produktion.</span><span class="sxs-lookup"><span data-stu-id="af5c2-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="af5c2-111">Du kan bruge siden **Omkostningsarter** til at definere en omkostningsart, der bruges i Produktionsstyring og Projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="af5c2-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="af5c2-112">**Bemærk!** Omkostningsregnskab har siden **Projektart**, men denne side har ingen relation til de funktioner, der beskrives i dette emne.</span><span class="sxs-lookup"><span data-stu-id="af5c2-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="af5c2-113">Når du bruger en omkostningsart i projekter, har siden **Omkostningsart** flere faner, der viser yderligere projektrelaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="af5c2-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="af5c2-114">Disse oplysninger omfatter artsgruppen, en linjeegenskab og finanskonti, der er knyttet til omkostningsarten.</span><span class="sxs-lookup"><span data-stu-id="af5c2-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="af5c2-115">Omkostningsarten skal knyttes til en kategorigruppe, der understøtter posteringstypen **Timer**.</span><span class="sxs-lookup"><span data-stu-id="af5c2-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="af5c2-116">Linjeegenskaben angiver standardoplysninger for, hvordan rapporteret tid kan faktureres i et projekt.</span><span class="sxs-lookup"><span data-stu-id="af5c2-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="af5c2-117">De finanskonti, der vedrører omkostninger og salg, defineres normalt for den kategorigruppe, der er knyttet til omkostningsarten.</span><span class="sxs-lookup"><span data-stu-id="af5c2-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="af5c2-118">Der kan dog angives bestemte konti for en individuel omkostningsart.</span><span class="sxs-lookup"><span data-stu-id="af5c2-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="af5c2-119">De ekstra knapper på siden **Omkostningsart** giver adgang til projektrelaterede oplysninger om en markeret omkostningsart.</span><span class="sxs-lookup"><span data-stu-id="af5c2-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="af5c2-120">Du kan f.eks. få vist projektrelaterede posteringer, definere medarbejdere eller projekter, definere timemæssige omkostninger og salgspriser samt få vist rapporter.</span><span class="sxs-lookup"><span data-stu-id="af5c2-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




