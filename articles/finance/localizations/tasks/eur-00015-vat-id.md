---
title: EUR 00015 Konfigurere moms-id
description: Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bf6fe6926a7cc1aecb1f0a2bb7f3c47cc8828e8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407680"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="d6331-103">EUR 00015 Konfigurere moms-id</span><span class="sxs-lookup"><span data-stu-id="d6331-103">EUR-00015 Set up VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6331-104">Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori.</span><span class="sxs-lookup"><span data-stu-id="d6331-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="d6331-105">Du kan finde flere oplysninger om registrering-id'er og behandling af registrering-id'er , herunder nødvendige forudsætninger, i Hjælp-emnet Registrerings-id'er.</span><span class="sxs-lookup"><span data-stu-id="d6331-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="d6331-106">Oplysningerne her gælder for alle europæiske lande/områder.</span><span class="sxs-lookup"><span data-stu-id="d6331-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="d6331-107">Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med Tyskland som primær adresse for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="d6331-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="d6331-108">Denne opgave er beregnet til systemadministratorer.</span><span class="sxs-lookup"><span data-stu-id="d6331-108">This task is intended for system administrators.</span></span> <span data-ttu-id="d6331-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="d6331-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d6331-110">Gå til Virksomhedsadministration > Globalt adressekartotek > Registreringstyper > Registreringstyper.</span><span class="sxs-lookup"><span data-stu-id="d6331-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="d6331-111">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d6331-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="d6331-112">Skriv "Moms-id" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d6331-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="d6331-113">Skriv Momsnummer i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d6331-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="d6331-114">Indtast eller vælg værdien DEU i feltet Land/område</span><span class="sxs-lookup"><span data-stu-id="d6331-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="d6331-115">Vælg Ja i feltet Entydig.</span><span class="sxs-lookup"><span data-stu-id="d6331-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="d6331-116">Marker dette afkrydsningsfelt for at kontrollere, om moms-id'et er entydigt.</span><span class="sxs-lookup"><span data-stu-id="d6331-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="d6331-117">Vælg Ja i feltet Primært til land/område.</span><span class="sxs-lookup"><span data-stu-id="d6331-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="d6331-118">Marker dette afkrydsningsfelt, hvis moms-id'et skal gælde for alle de adresser, der hører til det angivne land/område.</span><span class="sxs-lookup"><span data-stu-id="d6331-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="d6331-119">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="d6331-119">Click Create.</span></span>
9. <span data-ttu-id="d6331-120">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d6331-120">Click Add.</span></span>
10. <span data-ttu-id="d6331-121">Indtast eller vælg værdien ITA i feltet Land/område</span><span class="sxs-lookup"><span data-stu-id="d6331-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="d6331-122">Skriv '###########' i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="d6331-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="d6331-123">Når du angiver et registrerings-id af denne type for det valgte land/område, kontrolleres registrerings-id'et i forhold til dette format.</span><span class="sxs-lookup"><span data-stu-id="d6331-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="d6331-124">Marker afkrydsningsfeltet Entydig.</span><span class="sxs-lookup"><span data-stu-id="d6331-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="d6331-125">Marker dette afkrydsningsfelt for at kontrollere, om moms-id'et er entydigt.</span><span class="sxs-lookup"><span data-stu-id="d6331-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="d6331-126">Markér afkrydsningsfeltet Primært til land/område.</span><span class="sxs-lookup"><span data-stu-id="d6331-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="d6331-127">Marker dette afkrydsningsfelt, hvis moms-id'et skal gælde for alle de adresser, der hører til det angivne land/område.</span><span class="sxs-lookup"><span data-stu-id="d6331-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="d6331-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d6331-128">Click Save.</span></span>
15. <span data-ttu-id="d6331-129">Gå til Virksomhedsadministration > Globalt adressekartotek > Registreringstyper > Registreringskategorier.</span><span class="sxs-lookup"><span data-stu-id="d6331-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="d6331-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d6331-130">Click New.</span></span>
17. <span data-ttu-id="d6331-131">Indtast eller vælg Moms-id, DEU i feltet Land/område</span><span class="sxs-lookup"><span data-stu-id="d6331-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="d6331-132">Vælg 'Moms-id' i feltet Registreringskategori.</span><span class="sxs-lookup"><span data-stu-id="d6331-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="d6331-133">Tildel den registreringstype, som du oprettede tidligere, til en foruddefineret registreringskategori.</span><span class="sxs-lookup"><span data-stu-id="d6331-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="d6331-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d6331-134">Click New.</span></span>
20. <span data-ttu-id="d6331-135">Indtast eller vælg Moms-id, ITA i feltet Land/område</span><span class="sxs-lookup"><span data-stu-id="d6331-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="d6331-136">Vælg 'Moms-id' i feltet Registreringskategori.</span><span class="sxs-lookup"><span data-stu-id="d6331-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="d6331-137">Tildel den registreringstype, som du har oprettet, til en foruddefineret registreringskategori.</span><span class="sxs-lookup"><span data-stu-id="d6331-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="d6331-138">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d6331-138">Click Save.</span></span>

