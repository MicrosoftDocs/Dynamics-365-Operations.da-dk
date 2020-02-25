---
title: Adgang til privatadresser efter sikkerhedsrolle
description: I denne artikel beskrives det, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008510"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="b60d1-103">Adgang til private adresser efter sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="b60d1-103">Access to private addresses by security role</span></span>

<span data-ttu-id="b60d1-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="b60d1-104">**Issue**</span></span>

<span data-ttu-id="b60d1-105">Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.</span><span class="sxs-lookup"><span data-stu-id="b60d1-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="b60d1-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="b60d1-106">**Resolution**</span></span>

<span data-ttu-id="b60d1-107">For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="b60d1-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="b60d1-108">Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="b60d1-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="b60d1-109">Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="b60d1-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="b60d1-110">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b60d1-110">Select **Save**.</span></span>

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
