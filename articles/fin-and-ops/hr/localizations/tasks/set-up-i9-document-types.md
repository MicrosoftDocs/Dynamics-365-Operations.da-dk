--- 
title: Konfigurere I-9-dokumenttyper
description: "Denne fremgangsmåde viser, hvordan du kan få vist og konfigurere dokumenttyper, der bruges til I-9-bekræftelse."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="30cfc-103">Konfigurere I-9-dokumenttyper</span><span class="sxs-lookup"><span data-stu-id="30cfc-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="30cfc-104">Denne fremgangsmåde viser, hvordan du kan få vist og konfigurere dokumenttyper, der bruges til I-9-bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="30cfc-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="30cfc-105">Før du konfigurerer I-9-dokumenttyper, skal du også konfigurer de udstedende organer og identifikationstyper.</span><span class="sxs-lookup"><span data-stu-id="30cfc-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="30cfc-106">Demodatafirmaet, der bruges til at oprette denne procedure, er USMF, som indeholder eksempler udstedende agenturer og identifikationstyper, der er nødvendige for at fuldføre proceduren.</span><span class="sxs-lookup"><span data-stu-id="30cfc-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="30cfc-107">Gå til personale > Arbejdere > I-9 > I-9-dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="30cfc-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="30cfc-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30cfc-108">Click New.</span></span>
3. <span data-ttu-id="30cfc-109">Skriv en værdi i feltet I-9-dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="30cfc-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="30cfc-110">Eksempel: Skole-id.</span><span class="sxs-lookup"><span data-stu-id="30cfc-110">Example: School ID.</span></span>  
4. <span data-ttu-id="30cfc-111">Vælg identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="30cfc-111">Select the identification type.</span></span>  <span data-ttu-id="30cfc-112">Eksempel: Skole-id</span><span class="sxs-lookup"><span data-stu-id="30cfc-112">Example:  School ID</span></span>
    * <span data-ttu-id="30cfc-113">Eksempler på identifikationstyper er personnummer, visumnummer, pas-ID eller kørekort.</span><span class="sxs-lookup"><span data-stu-id="30cfc-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="30cfc-114">Vælg I-9-dokumentlisten, der bruges til dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="30cfc-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="30cfc-115">Som en del af I-9-processen skal medarbejdere fremlægge dokumentation, der viser deres identitet og tilladelse til arbejdsgiveren.</span><span class="sxs-lookup"><span data-stu-id="30cfc-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="30cfc-116">De amerikanske immigrationsmyndigheders websted indeholder oplysninger om, hvilke dokumenter der er acceptable og hvilken liste, de hører til.</span><span class="sxs-lookup"><span data-stu-id="30cfc-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="30cfc-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="30cfc-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="30cfc-118">Angiv dokumenttypens officielle blanketnummer i feltet Blanket.</span><span class="sxs-lookup"><span data-stu-id="30cfc-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="30cfc-119">Eksempel: Skole-id.</span><span class="sxs-lookup"><span data-stu-id="30cfc-119">Example: School ID.</span></span>
    * <span data-ttu-id="30cfc-120">Den officielle form tal findes på de amerikanske immigrationsmyndigheders websted.</span><span class="sxs-lookup"><span data-stu-id="30cfc-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="30cfc-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="30cfc-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="30cfc-122">Markér eller fjern markeringen i afkrydsningsfeltet Aktiv.</span><span class="sxs-lookup"><span data-stu-id="30cfc-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="30cfc-123">I feltet Udløb skal du angive datoen til "2019-10-27".</span><span class="sxs-lookup"><span data-stu-id="30cfc-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="30cfc-124">Udløbsdatoen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="30cfc-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="30cfc-125">Vælg den myndighed, der har udstedt dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="30cfc-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="30cfc-126">Eksempel: Provins/område</span><span class="sxs-lookup"><span data-stu-id="30cfc-126">Example: Province/territory</span></span>
10. <span data-ttu-id="30cfc-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30cfc-127">Click Save.</span></span>


