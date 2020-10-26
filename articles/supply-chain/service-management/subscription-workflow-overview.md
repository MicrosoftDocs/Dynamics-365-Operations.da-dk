---
title: Oversigt over arbejdsgang til abonnement
description: Dette emne giver en oversigt over arbejdsgang for abonnement.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f023ddd8d6f9350702f687763b53b057baa9aed8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985809"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="59635-103">Oversigt over arbejdsgang til abonnement</span><span class="sxs-lookup"><span data-stu-id="59635-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="59635-104">Du er abonnementsadministrator for et lysfirma, og dit firma tilbyder abonnementer på vedligeholdelse af lysinstallationer.</span><span class="sxs-lookup"><span data-stu-id="59635-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="59635-105">En kunde kontakter firmaet for at købe et årligt abonnement på vedligeholdelse af lysinstallationer.</span><span class="sxs-lookup"><span data-stu-id="59635-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="59635-106">Definere abonnementer</span><span class="sxs-lookup"><span data-stu-id="59635-106">Setting up subscriptions</span></span>

<span data-ttu-id="59635-107">Når du skal definere et abonnement, skal du først oprette en abonnementsgruppe til den nye serviceaftale eller kontrollere, at der findes en abonnementsgruppe.</span><span class="sxs-lookup"><span data-stu-id="59635-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="59635-108">Hvis der findes en abonnementsgruppe, skal den være angivet til at fakturere kunden årligt og til at tillade periodisering af omsætning hver måned i året.</span><span class="sxs-lookup"><span data-stu-id="59635-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="59635-109">Du kan finde flere oplysninger om oprettelse af abonnementer under [Konfigurere abonnementsgrupper](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="59635-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="59635-110">Når abonnementsgruppen er oprettet, kan du oprette abonnementet.</span><span class="sxs-lookup"><span data-stu-id="59635-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="59635-111">Du kan finde flere oplysninger om oprettelse af serviceabonnementer under [Oprette serviceabonnementer fra en abonnementsgruppe](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="59635-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="59635-112">Oprette og ændre abonnementstransaktioner</span><span class="sxs-lookup"><span data-stu-id="59635-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="59635-113">Når du har oprettet abonnementet, skal du oprette abonnementsgebyrtransaktionen for den første faktureringstermin, som er ét år.</span><span class="sxs-lookup"><span data-stu-id="59635-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="59635-114">Posteringerne er af typen **Regulær**.</span><span class="sxs-lookup"><span data-stu-id="59635-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="59635-115">Du kan derfor kun oprette abonnementstransaktioner, hvis fra-datoen og til-datoen svarer til perioder, der tidligere er oprettet i formularen **Periodetyper**.</span><span class="sxs-lookup"><span data-stu-id="59635-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="59635-116">Du kan finde flere oplysninger om gebyrposteringer under [Oprette posteringer for abonnementsgebyr](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="59635-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="59635-117">Når du har defineret transaktionen for kunden, kommer du i tanke om, at de har forhandlet sig til en rabat på 10 % på alle listepriser på servicetilbud.</span><span class="sxs-lookup"><span data-stu-id="59635-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="59635-118">Du skal derfor reducere prisen på det transaktionsgebyr, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="59635-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="59635-119">Senere på dagen ringer din kundens kontaktperson til dig for at sige, at selvom de stadig vil have serviceaftalen til lysinstallationen, planlægger de at introducere en ny lysinstallation senere på året.</span><span class="sxs-lookup"><span data-stu-id="59635-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="59635-120">De har derfor kun brug for vedligeholdelsesdækning frem til oktober 2013.</span><span class="sxs-lookup"><span data-stu-id="59635-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="59635-121">For at reducere antallet af måneder i kundens abonnement opretter du en ny abonnementsgebyrtransaktion af typen **Reduktionsdage**.</span><span class="sxs-lookup"><span data-stu-id="59635-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="59635-122">Du kan finde flere oplysninger om reducering af dage under [Reducere dagene på abonnementsgebyrer](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="59635-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="59635-123">Fakturere og periodisere abonnementstransaktioner</span><span class="sxs-lookup"><span data-stu-id="59635-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="59635-124">Du er nu færdig med at definere abonnementer og er klar til at fakturere kunden for det.</span><span class="sxs-lookup"><span data-stu-id="59635-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="59635-125">Du kan finde flere oplysninger om fakturering af abonnementer under [Fakturere abonnementstransaktioner](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="59635-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="59635-126">To dag senere ringer kunden for at sige, at abonnementet skal faktureres i amerikanske dollars og ikke i euro.</span><span class="sxs-lookup"><span data-stu-id="59635-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="59635-127">Du opretter derfor en kreditnota, og du opretter også en ny abonnementstransaktion i den rigtige valuta.</span><span class="sxs-lookup"><span data-stu-id="59635-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="59635-128">Du kan finde flere oplysninger om kreditering af abonnementstransaktioner i [Kreditere abonnementstransaktioner](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="59635-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="59635-129">I slutningen af hver måned kan du periodisere en måneds omsætning fra kundens abonnementer til driftskontoen og IGVA-konti.</span><span class="sxs-lookup"><span data-stu-id="59635-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="59635-130">Du kan finde flere oplysninger om periodisering af omsætning for abonnementer i [Periodisere abonnementsindtægt](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="59635-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


