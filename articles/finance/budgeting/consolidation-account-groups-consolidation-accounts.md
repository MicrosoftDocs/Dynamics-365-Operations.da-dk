---
title: Koncernkontogrupper og yderligere koncernkonti
description: Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af koncernkonti og om, hvordan de bruges i Microsoft Dynamics 365 Finance.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c1a819505343eaee93c7bf67b1364e61ad5c9c68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827348"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="48c7f-103">Koncernkontogrupper og yderligere koncernkonti</span><span class="sxs-lookup"><span data-stu-id="48c7f-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48c7f-104">Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af koncernkonti og om, hvordan de bruges i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="48c7f-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="48c7f-105">Koncernkontogrupper</span><span class="sxs-lookup"><span data-stu-id="48c7f-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="48c7f-106">Med koncernkontogrupper kan du oprette grupper af konti, du vil bruge til at konsolidere data.</span><span class="sxs-lookup"><span data-stu-id="48c7f-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="48c7f-107">Oftest repræsenterer en koncernkontogruppe en lovpligtig kontoplan eller knytter konti til en gruppe, der er defineret af virksomhedens hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="48c7f-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="48c7f-108">Du kan finde koncernkontogrupper i **Opsætning**-området af modulet **Konsolideringer**.</span><span class="sxs-lookup"><span data-stu-id="48c7f-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="48c7f-109">Når du tilføjer en ny gruppe, angiver du en entydig identifikator for kontogruppen og et navn.</span><span class="sxs-lookup"><span data-stu-id="48c7f-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="48c7f-110">Flere koncernkonti</span><span class="sxs-lookup"><span data-stu-id="48c7f-110">Additional consolidation accounts</span></span>
<span data-ttu-id="48c7f-111">Med flere koncernkonti kan du tildele en konto fra en eksisterende kontoplan til en koncernkontogruppe.</span><span class="sxs-lookup"><span data-stu-id="48c7f-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="48c7f-112">Du kan derefter angive en værdi og et navn til koncernkontoen.</span><span class="sxs-lookup"><span data-stu-id="48c7f-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="48c7f-113">Du kan finde flere koncernkonti i **Opsætning**-området af modulet **Konsolideringer**.</span><span class="sxs-lookup"><span data-stu-id="48c7f-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="48c7f-114">Når du opretter en ny koncernkonto, skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="48c7f-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="48c7f-115">**Hovedkonto** – Dette felt er et opslag, der viser alle de hovedkonti, der er baseret på de kontoplaner, som du valgte på siden.</span><span class="sxs-lookup"><span data-stu-id="48c7f-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="48c7f-116">Når du vælger en konto, angives navnet automatisk i feltet **Hovedkontonavn**.</span><span class="sxs-lookup"><span data-stu-id="48c7f-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="48c7f-117">**Koncernkontogruppe** – Brug dette felt til at angive den gruppe, kontoen skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="48c7f-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="48c7f-118">Hvis du konsoliderer på to forskellige måder, skal du føje den samme konto til alle fire koncernkontogrupper.</span><span class="sxs-lookup"><span data-stu-id="48c7f-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="48c7f-119">**Koncernkonto** – Angiv værdien af koncernkontoen.</span><span class="sxs-lookup"><span data-stu-id="48c7f-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="48c7f-120">Denne værdi behøver ikke være fra en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="48c7f-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="48c7f-121">Det kan være enhver værdi, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="48c7f-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="48c7f-122">**Navn på koncernkonto** – Angiv navnet på kontoen, som det skal vises i forespørgsler og rapporter.</span><span class="sxs-lookup"><span data-stu-id="48c7f-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="48c7f-123">**SAT niveau** – Dette felt bruges til at rapportere kontoudtog til de mexicanske myndigheder.</span><span class="sxs-lookup"><span data-stu-id="48c7f-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="48c7f-124">Når du har oprettet dine koncernkontogrupper og ekstra koncernkonti, kan du vælge gruppen under onlinekonsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="48c7f-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="48c7f-125">Du kan finde flere oplysninger under [Oprette koncerngrupper og supplerende koncernkonti](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="48c7f-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]