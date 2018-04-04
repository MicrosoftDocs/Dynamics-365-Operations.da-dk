---
title: "Engangsleverandører i den offentlige sektor"
description: Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 19801
ms.assetid: 403857a3-bebb-4ff7-b1b5-c88f41fc18ae
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f4ab83517c91fa3d31c8af572ac9acc583c52b9f
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="one-time-vendors-in-the-public-sector"></a><span data-ttu-id="0e8ca-103">Engangsleverandører i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="0e8ca-103">One-time vendors in the public sector</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0e8ca-104">Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-104">This article provides information about how to create a one-time vendor and invoice, and how to import and create multiple one-time vendors and invoices.</span></span> 

<span data-ttu-id="0e8ca-105">Der kan være situationer, hvor du er nødt til at oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssig relation til.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-105">Occasionally, you might have to create an invoice for a new vendor that you have no regular relationship with.</span></span> <span data-ttu-id="0e8ca-106">Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du i Microsoft Dynamics 365 for Finance and Operations hurtigt oprette en faktura, samtidig med at du opretter en post for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-106">In Microsoft Dynamics 365 for Finance and Operations, if approval or a contract in the form of a purchase order isn't required, you can quickly create an invoice at the same time that you create a record for the vendor.</span></span> <span data-ttu-id="0e8ca-107">Det kunne f.eks. være, at du er nødt til at betale referencer eller refusion, men der ikke findes en overordnet kreditorpost.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-107">For example, you have to pay referees or refunds, but a master vendor record doesn't exist.</span></span> <span data-ttu-id="0e8ca-108">Der kan også være situationer, hvor du er nødt til at oprette flere fakturaer for nye kreditorer, som du ikke har nogen regelmæssig relation til.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-108">Alternatively, you might have to create multiple invoices for new vendors that you have no regular relationship with.</span></span> <span data-ttu-id="0e8ca-109">Hvis der hverken kræves godkendelse eller en indkøbsordre, kan du hurtigt oprette fakturaer, samtidig med at du opretter poster for leverandørerne.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-109">If neither approval nor a purchase order is required, you can quickly create invoices at the same time that you create records for the vendors.</span></span> <span data-ttu-id="0e8ca-110">Det kan f.eks. være, at du vil understøtte kreditorbetalinger af deltagelse i jury, registreringsbetalinger og refusioner til kreditorer eller andre betalinger, men der ikke findes hovedkreditorposter.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-110">For example, you want to support vendor payments for jury duty, registration payments, and customer refunds or other payments, but master vendor records don't exist.</span></span> <span data-ttu-id="0e8ca-111">Du kan finde flere oplysninger under [Planlægning for engangsleverandører i den offentlige sektor.](plan-one-time-vendors-public-sector.md)</span><span class="sxs-lookup"><span data-stu-id="0e8ca-111">For more information, see [Planning for one-time vendors in the public-sector](plan-one-time-vendors-public-sector.md).</span></span>

## <a name="how-do-i-create-a-onetime-vendor-and-invoice"></a><span data-ttu-id="0e8ca-112">Hvordan opretter jeg en engangskreditor og -faktura?</span><span class="sxs-lookup"><span data-stu-id="0e8ca-112">How do I create a onetime vendor and invoice?</span></span>
<span data-ttu-id="0e8ca-113">Kreditorposten bruger værdier fra standardengangskreditorkontoen, medmindre der er indtastet nye værdier.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-113">The vendor record uses values from the default one-time vendor account, unless new values are entered.</span></span> <span data-ttu-id="0e8ca-114">Der er angivet en konto i afsnittet **Generelt** på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-114">That account is specified in the **General** section of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="0e8ca-115">Du kan få vist kontooplysningerne på siden **Alle kreditorer** og derefter klikke på kreditorkontonummeret for standardengangskreditoren.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-115">To view the account details, on the **All vendors** page, click the vendor account number of the default one-time vendor.</span></span>

## <a name="how-do-i-import-and-create-multiple-onetime-vendors-and-invoices"></a><span data-ttu-id="0e8ca-116">Hvordan importerer og opretter jeg flere engangskreditorer og fakturaer?</span><span class="sxs-lookup"><span data-stu-id="0e8ca-116">How do I import and create multiple onetime vendors and invoices?</span></span>
<span data-ttu-id="0e8ca-117">Hvis du vil oprette flere engangskreditorer og fakturaer, skal du først oprette en fil, der indeholder oplysninger om kreditoren og fakturaen, og derefter importere filen til en midlertidig tabel i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-117">To create multiple one-time vendors and invoices, you first create a file that contains the vendor and invoice information, and then import the file into a staging table in Finance and Operations.</span></span> <span data-ttu-id="0e8ca-118">Derefter skal du behandle den importerede fil og generere fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="0e8ca-118">You then process the imported file and generate the invoices.</span></span> <span data-ttu-id="0e8ca-119">Du kan se flere oplysninger om, hvordan du opretter filen i [Planlægning for engangsleverandører i den offentlige sektor](plan-one-time-vendors-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0e8ca-119">For information about how to create the file, see [Planning for one-time vendors in the public sector](plan-one-time-vendors-public-sector.md).</span></span>  




