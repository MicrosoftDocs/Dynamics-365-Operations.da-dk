---
title: Du kan kun tilføje hovedkontoen som kreditkontoen af afstemningsmæssige årsager
description: Når du konfigurerer en afstemningsårsag i Transportstyring, kan du kun tilføje hovedkontoen som kreditkonto.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026357"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="2b9ed-103">Du kan kun tilføje hovedkontoen som kreditkontoen af afstemningsmæssige årsager</span><span class="sxs-lookup"><span data-stu-id="2b9ed-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="2b9ed-104">KB-nummer: 4603538</span><span class="sxs-lookup"><span data-stu-id="2b9ed-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="2b9ed-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="2b9ed-105">Symptoms</span></span>

<span data-ttu-id="2b9ed-106">Når du konfigurerer en afstemningsårsag i Transportstyring, kan du kun tilføje hovedkontoen som kreditkonto.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="2b9ed-107">Du kan ikke tilføje en bærer eller en anden dimension som kreditkonto.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="2b9ed-108">Debetkontoen giver dig dog mulighed for at vælge andre dimensioner.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="2b9ed-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="2b9ed-109">Resolution</span></span>

<span data-ttu-id="2b9ed-110">Hvis afstemningen ikke sker for at betale kreditoren, men for at kreditere en bestemt hovedkonto, giver systemet dig ikke mulighed for at vælge en økonomisk dimension til kreditkontoen, når du konfigurerer afstemningsårsagen.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="2b9ed-111">Hvis kontostrukturen kræver en bestemt økonomisk dimensionsværdi for kredithovedkontoen, kan den kreditorkladde, der oprettes som resultat, ikke bogføres automatisk, fordi den økonomiske dimensionsværdi mangler.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="2b9ed-112">Derfor skal du først angive kreditkontoen manuelt ved hjælp af siden **Fakturakladde**.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="2b9ed-113">Da der kræves en dimensionsværdi for kreditkontoen, kan kreditorfakturakladden ikke bogføres automatisk.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="2b9ed-114">Du skal bogføre den manuelt, når du manuelt har føjet dimensionsværdien til hovedkontoen for kreditlinjen.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
