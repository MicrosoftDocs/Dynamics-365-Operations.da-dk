---
title: "Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog"
description: "I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b8ceee7486cae9ec0ff7dfedc35909e2f01d0616
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a><span data-ttu-id="058ec-103">Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog</span><span class="sxs-lookup"><span data-stu-id="058ec-103">Financial dimensions and main accounts in a right-to-left language</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="058ec-104">I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="058ec-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="058ec-105">Økonomiske dimensioner og hovedkonti er centrale komponenter i planlægningsfasen for en implementering.</span><span class="sxs-lookup"><span data-stu-id="058ec-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="058ec-106">Når økonomiske dimensioner og hovedkonti oprettes i systemet, bruges de på siderne **Konfigurer kontostrukturer**, **Avancerede regelstrukturer** og **Konfiguration af økonomisk dimension til integrering af programmer**.</span><span class="sxs-lookup"><span data-stu-id="058ec-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="058ec-107">Den rækkefølge, der er defineret på siderne, bruges til dataindtastning og forbrug i systemet.</span><span class="sxs-lookup"><span data-stu-id="058ec-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="058ec-108">Nogle steder i systemet vises de økonomiske dimensioner og hovedkonti i separate felter.</span><span class="sxs-lookup"><span data-stu-id="058ec-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="058ec-109">Men på andre steder, såsom kladder, økonomiske dimensioner og hovedkonti, vises de som en enkelt streng.</span><span class="sxs-lookup"><span data-stu-id="058ec-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="058ec-110">Bedste fremgangsmåder til at oprette økonomiske dimensioner og hovedkonti i et højre mod venstre-system</span><span class="sxs-lookup"><span data-stu-id="058ec-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="058ec-111">Når du vælger afgrænsningstegn til kontoplaner, kan du vælge en af indstillingerne for dobbelt afgrænser: dobbelt bindestreg (--), dobbeltstreg (||) eller dobbelt punktum (..) eller dobbelt et understregningstegn (\_\_).</span><span class="sxs-lookup"><span data-stu-id="058ec-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="058ec-112">Når du opretter en økonomisk dimension og hovedkontoværdier, skal du kun bruge tal og tegn fra højre mod venstre-sprog.</span><span class="sxs-lookup"><span data-stu-id="058ec-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="058ec-113">Undgå at bruge den valgte kontoplans afgrænser i den økonomiske dimension og hovedkontoværdier.</span><span class="sxs-lookup"><span data-stu-id="058ec-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="058ec-114">Ved at følge disse anbefalinger kan du bedre sikre ensartet repræsentation af den brugerdefinerede rækkefølge i hele systemet.</span><span class="sxs-lookup"><span data-stu-id="058ec-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




