---
title: EUR-00015 Parts søgning ved hjælp af moms-id
description: Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0427b6e961173543f860ef6e098fc6248afd3aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183525"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="321ab-103">EUR-00015 Parts søgning ved hjælp af moms-id</span><span class="sxs-lookup"><span data-stu-id="321ab-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="321ab-104">Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id.</span><span class="sxs-lookup"><span data-stu-id="321ab-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="321ab-105">Før du kan udføre denne procedure, skal du konfigurere moms-id'er og angive moms-id'er for kreditorer, debitorer eller juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="321ab-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="321ab-106">Denne procedure gælder for alle europæiske lande.</span><span class="sxs-lookup"><span data-stu-id="321ab-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="321ab-107">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland.</span><span class="sxs-lookup"><span data-stu-id="321ab-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="321ab-108">Denne fremgangsmåde er beregnet til en kreditorchef eller debitorchef.</span><span class="sxs-lookup"><span data-stu-id="321ab-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="321ab-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="321ab-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="321ab-110">Gå til Virksomhedsadministration > Globalt adressekartotek > Globalt adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="321ab-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="321ab-111">Klik på Søgning efter registrerings-id.</span><span class="sxs-lookup"><span data-stu-id="321ab-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="321ab-112">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="321ab-112">Click Add.</span></span>
4. <span data-ttu-id="321ab-113">Indtast eller vælg en værdi i feltet Registreringstype.</span><span class="sxs-lookup"><span data-stu-id="321ab-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="321ab-114">Hvis du f.eks. vil finde parter med et registrerings-id af typen moms-id, skal du vælge moms-id.</span><span class="sxs-lookup"><span data-stu-id="321ab-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="321ab-115">Indtast eller vælg en værdi i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="321ab-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="321ab-116">Angiv for eksempel DEU.</span><span class="sxs-lookup"><span data-stu-id="321ab-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="321ab-117">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="321ab-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="321ab-118">Klik på Søg.</span><span class="sxs-lookup"><span data-stu-id="321ab-118">Click Find.</span></span>
    * <span data-ttu-id="321ab-119">Alle parter med dette registrerings-id vises.</span><span class="sxs-lookup"><span data-stu-id="321ab-119">All parties with that registration ID will be displayed.</span></span>  

