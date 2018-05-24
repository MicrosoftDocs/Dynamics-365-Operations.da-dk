---
title: "Reducere dagene på abonnementsgebyrer"
description: "Hvis du vil reducere antallet af dage i et eksisterende abonnementsgebyr, kan du oprette en ny transaktion, hvor du fjerner den periode, der ikke længere skal være del af intervallet for abonnementsgebyret."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="da58f-103">Reducere dagene på abonnementsgebyrer</span><span class="sxs-lookup"><span data-stu-id="da58f-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="da58f-104">Hvis du vil reducere antallet af dage i et eksisterende abonnementsgebyr, kan du oprette en ny transaktion, hvor du fjerner den periode, der ikke længere skal være del af intervallet for abonnementsgebyret.</span><span class="sxs-lookup"><span data-stu-id="da58f-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="da58f-105">Reducere dagene i et abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="da58f-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="da58f-106">Klik på **Servicestyring** \> **Almindelige** \> **Serviceabonnementer** \> **Alle serviceabonnementer**.</span><span class="sxs-lookup"><span data-stu-id="da58f-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="da58f-107">Vælg serviceabonnementet, og klik på **Abonnementsgebyrer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="da58f-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="da58f-108">I feltet **Abonnementstype** skal du vælge **Reduktionsdage**.</span><span class="sxs-lookup"><span data-stu-id="da58f-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="da58f-109">Angiv datointervallet for det abonnementsgebyr, du vil fjerne fra abonnementsgebyrperioden, i feltet **Fra dato** og **Til dato**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="da58f-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="da58f-110">Hvis du vil have vist den transaktion, der er oprettet, skal du i formularen **Abonnement** klikke på **Gebyrtransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="da58f-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="da58f-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="da58f-111">Example</span></span>

<span data-ttu-id="da58f-112">Hvis en periode for en abonnementstransaktion løber fra 1. til 31. januar, og du vil reducere perioden med 10 dage, skal du oprette en ny transaktion, hvor reduktionsperioden er 1. til 10. januar.</span><span class="sxs-lookup"><span data-stu-id="da58f-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="da58f-113">(Reduktionsperioden kunne også være 5. til 15. januar).</span><span class="sxs-lookup"><span data-stu-id="da58f-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="da58f-114">Hvis **Fra dato** i reduktionsperioden desuden er 21. januar (31 minus 10), kan du indstille **Til dato** til en vilkårlig dato efter 31. januar, så fjernes der 10 dage fra gebyrtransaktionsperioden.</span><span class="sxs-lookup"><span data-stu-id="da58f-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="da58f-115">Se også</span><span class="sxs-lookup"><span data-stu-id="da58f-115">See also</span></span>

[<span data-ttu-id="da58f-116">Eksempel på reduktionsdage</span><span class="sxs-lookup"><span data-stu-id="da58f-116">Reduction days example</span></span>](reduction-days-example.md)

  



