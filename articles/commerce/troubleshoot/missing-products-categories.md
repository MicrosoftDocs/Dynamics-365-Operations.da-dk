---
title: Manglende produkter og kategorier efter miljøkopi
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når produkter og kategorier mangler, efter at et websted er kopieret mellem miljøer eller i det samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022392"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="2931a-103">Manglende produkter og kategorier efter miljøkopi</span><span class="sxs-lookup"><span data-stu-id="2931a-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2931a-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når produkter og kategorier mangler, efter at et websted er kopieret mellem miljøer eller i det samme miljø.</span><span class="sxs-lookup"><span data-stu-id="2931a-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="2931a-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2931a-105">Description</span></span>

<span data-ttu-id="2931a-106">Når en lokation er kopieret fra ét miljø til et andet eller i det samme miljø, mangler produkterne og kategorierne fra lokationen.</span><span class="sxs-lookup"><span data-stu-id="2931a-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="2931a-107">Produkterne og kategorierne mangler i e-commerce-butikken og fra fanen **Produkter** i Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="2931a-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="2931a-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="2931a-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="2931a-109">Knytte nummeret på kanalens driftsenhed til et nyligt kopieret websted i Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="2931a-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="2931a-110">Følg disse trin,for at knytte nummeret på kanalens driftsenhed (OUN) til et nyligt kopieret websted i Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="2931a-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2931a-111">Vælg det nyligt kopierede sted.</span><span class="sxs-lookup"><span data-stu-id="2931a-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="2931a-112">Vælg **Kanaler** nedenunder **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="2931a-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="2931a-113">Vælg ellipsen (**...**) ud for kanalnavnet, og vælg derefter **Skift onlinebutikskanal**.</span><span class="sxs-lookup"><span data-stu-id="2931a-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="2931a-114">Vælg den kanal, du vil knytte til det nyligt kopierede websted, i dialogboksen **Skift onlinebutikskanal**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2931a-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="2931a-115">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="2931a-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2931a-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2931a-116">Additional resources</span></span>

[<span data-ttu-id="2931a-117">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="2931a-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
