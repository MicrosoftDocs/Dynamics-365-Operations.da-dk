---
title: Vurder kunde- og produktrentabilitet
description: "Denne artikel forklarer, hvordan du kan bruge analysen i hukommelsen og i realtid til at få adgang til, udforske og få indsigt i kunder og produktrentabilitet fra Microsoft Dynamics 365 for Retail-data."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04ebc624212e6909eda7589b71cd84a22010e721
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="6a9a3-103">Vurdere kunde- og produktrentabilitet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="6a9a3-104">Denne artikel forklarer, hvordan du kan bruge analysen i hukommelsen og i realtid til at få adgang til, udforske og få indsigt i kunder og produktrentabilitet fra Microsoft Dynamics 365 for Retail-data.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="6a9a3-105">Som en del af Microsoft Dynamics 365 for Retail kan brugerne undersøge rentabilitet for de bedste kunder (10 til 100) på tværs af forskellige niveauer i organisationshierarkiet, baseret på et af følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="6a9a3-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="6a9a3-106">Salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="6a9a3-106">Sales amount</span></span>
-   <span data-ttu-id="6a9a3-107">Antal</span><span class="sxs-lookup"><span data-stu-id="6a9a3-107">Quantity</span></span>
-   <span data-ttu-id="6a9a3-108">Overskudsgrad, brutto</span><span class="sxs-lookup"><span data-stu-id="6a9a3-108">Gross profit margin</span></span>
-   <span data-ttu-id="6a9a3-109">DB-procent</span><span class="sxs-lookup"><span data-stu-id="6a9a3-109">Margin percentage</span></span>

<span data-ttu-id="6a9a3-110">Til denne vurdering kan du bruge den færdiglavede rapport **Vigtigste kunder**, som du kan åbne fra et af følgende steder:</span><span class="sxs-lookup"><span data-stu-id="6a9a3-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="6a9a3-111">Arbejdsområdet **Detailbutiksstyring** &gt; **Detail** &gt; **Kanaler** &gt; **Detailbutiksstyring** &gt; **Rapporter** &gt; **Rapport over vigtigste kunder**</span><span class="sxs-lookup"><span data-stu-id="6a9a3-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="6a9a3-112">Sektionen **Forespørgsler og rapporter** &gt; **Detail** &gt; **Forespørgsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport over vigtigste kunder**</span><span class="sxs-lookup"><span data-stu-id="6a9a3-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="6a9a3-113">På samme måde kan brugerne undersøge rentabiliteten for de vigtigste produkter (10 til 100) på tværs af forskellige niveauer i organisationshierarkiet, baseret på et af følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="6a9a3-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="6a9a3-114">Salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="6a9a3-114">Sales amount</span></span>
-   <span data-ttu-id="6a9a3-115">Antal</span><span class="sxs-lookup"><span data-stu-id="6a9a3-115">Quantity</span></span>
-   <span data-ttu-id="6a9a3-116">Overskudsgrad, brutto</span><span class="sxs-lookup"><span data-stu-id="6a9a3-116">Gross profit margin</span></span>
-   <span data-ttu-id="6a9a3-117">DB-procent</span><span class="sxs-lookup"><span data-stu-id="6a9a3-117">Margin percentage</span></span>

<span data-ttu-id="6a9a3-118">Til denne vurdering kan du bruge den færdiglavede rapport **Vigtigste produkter**, som du kan åbne fra et af følgende steder:</span><span class="sxs-lookup"><span data-stu-id="6a9a3-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="6a9a3-119">Arbejdsområdet **Detailbutiksstyring** &gt; **Detail** &gt; **Kanaler** &gt; **Detailbutiksstyring** &gt; **Rapporter** &gt; **Rapport over topprodukter**</span><span class="sxs-lookup"><span data-stu-id="6a9a3-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="6a9a3-120">**Kategori og produktstyring**-arbejdsområdet &gt; **Detail** &gt; **Produkter og kategorier** &gt; **Detailbutiksstyring** &gt; **Rapporter** &gt; **Rapport over topprodukter**</span><span class="sxs-lookup"><span data-stu-id="6a9a3-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="6a9a3-121">Sektionen **Forespørgsler og rapporter** &gt; **Detail** &gt; **Forespørgsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport over topprodukter**</span><span class="sxs-lookup"><span data-stu-id="6a9a3-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




