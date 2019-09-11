---
title: Konfigurer momsrapporteringskoder
description: Momsrapporteringskoderne refererer til et feltnummer i en momsrapport.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916085"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="2932f-103">Konfigurer momsrapporteringskoder</span><span class="sxs-lookup"><span data-stu-id="2932f-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2932f-104">Momsrapporteringskoderne refererer til et feltnummer i en momsrapport.</span><span class="sxs-lookup"><span data-stu-id="2932f-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="2932f-105">De bruges i landespecifikke rapportlayout og i rapporten Momsafregning pr. kode til at udskrive momsbeløb for en afregningsperiode, der er opsummeret pr. rapporteringskode.</span><span class="sxs-lookup"><span data-stu-id="2932f-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="2932f-106">Når du har oprettet momsrapporteringskoderne, kan du referere til dem i oversigtspanelet Rapportopsætning på siden Momskode.</span><span class="sxs-lookup"><span data-stu-id="2932f-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="2932f-107">Denne registrering anvender demofirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="2932f-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="2932f-108">Gå i **Navigationsrude** til **Moms > Opsætning > Moms > Momsrapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="2932f-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="2932f-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2932f-109">Click **New**.</span></span>
3. <span data-ttu-id="2932f-110">Vælg det rapportlayout, som rapporteringskoden hører til.</span><span class="sxs-lookup"><span data-stu-id="2932f-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="2932f-111">Dette layout bruges til at filtrere de tilgængelige rapporteringskoder til en momskode.</span><span class="sxs-lookup"><span data-stu-id="2932f-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="2932f-112">Hver momskode tilhører en afregningsperiode, der tilhører en momsmyndighed som bruger et rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="2932f-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="2932f-113">Angiv et tal i feltet **Rapporteringskode**.</span><span class="sxs-lookup"><span data-stu-id="2932f-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="2932f-114">Angiv en beskrivelse, der skal vises i rapporter, i feltet **Rapporttekst**.</span><span class="sxs-lookup"><span data-stu-id="2932f-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="2932f-115">Angiv en beskrivelse til interne formål i feltet **Kort beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="2932f-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="2932f-116">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2932f-116">Click **Save**.</span></span>

