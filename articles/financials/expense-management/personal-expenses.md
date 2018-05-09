---
title: Personlige udgifter i en udgiftsrapport
description: "Dette emne forklarer de to metoder til håndtering af en arbejders personlige udgifter i Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e21605dbe9d4f8182b868183e33a12e9b7e62422
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="f80b3-103">Personlige udgifter i en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="f80b3-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f80b3-104">Under forretningsrejser kan arbejdere undertiden kreditere personaleudgifter på deres firmaets kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f80b3-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="f80b3-105">Hvis du ikke definerer en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporter blive afbrudt, når arbejderne sender deres specificerede udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f80b3-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="f80b3-106">I Microsoft Dynamics 365 for Finance and Operations er der to metoder til håndtering af en arbejders personlige udgifter:</span><span class="sxs-lookup"><span data-stu-id="f80b3-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="f80b3-107">**Betalt af medarbejder** – Organisationen betaler ikke personlige udgifter, der figurerer på firmaets kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f80b3-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="f80b3-108">Den opretter i stedet en rapport, der viser de personlige udgifter sammen med de firmaudgifter, der blev krediteret på firmaets kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f80b3-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="f80b3-109">**Betalt af firma** – Organisationen betaler hele fakturaen, der er betalt med firmaets kreditkort, og debiterer derefter arbejderens konto for de personlige udgifter.</span><span class="sxs-lookup"><span data-stu-id="f80b3-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="f80b3-110">Du kan vælge den metode, som organisationen bruger, på siden **Parametre for udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="f80b3-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

