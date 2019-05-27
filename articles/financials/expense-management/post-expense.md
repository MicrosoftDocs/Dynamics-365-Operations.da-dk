---
title: Bogføre en udgiftsrapport
description: Dette emne forklarer, hvordan du bogfører en udgiftsrapport i finansmodulet.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1252825848aedcdaf633c04edddddca7dd09d774
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570661"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="fce95-103">Bogføre en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="fce95-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fce95-104">Når en udgiftsrapport er godkendt og overført til finanskladden, kan den bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="fce95-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="fce95-105">Når du bogfører en udgiftsrapport, identificeres alle udgifter, der er berettiget til momsrefusion.</span><span class="sxs-lookup"><span data-stu-id="fce95-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="fce95-106">Ansvaret for kontrol og opkrævning af momsbetalinger ligger hos den medarbejder, der er ansvarlig for kontrol af udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="fce95-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="fce95-107">Hvis udgifter i en udgiftsrapport opkræves et andet firma end det firma, som medarbejderen er ansat hos, skal du kontrollere det firma, der har betalingen for disse udgifter til gode, og det firma, der skal betale udgifterne.</span><span class="sxs-lookup"><span data-stu-id="fce95-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="fce95-108">Den medarbejder, der sendte en udgiftsrapport, arbejder f.eks. for firmaet DAT, men har opkrævet en udgift af firmaet DIR.</span><span class="sxs-lookup"><span data-stu-id="fce95-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="fce95-109">I så fald er DAT det firma, som har betaling for udgiften til gode, og DIR er det firma, der skal betale den.</span><span class="sxs-lookup"><span data-stu-id="fce95-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="fce95-110">Når du har kontrolleret kladdelinjerne, kan du bogføre udgiftslinjerne i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="fce95-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="fce95-111">Du bogfører en udgiftsrapport på siden **Godkendte udgiftsrapporter** ved at vælge udgiftsrapporten og derefter vælge **Bogfør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fce95-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="fce95-112">Du kan også bogføre alle udgiftsrapporter på listen på samme tid.</span><span class="sxs-lookup"><span data-stu-id="fce95-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="fce95-113">Vælg alle udgiftsrapporterne, og vælg derefter **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="fce95-113">Select all the expense reports, and then select **Post**.</span></span>
