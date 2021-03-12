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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005836"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="8b8d7-103">Forbedrede filtreringsindstillinger til søgning efter konfigurationer i RCS/det globale lager</span><span class="sxs-lookup"><span data-stu-id="8b8d7-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b8d7-104">I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager (Regulatory Configuration Service), der er blevet forbedret, så det giver mulighed for at filtrere med følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="8b8d7-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="8b8d7-105">**Land/område** - baseret på ISO-landekoder</span><span class="sxs-lookup"><span data-stu-id="8b8d7-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="8b8d7-106">**Kodetyper** for:</span><span class="sxs-lookup"><span data-stu-id="8b8d7-106">**Tags** types for:</span></span>
  - <span data-ttu-id="8b8d7-107">Funktionsområde</span><span class="sxs-lookup"><span data-stu-id="8b8d7-107">Functional area</span></span>
  - <span data-ttu-id="8b8d7-108">Funktionsområde</span><span class="sxs-lookup"><span data-stu-id="8b8d7-108">Feature area</span></span>
  - <span data-ttu-id="8b8d7-109">Branche</span><span class="sxs-lookup"><span data-stu-id="8b8d7-109">Industry</span></span> 
  - <span data-ttu-id="8b8d7-110">Forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="8b8d7-110">Business document</span></span> 

<span data-ttu-id="8b8d7-111">Du kan anvende filtre, enten individuelt eller som gruppe, for at gøre det lettere at finde bestemte eller relaterede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="8b8d7-112">Hvis du f.eks. vil finde en enkelt type af forretningsdokumenter, der kan konfigureres, med relation til kreditorfakturaer, kan du anvende et **Forretningsdokumenttype**-filter til at søge efter den pågældende dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="8b8d7-113">[![Filtersektion for globalt lager](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="8b8d7-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="8b8d7-114">Du kan yderligere indsnævre søgningen ved at vælge dokumenttype, f.eks. 'kreditorfaktura', og klikke på **Anvend filter**.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="8b8d7-115">Følgende eksempel viser resultaterne, når du filtrerer efter **Forretningsdokumenttype** med tilføjet dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="8b8d7-116">[![Anvendte filter og import for forretningsdokumenttype](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="8b8d7-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="8b8d7-117">Filtrerede resultater kan importeres til en brugers RCS-lager eller et Dynamics 365 Finance-miljø, enten individuelt eller som et sæt.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="8b8d7-118">Det gør du ved at vælge gruppen af konfigurationer og klikke på **Importér**.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-118">To do this, select the group of configurations, and click **Import**.</span></span>
