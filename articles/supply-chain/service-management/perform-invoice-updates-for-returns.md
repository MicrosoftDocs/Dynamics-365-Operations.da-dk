---
title: "Udføre fakturaopdateringer til returneringer"
description: "Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 53ae1c3bda06d07a0ca633981ddd46092eae507e
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---


# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="dc922-103">Udføre fakturaopdateringer til returneringer</span><span class="sxs-lookup"><span data-stu-id="dc922-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dc922-104">En returordre en form for salgsordre, der er markeret som en returneret ordre.</span><span class="sxs-lookup"><span data-stu-id="dc922-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="dc922-105">Listesiden **Alle salgsordrer** bruges derfor til at oprette fakturaer for returordrer i stedet for formularen **Returordrer**.</span><span class="sxs-lookup"><span data-stu-id="dc922-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="dc922-106">Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person.</span><span class="sxs-lookup"><span data-stu-id="dc922-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="dc922-107">Da fakturaen for en returneret vare til et negativt beløb, kaldes det en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="dc922-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="dc922-108">Når du konfigurerer fakturaopdateringen til batchafvikling, skal salgsordren af typen **Returordre** have statussen **Modtaget** for returlinjen, hvilket angiver, at ordrens følgeseddel er opdateret.</span><span class="sxs-lookup"><span data-stu-id="dc922-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="dc922-109">Bogføre en faktura for en returvareordre</span><span class="sxs-lookup"><span data-stu-id="dc922-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="dc922-110">Klik på **Debitor** \> **Almindelige** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="dc922-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="dc922-111">Vælg en salgsordre, som **Returordre** vises for i feltet **Ordretype**.</span><span class="sxs-lookup"><span data-stu-id="dc922-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="dc922-112">Klik på **Faktura** i gruppen **Generer** under fanen **Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc922-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="dc922-113">Vælg fanen **Parametre** i dialogboksen **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="dc922-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="dc922-114">Gennemse oplysningerne i formen, og foretag de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="dc922-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="dc922-115">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc922-115">Click **OK**.</span></span> <span data-ttu-id="dc922-116">Kreditnoten bogføres.</span><span class="sxs-lookup"><span data-stu-id="dc922-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc922-117">Se også</span><span class="sxs-lookup"><span data-stu-id="dc922-117">See also</span></span>

[<span data-ttu-id="dc922-118">Følgeseddelopdateringer til returneringer</span><span class="sxs-lookup"><span data-stu-id="dc922-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


