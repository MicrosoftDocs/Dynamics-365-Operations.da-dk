---
title: Bogfør kladdeposteringer for transaktionsjusteringen i aktivleasing
description: I dette emne beskrives den funktion, du kan bruge til at overføre en leasingaftales portefølje til de nye regnskabsstandarder for leasing, Accounting Standards Codification Topic 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969547"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="55ff6-103">Bogfør kladdeposteringer for transaktionsjusteringen i aktivleasing</span><span class="sxs-lookup"><span data-stu-id="55ff6-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55ff6-104">I dette emne beskrives de funktioner, du kan bruge til at overføre en leasingaftales oversigt til de nye kontostandarder for leasing: Accounting Standards Codification Topic 842 (ASC 842), som er standarden i Generally Accepted Accounting Principles i USA (US GAAP) og International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="55ff6-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="55ff6-105">Du kan finde flere oplysninger om, hvordan du konfigurerer et kartotek til overgangen til de nye standarder, i [Konfigurere leasingkartoteker](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="55ff6-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="55ff6-106">Når du opretter en kladdepostering for en overgangsregulering, genereres der en kladdepost.</span><span class="sxs-lookup"><span data-stu-id="55ff6-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="55ff6-107">Denne post afspejler balancevirkningen for registrering af leasingaftaler under de nye standarder på den pågældende dato.</span><span class="sxs-lookup"><span data-stu-id="55ff6-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="55ff6-108">Den relevante aktivkonto debiteres for dette beløb på denne dato, og passivkontoen krediteres.</span><span class="sxs-lookup"><span data-stu-id="55ff6-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="55ff6-109">Differencen er enten debiteret eller krediteret overførte tillæg.</span><span class="sxs-lookup"><span data-stu-id="55ff6-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="55ff6-110">Hvis du vil bogføre en overgangsjustering i overensstemmelse med de nye regnskabsstandarder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="55ff6-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="55ff6-111">På siden **Leasingoversigt** skal du vælge en leasingaftale, og derefter **Kartoteker**.</span><span class="sxs-lookup"><span data-stu-id="55ff6-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="55ff6-112">Vælg **Betalingsplan** i kartoteket.</span><span class="sxs-lookup"><span data-stu-id="55ff6-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="55ff6-113">Vælg **Bekræft** i dialogboksen **Betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="55ff6-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="55ff6-114">Luk derefter dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="55ff6-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="55ff6-115">Vælg **Overgangsjustering**.</span><span class="sxs-lookup"><span data-stu-id="55ff6-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="55ff6-116">Der kan kun oprettes en overgangsjustering for leasingkartoteker, der er tildelt et kartotek, hvor feltet **Overgangskartoteket** er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="55ff6-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="55ff6-117">Hvis værdien i feltet **Leasingaftale påbegyndes** er senere end overførselsdatoen, opdateres værdien i feltet **Overgangsjustering** ikke.</span><span class="sxs-lookup"><span data-stu-id="55ff6-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="55ff6-118">Hvis du vil se kladdeposten, skal du vælge **Aktivleasingkladde**.</span><span class="sxs-lookup"><span data-stu-id="55ff6-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="55ff6-119">Vælg den nye kladde, og vælg derefter **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="55ff6-119">Select the new journal, and then select **Post**.</span></span>
