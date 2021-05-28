---
title: Lokationsprofil tillader ikke negativt lager, men negativ disponeret lagerbeholdning tillades
description: Indstillingen Tillad negativ lagerbeholdning for lokationsprofilen er indstillet til Nej, men systemet tillader stadig negativ lagerbeholdning.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026369"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="cc8ea-103">Lokationsprofil tillader ikke negativt lager, men negativ disponeret lagerbeholdning tillades</span><span class="sxs-lookup"><span data-stu-id="cc8ea-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="cc8ea-104">KB-nummer: 4613622</span><span class="sxs-lookup"><span data-stu-id="cc8ea-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="cc8ea-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="cc8ea-105">Symptoms</span></span>

<span data-ttu-id="cc8ea-106">Indstillingen **Tillad negativ lagerbeholdning** for lokationsprofilen er indstillet til *Nej*, men systemet tillader stadig negativ lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="cc8ea-107">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="cc8ea-107">Example scenario</span></span>

<span data-ttu-id="cc8ea-108">For offentligt regulerede transaktioner skal systemet kunne registrere negativt lager for at kunne registrere tab.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="cc8ea-109">Du vil have, at en vare skal kunne vise negativ lagerbeholdning, men kun på angivne lokationer, f.eks. tankstationer.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="cc8ea-110">Hvis varemodelgruppen tillader negativt lager, opdager du dog, at det er ligegyldigt, om lokationen er indstillet til at tillade negativt lager.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="cc8ea-111">Hvis varen er konfigureret, så negativt lager ikke er tilladt, er det ligegyldigt, hvordan lokationsprofilen er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="cc8ea-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="cc8ea-112">Resolution</span></span>

<span data-ttu-id="cc8ea-113">Indstillingen **Tillad negativ lagerbeholdning** fra lokationsprofilen gælder kun for lagerprocesser som f.eks. plukning.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="cc8ea-114">Varemodelgrupper, der er indstillet til at tillade negativt lager, påvirker dog alle processer fra modulerne Lagerstyring og Lokationsstyring, og lokalitetsprofilen tilsidesætter ikke indstillingen.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="cc8ea-115">Du kan styre, om et lagersted må have negativt lager.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="cc8ea-116">Indstil varemodelgrupperne til at forbyde negativt fysisk lager, og indstil kun det relevante lagersted til at tillade negativt lager.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
