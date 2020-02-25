---
title: Sælge og returnere produkter, der ikke er en del af en butiks sortiment
description: Med Dynamics 365 Commerce kan du sælge og returnere produkter uden for sortimenter.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022024"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="6be8a-103">Sælge og returnere produkter, der ikke er en del af en butiks sortiment</span><span class="sxs-lookup"><span data-stu-id="6be8a-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6be8a-104">Et almindeligt scenarie for enhver detailhandler er at sælge produkter til kunderne eller acceptere returvarer fra kunderne, selvom de ikke fører de konkrete produkter i deres butik (med andre ord er produkterne ikke i butikssortimentet).</span><span class="sxs-lookup"><span data-stu-id="6be8a-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="6be8a-105">Her er nogle typiske scenarier:</span><span class="sxs-lookup"><span data-stu-id="6be8a-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="6be8a-106">En detailhandler fører ikke alle sine produkter i en bestemt butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="6be8a-107">De resterende produkter opbevares på lageret.</span><span class="sxs-lookup"><span data-stu-id="6be8a-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="6be8a-108">Den butiksansatte kan hjælpe kunden med at søge efter produkter på lageret, føje dem til indkøbsvognen og betale ved kassen ved at vælge en leveringsmetode, f.eks. afsendelse til en adresse fra lagerstedet eller at lade kunden afhente produktet fra det aktuelle lager eller fra en anden butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="6be8a-109">En detailhandler fører ikke bestemte produkter i butikken eller har dem ikke på lager i den butik, kunden har besøgt, men produkterne er tilgængelige i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="6be8a-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="6be8a-110">Den butiksansatte kan hjælpe kunden med at søge efter produkter i den anden butik, føje dem til indkøbsvognen og betale ved kassen ved at vælge en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="6be8a-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="6be8a-111">En detailhandler har mange butikker i og omkring en bestemt by eller et postnummer og vil ikke vinge kunder til at returnere varer til den samme butik, som de er købt i.</span><span class="sxs-lookup"><span data-stu-id="6be8a-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="6be8a-112">I stedet kan kunder returnere varer til enhver butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="6be8a-113">Disse almindelige scenarier er tilgængelige for detailhandlere ved hjælp af Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be8a-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="6be8a-114">Med Commerce kan du:</span><span class="sxs-lookup"><span data-stu-id="6be8a-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="6be8a-115">Søge efter produkter i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="6be8a-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="6be8a-116">Gennemse alle frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="6be8a-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="6be8a-117">Oprette kontant og afhentet-transaktioner eller kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="6be8a-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="6be8a-118">Vælge leveringsmuligheder for kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="6be8a-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="6be8a-119">Hente produkter i den aktuelle butik eller en anden butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="6be8a-120">Annullere en ordre i den aktuelle butik eller en anden butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="6be8a-121">Returnere en ordre med eller uden kvitteringen i den aktuelle butik eller en anden butik.</span><span class="sxs-lookup"><span data-stu-id="6be8a-121">Return an order with or without the receipt at the current store or another store.</span></span>
