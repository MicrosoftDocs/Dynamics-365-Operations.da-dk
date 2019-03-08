---
title: Føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør
description: I dette emne forklares, hvordan du kan føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør, så de kan bruges til rapporter for finans- og budgetposteringer.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a15414eff99751d4e77e5b3bf315a556efb7ad5d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "332673"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="8bd40-103">Føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør</span><span class="sxs-lookup"><span data-stu-id="8bd40-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bd40-104">I dette emne forklares, hvordan du kan føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør (CFO), så de kan bruges til rapporter for finans- og budgetposteringer.</span><span class="sxs-lookup"><span data-stu-id="8bd40-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="8bd40-105">Regnskabsdirektørens arbejdsområde har fanerne **Oversigt** og **Finans**. Rapporterne under disse to faner understøttes af to målpunkter: LedgerActivityMeasure og BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="8bd40-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="8bd40-106">I Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), er der en relation mellem disse to målepunkter og DimensionCombinationEntity-enheden.</span><span class="sxs-lookup"><span data-stu-id="8bd40-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="8bd40-107">Derfor kan du vælge dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8bd40-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="8bd40-108">I Finance and Operations skal du på siden **Enhedslager** opdatere målpunkterne **LedgerActivityMeasure** og **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="8bd40-109">Åbn Application Explorer i Microsoft Visual Studio, og søg efter **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="8bd40-110">Under **Resources** (Ressourcer) skal du åbne **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="8bd40-111">Når ressourcen åbnes i Microsoft Power BI Desktop, skal du vælge **Get Data** (Hent Data). Vælg **SQL Server-database**, og vælg derefter **Connect** (Forbind).</span><span class="sxs-lookup"><span data-stu-id="8bd40-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="8bd40-112">Angiv en navnet på serveren og **AxDW** som database.</span><span class="sxs-lookup"><span data-stu-id="8bd40-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="8bd40-113">Vælg **DirectQuery**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="8bd40-114">Søg efter og vælg **LedgerActivityMeasure\_DimensionCombination**, og vælg derefter **Indlæs**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="8bd40-115">I listen **Fields** (Felter) skal du omdøbe tabellen **Økonomiske dimensioner**, så den er nem at identificere.</span><span class="sxs-lookup"><span data-stu-id="8bd40-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="8bd40-116">Vælg **Administrer relationer**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="8bd40-117">Vælg i det første felt **Finansaktiviteter**, og vælg derefter **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="8bd40-118">I det andet felt skal du vælge **LedgerActivityMeasure\_DimensionCombination** (eller **Financial dimensions** (Økonomiske dimensioner), hvis du omdøbte tabellen).</span><span class="sxs-lookup"><span data-stu-id="8bd40-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="8bd40-119">Vælg hovedet **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="8bd40-120">I feltet **Cardinality** (Kardinalitet) skal du vælge **Many to One** (Mange til en).</span><span class="sxs-lookup"><span data-stu-id="8bd40-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="8bd40-121">Vælg værdien **Single** (Enkelt) for **Cross filter direction** (Tværgående filterretning).</span><span class="sxs-lookup"><span data-stu-id="8bd40-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="8bd40-122">Vælg både **Aktivér denne relation** og **Antag referentiel integritet**, vælg **OK**, og vælg derefter **Luk**.</span><span class="sxs-lookup"><span data-stu-id="8bd40-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="8bd40-123">[![Oprette en relation](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="8bd40-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="8bd40-124">I listen **Fields** (Felter) skal du nu kunne se tabellen og de tilgængelige økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8bd40-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="8bd40-125">Træk de økonomiske dimensioner, du ønsker, til rapportniveaufilterne.</span><span class="sxs-lookup"><span data-stu-id="8bd40-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="8bd40-126">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="8bd40-126">Save your changes.</span></span>
15. <span data-ttu-id="8bd40-127">I applikationsobjekttræet (AOT) skal du højreklikke på projektet og derefter vælge **Synchronize** (Synkroniser).</span><span class="sxs-lookup"><span data-stu-id="8bd40-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="8bd40-128">Opbyg projektet, og åbn derefter programmet for at se resultaterne.</span><span class="sxs-lookup"><span data-stu-id="8bd40-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="8bd40-129">[![Fuldført arbejdsområde](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="8bd40-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
