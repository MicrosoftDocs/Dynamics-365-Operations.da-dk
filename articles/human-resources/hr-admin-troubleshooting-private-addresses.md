---
title: Adgang til privatadresser efter sikkerhedsrolle
description: I denne artikel beskrives det, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 6598094e7877a30c35e1b03794f82c8a4ec001a7
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111901"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="f7dfe-103">Adgang til private adresser efter sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="f7dfe-103">Access to private addresses by security role</span></span>

<span data-ttu-id="f7dfe-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="f7dfe-104">**Issue**</span></span>

<span data-ttu-id="f7dfe-105">Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.</span><span class="sxs-lookup"><span data-stu-id="f7dfe-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="f7dfe-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="f7dfe-106">**Resolution**</span></span>

<span data-ttu-id="f7dfe-107">For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="f7dfe-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="f7dfe-108">Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="f7dfe-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="f7dfe-109">Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="f7dfe-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="f7dfe-110">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f7dfe-110">Select **Save**.</span></span>

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
