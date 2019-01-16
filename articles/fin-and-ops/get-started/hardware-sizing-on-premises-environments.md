---
title: "Krav til tilpasning af hardware til lokale miljøer"
description: "Krav til tilpasning af hardware til lokale miljøer"
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: d277bc4c4c815317bade8a04b9111232fb707086
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2018

---

# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="b1f21-103">Krav til tilpasning af hardware til lokale miljøer</span><span class="sxs-lookup"><span data-stu-id="b1f21-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1f21-104">Før du begynder at tilpasse hardware og infrastruktur til et lokalt miljø, skal du sætte dig ind i [Systemkrav](system-requirements.md) og læse [Vejledning til installation og implementering](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) for at få en ordentlig forståelse af den underliggende struktur.</span><span class="sxs-lookup"><span data-stu-id="b1f21-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="b1f21-105">Vær særligt opmærksom på best practices for opsætning af systemet for at opnå optimal ydelse.</span><span class="sxs-lookup"><span data-stu-id="b1f21-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="b1f21-106">Når du har gennemgået dokumentationen, kan du begynde at vurdere dit antal af transaktioner og samtidige brugere og tilpasse dit miljø baseret på det gennemsnitlige systemgennemløb.</span><span class="sxs-lookup"><span data-stu-id="b1f21-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="b1f21-107">Faktorer, der påvirker kapacitet</span><span class="sxs-lookup"><span data-stu-id="b1f21-107">Factors that affect sizing</span></span>

