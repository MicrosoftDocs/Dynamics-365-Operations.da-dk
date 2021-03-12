---
title: Bekræft betalingsplaner for aktivleasing i en batch
description: Dette emne forklarer, hvordan du kan bekræfte flere betalingsplaner i en batch.
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
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971372"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="9bc53-103">Bekræft betalingsplaner for aktivleasing i en batch</span><span class="sxs-lookup"><span data-stu-id="9bc53-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bc53-104">Dette emne forklarer, hvordan du kan bekræfte flere betalingsplaner i en batch.</span><span class="sxs-lookup"><span data-stu-id="9bc53-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="9bc53-105">Betalingsplaner bekræftes enten på grundlag af en leasing-til-leasing eller via bekræftelsesbatchprocessen.</span><span class="sxs-lookup"><span data-stu-id="9bc53-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="9bc53-106">En kladdepostering kan kun bogføres i forhold til en leasing, der har en bekræftet betalingsplan.</span><span class="sxs-lookup"><span data-stu-id="9bc53-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="9bc53-107">Bekræftelse af betalingsplanen fungerer som endelig godkendelse af de økonomiske oplysninger for leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="9bc53-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="9bc53-108">Alle fremtidige ændringer af de økonomiske oplysninger for leasingaftalen, f. eks. betalinger og leasingperioden, udgør en justering af rettigheder og bør behandles på denne måde.</span><span class="sxs-lookup"><span data-stu-id="9bc53-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="9bc53-109">Benyt følgende fremgangsmåde for at bekræfte flere betalingsplaner.</span><span class="sxs-lookup"><span data-stu-id="9bc53-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="9bc53-110">Gå til det **Aktivleasing \> Periodisk \> Bekræftelsesbatch**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="9bc53-111">På siden **Bekræftelsesbatch** skal du vælge **Bekræftelsesbatch**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="9bc53-112">Filtrer efter de bøger, du vil bekræfte, i dialogboksen, der vises.</span><span class="sxs-lookup"><span data-stu-id="9bc53-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="9bc53-113">Hvis du vil bekræfte alle bøgerne i en bestemt leasinggruppe, skal du vælge gruppen i feltet **Leasinggruppe**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="9bc53-114">Hvis du vil bekræfte bestemte bøger, skal du vælge kartoteker i feltet **Kartoteks-id**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="9bc53-115">Hvis du vil bekræfte alle kartoteker, skal du aktivere parameteren **For alle kartoteker**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="9bc53-116">Oplysningerne for de senest bekræftede kartoteker vises på siden **Bekræftede kartoteker**.</span><span class="sxs-lookup"><span data-stu-id="9bc53-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="9bc53-117">Når betalingsplanerne er bekræftet, kan de oprindelige genkendelseskladdeposteringer bogføres i forhold til rettighederne.</span><span class="sxs-lookup"><span data-stu-id="9bc53-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
