---
title: Oprette betalingsfakturaer
description: Dette emne forklarer, hvordan du opretter månedlige leasingfakturaer. Du kan oprette fakturaer for individuelle leasingaftaler, eller du kan bruge en batchproces til at oprette dem for flere leasingaftaler.
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
ms.openlocfilehash: a8b9457b158afaa32718976a7a97f48411be0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241516"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="495bc-104">Oprette betalingsfakturaer</span><span class="sxs-lookup"><span data-stu-id="495bc-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="495bc-105">Du kan oprette månedlige fakturaer for individuelle leasingaftaler, eller du kan bruge en batchproces til at oprette dem for flere leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="495bc-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="495bc-106">Følgende procedure viser, hvordan du opretter en individuel leasingbetalingspost, når parameteren **Betal til kreditor** på siden **opsætning af leasingkartotek** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="495bc-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="495bc-107">På siden **Leasingoversigt** skal du vælge en leasingaftale, og derefter **Kartoteker \> Betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="495bc-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="495bc-108">Vælg den betaling, der skal foretages, og vælg derefter **Opret kladde**.</span><span class="sxs-lookup"><span data-stu-id="495bc-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="495bc-109">Du får vist en meddelelse, der angiver, at der er oprettet en kladde mod den valgte betaling.</span><span class="sxs-lookup"><span data-stu-id="495bc-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="495bc-110">Vælg **Fakturakladder**, og vælg derefter den faktura, der skal betales.</span><span class="sxs-lookup"><span data-stu-id="495bc-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="495bc-111">Gennemse kladdeposteringen på fanen **Linjer**, før du bogfører den til Finanskladde.</span><span class="sxs-lookup"><span data-stu-id="495bc-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="495bc-112">Som standard vil de kreditorfakturalinjer, der oprettes, bruge kreditorposteringsprofilen fra siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="495bc-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="495bc-113">Vælg den korrekte kladde, og vælg derefter den faktura, der skal betales.</span><span class="sxs-lookup"><span data-stu-id="495bc-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="495bc-114">I dette eksempel er parameteren **Betal til kreditor** i leasingkartoteket aktiveret.</span><span class="sxs-lookup"><span data-stu-id="495bc-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="495bc-115">Fakturaen vil derfor være i fakturakladden.</span><span class="sxs-lookup"><span data-stu-id="495bc-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="495bc-116">Afsnittet **Oversigt** indeholder en oversigt over kladdeposteringen, og afsnittet **Linjer** indeholder oplysninger om de faktiske kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="495bc-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="495bc-117">Hvis parameteren **Betal til kreditor** er deaktiveret, vises betalingskladdeposterne på siden **Aktivleasing** for leasingkartoteket, og systemet opretter en post for aktivleasing i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="495bc-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="495bc-118">Betalingsposten for leasing bogføres til det kladdenavn, der er angivet i feltet **Månedlig leasingkladde**.</span><span class="sxs-lookup"><span data-stu-id="495bc-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="495bc-119">Når posteringen er bogført, kan du få vist posteringsoplysningerne og bære ansvarsværdien for leasingforpligtelserne ved at vælge **Ansvarsposteringer** i leasingkartoteket.</span><span class="sxs-lookup"><span data-stu-id="495bc-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="495bc-120">Afkrydsningsfeltet i betalingsplanen **Kladde bogført** er markeret i betalingsplanen, og linjen viser fakturakladdenummeret.</span><span class="sxs-lookup"><span data-stu-id="495bc-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="495bc-121">Når en betalingskladde og en post for den pågældende kladde er oprettet, skal du tilbageføre posten, før den kan oprettes igen.</span><span class="sxs-lookup"><span data-stu-id="495bc-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]