---
title: Tilknytte anlægsaktiv med en leasingaftale
description: I emnet forklares, hvordan et eksisterende anlægsaktiv knyttes til en ny leasingaftale.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881342"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="91629-103">Tilknytte anlægsaktiv med en leasingaftale</span><span class="sxs-lookup"><span data-stu-id="91629-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91629-104">I emnet forklares, hvordan et eksisterende anlægsaktiv knyttes til en ny leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="91629-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="91629-105">Når du knytter et anlægsaktiv til en rettighed, vil aktivets aktivværdi (ROU) ved første anerkendelse blive anskaffelsesomkostningen for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="91629-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="91629-106">Før du kan knytte et anlægsaktiv til en leasingaftale, skal du oprette en post for anlægsaktivet i anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="91629-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="91629-107">Derefter skal du på siden **Leasingoversigt** oprette en leasingaftale og knytte aktivet til den pågældende leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="91629-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="91629-108">Tilføj en leasignaftale ved at følge trinnene i [Tilføj eller Kopiér leasingaftaler](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="91629-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="91629-109">På siden **Tilføj leasingaftale** i feltet **Anlægsaktivnummer** skal du vælge det aktiv, der endnu ikke er anskaffet.</span><span class="sxs-lookup"><span data-stu-id="91629-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="91629-110">Vælg **Kartoteker**, og bekræft betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="91629-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="91629-111">Vælg **Første indregning**.</span><span class="sxs-lookup"><span data-stu-id="91629-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="91629-112">Vælg **Aktivleasingkladde**.</span><span class="sxs-lookup"><span data-stu-id="91629-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="91629-113">Postering af den oprindelige genkendelseskladde for leasingaftalen afskaffer anlægsaktivet for det beløb, der normalt debiteres på ROU aktivkontoen.</span><span class="sxs-lookup"><span data-stu-id="91629-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="91629-114">Du kan nu se posteringstypen og bogføre anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="91629-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="91629-115">Vælg **Kladdedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="91629-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="91629-116">Vælg **linjer** for at se de enkelte linjer til kladdeposteringen.</span><span class="sxs-lookup"><span data-stu-id="91629-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="91629-117">Vælg den kladdelinje, der indeholder aktivet, og vælg derefter fanen **Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="91629-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="91629-118">Fanen **Anlægsaktiver** vises posteringstypen og bogføringen.</span><span class="sxs-lookup"><span data-stu-id="91629-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="91629-119">Feltet **Transaktiontype** er som standard angivet til **Anskaffelse**, og feltet **Kartotek** angives til den aktuelle bogføringsmodel for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="91629-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="91629-120">Når du har bogført den første genkendelseskladdepost, vises transaktionen som en anskaffelsespostering for anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="91629-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="91629-121">Hvis du vil se transaktionstabellen, skal du gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver** og vælge **Vurderinger**.</span><span class="sxs-lookup"><span data-stu-id="91629-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="91629-122">Du bør se, at den første genkendelseskladdepost har oprettet en anskaffelsespostering for det angivne anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="91629-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="91629-123">Anlægsaktivet kan nu afskrives med standardafskrivningsfunktionen i anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="91629-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="91629-124">Du kan finde flere oplysninger om afskrivning under [Afskrivningsmetoder og -principper](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="91629-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="91629-125">Hvis du knytter et anlægsaktiv til en leasingaftale, deaktiveres knapperne til **Afskrivning af aktiv** og **Værdiforringelse af leasingaftale**.</span><span class="sxs-lookup"><span data-stu-id="91629-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="91629-126">Du kan se anlægsaktivafskrivninger og leasingaftalens værdiforringelsestransaktioner fra anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="91629-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="91629-127">Knappen **Aaktivtransaktioner**, der åbner en forespørgselsform, deaktiveres også.</span><span class="sxs-lookup"><span data-stu-id="91629-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="91629-128">Du kan også åbne formularen **Aktivtransaktioner** i anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="91629-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
