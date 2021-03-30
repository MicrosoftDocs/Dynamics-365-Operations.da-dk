---
title: Lagring af Rapporten Aldersfordelt lager
description: I dette emne beskrives de funktioner, der giver mulighed for at køre en aldersfordelt lagerrapport, og gøre outputtet tilgængeligt som en formel og et diagram.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40b15448677f319c650c667cd7c4981c343f7a02
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205340"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="812bc-103">Lagring af Rapporten Aldersfordelt lager</span><span class="sxs-lookup"><span data-stu-id="812bc-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="812bc-104">I Microsoft Dynamics 365 Supply Chain Management kan du køre rapporten **Lager for aldersfordelt lagerrapport** og gøre outputtet tilgængeligt som en formular og et diagram.</span><span class="sxs-lookup"><span data-stu-id="812bc-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="812bc-105">I formularen reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det konfigurerede layout.</span><span class="sxs-lookup"><span data-stu-id="812bc-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="812bc-106">Diagrammet indeholder en visuel oversigt, der understøtter filtrering og giver dig mulighed for at gå i detaljer.</span><span class="sxs-lookup"><span data-stu-id="812bc-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="812bc-107">Derudover giver en dataenhed ved navn **Aldersfordelt lagerrapport** dig mulighed for at eksportere resultaterne af rapporten **Lager for aldersfordelt lagerrapport** til et format som f.eks en Microsoft Excel-fil eller en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="812bc-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="812bc-108">Denne metode til kørsel af rapporten **Lager for aldersfordelt lagerrapport** er nyttig i de tilfælde, hvor outputtet indeholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="812bc-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="812bc-109">Outputtet indeholder f.eks. mange linjer, hvis du har 50.000 varer og 300 butikker, der oprettes som lagersteder, og du anmoder om lagerets aldersfordeling pr. vare, lokation og lagersted.</span><span class="sxs-lookup"><span data-stu-id="812bc-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="812bc-110">Aktivere lagerrapportfunktionen for lagerværdi</span><span class="sxs-lookup"><span data-stu-id="812bc-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="812bc-111">Før du kan bruge denne funktion, skal du aktivere den i dit system.</span><span class="sxs-lookup"><span data-stu-id="812bc-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="812bc-112">Administratorer kan bruge indstillingerne [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="812bc-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="812bc-113">Her er funktionen angivet som:</span><span class="sxs-lookup"><span data-stu-id="812bc-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="812bc-114">**Modul** - Omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="812bc-114">**Module** - Cost management</span></span>
- <span data-ttu-id="812bc-115">**Funktionsnavn** - Lager for aldersfordelt lagerrapport</span><span class="sxs-lookup"><span data-stu-id="812bc-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="812bc-116">Køre en Lager for aldersfordelt lagerrapport</span><span class="sxs-lookup"><span data-stu-id="812bc-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="812bc-117">Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lager for aldersfordelte lagerrapporter**.</span><span class="sxs-lookup"><span data-stu-id="812bc-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="812bc-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="812bc-118">Select **New**.</span></span>
1. <span data-ttu-id="812bc-119">kriv et entydigt navn for rapporten i feltet **Procesidentifikator – Navn**.</span><span class="sxs-lookup"><span data-stu-id="812bc-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="812bc-120">Vælg rapporten **Identifikation – Id**, og filtrer den efter behov.</span><span class="sxs-lookup"><span data-stu-id="812bc-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="812bc-121">Rapportafviklingen udføres altid i et batchjob.</span><span class="sxs-lookup"><span data-stu-id="812bc-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="812bc-122">Når batchjobbet er fuldført, vises outputtet på siden **Lager for aldersfordelt lagerrapport**.</span><span class="sxs-lookup"><span data-stu-id="812bc-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="812bc-123">Hvis du vil have vist outputtet som en formular med et traditionelt gitterlayout, skal du vælge **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="812bc-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="812bc-124">Hvis du vil have vist outputtet som et samlet diagram, skal du vælge **Vis diagram**.</span><span class="sxs-lookup"><span data-stu-id="812bc-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="812bc-125">Formularen omfatter ikke subtotaler, der er defineret i rapportlayoutet.</span><span class="sxs-lookup"><span data-stu-id="812bc-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="812bc-126">Med dataenheden **Aldersfordelt lagerrapport** kan du eksportere outputtet fra rapporten **Lager for aldersfordelt lagerrapport** ved at anvende et filter i feltet **Procesindentifikator – Navn** for et hvilket som helst format, som Datastyring understøtter.</span><span class="sxs-lookup"><span data-stu-id="812bc-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]