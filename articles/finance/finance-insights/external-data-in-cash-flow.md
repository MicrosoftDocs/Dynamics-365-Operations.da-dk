---
title: Bruge eksterne data i likviditetsbudgetter (prøveversion)
description: I dette emne beskrives de opsætningstrin, du skal udføre, så eksterne data kan angives eller importeres i likviditetsbudgetter.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186684"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="d862e-103">Bruge eksterne data i likviditetsbudgetter (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="d862e-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d862e-104">Eksterne data kan indtastes eller importeres i likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="d862e-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="d862e-105">I dette emne beskrives de opsætningstrin, der er specifikke for brugen af eksterne data, og som gør det muligt at inkludere de eksterne data i et likviditetsbudget.</span><span class="sxs-lookup"><span data-stu-id="d862e-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="d862e-106">Ekstern opsætning af data</span><span class="sxs-lookup"><span data-stu-id="d862e-106">External data setup</span></span>

<span data-ttu-id="d862e-107">Brug fanen **Ekstern kilde** på siden **Opsætning af likviditetsbudget** (**Likviditets- og bankstyring \> Likviditetsbudget**) til at angive indstillinger, der understøtter brugen af eksterne data i likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="d862e-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="d862e-108">Du kan finde flere oplysninger om opsætningen finder du i [Likviditetsbudget](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="d862e-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="d862e-109">Hvis du vil angive eksterne data til likviditetsbudgetter, kan du bruge funktionen Åbn i Excel til at indtaste og redigere eksterne data.</span><span class="sxs-lookup"><span data-stu-id="d862e-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="d862e-110">Vælg knappen **Eksterne data**, og vælg derefter enten **Tilføj eksterne data** eller **Rediger eksisterende eksterne data**.</span><span class="sxs-lookup"><span data-stu-id="d862e-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="d862e-111">Når Microsoft Excel-filen åbnes, kan du angive oplysninger i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="d862e-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="d862e-112">**Adgangskode**</span><span class="sxs-lookup"><span data-stu-id="d862e-112">**Entry ID**</span></span>
- <span data-ttu-id="d862e-113">**Beskrivelse** (valgfri)</span><span class="sxs-lookup"><span data-stu-id="d862e-113">**Description** (optional)</span></span>
- <span data-ttu-id="d862e-114">**Navn på ekstern kilde** – Vælg en af de værdier på listen, som du definerede, da du konfigurerede Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="d862e-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="d862e-115">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="d862e-115">**Legal Entity**</span></span>
- <span data-ttu-id="d862e-116">**Dato**</span><span class="sxs-lookup"><span data-stu-id="d862e-116">**Date**</span></span>
- <span data-ttu-id="d862e-117">**Beløb i transaktionsvaluta**</span><span class="sxs-lookup"><span data-stu-id="d862e-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="d862e-118">**Valutakode**</span><span class="sxs-lookup"><span data-stu-id="d862e-118">**Currency Code**</span></span>
- <span data-ttu-id="d862e-119">**Standarddimension** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="d862e-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="d862e-120">**Dokumentnummer** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="d862e-120">**Document number** (optional)</span></span>
- <span data-ttu-id="d862e-121">**Kontonummer** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="d862e-121">**Account number** (optional)</span></span>
- <span data-ttu-id="d862e-122">**Kontonavn** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="d862e-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="d862e-123">Importere eksterne data ved hjælp af data Management Framework</span><span class="sxs-lookup"><span data-stu-id="d862e-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="d862e-124">Du kan importere eksterne data til likviditetsbudgetter ved hjælp af arbejdsområdet **Datastyring** og den enhed, der hedder **Eksternt likviditetsbudget**.</span><span class="sxs-lookup"><span data-stu-id="d862e-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="d862e-125">Hvis du desuden skal flytte konfigurationsdata fra ét miljø til et andet, er området for følgende objekter tilgængelige for de opsætningstabeller, der er nødvendige:</span><span class="sxs-lookup"><span data-stu-id="d862e-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="d862e-126">Konfiguration af ekstern kilde til likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="d862e-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="d862e-127">Konfiguration af ekstern kildes juridiske enhed til likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="d862e-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
