---
title: Adgang til private adresser efter sikkerhedsrolle
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "859476"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="263c4-103">Adgang til private adresser efter sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="263c4-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="263c4-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="263c4-104">**Issue**</span></span>

<span data-ttu-id="263c4-105">Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.</span><span class="sxs-lookup"><span data-stu-id="263c4-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="263c4-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="263c4-106">**Resolution**</span></span>

<span data-ttu-id="263c4-107">For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="263c4-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="263c4-108">Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="263c4-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="263c4-109">Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="263c4-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="263c4-110">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="263c4-110">Select **Save**.</span></span>

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
