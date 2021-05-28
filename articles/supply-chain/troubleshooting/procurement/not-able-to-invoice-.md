---
title: Du kan ikke fakturere en kundehenvendt salgsordre
description: Du kan ikke længere fakturere den oprindelige salgsordre og den oprindelige indkøbsordre for direkte levering, når du har aktiveret indstillingen Bogfør faktura automatisk.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026367"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="dbf93-103">Du kan ikke fakturere en kundehenvendt salgsordre</span><span class="sxs-lookup"><span data-stu-id="dbf93-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="dbf93-104">KB-nummer: 4611793</span><span class="sxs-lookup"><span data-stu-id="dbf93-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="dbf93-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="dbf93-105">Symptoms</span></span>

<span data-ttu-id="dbf93-106">Du kan ikke længere fakturere den oprindelige salgsordre og den oprindelige indkøbsordre for direkte levering, når du har aktiveret indstillingen **Bogfør faktura automatisk** på siden **Intern** for en leverandør.</span><span class="sxs-lookup"><span data-stu-id="dbf93-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="dbf93-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="dbf93-107">Resolution</span></span>

<span data-ttu-id="dbf93-108">Synkroniseringsfunktionsmåden for interne og direkte leveringsordrefakturaer styres og gennemtvinges af de parametre, der er beskrevet i [Definere parametre for bogføring af en intern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="dbf93-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="dbf93-109">Når du har angivet disse parametre, skal du fakturere den interne salgsordre først.</span><span class="sxs-lookup"><span data-stu-id="dbf93-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="dbf93-110">De oprindelige salgsordrer og indkøbsordrer synkroniseres derefter.</span><span class="sxs-lookup"><span data-stu-id="dbf93-110">The original sales orders and purchase orders will then be synchronized.</span></span>
