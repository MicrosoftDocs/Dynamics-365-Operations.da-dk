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
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834331"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="bc2db-103">Lokalisere fejl i salgstilbud</span><span class="sxs-lookup"><span data-stu-id="bc2db-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="bc2db-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="bc2db-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="bc2db-105">Salgsantallet i et salgstilbud kan ikke ændres for en servicevare.</span><span class="sxs-lookup"><span data-stu-id="bc2db-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc2db-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bc2db-106">Issue description</span></span>

<span data-ttu-id="bc2db-107">Hvis du forsøger at angive et salgsantal (**SalesQty**-felt) for en vare af typen *Service* på en salgstilbudslinje, får du vist følgende meddelelse: "Opdatering ikke tilladt for feltantal".</span><span class="sxs-lookup"><span data-stu-id="bc2db-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bc2db-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bc2db-108">Issue resolution</span></span>

<span data-ttu-id="bc2db-109">Du kan ikke angive et salgsantal for produkter, der er servicevarer.</span><span class="sxs-lookup"><span data-stu-id="bc2db-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="bc2db-110">Hvis du f.eks. tilbyder en service til installation af en vare, giver det ikke mening at registrere et antal, da der ikke er nogen fysisk vare.</span><span class="sxs-lookup"><span data-stu-id="bc2db-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="bc2db-111">Der er kun en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="bc2db-111">There is only a service.</span></span>

