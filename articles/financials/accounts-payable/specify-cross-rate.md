---
title: Angive gennemsnitskursen
description: Dette emne indeholder oplysninger om krydskurser i Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="85f5b-103">Angive gennemsnitskursen</span><span class="sxs-lookup"><span data-stu-id="85f5b-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85f5b-104">Dette emne forklarer formålet med en gennemsnitskurs, og hvordan du angiver gennemsnitskursen, når du udligner en betaling med en faktura.</span><span class="sxs-lookup"><span data-stu-id="85f5b-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="85f5b-105">Du kan bruge en gennemsnitskurs, når alle af følgende kriterier gælder:</span><span class="sxs-lookup"><span data-stu-id="85f5b-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="85f5b-106">Du udligner en betaling med en faktura.</span><span class="sxs-lookup"><span data-stu-id="85f5b-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="85f5b-107">Betalingslinjen og fakturalinjen anvender forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="85f5b-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="85f5b-108">Ingen af valutaerne er regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="85f5b-109">Krydskursen bruges ikke til at beregne valutaomregning ved betalingstransaktioner til regnskabsvalutaen for betalingen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="85f5b-110">I stedet hentes valutakurserne fra valutakurstabellerne for at beregne værdien af valutabeløbet for betalingstransaktionen og betalingsbeløbet i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="85f5b-111">For eksempel er regnskabsvalutaen i USD, fakturavalutaen er i CAD, og betalingsvalutaen er i EUR.</span><span class="sxs-lookup"><span data-stu-id="85f5b-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="85f5b-112">Med gennemsnitskursen kan du angive en valutakurs til at oversætte direkte mellem CAD og EUR og behøver ikke at oversætte via USD.</span><span class="sxs-lookup"><span data-stu-id="85f5b-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="85f5b-113">Når du vælger en faktura og en primær betaling, kan du angive en gennemsnitskurs for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="85f5b-114">Gennemsnitskursen er valutakursen mellem valutaer for disse transaktioner pr. afregningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="85f5b-115">Gå til en af følgende sider:</span><span class="sxs-lookup"><span data-stu-id="85f5b-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="85f5b-116">**Debitor > Generelt > Kunder > Alle kunder**</span><span class="sxs-lookup"><span data-stu-id="85f5b-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="85f5b-117">**Kreditor > Almindelige > Kreditorer > Alle kreditorer**</span><span class="sxs-lookup"><span data-stu-id="85f5b-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="85f5b-118">**Indkøb og forsyning > Almindelige > Kreditorer > Alle kreditorer**</span><span class="sxs-lookup"><span data-stu-id="85f5b-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="85f5b-119">Vælg den debitor eller kreditor, hvis åbne posteringer skal afregnes.</span><span class="sxs-lookup"><span data-stu-id="85f5b-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="85f5b-120">For en debitor skal du på listesiden **Alle debitorer** gå til **Indsaml > Udlign åbne posteringer**.</span><span class="sxs-lookup"><span data-stu-id="85f5b-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="85f5b-121">For en kreditor skal du på listesiden **Alle kreditorer** gå til **Faktura > Udlign åbne posteringer**.</span><span class="sxs-lookup"><span data-stu-id="85f5b-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="85f5b-122">Vælg den postering, der er den primære betaling, og klik derefter på **Marker betaling**.</span><span class="sxs-lookup"><span data-stu-id="85f5b-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="85f5b-123">Afkrydsningsfeltet i kolonnen **Marker** markeres, og der vises et informationsikon i kolonnen **Primær betaling**.</span><span class="sxs-lookup"><span data-stu-id="85f5b-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="85f5b-124">I feltet **Krydskurs** skal du angive fakturavalutaen og betalingsvalutaen pr. udligningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="85f5b-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 

