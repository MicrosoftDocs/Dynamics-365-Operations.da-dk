---
title: Tilbageføre bogførte leasingtransaktioner
description: Dette emne forklarer, hvordan du tilbagefører en bogført leasingtransaktion. Alle transaktioner, der oprettes via aktivleasing, kan tilbageføres.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441760"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="bdb5b-104">Tilbageføre bogførte leasingtransaktioner</span><span class="sxs-lookup"><span data-stu-id="bdb5b-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdb5b-105">Alle transaktioner, der oprettes via aktivleasing, kan tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="bdb5b-106">Posteringer, der tilbageføres via aktivleasing, opdaterer dine leasingdata.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="bdb5b-107">De opdaterer derfor også leveringsværdierne i leasingforpligtelsen og brugsretsaktivet (ROU).</span><span class="sxs-lookup"><span data-stu-id="bdb5b-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="bdb5b-108">Udfør følgende trin for at oprette en tilbageførselstransaktion for en leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="bdb5b-109">På siden **Aktivtransaktioner** eller siden **Ansvarsposteringer** skal du vælge transaktion og derefter vælge **Tilbagefør transaktion**.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="bdb5b-110">I den dialogboks, der vises, kan du redigere den dato, hvor tilbageførslen vil blive bogført.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="bdb5b-111">Som standard er feltet **Dato** angivet til bogføringsdatoen for transaktionen for den valgte postering.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="bdb5b-112">Tilbageførselsposten kan ikke bogføres tidligere end den oprindelige bogføringsdato for den valgte transaktion.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="bdb5b-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-113">Select **OK**.</span></span> <span data-ttu-id="bdb5b-114">Der bogføres en kladdepost, der tilbagefører den valgte post.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="bdb5b-115">Tilbageførslen vises på siden **Aktiv posteringer** eller siden **Ansvarsposteringer**, og nettototalen for den aktuelle saldo, der vises på siden, opdateres.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="bdb5b-116">Når du vælger **Tilbagefør sporing**, vises en dialogboks, der viser både de oprindelige posteringer og de tilbageførte posteringer sammen med et nummer, der kaldes et *sporingsnummer*.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="bdb5b-117">Hvis tilbageførslen skal være nemmere at forstå og for at forbedre synligheden, kan du også spore tilbageførsler ved hjælp af planlægningen af rettigheder.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="bdb5b-118">Feltet **Seneste kladdenummer** på siden **Tidsplan** viser kladdenumrene på posteringerne.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="bdb5b-119">Når en postering tilbageføres, opdateres dette felt med kladdenummeret på en tilbageført postering.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="bdb5b-120">Desuden markeres afkrydsningsfeltet **Tilbageført** for at angive, at transaktionen skal tilbageføres, og at feltet **Bogført** er markeret.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="bdb5b-121">Fortryde en tilbageført postering</span><span class="sxs-lookup"><span data-stu-id="bdb5b-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="bdb5b-122">Udfør følgende trin for at annullere en tilbageført postering.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="bdb5b-123">På siden **Tidsplan** eller siden **Transaktioner** skal du vælge den oprindelige postering.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="bdb5b-124">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="bdb5b-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="bdb5b-125">Hvis du har valgt transaktionen på siden **Planlæg** skal du udføre trinnene til oprettelse af en kladde i [Oprette månedskladdeposteringer i en batch](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="bdb5b-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="bdb5b-126">Du skal bogføre kladden manuelt.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="bdb5b-127">Hvis du valgte posteringen på siden **Transaktioner** skal du vælge **Tilbagefør transaktion**.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="bdb5b-128">Du får vist en meddelelse, der angiver, at denne tilbagekaldelse er en tilbageføring af en tidligere tilbageførsel, og at du kan redigere bogføringsdatoen for denne tilbagekaldelse.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="bdb5b-129">De generelle forretningsvalideringer har dog indflydelse på de datoer, der kan angives i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="bdb5b-130">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-130">Select **OK**.</span></span> <span data-ttu-id="bdb5b-131">Der bogføres en kladdepost, der tilbagefører den valgte post.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="bdb5b-132">Tilbageførslen vises på siden **Transaktioner**, og den samlede nettosaldo er gendannet til hvad, den var før den første tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="bdb5b-133">Derfor er den påvirkning, tilbageførslen havde på saldiene negativ.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="bdb5b-134">Når du vælger **Tilbagefør sporing**, vises en dialogboks, der viser både de oprindelige posteringer og de tilbageførte posteringer sammen med et nummer, der kaldes et sporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="bdb5b-135">Du kan også spore annulleringer ved hjælp af den relevante **Tidsplan**-side.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="bdb5b-136">Feltet **Tilbagefør** fjernes, mens feltet **Kladde** er markeret.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="bdb5b-137">Derudover opdateres feltet **Seneste journalnummer** med kladdenummeret for den tilbagekaldte postering, og feltet **Kladdenummer** opdateres med kladdenummeret for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="bdb5b-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
