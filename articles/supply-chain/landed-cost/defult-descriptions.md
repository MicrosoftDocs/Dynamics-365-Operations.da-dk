---
title: Standardbeskrivelser af finans
description: Standardbeskrivelser kan bruges til opdatering af feltet Beskrivelse i bilagsbogføringer til finans.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841884"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="584f1-103">Standardbeskrivelser af finans</span><span class="sxs-lookup"><span data-stu-id="584f1-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="584f1-104">Standardbeskrivelser kan bruges til opdatering af feltet **Beskrivelse** i bilagsbogføringer til finans.</span><span class="sxs-lookup"><span data-stu-id="584f1-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="584f1-105">Denne funktionalitet er forbedret, så den kan fungere med Landingsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="584f1-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="584f1-106">Du kan oprette standardbeskrivelser til finansbogføringer ved at gå til **Organisationsadministration \> Opsætning \> Standardbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="584f1-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="584f1-107">Følgende tabel indeholder de nye værdier, der er blevet føjet til feltet **Beskrivelse** på siden **Standardbeskrivelser** for at understøtte landingsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="584f1-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="584f1-108">Beskrivelsestype</span><span class="sxs-lookup"><span data-stu-id="584f1-108">Description type</span></span> | <span data-ttu-id="584f1-109">Notater</span><span class="sxs-lookup"><span data-stu-id="584f1-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="584f1-110">Importér efterkalkulation - omkostningsperiodisering</span><span class="sxs-lookup"><span data-stu-id="584f1-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="584f1-111">Når en indkøbsordrefaktura bogføres, behandles en omkostningsperiodisering for de estimerede fragtomkostninger.</span><span class="sxs-lookup"><span data-stu-id="584f1-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="584f1-112">Der kan angives standardbeskrivelser, hvis du vil føje fragtnummeret til beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="584f1-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="584f1-113">Brug *%4* som forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="584f1-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="584f1-114">Importefterkalkulation – Ordre i varer i transit</span><span class="sxs-lookup"><span data-stu-id="584f1-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="584f1-115">Hvis du bruger behandling i transit, bogføres indkøbsordrefakturaen, og varerne på en konto for varer i transit.</span><span class="sxs-lookup"><span data-stu-id="584f1-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="584f1-116">Der kan angives standardbeskrivelser, hvis du vil føje transitordrenummeret til beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="584f1-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="584f1-117">Brug *%4* til transitordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="584f1-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="584f1-118">Lager - Lukning - Regulering</span><span class="sxs-lookup"><span data-stu-id="584f1-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="584f1-119">Når kreditorfakturaen behandles for en fragtomkostning, behandles der en lagerregulering for at estimere fragtomkostninger.</span><span class="sxs-lookup"><span data-stu-id="584f1-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="584f1-120">Der kan angives standardbeskrivelser, hvis du vil føje fragtnummeret til beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="584f1-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="584f1-121">Brug *%4* som forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="584f1-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="584f1-122">Du kan finde flere oplysninger om, hvordan du arbejder med siden **Standardbeskrivelser**, i [Oprette standardbeskrivelser til automatisk bogføring](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="584f1-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
