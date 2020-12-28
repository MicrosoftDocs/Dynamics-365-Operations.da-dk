---
title: Tillæg i transportstyring
description: I dette emne forklares det, hvordan transportgenererede gebyrer skal knyttes til en gebyrkode.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425098"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="61a27-103">Tillæg i transportstyring</span><span class="sxs-lookup"><span data-stu-id="61a27-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61a27-104">Som med alle tillæg skal transportgenererede gebyrer knyttes til en gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="61a27-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="61a27-105">Ellers føjes de ikke tilbage til ordren som et tillæg.</span><span class="sxs-lookup"><span data-stu-id="61a27-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="61a27-106">**Gebyrkode** bestemmer, hvordan tillægget beregnes i forhold til ordren og ordrelinjen, hvor det tilføjes.</span><span class="sxs-lookup"><span data-stu-id="61a27-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="61a27-107">Gå til **Transportstyring > Opsætning > Vurdering > Tillæg** for at definere de kvalifikationskriterier, der bestemmer, hvornår en bestemt **Gebyrkode** anvendes på et gebyr.</span><span class="sxs-lookup"><span data-stu-id="61a27-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="61a27-108">Der skal være mindst én opsætning for hver relevante **Gebyrmodul**-indstilling (*Debitor* og *Kreditor*), hvor **Tillægstype** angives til *Ingen*.</span><span class="sxs-lookup"><span data-stu-id="61a27-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="61a27-109">Hvis dette mangler, føjes tillægget *ikke* til ordren.</span><span class="sxs-lookup"><span data-stu-id="61a27-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
