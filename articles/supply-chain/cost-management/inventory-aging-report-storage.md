---
title: Rapporten Aldersfordelt lager
description: I dette emne beskrives de funktioner, der giver mulighed for at køre en aldersfordelt lagerrapport, og gøre outputtet tilgængeligt som en formel og et diagram.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810245"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="401bc-103">Rapporten Aldersfordelt lager</span><span class="sxs-lookup"><span data-stu-id="401bc-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="401bc-104">I Microsoft Dynamics 365 Supply Chain Management kan du køre en rapport over **Lagerets aldersfordeling** og gøre outputtet tilgængeligt som en formular og et diagram.</span><span class="sxs-lookup"><span data-stu-id="401bc-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="401bc-105">I formularen reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det konfigurerede layout.</span><span class="sxs-lookup"><span data-stu-id="401bc-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="401bc-106">Diagrammet indeholder en visuel oversigt, der understøtter filtrering og giver dig mulighed for at gå i detaljer.</span><span class="sxs-lookup"><span data-stu-id="401bc-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="401bc-107">Derudover giver en dataenhed ved navn **Aldersfordelt lagerrapport** dig mulighed for at eksportere resultaterne af en rapport over **Lagerets aldersfordeling** til et format som f.eks en Microsoft Excel-fil eller en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="401bc-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="401bc-108">Denne metode til kørsel af rapport over **Lagerets aldersfordeling** er nyttig i de tilfælde, hvor outputtet indeholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="401bc-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="401bc-109">Outputtet indeholder f.eks. mange linjer, hvis du har 50.000 varer og 300 butikker, der oprettes som lagersteder, og du anmoder om lagerets aldersfordeling pr. vare, lokation og lagersted.</span><span class="sxs-lookup"><span data-stu-id="401bc-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="401bc-110">Kør en Aldersfordelt lagerrapport</span><span class="sxs-lookup"><span data-stu-id="401bc-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="401bc-111">Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lager for aldersfordelte lagerrapporter**.</span><span class="sxs-lookup"><span data-stu-id="401bc-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="401bc-112">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="401bc-112">Select **New**.</span></span>
1. <span data-ttu-id="401bc-113">kriv et entydigt navn for rapporten i feltet **Procesidentifikator – Navn**.</span><span class="sxs-lookup"><span data-stu-id="401bc-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="401bc-114">Vælg rapporten **Identifikation – Id**, og filtrer den efter behov.</span><span class="sxs-lookup"><span data-stu-id="401bc-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="401bc-115">Rapportafviklingen udføres altid i et batchjob.</span><span class="sxs-lookup"><span data-stu-id="401bc-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="401bc-116">Når batchjobbet er fuldført, vises outputtet på siden **Lager for aldersfordelt lagerrapport**.</span><span class="sxs-lookup"><span data-stu-id="401bc-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="401bc-117">Hvis du vil have vist outputtet som en formular med et traditionelt gitterlayout, skal du vælge **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="401bc-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="401bc-118">Hvis du vil have vist outputtet som et samlet diagram, skal du vælge **Vis diagram**.</span><span class="sxs-lookup"><span data-stu-id="401bc-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="401bc-119">Formularen omfatter ikke subtotaler, der er defineret i rapportlayoutet.</span><span class="sxs-lookup"><span data-stu-id="401bc-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="401bc-120">Med dataenheden **Aldersfordelt lagerrapport** kan du eksportere outputtet fra en rapport for **Lagerets aldersfordeling** ved at anvende et filter i feltet **Procesindentifikator –Navn** for et hvilket som helst format, som Datastyring understøtter.</span><span class="sxs-lookup"><span data-stu-id="401bc-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
