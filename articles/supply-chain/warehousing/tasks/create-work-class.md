---
title: Oprette en arbejdsklasse
description: Denne procedure viser, hvordan du opretter en arbejdsklasse.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49b110b93e6f0f886d180f9f2725245faad7afab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239032"
---
# <a name="create-a-work-class"></a><span data-ttu-id="e3ec7-103">Oprette en arbejdsklasse</span><span class="sxs-lookup"><span data-stu-id="e3ec7-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3ec7-104">Denne procedure viser, hvordan du opretter en arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="e3ec7-105">Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="e3ec7-106">De linjer, som en medarbejder kan behandle, bestemmes fra arbejdsklasserne på de varer i mobilenhedsmenuen, som lagermedarbejderen har adgang til, og arbejdsklassen, der er angivet på arbejdslinjerne.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="e3ec7-107">Arbejdsklasser kan også bruges til at validere placeringslokalitet for en arbejdsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="e3ec7-108">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e3ec7-109">Denne procedure er beregnet til lagerchefen.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="e3ec7-110">Gå til Lagerstyring > Opsætning > Arbejde > Arbejdsklasser.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="e3ec7-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-111">Click New.</span></span>
3. <span data-ttu-id="e3ec7-112">Skriv en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="e3ec7-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e3ec7-114">Vælg en indstilling i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="e3ec7-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-115">Click New.</span></span>
7. <span data-ttu-id="e3ec7-116">Indtast en værdi i feltet Lokalitetstype.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="e3ec7-117">Hvis du vælger en lokalitetstype, angiver dette en begrænsning på, hvor varer kan placeres, når de er valgt.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="e3ec7-118">Denne indstilling bruges, når en lokalitetsvejledning forsøger at finde lokaliteten, eller hvis en lagermedarbejder manuelt angiver lokaliteten for varen i mobilenhedsmenuen.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="e3ec7-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]