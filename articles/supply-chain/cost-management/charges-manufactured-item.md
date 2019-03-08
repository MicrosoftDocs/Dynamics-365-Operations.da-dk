---
title: Vise gebyrer for en produceret vare
description: En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b8fcfc1a9386d05c2adbcb4208e7ef5d01644430
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "316665"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="c58b3-103">Vise gebyrer for en produceret vare</span><span class="sxs-lookup"><span data-stu-id="c58b3-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c58b3-104">En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.</span><span class="sxs-lookup"><span data-stu-id="c58b3-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="c58b3-105">Det beregnede beløb for en vares gebyrer kan vises med varens enhedsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="c58b3-106">Gebyrerne vises dog nogle gange som separate felter, og de medtages ikke i varens enhedsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="c58b3-107">Når gebyrerne vises i separate felter, viser et felt det samlede gebyrbeløb, og et andet felt viser, hvilken lotstørrelse for efterkalkulationen der blev brugt til at amortisere beløbet.</span><span class="sxs-lookup"><span data-stu-id="c58b3-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="c58b3-108">På siden Varepris vises f.eks. gebyrerne som to separate felter.</span><span class="sxs-lookup"><span data-stu-id="c58b3-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="c58b3-109">På siden Fuldført vises dog varens samlede omkostninger pr. enhed, og de amortiserede omkostninger medtages i enhedsomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="c58b3-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="c58b3-110">Gebyrerne for en produceret vare medtages altid i varens enhedsomkostning til brug i standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="c58b3-111">Hvis det ønskes, kan de medtages til brug i planlagte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="c58b3-112">En politik i efterkalkulationsversionen gennemtvinger inkludering af gebyrer i en produceret vares omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="c58b3-113">Når du aktiverer en vares omkostningspost, opdaterer du gebyrerne for varens basisomkostningsoplysninger, som de vises på siden Varepris.</span><span class="sxs-lookup"><span data-stu-id="c58b3-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="c58b3-114">Gebyrerne vises som to separate felter, og de medtages ikke i varens enhedsomkostning.</span><span class="sxs-lookup"><span data-stu-id="c58b3-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="c58b3-115">Ved hver enkelt aktivering opdateres oplysningerne om varens basiskostpris, selvom aktiveringen afspejler forskellige lokationer.</span><span class="sxs-lookup"><span data-stu-id="c58b3-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="c58b3-116">Derfor skal oplysninger om basiskostpris betragtes som referenceoplysninger.</span><span class="sxs-lookup"><span data-stu-id="c58b3-116">Therefore, you should view the base cost information as reference information.</span></span>





