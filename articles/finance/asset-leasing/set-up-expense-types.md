---
title: Konfigurere udgiftstyper
description: Dette emne beskriver, hvordan du konfigurerer udgiftstyper i Aktivleasing.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880978"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="56b99-103">Konfigurere udgiftstyper</span><span class="sxs-lookup"><span data-stu-id="56b99-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56b99-104">Dette emne beskriver, hvordan du konfigurerer udgiftstyper i Aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="56b99-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="56b99-105">Omkostninger, der ikke er repræsenteret af betalingsplanen, kaldes *udgiftsomkostninger*.</span><span class="sxs-lookup"><span data-stu-id="56b99-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="56b99-106">Eksempler på disse omkostninger omfatter ejendomsskatter, omkostninger til fælles områdevedligeholdelse og forsikringsudgifter.</span><span class="sxs-lookup"><span data-stu-id="56b99-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="56b99-107">Tilføje en administrativ udgiftstype</span><span class="sxs-lookup"><span data-stu-id="56b99-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="56b99-108">Gå til **Aktivleasing \> Konfiguration \> Udgiftstyper**.</span><span class="sxs-lookup"><span data-stu-id="56b99-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="56b99-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="56b99-109">Select **New**.</span></span>
3. <span data-ttu-id="56b99-110">Angiv den nye udgiftstype og en beskrivelse i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="56b99-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="56b99-111">Tildele konti til administrative omkostninger</span><span class="sxs-lookup"><span data-stu-id="56b99-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="56b99-112">Derefter skal du knytte konti til udgiftstyperne.</span><span class="sxs-lookup"><span data-stu-id="56b99-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="56b99-113">Disse konti debiteres, når posterne i udgiftsplanen bogføres.</span><span class="sxs-lookup"><span data-stu-id="56b99-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="56b99-114">Modkontoen er angivet i **Betalingsplanlinjerne for udligningsomkostninger** på de enkelte leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="56b99-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="56b99-115">Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.</span><span class="sxs-lookup"><span data-stu-id="56b99-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="56b99-116">Vælg udgiftstypen i feltet **Konti** i **Udligningsomkostninger** i feltet **Udgiftstype**.</span><span class="sxs-lookup"><span data-stu-id="56b99-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="56b99-117">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="56b99-117">Select **Add**.</span></span>
4. <span data-ttu-id="56b99-118">I feltet **Kartotekstype** skal du vælge den type, der skal knyttes til de administrative omkostninger.</span><span class="sxs-lookup"><span data-stu-id="56b99-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56b99-119">Flere forskellige kartotekstyper kan knyttes til samme udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="56b99-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="56b99-120">I feltet **Kontokode** skal du angive, hvilke rettigheder kartoteket skal udlignes med:</span><span class="sxs-lookup"><span data-stu-id="56b99-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="56b99-121">**Alle** – Tildel kartoteket til alle leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="56b99-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="56b99-122">**Gruppe** – Tildel kartoteket til en bestemt leasinggruppe.</span><span class="sxs-lookup"><span data-stu-id="56b99-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="56b99-123">**Tabel** – Tildel kartoteket til specifikke leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="56b99-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="56b99-124">Hvis du har valgt **Gruppe** eller **Tabel** i feltet **Kontokode**, skal du vælge et kontonummer eller gruppenummer i feltet **Konto-/gruppenummer**.</span><span class="sxs-lookup"><span data-stu-id="56b99-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="56b99-125">I felterne skal du vælge hovedkontoen for finanskonto og hovedkonto for driftsleasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="56b99-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="56b99-126">Når du har gennemført disse trin, kan du tilføje udgifter via linjerne **Betalingsplan for udførelsesomkostninger** på siden **leasingaftaledetaljer** for den valgte leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="56b99-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="56b99-127">Du kan også tilføje udgifter, når du opretter en ny leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="56b99-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
