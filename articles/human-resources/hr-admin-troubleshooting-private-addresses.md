---
title: Adgang til privatadresser efter sikkerhedsrolle
description: I denne artikel beskrives det, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053317"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="8415c-103">Adgang til private adresser efter sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="8415c-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8415c-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="8415c-104">**Issue**</span></span>

<span data-ttu-id="8415c-105">Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.</span><span class="sxs-lookup"><span data-stu-id="8415c-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="8415c-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="8415c-106">**Resolution**</span></span>

<span data-ttu-id="8415c-107">For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="8415c-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="8415c-108">Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="8415c-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="8415c-109">Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="8415c-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="8415c-110">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8415c-110">Select **Save**.</span></span>

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]