---
title: Detailprisrapporter
description: Dette emne indeholder en oversigt over prisrapportfunktionen, der kan bruges til at få vist kommende prisændringer for udvalgte produkter.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "353051"
---
# <a name="retail-price-reports"></a><span data-ttu-id="47d22-103">Detailprisrapporter</span><span class="sxs-lookup"><span data-stu-id="47d22-103">Retail price reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


<span data-ttu-id="47d22-104">Når forhandlere vil give deres kunder konkurrencedygtige priser, ændrer de ofte priserne på produkter.</span><span class="sxs-lookup"><span data-stu-id="47d22-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="47d22-105">Butikschefer vil gerne have nem adgang til de seneste eller kommende prisændringer, så de kan planlægge, hvilke ressourcer de skal bruge til at opdatere de prisetiketter, der vises på hylderne.</span><span class="sxs-lookup"><span data-stu-id="47d22-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="47d22-106">Med udgivelse 10.0 af Dynamics 365 for Retail kan en butikschef åbne **Pris**-rapporten ved at gå til **Alle detailbutikker \> Butik \> Prisrapport** og få vist de opdaterede priser for de produkter, der er knyttet til butikken.</span><span class="sxs-lookup"><span data-stu-id="47d22-106">With release 10.0 of Dynamics 365 for Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="47d22-107">Når du vil aktivere prisrapporten, skal parameteren **Aktiver prisrapport for detailbutik** skal være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="47d22-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="47d22-108">Denne parameter findes under fanen **Detailparametre \> Rabatter \> Diverse**. Når du åbner siden **Prisrapport** , vises en dialogboks med forskellige konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="47d22-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="47d22-109">De tilgængelige konfigurationer er angivet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="47d22-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="47d22-110">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="47d22-110">Configuration</span></span> | <span data-ttu-id="47d22-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="47d22-111">Description</span></span> |
|---|---|
| <span data-ttu-id="47d22-112">Fra dato/Til dato</span><span class="sxs-lookup"><span data-stu-id="47d22-112">From date / To date</span></span>| <span data-ttu-id="47d22-113">Det datointerval, som prisrapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="47d22-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="47d22-114">Varigheden er i øjeblikket begrænset til syv dage.</span><span class="sxs-lookup"><span data-stu-id="47d22-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="47d22-115">Salgskanal</span><span class="sxs-lookup"><span data-stu-id="47d22-115">Channel</span></span>| <span data-ttu-id="47d22-116">Den detailbutik, som prisrapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="47d22-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="47d22-117">Vis produkter med tilgængeligt lager</span><span class="sxs-lookup"><span data-stu-id="47d22-117">Display products with available inventory</span></span>| <span data-ttu-id="47d22-118">Når du indstiller dette til **Ja**, er det kun priserne for de produkter, som har en tilgængelig fysiske lagerbeholdning i butikken, der vises.</span><span class="sxs-lookup"><span data-stu-id="47d22-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="47d22-119">Vis priser for varianter</span><span class="sxs-lookup"><span data-stu-id="47d22-119">Display prices for variants</span></span> | <span data-ttu-id="47d22-120">Når du vælger **Ja**, vises priser for varianterne sammen med produktmasterne.</span><span class="sxs-lookup"><span data-stu-id="47d22-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="47d22-121">Du skal kun slå denne indstilling **Til**, hvis du har variantspecifikke priser, fordi antallet af rækker bliver meget stort.</span><span class="sxs-lookup"><span data-stu-id="47d22-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="47d22-122">I fremtidige versioner anvender vi priser, der er baseret på dimensioner, så butikschefen kan vælge de dimensioner, som priserne skal vises for.</span><span class="sxs-lookup"><span data-stu-id="47d22-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="47d22-123">Vis produkter med prisændringer</span><span class="sxs-lookup"><span data-stu-id="47d22-123">Display products with price changes</span></span> | <span data-ttu-id="47d22-124">Hvis du vælger **Ja** i denne indstilling, viser kun priserne for de datoer, hvor prisen er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="47d22-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="47d22-125">Prisen for *én dag før* den valgte **Fra dato** vises altid, så butikschefen kan nemt identificere de produkter, der ikke har ændret pris i den samlede valgte varighed, og de kan også få vist den aktuelle pris.</span><span class="sxs-lookup"><span data-stu-id="47d22-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="47d22-126">Når rapporten er oprettes, kan Excel-filen hentes ved eventuelle yderligere behov for filtrering.</span><span class="sxs-lookup"><span data-stu-id="47d22-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="47d22-127">Prisrapporten kan også bruges til at kontrollere historiske priser på varer for datoer i fortiden.</span><span class="sxs-lookup"><span data-stu-id="47d22-127">The price report can also be used to check the historical prices of products for past dates.</span></span>