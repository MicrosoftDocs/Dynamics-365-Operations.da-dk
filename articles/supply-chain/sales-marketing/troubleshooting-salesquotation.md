---
title: Lokalisere fejl i salgstilbud
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgstilbud.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424583"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="e465f-103">Lokalisere fejl i salgstilbud</span><span class="sxs-lookup"><span data-stu-id="e465f-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="e465f-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="e465f-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="e465f-105">Salgsantallet i et salgstilbud kan ikke ændres for en servicevare.</span><span class="sxs-lookup"><span data-stu-id="e465f-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e465f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="e465f-106">Issue description</span></span>

<span data-ttu-id="e465f-107">Hvis du forsøger at angive et salgsantal (**SalesQty**-felt) for en vare af typen *Service* på en salgstilbudslinje, får du vist følgende meddelelse: "Opdatering ikke tilladt for feltantal".</span><span class="sxs-lookup"><span data-stu-id="e465f-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e465f-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="e465f-108">Issue resolution</span></span>

<span data-ttu-id="e465f-109">Du kan ikke angive et salgsantal for produkter, der er servicevarer.</span><span class="sxs-lookup"><span data-stu-id="e465f-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="e465f-110">Hvis du f.eks. tilbyder en service til installation af en vare, giver det ikke mening at registrere et antal, da der ikke er nogen fysisk vare.</span><span class="sxs-lookup"><span data-stu-id="e465f-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="e465f-111">Der er kun en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="e465f-111">There is only a service.</span></span>

