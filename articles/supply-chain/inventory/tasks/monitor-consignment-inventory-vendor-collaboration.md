---
title: Overvåge konsignationslager ved hjælp af kreditorsamarbejde
description: Denne fremgangsmåde viser, hvordan du kan bruge leverandørsamarbejde til at få vist oplysninger om lagerbeholdning for det produkt, som du har i konsignation hos en kunde.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c74f09ee2056ce88442bf8f8ccba3985638525a6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213932"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="e5a4e-103">Overvåge konsignationslager ved hjælp af kreditorsamarbejde</span><span class="sxs-lookup"><span data-stu-id="e5a4e-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5a4e-104">Denne fremgangsmåde viser, hvordan du kan bruge leverandørsamarbejde til at få vist oplysninger om lagerbeholdning for det produkt, som du har i konsignation hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="e5a4e-105">Du kan også overvåge forbruget af lager, når kunden overtager ejerskabet af lageret.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="e5a4e-106">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="e5a4e-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="e5a4e-108">Vis forbrugt lager</span><span class="sxs-lookup"><span data-stu-id="e5a4e-108">View consumed inventory</span></span>
1. <span data-ttu-id="e5a4e-109">Gå til Kreditorsamarbejde > Konsignationslager > Produkter, der er modtaget fra konsignationslager.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="e5a4e-110">Listen viser de produktkvitteringslinjer, der blev genereret, da ejerskabet af konsignationslageret blev ændret fra leverandøren til kunden.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="e5a4e-111">Du skal muligvis rulle til højre for at se mængder og andre oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="e5a4e-112">Du kan bruge oplysningerne på denne liste til at generere fakturaer for kunden.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="e5a4e-113">Du kan også eksportere dataene til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="e5a4e-114">Klik på Vis indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-114">Click View purchase order.</span></span>
3. <span data-ttu-id="e5a4e-115">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="e5a4e-116">Linjen er markeret som Konsignation, og sektionsoverskriften viser, at købsordren har statussen Modtaget.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="e5a4e-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="e5a4e-118">Få vist disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="e5a4e-118">View on-hand inventory</span></span>
1. <span data-ttu-id="e5a4e-119">Gå til Kreditorsamarbejde > Konsignationslager > Disponibelt konsignationslager.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="e5a4e-120">Siden Disponibelt konsignationslager viser det lager, du ejer på kundens lagersted.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="e5a4e-121">Du kan se yderligere dimensioner, såsom lokation og lagersted, ved at klikke på fanen Vis dimensioner.</span><span class="sxs-lookup"><span data-stu-id="e5a4e-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

