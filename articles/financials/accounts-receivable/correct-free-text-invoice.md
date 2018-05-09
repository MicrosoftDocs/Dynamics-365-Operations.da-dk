---
title: Rette en fritekstfaktura
description: "I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1439a52c6096be93902f812aa912959347e8009
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="3fe5f-103">Rette en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="3fe5f-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fe5f-104">I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="3fe5f-105">Hvis du vil rette en fritekstfaktura eller salgsfaktura, der allerede er bogført, skal du åbne den bogførte fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="3fe5f-106">På siden **Faktura** skal vælge **Annuller** og derefter vælge **Ret faktura**.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="3fe5f-107">Vælg en årsagskode, tilføj kommentarer, og vælg datoen for den nye rettede faktura.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="3fe5f-108">Du kan ændre den rettede faktura og bogføre den.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="3fe5f-109">Når du bogfører den rettede faktura, oprettes der en annullering af fakturaen for et kreditbeløb, der er lig med det oprindelige fakturabeløb.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="3fe5f-110">Derfor bliver den samlede saldo af den oprindelige faktura og annulleringen af fakturaen 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="3fe5f-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="3fe5f-111">Annulleringen af fakturaen udlignes mod den oprindelige faktura.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="3fe5f-112">Når du bogfører den rettede faktura, har du tre fakturaer:</span><span class="sxs-lookup"><span data-stu-id="3fe5f-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="3fe5f-113">**Oprindelig faktura** – Den faktura, der indeholder de oplysninger, du skal rette.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="3fe5f-114">**Annulleringsfaktura** – Den systemgenererede kreditfaktura, der er oprettet for at annullere den faktura, der senest er rettet.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="3fe5f-115">**Rettet faktura** – Den faktura, der indeholder oplysninger om den rettede faktura.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="3fe5f-116">Du kan identificere annullerede og rettede fakturaer på to måder:</span><span class="sxs-lookup"><span data-stu-id="3fe5f-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="3fe5f-117">Siden **Alle fritekstfakturaer** indeholder en kolonne af typen **Rettelse**, hvor du kan se, hvilke fakturaer der er annullerede fakturaer og rettede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="3fe5f-118">Overskriften for fritekstfakturaen viser en status for **Annulleringsfaktura '\[fakturanummer\]'** eller **Rettet faktura '\[fakturanummer\]'**.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe5f-119">Denne funktion er kun tilgængelig, hvis konfigurationsnøglen **Fri tekst til rettelse af faktura** er valgt.</span><span class="sxs-lookup"><span data-stu-id="3fe5f-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>




