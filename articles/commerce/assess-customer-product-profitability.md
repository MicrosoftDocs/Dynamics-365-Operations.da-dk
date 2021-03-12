---
title: Vurder kunde- og produktrentabilitet
description: Denne artikel forklarer, hvordan du kan bruge analysen i hukommelsen og i realtid til at få adgang til, udforske og få indsigt i kunder og produktrentabilitet fra Dynamics 365 Commerce-data.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3770832cb8eee96931d8f8e68c726d5e09d3fceb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980048"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="2a229-103">Vurdere kunde- og produktrentabilitet</span><span class="sxs-lookup"><span data-stu-id="2a229-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a229-104">Denne artikel forklarer, hvordan du kan bruge analysen i hukommelsen og i realtid til at få adgang til, udforske og få indsigt i kunder og produktrentabilitet fra Dynamics 365 Commerce-data.</span><span class="sxs-lookup"><span data-stu-id="2a229-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="2a229-105">Som en del af Commerce kan brugerne undersøge rentabiliteten for de vigtigste kunder (10 til 100) på tværs af forskellige niveauer i organisationshierarkiet, baseret på et af følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="2a229-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="2a229-106">Salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="2a229-106">Sales amount</span></span>
- <span data-ttu-id="2a229-107">Antal</span><span class="sxs-lookup"><span data-stu-id="2a229-107">Quantity</span></span>
- <span data-ttu-id="2a229-108">Overskudsgrad, brutto</span><span class="sxs-lookup"><span data-stu-id="2a229-108">Gross profit margin</span></span>
- <span data-ttu-id="2a229-109">DB-procent</span><span class="sxs-lookup"><span data-stu-id="2a229-109">Margin percentage</span></span>

<span data-ttu-id="2a229-110">Til denne vurdering kan du bruge den færdiglavede rapport **Vigtigste kunder**, som du kan åbne fra et af følgende steder:</span><span class="sxs-lookup"><span data-stu-id="2a229-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="2a229-111">Arbejdsområdet **Butiksstyring** &gt; **Retail og Commerce** &gt; **Kanaler** &gt; **Butiksstyring** &gt; **Rapporter** &gt; **Rapport over vigtigste kunder**</span><span class="sxs-lookup"><span data-stu-id="2a229-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="2a229-112">Sektionen **Forespørgsler og rapporter** &gt; **Retail og Commerce** &gt; **Forespørgsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport over vigtige kunder**</span><span class="sxs-lookup"><span data-stu-id="2a229-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="2a229-113">På samme måde kan brugerne undersøge rentabiliteten for de vigtigste produkter (10 til 100) på tværs af forskellige niveauer i organisationshierarkiet, baseret på et af følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="2a229-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="2a229-114">Salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="2a229-114">Sales amount</span></span>
- <span data-ttu-id="2a229-115">Antal</span><span class="sxs-lookup"><span data-stu-id="2a229-115">Quantity</span></span>
- <span data-ttu-id="2a229-116">Overskudsgrad, brutto</span><span class="sxs-lookup"><span data-stu-id="2a229-116">Gross profit margin</span></span>
- <span data-ttu-id="2a229-117">DB-procent</span><span class="sxs-lookup"><span data-stu-id="2a229-117">Margin percentage</span></span>

<span data-ttu-id="2a229-118">Til denne vurdering kan du bruge den færdiglavede rapport **Vigtigste produkter**, som du kan åbne fra et af følgende steder:</span><span class="sxs-lookup"><span data-stu-id="2a229-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="2a229-119">Arbejdsområdet **Butiksstyring** &gt; **Retail og Commerce** &gt; **Kanaler** &gt; **Butiksstyring** &gt; **Rapporter** &gt; **Rapport over vigtigste produkter**</span><span class="sxs-lookup"><span data-stu-id="2a229-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="2a229-120">Arbejdsområdet **Kategori og produktstyring** &gt; **Retail og Commerce** &gt; **Produkter og kategorier** &gt; **Butiksstyring** &gt; **Rapporter** &gt; **Rapport over topprodukter**</span><span class="sxs-lookup"><span data-stu-id="2a229-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="2a229-121">Sektionen **Forespørgsler og rapporter** &gt; **Retail og Commerce** &gt; **Forespørgsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport over vigtige produkter**</span><span class="sxs-lookup"><span data-stu-id="2a229-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
