---
title: Sporing af regnskabskilde
description: Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 421b371c70abc82907810244e8224d859da9fab2
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="1bda1-103">Sporing af regnskabskilde</span><span class="sxs-lookup"><span data-stu-id="1bda1-103">Accounting source explorer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1bda1-104">Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="1bda1-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="1bda1-105">Sporing af regnskabskilde er en ny side, der viser kildeoplysninger.</span><span class="sxs-lookup"><span data-stu-id="1bda1-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="1bda1-106">Du kan bruge Sporing af regnskabskilde enten som et separat værktøj eller til at analysere detaljerne bag regnskabsposter i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="1bda1-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="1bda1-107">Du kan eksempelvis bruge Sporing af regnskabskilde til at få de mest detaljerede kildeoplysninger til en saldo i råbalancen eller til en bilagspostering.</span><span class="sxs-lookup"><span data-stu-id="1bda1-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="1bda1-108">Du kan derefter bruge funktionen Eksportér til Microsoft Excel til at inddele oplysningerne i Microsoft Excel yderligere (for eksempel i en pivottabel eller i en pivottabelrapport).</span><span class="sxs-lookup"><span data-stu-id="1bda1-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="1bda1-109">Sporing af regnskabskilde viser altid det samme samlede beløb pr. finanskonto som Finans viser (for eksempel i råbalancen).</span><span class="sxs-lookup"><span data-stu-id="1bda1-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="1bda1-110">Som med råbalancen kan du få vist segmenter i separate kolonner.</span><span class="sxs-lookup"><span data-stu-id="1bda1-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="1bda1-111">Du skal blot vælge det relevante sæt økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="1bda1-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="1bda1-112">Du kan bruge parametre til at definere et datointerval for analysen.</span><span class="sxs-lookup"><span data-stu-id="1bda1-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="1bda1-113">Denne funktionalitet minder også om funktionerne i råbalance.</span><span class="sxs-lookup"><span data-stu-id="1bda1-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="1bda1-114">Sporing af regnskabskilde viser yderligere oplysninger, der er baseret på regnskabsfordelinger, og eventuelt projektregnskabsfordelinger for alle dokumenter, der bruger kildedokumentstrukturen.</span><span class="sxs-lookup"><span data-stu-id="1bda1-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="1bda1-115">Disse oplysninger omfatter typen af pengebeløb-, projekt-, aktivitets-, kategori- og linjeegenskaben.</span><span class="sxs-lookup"><span data-stu-id="1bda1-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="1bda1-116">Her er nogle eksempler på den analyse, du kan foretage:</span><span class="sxs-lookup"><span data-stu-id="1bda1-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="1bda1-117">Afvigelser mellem indkøbsordrer og kreditorfakturaer, da hver afvigelse er repræsenteret af typen pengebeløb, som f.eks. gebyrafvigelse</span><span class="sxs-lookup"><span data-stu-id="1bda1-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="1bda1-118">Fakturerbare og ikke-fakturerbare timer og udgifter pr. projekt, virksomhedsenhed og hovedkonto</span><span class="sxs-lookup"><span data-stu-id="1bda1-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="1bda1-119">Til kildedokumenter, der anvender begrebet reference-id'er til kildedokumenter, viser Sporing af regnskabskilde endnu flere detaljer, som debitor, kreditor, arbejder, produkt, antal, enhedsteksten og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="1bda1-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="1bda1-120">Her er nogle eksempler på den analyse, du kan foretage:</span><span class="sxs-lookup"><span data-stu-id="1bda1-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="1bda1-121">Hoteludgifter pr. virksomhedsenhed og hotelmærke for en regnskabsperiode baseret på udgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="1bda1-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="1bda1-122">Rabatter pr. leverandør, produkt, afdeling</span><span class="sxs-lookup"><span data-stu-id="1bda1-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="1bda1-123">For disse dokumenter kan du også navigere til det faktiske kildedokument fra Sporing af regnskabskilde.</span><span class="sxs-lookup"><span data-stu-id="1bda1-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




