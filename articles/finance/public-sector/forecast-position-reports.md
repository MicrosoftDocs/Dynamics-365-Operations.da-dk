---
title: Rapporter over budgetteret stilling for den offentlige sektor
description: Du kan bruge rapporten oversigten over budgetteret stilling og den detaljerede rapport over budgetteret stilling til at generere oplysninger om budgetterede stillinger under en budgetplan og det scenarie, du angiver.
author: velofog
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: roschlom
ms.search.validFrom: 2019-8-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 10b1804dc0b4ab6ea2074108429297e4ad95deaa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407653"
---
# <a name="forecast-position-reports-for-the-public-sector"></a><span data-ttu-id="f8d63-103">Rapporter over budgetteret stilling for den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="f8d63-103">Forecast position reports for the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8d63-104">Du kan bruge rapporterne **Oversigt over budgetteret stilling** og **Detaljer for budgetteret stilling** til at generere oplysninger om budgetterede stillinger under en budgetplan og det scenarie, du angiver.</span><span class="sxs-lookup"><span data-stu-id="f8d63-104">You can use the **Forecast position summary** and **Forecast position detail** reports to generate information about forecast positions during a budget plan and scenario that you specify.</span></span>  

<span data-ttu-id="f8d63-105">Rapporten **Oversigt over budgetteret stilling** viser budgetterede stillingsomkostninger efter kontofordelinger.</span><span class="sxs-lookup"><span data-stu-id="f8d63-105">The **Forecast position summary** report shows forecast position costs by account distributions.</span></span> <span data-ttu-id="f8d63-106">Omkostningerne til budgetterede stillinger vises grupperet efter deres tildelte kontofordelinger.</span><span class="sxs-lookup"><span data-stu-id="f8d63-106">The forecast position costs are shown, grouped by their assigned account distributions.</span></span> <span data-ttu-id="f8d63-107">Kostbeløbene omregnes med den procent, der er tildelt kontofordelingen.</span><span class="sxs-lookup"><span data-stu-id="f8d63-107">The cost amounts are factored by the percentage assigned to the account distribution.</span></span> 

<span data-ttu-id="f8d63-108">Rapporten **Detaljer for budgetteret stilling** indeholder de fleste oplysninger, der vises i formularen for budgetteret stilling.</span><span class="sxs-lookup"><span data-stu-id="f8d63-108">The **Forecast position details** report contains most of the information displayed on the forecast position form.</span></span> <span data-ttu-id="f8d63-109">De kontofordelinger, der er tilknyttet budgetstillingen via økonomiske dimensioner og økonomiske dimensionsskabeloner, vises sammen med de omkostninger, der er knyttet til den enkelte fordelingskombination for den budgetterede stilling.</span><span class="sxs-lookup"><span data-stu-id="f8d63-109">The account distributions assigned to the forecast position via financial dimensions and financial dimension templates are shown, along with the costs associated with each distribution combination for the forecast position.</span></span> 

<span data-ttu-id="f8d63-110">Hvis du vil have vist flere oplysninger om en budgetteret stilling, skal du vælge stillingsnummeret for at åbne siden med budgetterede stillinger.</span><span class="sxs-lookup"><span data-stu-id="f8d63-110">To view more information about a Forecast position, select the Position number to open the Forecast position page.</span></span>

## <a name="filter-the-data-on-this-report"></a><span data-ttu-id="f8d63-111">Filtrere dataene i denne rapport</span><span class="sxs-lookup"><span data-stu-id="f8d63-111">Filter the data on this report</span></span>

<span data-ttu-id="f8d63-112">Når du opretter rapporten, vises følgende standardparametre.</span><span class="sxs-lookup"><span data-stu-id="f8d63-112">When you generate the report, the following default parameters are shown.</span></span>  <span data-ttu-id="f8d63-113">Du kan bruge disse parametre til at filtrere de data, der vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="f8d63-113">You can use these parameters to filter the data that appears on the report.</span></span>  

