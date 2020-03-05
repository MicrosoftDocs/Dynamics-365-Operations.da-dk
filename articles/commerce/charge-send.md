---
title: Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr
description: Dette emne beskriver sendefunktionen Gebyr.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021963"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="22382-103">Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr</span><span class="sxs-lookup"><span data-stu-id="22382-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22382-104">Med sendefunktionen Gebyr i Commerce kan kundeordrer placeres i én butik og leveres fra en anden butik.</span><span class="sxs-lookup"><span data-stu-id="22382-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="22382-105">Kundeordrer i POS-klienten understøtter flere indstillinger til ordreopfyldelse.</span><span class="sxs-lookup"><span data-stu-id="22382-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="22382-106">Nogle eksempler på indstillinger for ordreopfyldelse omfatter:</span><span class="sxs-lookup"><span data-stu-id="22382-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="22382-107">Afhentning fra den samme butik på en anden dato.</span><span class="sxs-lookup"><span data-stu-id="22382-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="22382-108">Afhentning fra en anden butik på den samme dato eller en anden dato.</span><span class="sxs-lookup"><span data-stu-id="22382-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="22382-109">Afsendelse fra det standardforsendelseslagersted, der er tildelt til butikken, og levering på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="22382-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="22382-110">Sendefunktionen Gebyr bruger følgende POS-handlinger: afsendelse af alle produkter og afsendelse af udvalgte produkter.</span><span class="sxs-lookup"><span data-stu-id="22382-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="22382-111">Dette giver butiksmedarbejderen mulighed for at vælge den "afsend fra"-lokalitet, som ordren eller ordrelinjen kan opfyldes fra.</span><span class="sxs-lookup"><span data-stu-id="22382-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="22382-112">Som standard er "afsend fra"-lokaliteten det forsendelseslagersted, der er knyttet til butikken.</span><span class="sxs-lookup"><span data-stu-id="22382-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="22382-113">Butiksmedarbejderen kan dog ændre denne placering og vælge enhver butik, der er defineret i den butikssøgegruppe, der er tildelt til butikken.</span><span class="sxs-lookup"><span data-stu-id="22382-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="22382-114">Muligheden for at vælge "levér til"-adresser forbliver uændret.</span><span class="sxs-lookup"><span data-stu-id="22382-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="22382-115">De forsendelsesmetoder, der kan bruges til at opfylde ordrelinjen er baseret på konfigurationen af gyldige leveringsmåder for produkter og adresser.</span><span class="sxs-lookup"><span data-stu-id="22382-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="22382-116">Da reglerne om gyldige leveringsmåder kun vedligeholdes i Headquarters (Hovedkontoret), foretager POS-klienten et realtidsopkald for at hente de gyldige leveringsmåder for en forsendelseslinje.</span><span class="sxs-lookup"><span data-stu-id="22382-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>