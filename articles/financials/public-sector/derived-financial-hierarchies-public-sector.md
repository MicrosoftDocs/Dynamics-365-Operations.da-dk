---
title: Afledte finansielle hierarkier i den offentlige sektor
description: "I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResCategory, EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchies, LedgerDerivedFinHierarchyFilterResults, LedgerDerivedFinHierarchyLegalEntities
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 20911
ms.assetid: a1b30d2a-a370-402a-b3bd-d562adca55f0
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 507d72973cef9a995d80971cdff6378561b6b4fb
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="derived-financial-hierarchies-in-the-public-sector"></a><span data-ttu-id="f5407-103">Afledte finansielle hierarkier i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="f5407-103">Derived financial hierarchies in the public sector</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f5407-104">I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="f5407-104">This article describes the derived financial hierarchies functionality that is available for the public sector.</span></span> 

<span data-ttu-id="f5407-105">For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="f5407-105">To meet Common Government-wide Accounting Classification (CGAC) requirements, public-sector organizations can use derived financial hierarchies to collect and analyze posted transaction data for specific main account numbers, full account numbers, and financial dimension values.</span></span> 

<span data-ttu-id="f5407-106">Kategorihierarkier konfigureres normalt for at klassificere posteringer til rapportering og analyse ud fra de økonomiske dimensioner i en kontostruktur på bogføringstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="f5407-106">Typically, category hierarchies are set up to classify transactions for reporting and analysis based on the financial dimensions in an account structure at the time of posting.</span></span> <span data-ttu-id="f5407-107">Ved hjælp af kategorihierarkier med kategoritypen Afledt finansielt hierarki kan du oprette filterregler, der opretter økonomiske kategorier og de dimensionsværdier, der ikke er en del af kontonummeret.</span><span class="sxs-lookup"><span data-stu-id="f5407-107">However, by using category hierarchies with a Derived financial hierarchy category type, you can create filter rules that create financial categories and dimension values that are not part of the account number.</span></span> <span data-ttu-id="f5407-108">De økonomiske kategorier og dimensionsværdier, der er defineret i filterreglerne, er afledt fra kontonummerets dimensionsværdier, som bruges i de bogførte posteringer.</span><span class="sxs-lookup"><span data-stu-id="f5407-108">The financial categories and dimension values defined in the filter rules are derived from the account number dimension values that are used in the posted transactions.</span></span>

<span data-ttu-id="f5407-109">Afledte finansielle hierarkier giver dig en mere fleksibel tilgang i forhold til at gruppere posteringer til ad hoc-analyse.</span><span class="sxs-lookup"><span data-stu-id="f5407-109">Derived financial hierarchies give you a more flexible approach to grouping transactions for ad hoc analytics.</span></span> <span data-ttu-id="f5407-110">De giver dig mulighed for at kategorisere posteringer uden at skulle udvide kontostrukturen, så den omfatter de ekstra kategorier eller dimensioner, du vil spore.</span><span class="sxs-lookup"><span data-stu-id="f5407-110">They allow you to categorize transactions without having to expand the account structure to include the additional categories or dimensions you want to track.</span></span>

## <a name="example"></a><span data-ttu-id="f5407-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f5407-111">Example</span></span>
<span data-ttu-id="f5407-112">En organisation har et medarbejdersundhedsprogram og et medarbejderuddannelsesprogram.</span><span class="sxs-lookup"><span data-stu-id="f5407-112">An organization has an employee wellness program and an employee education program.</span></span> <span data-ttu-id="f5407-113">Disse programmer er ikke knyttet til økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f5407-113">These programs are not associated with financial dimensions.</span></span> <span data-ttu-id="f5407-114">Hvis du vil indsamle kontonumre, der er brugt i de bogførte posteringer til disse programmer, kan du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="f5407-114">To collect account numbers used in the posted transactions for these programs, you could do the following:</span></span>

-   <span data-ttu-id="f5407-115">**Oprette kategorihierarkier og de afledte finansielle hierarkier:** Opret et kategorihierarki, der hedder "Medarbejderprogrammer", med en overordnet node, der hedder "Programmer", og to underordnede noder, der hedder "Medarbejdersundhed" og "Medarbejderuddannelse".</span><span class="sxs-lookup"><span data-stu-id="f5407-115">**Set up the category hierarchies and the derived financial hierarchies:** Create a category hierarchy named “Employee programs” with a parent node named “Programs” and two child nodes named “Employee wellness” and “Employee education.”</span></span> <span data-ttu-id="f5407-116">Tildel kategoritypen **Afledt økonomisk hierarki** til kategorihierarkiet "Medarbejderprogrammer".</span><span class="sxs-lookup"><span data-stu-id="f5407-116">Assign the **Derived financial hierarchy** category type to the “Employee programs” category hierarchy.</span></span> <span data-ttu-id="f5407-117">Knyt det afledte finansielle hierarki for "Medarbejderprogrammer" til den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="f5407-117">Associate the “Employee programs” derived financial hierarchy with the legal entity.</span></span>
-   <span data-ttu-id="f5407-118">**Konfigurere filterregler** Brug siden **Afledte økonomiske hierarkier** til at oprette filterregler for hovedkonti og økonomiske dimensionsværdier, der er knyttet til noderne "Medarbejdersundhed" og "Medarbejderuddannelse" i det afledte finansielle hierarki for "Medarbejderprogrammer".</span><span class="sxs-lookup"><span data-stu-id="f5407-118">**Set up filter rules:** Use the **Derived financial hierarchies** page to create filter rules for the main accounts and financial dimension values associated with the “Employee wellness” and “Employee education” nodes in the “Employee programs” derived financial hierarchy.</span></span> <span data-ttu-id="f5407-119">**Tip!** Hvis du vil angive mere end én dimensionsværdi i et filter, skal du bruge et komma uden mellemrum som skilletegn.</span><span class="sxs-lookup"><span data-stu-id="f5407-119">**Tip:** To enter more than one dimension value in a filter, use a comma without spaces as a separator.</span></span> <span data-ttu-id="f5407-120">Angiv for eksempel 100,110 eller Frynsegoder,Forsikring.</span><span class="sxs-lookup"><span data-stu-id="f5407-120">For example, enter 100,110 or Benefits,Insurance.</span></span>
-   <span data-ttu-id="f5407-121">**Analysere bogførte transaktionsdata:** I de filtrerede resultater skal du se på kontonumre og kontooplysninger og oplysninger om økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="f5407-121">**Analyze posted transaction data:** In the filter results, view account numbers and their account and financial dimension details.</span></span>

 





