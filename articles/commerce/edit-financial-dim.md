---
title: Redigere økonomiske dimensioner for detailtransaktioner
description: Dette emne beskriver, hvordan du redigerer økonomiske dimensioner for detailtransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: ff16d8e2e75a877e5ca7de604c7915e908473da6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792699"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="c251f-103">Redigere økonomiske dimensioner for detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="c251f-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c251f-104">Dette emne beskriver, hvordan du redigerer økonomiske dimensioner for detailtransaktioner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c251f-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="c251f-105">Redigere økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="c251f-105">Edit financial dimensions</span></span>

<span data-ttu-id="c251f-106">Hvis du vil redigere økonomiske dimensioner for detailtransaktioner i hovedkontoret Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c251f-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c251f-107">Åbn siden **Konfiguration af økonomiske dimensioner til integrering af ansøgninger**.</span><span class="sxs-lookup"><span data-stu-id="c251f-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="c251f-108">Vælg den aktive post **Standarddimensioner til integrering**.</span><span class="sxs-lookup"><span data-stu-id="c251f-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="c251f-109">På oversigtspanelet **Økonomiske dimensioner** skal du sørge for, at alle de dimensioner, du vil redigere i Excel-regnearket, findes på listen **Valgte**.</span><span class="sxs-lookup"><span data-stu-id="c251f-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="c251f-110">Du kan finde flere oplysninger under [Dataenheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="c251f-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="c251f-111">Overfør og åbn Excel-filen fra siden **Opgørelser**, siden **Detailtransaktioner** eller feltet **Transaktionsvalideringsfejl** i arbejdsområdet **Butiksøkonomi**.</span><span class="sxs-lookup"><span data-stu-id="c251f-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="c251f-112">Hvis du vil ændre den økonomiske dimension for transaktionen, skal du vælge **Design** og derefter vælge blyantsymbolet ud for rækken **Transaktion (reviderbar)**.</span><span class="sxs-lookup"><span data-stu-id="c251f-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="c251f-113">Find og markér feltet **FinancialDimensionDisplayValue** , vælg en celle i øverste del af Excel-regnearket, og vælg derefter **Tilføj etiket**.</span><span class="sxs-lookup"><span data-stu-id="c251f-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="c251f-114">Markér en celle under den celle, du har valgt i forrige trin, vælg **Tilføj værdi**, og vælg derefter **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="c251f-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="c251f-115">De økonomiske dimensioner føjes til Excel-regnearket, og de kan derefter redigeres og publiceres.</span><span class="sxs-lookup"><span data-stu-id="c251f-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="c251f-116">Hvis du vil ændre dimensionerne på transaktionslinjerne, skal du vælge rækken **Salgstransaktioner (reviderbar)**, vælge blyantsymbolet og derefter gentage trin 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="c251f-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="c251f-117">Hvis du vil ændre dimensionerne på betalingslinjerne, skal du vælge rækken **Betalingstransaktioner (reviderbar)**, vælge blyantsymbolet og derefter gentage trin 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="c251f-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c251f-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c251f-118">Additional resources</span></span>

[<span data-ttu-id="c251f-119">Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="c251f-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="c251f-120">Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="c251f-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="c251f-121">Oprette en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="c251f-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="c251f-122">Føje felter til en Excel-projektmappe for at redigere detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="c251f-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]