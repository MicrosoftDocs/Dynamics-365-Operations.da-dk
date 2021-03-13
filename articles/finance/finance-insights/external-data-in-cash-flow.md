---
title: Bruge eksterne data i likviditetsbudgetter (prøveversion)
description: I dette emne beskrives de opsætningstrin, du skal udføre, så eksterne data kan angives eller importeres i likviditetsbudgetter.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ae0eba6d397725cf425d9781a597d904e1958d44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009383"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="dd0e3-103">Bruge eksterne data i likviditetsbudgetter (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="dd0e3-104">Eksterne data kan indtastes eller importeres i likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="dd0e3-105">I dette emne beskrives de opsætningstrin, der er specifikke for brugen af eksterne data, og som gør det muligt at inkludere de eksterne data i et likviditetsbudget.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="dd0e3-106">Ekstern opsætning af data</span><span class="sxs-lookup"><span data-stu-id="dd0e3-106">External data setup</span></span>

<span data-ttu-id="dd0e3-107">Brug fanen **Ekstern kilde** på siden **Opsætning af likviditetsbudget** (**Likviditets- og bankstyring \> Likviditetsbudget**) til at angive indstillinger, der understøtter brugen af eksterne data i likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="dd0e3-108">Du kan finde flere oplysninger om opsætningen finder du i [Likviditetsbudget](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="dd0e3-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="dd0e3-109">Hvis du vil angive eksterne data til likviditetsbudgetter, kan du bruge funktionen Åbn i Excel til at indtaste og redigere eksterne data.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="dd0e3-110">Vælg knappen **Eksterne data**, og vælg derefter enten **Tilføj eksterne data** eller **Rediger eksisterende eksterne data**.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="dd0e3-111">Når Microsoft Excel-filen åbnes, kan du angive oplysninger i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="dd0e3-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="dd0e3-112">**Adgangskode**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-112">**Entry ID**</span></span>
- <span data-ttu-id="dd0e3-113">**Beskrivelse** (valgfri)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-113">**Description** (optional)</span></span>
- <span data-ttu-id="dd0e3-114">**Navn på ekstern kilde** – Vælg en af de værdier på listen, som du definerede, da du konfigurerede Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="dd0e3-115">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-115">**Legal Entity**</span></span>
- <span data-ttu-id="dd0e3-116">**Dato**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-116">**Date**</span></span>
- <span data-ttu-id="dd0e3-117">**Beløb i transaktionsvaluta**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="dd0e3-118">**Valutakode**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-118">**Currency Code**</span></span>
- <span data-ttu-id="dd0e3-119">**Standarddimension** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="dd0e3-120">**Dokumentnummer** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-120">**Document number** (optional)</span></span>
- <span data-ttu-id="dd0e3-121">**Kontonummer** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-121">**Account number** (optional)</span></span>
- <span data-ttu-id="dd0e3-122">**Kontonavn** (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="dd0e3-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="dd0e3-123">Importere eksterne data ved hjælp af data Management Framework</span><span class="sxs-lookup"><span data-stu-id="dd0e3-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="dd0e3-124">Du kan importere eksterne data til likviditetsbudgetter ved hjælp af arbejdsområdet **Datastyring** og den enhed, der hedder **Eksternt likviditetsbudget**.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="dd0e3-125">Hvis du desuden skal flytte konfigurationsdata fra ét miljø til et andet, er området for følgende objekter tilgængelige for de opsætningstabeller, der er nødvendige:</span><span class="sxs-lookup"><span data-stu-id="dd0e3-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="dd0e3-126">Konfiguration af ekstern kilde til likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="dd0e3-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="dd0e3-127">Konfiguration af ekstern kildes juridiske enhed til likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="dd0e3-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="dd0e3-128">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="dd0e3-128">Privacy notice</span></span>
<span data-ttu-id="dd0e3-129">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