<span data-ttu-id="b1f21-108">Alle faktorer, der er vist i følgende illustration, skal tages i betragtning, når du vurderer hardwarens størrelse eller kapacitet.</span><span class="sxs-lookup"><span data-stu-id="b1f21-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="b1f21-109">Jo mere detaljerede oplysninger, der indsamles, desto mere præcist kan du bestemme størrelsen.</span><span class="sxs-lookup"><span data-stu-id="b1f21-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="b1f21-110">Hvis du vurderer hardwarestørrelsen uden understøttende data, bliver resultatet næppe nøjagtigt.</span><span class="sxs-lookup"><span data-stu-id="b1f21-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="b1f21-111">Det absolutte minimumkrav for de nødvendige data er spidsbelastningen pr. transaktionslinje pr. time.</span><span class="sxs-lookup"><span data-stu-id="b1f21-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="b1f21-112">[![Tilpasning af hardware til lokale miljøer](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="b1f21-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="b1f21-113">Set fra venstre mod højre er den første og vigtigste faktor, der er nødvendig for at anslå den korrekte størrelse, er en transaktionsprofil eller transaktionsbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b1f21-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="b1f21-114">Det er vigtigt altid at finde spidsbelastningen for transaktionsvolumen pr. time.</span><span class="sxs-lookup"><span data-stu-id="b1f21-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="b1f21-115">Hvis der er flere perioder med spidsbelastning, skal disse perioder defineres korrekt.</span><span class="sxs-lookup"><span data-stu-id="b1f21-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="b1f21-116">Efterhånden som du forstår i, hvilken belastning der har indflydelse på infrastrukturen, skal du også have en mere detaljeret forståelse af disse faktorer:</span><span class="sxs-lookup"><span data-stu-id="b1f21-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="b1f21-117">**Transaktioner** – Transaktioner har typisk visse toppe i dagens/ugens løb.</span><span class="sxs-lookup"><span data-stu-id="b1f21-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="b1f21-118">Dette afhænger hovedsageligt af transaktionstypen.</span><span class="sxs-lookup"><span data-stu-id="b1f21-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="b1f21-119">Tids- og udgiftsposter topper normalt én gang om ugen, mens salgordreposteringer ofte foregår samlet via integration eller kommer lidt efter lidt i løbet af dagen.</span><span class="sxs-lookup"><span data-stu-id="b1f21-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="b1f21-120">**Antal samtidige brugere** – Antallet af samtidige brugere er den næstvigtigste faktor ved tilpasning af størrelse.</span><span class="sxs-lookup"><span data-stu-id="b1f21-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="b1f21-121">Du kan ikke få pålidelige størrelsesestimater, der er baseret på antallet af samtidige brugere, så hvis du kun har disse data til rådighed, skal du anslå et omtrentligt antal og derefter genoverveje dette, når du har flere data.</span><span class="sxs-lookup"><span data-stu-id="b1f21-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="b1f21-122">En nøjagtig definition af samtidige brugere indebærer, at:</span><span class="sxs-lookup"><span data-stu-id="b1f21-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="b1f21-123">Navngivne brugere ikke er samtidige brugere.</span><span class="sxs-lookup"><span data-stu-id="b1f21-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="b1f21-124">Samtidige brugere altid er et undersæt af navngivne brugere.</span><span class="sxs-lookup"><span data-stu-id="b1f21-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="b1f21-125">Spidsbelastning definerer den maksimale samtidighed ved størrelsestilpasning.</span><span class="sxs-lookup"><span data-stu-id="b1f21-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="b1f21-126">Kriterier for samtidige brugere er, at brugeren opfylder alle følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="b1f21-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="b1f21-127">Er logget på.</span><span class="sxs-lookup"><span data-stu-id="b1f21-127">Logged on.</span></span>
    - <span data-ttu-id="b1f21-128">Arbejder med transaktioner/forespørgsler på tidspunktet for optælling.</span><span class="sxs-lookup"><span data-stu-id="b1f21-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="b1f21-129">Ikke en inaktiv session.</span><span class="sxs-lookup"><span data-stu-id="b1f21-129">Not an idle session.</span></span>

- <span data-ttu-id="b1f21-130">**Datakomposition** – Dette drejer sig primært om, hvordan systemet bliver indstillet og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="b1f21-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="b1f21-131">F.eks. hvor mange juridiske enheder, du skal have, hvor mange varer, hvor mange styklisteniveauer, og hvor kompleks konfigurationen af sikkerheden bliver.</span><span class="sxs-lookup"><span data-stu-id="b1f21-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="b1f21-132">Hver af disse faktorer kan påvirke ydeevnen en lille smule, så disse faktorer kan blive udlignet ved hjælp af intelligent valgmuligheder, når det drejer sig om infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="b1f21-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="b1f21-133">**Udvidelser** – Tilpasninger kan være simple eller komplekse.</span><span class="sxs-lookup"><span data-stu-id="b1f21-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="b1f21-134">Antallet af tilpasninger og arten af kompleksitet og forbrug har varierende indflydelse på størrelsen af den nødvendige infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="b1f21-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="b1f21-135">For komplekse tilpasninger anbefales det at foretage en evaluering af ydeevnen for at sikre, at de ikke kun testes for effektiviteten, men også gør det lettere at forstå infrastrukturbehovene.</span><span class="sxs-lookup"><span data-stu-id="b1f21-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="b1f21-136">Dette er endnu vigtigere, når udvidelserne ikke er kodet i overensstemmelse med best practices for ydeevne og skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="b1f21-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="b1f21-137">**Rapportering og analyser** – Disse faktorer omfatter typisk kørsel af komplekse forespørgsler i de forskellige databaser i Finance and Operations-databasesystemer.</span><span class="sxs-lookup"><span data-stu-id="b1f21-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</span></span> <span data-ttu-id="b1f21-138">Når du ved kørsel af dyre rapporter forstår og kan reducere hyppigheden, kan du også bedre forstå virkningen af dem.</span><span class="sxs-lookup"><span data-stu-id="b1f21-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="b1f21-139">**Løsninger fra tredjepart** – For disse løsninger, f.eks. fra softwareproducenter, gælder samme implikationer og anbefalinger som for udvidelser.</span><span class="sxs-lookup"><span data-stu-id="b1f21-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-finance-and-operations-environment"></a><span data-ttu-id="b1f21-140">Tilpasse dit Finance and Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="b1f21-140">Sizing your Finance and Operations environment</span></span>

<span data-ttu-id="b1f21-141">For at kende kravene til størrelsestilpasning skal du kende det maksimale antal transaktioner, som du har brug for at behandle.</span><span class="sxs-lookup"><span data-stu-id="b1f21-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="b1f21-142">De fleste hjælpesystemer, som Management Reporter eller SSRS, er mindre missionskritiske.</span><span class="sxs-lookup"><span data-stu-id="b1f21-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="b1f21-143">Derfor fokuseres der oftest på AOS og SQL Server i dette dokument.</span><span class="sxs-lookup"><span data-stu-id="b1f21-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="b1f21-144">Generelt udskaleres beregningsniveauerne og skal være konfigureret som N + 1, dvs. at hvis du beregner tre AOS, skal du tilføje en fjerde AOS.</span><span class="sxs-lookup"><span data-stu-id="b1f21-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="b1f21-145">Databaseniveauet skal konfigureres i en Always On-opsætning med høj tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="b1f21-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="b1f21-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="b1f21-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="b1f21-147">Størrelsestilpasning</span><span class="sxs-lookup"><span data-stu-id="b1f21-147">Sizing</span></span>

- <span data-ttu-id="b1f21-148">3K og 15K transaktionslinjer pr. time, pr. processorkerne på DB-server.</span><span class="sxs-lookup"><span data-stu-id="b1f21-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="b1f21-149">Typisk AOS-til-SQL-kerneforhold 3:1 for den primære SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b1f21-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="b1f21-150">Ekstra kerner er påkrævet, baseret på den valgte højtilgængelighedskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b1f21-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="b1f21-151">Behandling af handlinger, der trækker meget på databasen, kan sætte dette tilbage til 2:1.</span><span class="sxs-lookup"><span data-stu-id="b1f21-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="b1f21-152">Følgende faktorer påvirker variationer:</span><span class="sxs-lookup"><span data-stu-id="b1f21-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="b1f21-153">Aktuelt anvendte parameterindstillinger.</span><span class="sxs-lookup"><span data-stu-id="b1f21-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="b1f21-154">Udvidelsesniveauer.</span><span class="sxs-lookup"><span data-stu-id="b1f21-154">Levels of extensions.</span></span>
    - <span data-ttu-id="b1f21-155">Brug af flere funktioner, f.eks. databaselog og påmindelser.</span><span class="sxs-lookup"><span data-stu-id="b1f21-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="b1f21-156">Ekstremt omfang af databaselogning reducerer yderligere gennemløbet pr. time pr. processorkerne under 3K linjer.</span><span class="sxs-lookup"><span data-stu-id="b1f21-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="b1f21-157">Kompleksiteten af datasammensætningen – En simpel kontoplan kontra en detaljeret kontoplan f.eks. har konsekvenser for gennemløbet.</span><span class="sxs-lookup"><span data-stu-id="b1f21-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="b1f21-158">Transaktionsbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b1f21-158">Transaction characterization.</span></span>
    - <span data-ttu-id="b1f21-159">2 GB til 4 GB hukommelse for hver kerne.</span><span class="sxs-lookup"><span data-stu-id="b1f21-159">2 GB to 4 GB memory for each core.</span></span>
    - <span data-ttu-id="b1f21-160">Ekstra databaser på DB-server som f.eks. Management Reporter og SSRS-databaser.</span><span class="sxs-lookup"><span data-stu-id="b1f21-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="b1f21-161">Temp DB = 15 % af DB størrelse, med lige så mange filer som fysiske processorer.</span><span class="sxs-lookup"><span data-stu-id="b1f21-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="b1f21-162">SAN-størrelse og -gennemløb baseret på det samlede antal/brug af samtidige transaktioner.</span><span class="sxs-lookup"><span data-stu-id="b1f21-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="b1f21-163">Høj tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="b1f21-163">High availability</span></span>

<span data-ttu-id="b1f21-164">Vi anbefaler altid at benytte SQL Server i en klynge- eller spejlingskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b1f21-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="b1f21-165">Den sekundære SQL-node skal have det samme antal kerner, som den primære node.</span><span class="sxs-lookup"><span data-stu-id="b1f21-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="b1f21-166">Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="b1f21-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="b1f21-167">Du kan finde oplysninger om tilpasning af AD FS størrelse i [Dokumentationen til AD FS-serverkapacitet](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="b1f21-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="b1f21-168">Du kan finde et [størrelsestilpasningsregneark](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) til planlægning af antallet af forekomster i installationen.</span><span class="sxs-lookup"><span data-stu-id="b1f21-168">A [sizing spreadsheet](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="b1f21-169">AOS (Online og batch)</span><span class="sxs-lookup"><span data-stu-id="b1f21-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="b1f21-170">Størrelsestilpasning</span><span class="sxs-lookup"><span data-stu-id="b1f21-170">Sizing</span></span>

- <span data-ttu-id="b1f21-171">Tilpasning efter antal/brug af transaktioner</span><span class="sxs-lookup"><span data-stu-id="b1f21-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="b1f21-172">2K til 6K linjer pr. processorkerne</span><span class="sxs-lookup"><span data-stu-id="b1f21-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="b1f21-173">16 GB pr. forekomst</span><span class="sxs-lookup"><span data-stu-id="b1f21-173">16 GB per instance</span></span>
    - <span data-ttu-id="b1f21-174">Standardpakke – 4-24 kerner</span><span class="sxs-lookup"><span data-stu-id="b1f21-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="b1f21-175">10-15 Enterprise-brugere pr. processorkerne</span><span class="sxs-lookup"><span data-stu-id="b1f21-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="b1f21-176">15-25 Activity-brugere pr. processorkerne</span><span class="sxs-lookup"><span data-stu-id="b1f21-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="b1f21-177">25-50 teammedlemmer pr. processorkerne</span><span class="sxs-lookup"><span data-stu-id="b1f21-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="b1f21-178">Batch</span><span class="sxs-lookup"><span data-stu-id="b1f21-178">Batch</span></span>

    - <span data-ttu-id="b1f21-179">1 til 4 batchtråde pr. processorkerne</span><span class="sxs-lookup"><span data-stu-id="b1f21-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="b1f21-180">Størrelse baseret på en beskrivelse af batchvindue</span><span class="sxs-lookup"><span data-stu-id="b1f21-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="b1f21-181">Bemærk, at AOS, Datastyring og Batch er i den samme rolle i Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b1f21-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="b1f21-182">Du skal tilpasse størrelsen for disse tre arbejdsbyrder samlet og ikke adskille dem som i Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="b1f21-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="b1f21-183">De samme variationsfaktorer som for SQL Server gælder her.</span><span class="sxs-lookup"><span data-stu-id="b1f21-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="b1f21-184">Høj tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="b1f21-184">High availability</span></span>

- <span data-ttu-id="b1f21-185">Sørg for at have mindst 1 til 2 flere AOS'er tilgængelig, end du beregner.</span><span class="sxs-lookup"><span data-stu-id="b1f21-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="b1f21-186">Sørg for at have mindst 3 til 4 tilgængelige virtuelle værter.</span><span class="sxs-lookup"><span data-stu-id="b1f21-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="b1f21-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="b1f21-187">Management reporter</span></span>

<span data-ttu-id="b1f21-188">I de fleste tilfælde bør de anbefalede minimumkrav med to noder være velegnet, medmindre anvendelsesomfanget er særlig stort.</span><span class="sxs-lookup"><span data-stu-id="b1f21-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="b1f21-189">Kun i tilfælde med ekstraordinær stor anvendelse har du brug for mere end to noder.</span><span class="sxs-lookup"><span data-stu-id="b1f21-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="b1f21-190">Skaler efter behov.</span><span class="sxs-lookup"><span data-stu-id="b1f21-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="b1f21-191">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="b1f21-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="b1f21-192">I versionen til almindelig tilgængelighed kan kun én SSRS-node installeres.</span><span class="sxs-lookup"><span data-stu-id="b1f21-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="b1f21-193">Overvåg SSRS-noden under test, og øg antallet af kerner, der er tilgængelige for SSRS, på grundlag af behovet.</span><span class="sxs-lookup"><span data-stu-id="b1f21-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="b1f21-194">Sørg for at have en forudkonfigureret sekundær node på en virtuel vært, som er forskellig fra SSRS VM'en.</span><span class="sxs-lookup"><span data-stu-id="b1f21-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="b1f21-195">Det er vigtigt, hvis der er et problem med den virtuelle maskine, der er vært for SSRS, eller den virtuelle vært.</span><span class="sxs-lookup"><span data-stu-id="b1f21-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="b1f21-196">Hvis det er tilfældet, skal den udskiftes.</span><span class="sxs-lookup"><span data-stu-id="b1f21-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="b1f21-197">Miljø-Orchestrator</span><span class="sxs-lookup"><span data-stu-id="b1f21-197">Environment Orchestrator</span></span>

<span data-ttu-id="b1f21-198">Tjenesten Orchestrator er den tjeneste, der styrer installationen og den relaterede kommunikation med LCS.</span><span class="sxs-lookup"><span data-stu-id="b1f21-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="b1f21-199">Denne tjeneste installeres som den primære Service Fabric-tjeneste og kræver mindst tre VM'er.</span><span class="sxs-lookup"><span data-stu-id="b1f21-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="b1f21-200">Tjenesten er placeret sammen med Service Fabric Orchestration-tjenesterne.</span><span class="sxs-lookup"><span data-stu-id="b1f21-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="b1f21-201">Dette og skal tilpasses klyngens spidsbelastning.</span><span class="sxs-lookup"><span data-stu-id="b1f21-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="b1f21-202">Yderligere oplysninger finder du i [Overvejelser i forbindelse med planlægning af Service Fabric-klyngekapacitet](/azure/service-fabric/service-fabric-cluster-capacity).</span><span class="sxs-lookup"><span data-stu-id="b1f21-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="b1f21-203">Virtualisering og overtegning</span><span class="sxs-lookup"><span data-stu-id="b1f21-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="b1f21-204">Missionskritiske tjenester som AOS skal hostes på virtuelle værter, der har dedikerede ressourcer – kerner, hukommelse og diskplads.</span><span class="sxs-lookup"><span data-stu-id="b1f21-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>

