---
title: Adgang til private adresser efter sikkerhedsrolle
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303687"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="bdc11-103">Adgang til private adresser efter sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="bdc11-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdc11-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="bdc11-104">**Issue**</span></span>

<span data-ttu-id="bdc11-105">Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.</span><span class="sxs-lookup"><span data-stu-id="bdc11-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="bdc11-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="bdc11-106">**Resolution**</span></span>

<span data-ttu-id="bdc11-107">For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="bdc11-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="bdc11-108">Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="bdc11-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="bdc11-109">Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="bdc11-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="bdc11-110">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="bdc11-110">Select **Save**.</span></span>

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
