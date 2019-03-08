---
title: Lagermærkatoptælling
description: Denne artikel indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "328947"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="6daa3-103">Lagermærkatoptælling</span><span class="sxs-lookup"><span data-stu-id="6daa3-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="6daa3-104">Denne artikel indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="6daa3-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="6daa3-105">Ved at oprette linjer på siden **Mærkatoptælling** placerer du et mærkatnummer på hver lagervare, som et tal mellem 1 og 500.</span><span class="sxs-lookup"><span data-stu-id="6daa3-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="6daa3-106">Under optællingen skal du angive varenummeret og antallet på et tilsvarende mærkat.</span><span class="sxs-lookup"><span data-stu-id="6daa3-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="6daa3-107">Denne mærkat kan derefter bruges som grundlag for input i kladden til mærkatoptælling.</span><span class="sxs-lookup"><span data-stu-id="6daa3-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="6daa3-108">Når du bogfører mærkatoptællingskladden, oprettes en ny optællingskladde på siden **Optælling**.</span><span class="sxs-lookup"><span data-stu-id="6daa3-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="6daa3-109">Den nye kladde er baseret på de kladdelinjer til mærkatoptælling, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="6daa3-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="6daa3-110">Når du vil mærkatoptælle elementer efter en bestemt lagerdimension, kan du vælge dimensionen på siden **Vis dimension**, som vises, når du opretter kladden til mærkatoptælling.</span><span class="sxs-lookup"><span data-stu-id="6daa3-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="6daa3-111">Hvis du f.eks. vil tælle varer på et bestemt lagersted, skal du markere afkrydsningsfeltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="6daa3-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="6daa3-112">Hvis slideren **Lås varer under optælling** på siden **Parametre til lager- og lokationsstyring** er valgt på siden, kan varer ikke opdateres fysisk under optælling.</span><span class="sxs-lookup"><span data-stu-id="6daa3-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="6daa3-113">Dog låses varer i mærkatoptællingskladder ikke under optælling.</span><span class="sxs-lookup"><span data-stu-id="6daa3-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="6daa3-114">Der oprettes ikke lagertransaktioner, før mærkatoptællingslinjerne er bogført og overført til en optællingskladde.</span><span class="sxs-lookup"><span data-stu-id="6daa3-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="6daa3-115">Hvis mærkaterne angives i vilkårlig rækkefølge, og du vil identificere de manglende mærkater, skal du klikke på kolonneoverskriften **Mærkat**.</span><span class="sxs-lookup"><span data-stu-id="6daa3-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6daa3-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6daa3-116">Additional resources</span></span>
--------

[<span data-ttu-id="6daa3-117">Cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="6daa3-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
