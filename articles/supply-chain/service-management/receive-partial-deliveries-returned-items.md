---
title: Modtage delleveringer af returvarer
description: "Delleverancer defineres ved hjælp af returordrelinjer, ikke returordreforsendelser."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="ae54e-103">Modtage delleveringer af returvarer</span><span class="sxs-lookup"><span data-stu-id="ae54e-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ae54e-104">Delleverancer defineres ved hjælp af returordrelinjer, ikke returordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="ae54e-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="ae54e-105">Hvis du modtager hele det antal, der er angivet på en returordrelinje, men intet fra de andre linjer i returordren, er leverancen ikke en delleverance.</span><span class="sxs-lookup"><span data-stu-id="ae54e-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="ae54e-106">Hvis en returordrelinje derimod angiver, at ti enheder af en bestemt vare skal returneres, men du kun modtager fire, er det en delleverance.</span><span class="sxs-lookup"><span data-stu-id="ae54e-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="ae54e-107">Hvis en returforsendelse indeholder mindre end det samlede antal for en returordrelinje, kan du sætte forsendelsen til side og vente, indtil resten af det returnerede antal modtages, eller du kan registrere og bogføre den pågældende del af antallet.</span><span class="sxs-lookup"><span data-stu-id="ae54e-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="ae54e-108">Registrere og bogføre en del af et antal</span><span class="sxs-lookup"><span data-stu-id="ae54e-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="ae54e-109">Når du har valgt en returordre til modtagelse i formularen **Oversigt over modtagelse - Lagersted: %1, område: %2, Kladdenavn: %3** skal du klikke på **Start modtagelse** for at oprette modtagelseskladden og derefter klikke på **Kladder** \> **Vis modtagelser fra tilgange** at åbne formularen **Lokationskladde**.</span><span class="sxs-lookup"><span data-stu-id="ae54e-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="ae54e-110">Vælg den kladdelinje, du vil arbejde med, og klik derefter på **Linjer** for at åbne formularen **Kladdelinjer, lokationer**.</span><span class="sxs-lookup"><span data-stu-id="ae54e-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="ae54e-111">Vælg linjen for det varenummer, som du kun har modtaget en del af antallet af, og klik derefter på **Funktioner** \> **Splitning** for at åbne formularen **Splitning**.</span><span class="sxs-lookup"><span data-stu-id="ae54e-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="ae54e-112">Angiv mængden af det samlede antal varer, der er modtaget, i feltet **Splitantal**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae54e-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="ae54e-113">Vælg linjen for det antal varer, der er modtaget, i formularen **Kladdelinjer, lokationer**, og klik derefter på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="ae54e-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="ae54e-114">Du kan bogføre linjen for det yderligere antal, når varerne er modtaget.</span><span class="sxs-lookup"><span data-stu-id="ae54e-114">You can post the line for the additional quantity after the items have arrived.</span></span>




