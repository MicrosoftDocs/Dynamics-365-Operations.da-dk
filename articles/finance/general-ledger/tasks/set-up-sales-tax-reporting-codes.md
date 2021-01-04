---
title: Konfigurer momsrapporteringskoder
description: Momsrapporteringskoderne refererer til et feltnummer, der er angivet i en momsrapport.
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646175"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="ed9ee-103">Konfigurer momsrapporteringskoder</span><span class="sxs-lookup"><span data-stu-id="ed9ee-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed9ee-104">Momsrapporteringskoderne refererer til et feltnummer, der er angivet i en momsrapport.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="ed9ee-105">De bruges i landespecifikke rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="ed9ee-106">De anvendes også i momsafregning pr. kode i rapport.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="ed9ee-107">Denne rapport viser momsbeløb for en opsummeringsperiode for hver enkelt rapporteringskode.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="ed9ee-108">Når du har oprettet momsrapporteringskoderne, kan du referere til disse koder i oversigtspanelet Rapportopsætning, som då får adgang til fra siden **Momskode** .</span><span class="sxs-lookup"><span data-stu-id="ed9ee-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="ed9ee-109">Denne registrering anvender demofirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ed9ee-110">Gå i **Navigationsrude** til **Moms > Opsætning > Moms > Momsrapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="ed9ee-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-111">Click **New**.</span></span>
3. <span data-ttu-id="ed9ee-112">Vælg det rapportlayout, som rapporteringskoden hører til.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="ed9ee-113">Dette layout bruges til at filtrere de tilgængelige rapporteringskoder til en salgsmomskode.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="ed9ee-114">Hver salgsmomskode tilhører en afregningsperiode, der tilhører en momsmyndighed, som bruger et rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="ed9ee-115">Angiv et tal i feltet **Rapporteringskode**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="ed9ee-116">Angiv en beskrivelse, der skal vises i rapporter, i feltet **Rapporttekst**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="ed9ee-117">Angiv en beskrivelse til interne formål i feltet **Kort beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="ed9ee-118">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ed9ee-118">Click **Save**.</span></span>

