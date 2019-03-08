---
title: Serviceobjekter
description: Serviceobjekter er en kundes aktiver og produkter, som du kan udføre en service på.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5641077de84b6702d2c5621edef74783f2f104fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "353396"
---
# <a name="service-objects"></a><span data-ttu-id="4860f-103">Serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="4860f-103">Service objects</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4860f-104">Serviceobjekter er en kundes aktiver og produkter, som du kan udføre en service på.</span><span class="sxs-lookup"><span data-stu-id="4860f-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="4860f-105">Afhængigt af, hvilken form for service og ydelser du kan tilbyde, kan objekterne være materielle eller immaterielle:</span><span class="sxs-lookup"><span data-stu-id="4860f-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="4860f-106">Materielle objekter er ting, f.eks. maskiner eller en bygning, som du kan udføre en fysisk serviceopgave på.</span><span class="sxs-lookup"><span data-stu-id="4860f-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="4860f-107">Et materielt serviceobjekt kan også være en lagervare, som du opretter i formularen Frigivne produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="4860f-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="4860f-108">Afhængigt af den lagerdimensionsgruppe, som du knytter til varen, kan du oprette et serviceobjekt til et detaljeniveau, som omfatter vareserienummeret.</span><span class="sxs-lookup"><span data-stu-id="4860f-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="4860f-109">Det er en fordel, når du skal kunne følge netop den vare, som serviceobjektet repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="4860f-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="4860f-110">Et materielt serviceobjekt kan også være en vare, der ikke er direkte relateret til et firmas direkte produktion eller forsyningskæde.</span><span class="sxs-lookup"><span data-stu-id="4860f-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="4860f-111">En værktøjskasse, der anvendes til reparation i en serviceordre, kan for eksempel være et serviceobjekt, der ikke findes på lageret.</span><span class="sxs-lookup"><span data-stu-id="4860f-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="4860f-112">I så fald skal du ikke registrere det som en lagervare.</span><span class="sxs-lookup"><span data-stu-id="4860f-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="4860f-113">Immaterielle objekter er ikke-fysiske ting, f.eks. en række konti eller et juridisk dokument, som du kan udføre en serviceopgave på.</span><span class="sxs-lookup"><span data-stu-id="4860f-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="4860f-114">Eksempel på et immaterielt serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="4860f-114">Example of an intangible service object</span></span>

<span data-ttu-id="4860f-115">Firma A fører finansielle poster for flere små virksomheder.</span><span class="sxs-lookup"><span data-stu-id="4860f-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="4860f-116">En af virksomhed A's kunder er det lokale fodboldhold, for hvem virksomhed A har den ugentlige bogføring og den årlige revision af klubbens konti.</span><span class="sxs-lookup"><span data-stu-id="4860f-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="4860f-117">Klubbens konti er oprettet i formularen Serviceobjekter og angives som objektet i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="4860f-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="4860f-118">Der er to linjer i serviceaftalen for objektet.</span><span class="sxs-lookup"><span data-stu-id="4860f-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="4860f-119">Linje 1 er den ugentlige bogføring med et ugentligt interval, der er knyttet til linjen, og linje 2 er den årlige revision med et årligt interval tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="4860f-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4860f-120">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="4860f-120">Related topics</span></span>

[<span data-ttu-id="4860f-121">Oprette serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="4860f-121">Create service objects</span></span>](create-service-objects.md)

