---
title: Forbedret filtrering i RCS/Globalt lager
description: I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager, der er blevet forbedret, så det indeholder ekstra filtre.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441435"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="324e5-103">Forbedrede filtreringsindstillinger til søgning efter konfigurationer i RCS/det globale lager</span><span class="sxs-lookup"><span data-stu-id="324e5-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="324e5-104">I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager (Regulatory Configuration Service), der er blevet forbedret, så det giver mulighed for at filtrere med følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="324e5-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="324e5-105">**Land/område** - baseret på ISO-landekoder</span><span class="sxs-lookup"><span data-stu-id="324e5-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="324e5-106">**Kodetyper** for:</span><span class="sxs-lookup"><span data-stu-id="324e5-106">**Tags** types for:</span></span>
  - <span data-ttu-id="324e5-107">Funktionsområde</span><span class="sxs-lookup"><span data-stu-id="324e5-107">Functional area</span></span>
  - <span data-ttu-id="324e5-108">Funktionsområde</span><span class="sxs-lookup"><span data-stu-id="324e5-108">Feature area</span></span>
  - <span data-ttu-id="324e5-109">Branche</span><span class="sxs-lookup"><span data-stu-id="324e5-109">Industry</span></span> 
  - <span data-ttu-id="324e5-110">Forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="324e5-110">Business document</span></span> 

<span data-ttu-id="324e5-111">Du kan anvende filtre, enten individuelt eller som gruppe, for at gøre det lettere at finde bestemte eller relaterede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="324e5-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="324e5-112">Hvis du f.eks. vil finde en enkelt type af forretningsdokumenter, der kan konfigureres, med relation til kreditorfakturaer, kan du anvende et **Forretningsdokumenttype**-filter til at søge efter den pågældende dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="324e5-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="324e5-113">[![Filtersektion for globalt lager](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="324e5-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="324e5-114">Du kan yderligere indsnævre søgningen ved at vælge dokumenttype, f.eks. 'kreditorfaktura', og klikke på **Anvend filter**.</span><span class="sxs-lookup"><span data-stu-id="324e5-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="324e5-115">Følgende eksempel viser resultaterne, når du filtrerer efter **Forretningsdokumenttype** med tilføjet dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="324e5-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="324e5-116">[![Anvendte filter og import for forretningsdokumenttype](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="324e5-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="324e5-117">Filtrerede resultater kan importeres til en brugers RCS-lager eller et Dynamics 365 Finance-miljø, enten individuelt eller som et sæt.</span><span class="sxs-lookup"><span data-stu-id="324e5-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="324e5-118">Det gør du ved at vælge gruppen af konfigurationer og klikke på **Importér**.</span><span class="sxs-lookup"><span data-stu-id="324e5-118">To do this, select the group of configurations, and click **Import**.</span></span>