| <span data-ttu-id="f8d63-114">Felt</span><span class="sxs-lookup"><span data-stu-id="f8d63-114">Field</span></span> | <span data-ttu-id="f8d63-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f8d63-115">Description</span></span> |
| --------- | ------- |
| <span data-ttu-id="f8d63-116">Budgetplansscenarie</span><span class="sxs-lookup"><span data-stu-id="f8d63-116">Budget plan scenario</span></span> | <span data-ttu-id="f8d63-117">Vælg det budgetplanscenarie, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="f8d63-117">Select the budget plan scenario that should be listed on the report.</span></span> <p> <span data-ttu-id="f8d63-118">Budgetplanscenarier definerer kategorier af data for budgetplanerne.</span><span class="sxs-lookup"><span data-stu-id="f8d63-118">Budget plan scenarios define categories of data for the budget plans.</span></span> <span data-ttu-id="f8d63-119">Du kan definere scenarier for budgetplaner for at understøtte monetære og andre måleenhedsklasser, f.eks. mængde.</span><span class="sxs-lookup"><span data-stu-id="f8d63-119">You define budget plan scenarios to support monetary and other unit of measure classes, such as quantity.</span></span> <span data-ttu-id="f8d63-120">Eksempler på scenarier med monetære budgetplaner inkluderer Afdeling forrige år og Afdelingsforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="f8d63-120">Examples of monetary budget plan scenarios include Department previous year and Department requests.</span></span> <span data-ttu-id="f8d63-121">Eksempler på budgetplansscenarier, der bruger antal, omfatter forrige års supportopkald og antal fuldtidsækvivalenter.</span><span class="sxs-lookup"><span data-stu-id="f8d63-121">Examples of budget plan scenarios that use quantities include Previous year support calls and Full-time equivalent (FTE) count.</span></span> </p>  |
| <span data-ttu-id="f8d63-122">Budgetplanlægningsproces</span><span class="sxs-lookup"><span data-stu-id="f8d63-122">Budget planning process</span></span> | <span data-ttu-id="f8d63-123">Vælg den budgetplanlægningsproces, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="f8d63-123">Select the budget planning process that should be listed on the report.</span></span><p> <span data-ttu-id="f8d63-124">Budgetplanlægningsprocesser bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering.</span><span class="sxs-lookup"><span data-stu-id="f8d63-124">Budget planning processes determine how budget plans can be updated, routed, reviewed, and approved in the budgeting organization hierarchy.</span></span> <span data-ttu-id="f8d63-125">En budgetplanlægningsproces er knyttet til en budgetcyklus og en organisation via en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="f8d63-125">A budget planning process is linked to a budget cycle and an organization via a legal entity.</span></span> </p> |
| <span data-ttu-id="f8d63-126">Standardkontostruktur</span><span class="sxs-lookup"><span data-stu-id="f8d63-126">Default account structure</span></span> | <span data-ttu-id="f8d63-127">Vælg standardkontostrukturen for visning af regnskabsdimensionerne på de budgetterede stillinger i den ønskede rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="f8d63-127">Select the default account structure to display the accounting dimensions on the forecast positions in the order you desire.</span></span>|
| <span data-ttu-id="f8d63-128">Afdeling</span><span class="sxs-lookup"><span data-stu-id="f8d63-128">Department</span></span> | <span data-ttu-id="f8d63-129">Vælg en afdeling, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="f8d63-129">Select a department that should be listed on the report.</span></span> <span data-ttu-id="f8d63-130">Lad feltet være tomt for at køre rapporten for alle konti.</span><span class="sxs-lookup"><span data-stu-id="f8d63-130">Leave the field blank to run the report for all accounts.</span></span> |
| <span data-ttu-id="f8d63-131">Kun ikke-udfyldte</span><span class="sxs-lookup"><span data-stu-id="f8d63-131">Unfilled only</span></span> | <span data-ttu-id="f8d63-132">Angiv denne indstilling til Ja for at udelade stillinger, der i øjeblikket er besat.</span><span class="sxs-lookup"><span data-stu-id="f8d63-132">Set this option to Yes to exclude positions that are currently filled.</span></span> |
| <span data-ttu-id="f8d63-133">Undertryk total</span><span class="sxs-lookup"><span data-stu-id="f8d63-133">Suppress total</span></span> | <span data-ttu-id="f8d63-134">Angiv denne indstilling til Ja for at udelade totaler i rapporten.</span><span class="sxs-lookup"><span data-stu-id="f8d63-134">Set this option to Yes to exclude totals from appearing on the report.</span></span> |

