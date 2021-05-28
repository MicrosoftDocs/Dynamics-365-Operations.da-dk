---
title: Tilbageførsel af færdigmeldingen opretter en uventet åben postering
description: Tilbageførsel af færdigmelding med afmærkning opretter en åben postering, hvor det tilbageførte antal har samme lagerdimensioner som den tilbageførte postering.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026383"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="7b341-103">Tilbageførsel af færdigmeldingen opretter en uventet åben postering</span><span class="sxs-lookup"><span data-stu-id="7b341-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="7b341-104">KB-nummer: 4612469</span><span class="sxs-lookup"><span data-stu-id="7b341-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b341-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7b341-105">Symptoms</span></span>

<span data-ttu-id="7b341-106">Hvis du tilbagefører færdigmelding med afmærkning, opretter systemet en åben postering, hvor det tilbageførte antal har samme lagerdimensioner som den postering, der blev tilbageført.</span><span class="sxs-lookup"><span data-stu-id="7b341-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b341-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="7b341-107">Resolution</span></span>

<span data-ttu-id="7b341-108">Når du tilbagefører en færdigmeldingshandling, initialiseres lagerdimensionen fra produktionskladden.</span><span class="sxs-lookup"><span data-stu-id="7b341-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="7b341-109">Den får derfor batchnummeret.</span><span class="sxs-lookup"><span data-stu-id="7b341-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="7b341-110">På grund af afmærkningen arver salgsordretransaktionerne batchnummeret.</span><span class="sxs-lookup"><span data-stu-id="7b341-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="7b341-111">Dimensionen kan nulstilles, når færdigmeldingen er bogført.</span><span class="sxs-lookup"><span data-stu-id="7b341-111">The dimension can be reset when the reporting as finished is posted.</span></span>
