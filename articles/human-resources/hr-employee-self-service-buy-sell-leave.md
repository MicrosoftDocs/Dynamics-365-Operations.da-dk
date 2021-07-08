---
title: Køb og sælg orlov
description: I Dynamics 365 Human Resources kan du sende anmodninger om køb og salg af orlov på grundlag af de politikker for køb og salg af orlov, der er konfigureret af din virksomhed.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271473"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="ac617-103">Køb og sælg orlov</span><span class="sxs-lookup"><span data-stu-id="ac617-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ac617-104">I Dynamics 365 Human Resources kan du sende anmodninger om køb og salg af orlov på grundlag af de politikker for køb og salg af orlov, der er konfigureret af din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="ac617-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="ac617-105">Anmod om at købe orlov</span><span class="sxs-lookup"><span data-stu-id="ac617-105">Request to buy leave</span></span>

1. <span data-ttu-id="ac617-106">I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Anmodning om at købe orlov** i feltet **Fritidssaldi**.</span><span class="sxs-lookup"><span data-stu-id="ac617-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="ac617-107">Tilføj en **Orlovstype**, og angiv et **Antal** for det antal orlovsdage, du vil købe.</span><span class="sxs-lookup"><span data-stu-id="ac617-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="ac617-108">Vælg **Send**, når du er klar til at sende din anmodning.</span><span class="sxs-lookup"><span data-stu-id="ac617-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="ac617-109">Dine saldi opdateres enten automatisk eller gennem en godkendelsesproces, inden de opdateres.</span><span class="sxs-lookup"><span data-stu-id="ac617-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="ac617-110">Dette afhænger af, hvordan købspolitikken er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="ac617-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="ac617-111">Anmode om at sælge orlov</span><span class="sxs-lookup"><span data-stu-id="ac617-111">Request to sell leave</span></span>

1. <span data-ttu-id="ac617-112">I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Anmodning om at sælge orlov** i feltet **Fritidssaldi**.</span><span class="sxs-lookup"><span data-stu-id="ac617-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="ac617-113">Tilføj en **Orlovstype**, og angiv et **Antal** for det antal orlovsdage, du vil sælge.</span><span class="sxs-lookup"><span data-stu-id="ac617-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="ac617-114">Vælg **Send**, når du er klar til at sende din anmodning.</span><span class="sxs-lookup"><span data-stu-id="ac617-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="ac617-115">Dine saldi opdateres enten automatisk eller gennem en godkendelsesproces, inden de opdateres.</span><span class="sxs-lookup"><span data-stu-id="ac617-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="ac617-116">Dette afhænger af, hvordan købspolitikken er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="ac617-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="ac617-117">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="ac617-117">Troubleshooting</span></span> 

<span data-ttu-id="ac617-118">Hvis en arbejdsgang for anmodning om køb eller salg af orlov mislykkes, kan brugere med rettigheden **EssLeaveBuySellRequestApprover** gennemse meddelelsesloggen for alle anmodninger om køb og salg af orlov.</span><span class="sxs-lookup"><span data-stu-id="ac617-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="ac617-119">Hvis du vil gøre det, skal du gå til **Orlov og fravær > Link > Anmodninger om køb og salg af orlov > Meddelelseslog** (øverst til venstre).</span><span class="sxs-lookup"><span data-stu-id="ac617-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="ac617-120">**Meddelelsesloggen** viser brugerne, hvordan transaktionerne blev behandlet, og den tilknyttede arbejdsgangshistorik.</span><span class="sxs-lookup"><span data-stu-id="ac617-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="ac617-121">Se også</span><span class="sxs-lookup"><span data-stu-id="ac617-121">See also</span></span>

[<span data-ttu-id="ac617-122">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="ac617-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="ac617-123">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="ac617-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
