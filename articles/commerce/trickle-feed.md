---
title: Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik
description: I dette emne beskrives den sivende feedbaserede ordreoprettelse til butikstransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991328"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="49c4a-103">Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik</span><span class="sxs-lookup"><span data-stu-id="49c4a-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49c4a-104">I Dynamics 365 Retail version 10.0.4 og tidligere er opgørelsesbogføring en handling ved afslutningen af dagen, og alle transaktioner bogføres i bøgerne sidst på dagen.</span><span class="sxs-lookup"><span data-stu-id="49c4a-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="49c4a-105">Store transaktioner skal derefter behandles i et begrænset tidsvindue, og det kan nogle gange resultere i belastning og låsning og fejl ved bogføring af opgørelse.</span><span class="sxs-lookup"><span data-stu-id="49c4a-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="49c4a-106">Detailhandlere kan heller ikke genkende indtægter og betalinger i deres bøger i løbet af dagen.</span><span class="sxs-lookup"><span data-stu-id="49c4a-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="49c4a-107">Med den sivende feedbaseret ordreoprettelse der blev introduceret i Retail version 10.0.5, behandles transaktionerne i løbet af dagen, og det er kun den økonomiske afstemning af betalingsmidler og andre kassestyringstransaktioner, der behandles ved afslutningen af dagen.</span><span class="sxs-lookup"><span data-stu-id="49c4a-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="49c4a-108">Denne funktion opdeler belastningen fra oprettelsen af salgsordrer, fakturaer og betalinger over hele dagen, hvilket giver en bedre formodet performance og muligheden for at genkende indtægter og betalinger i bøgerne i næsten realtid.</span><span class="sxs-lookup"><span data-stu-id="49c4a-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="49c4a-109">Sådan bruges sivende feedbaseret bogføring</span><span class="sxs-lookup"><span data-stu-id="49c4a-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="49c4a-110">Hvis du vil aktivere sivende feedbaseret bogføring af detailtransaktioner, skal du aktivere funktionen **Detailopgørelser – Sivende feed** ved hjælp af Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="49c4a-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="49c4a-111">Før du aktiverer funktionen, skal du sikre dig, at der ikke er nogen opgørelser, der venter på at blive bogført.</span><span class="sxs-lookup"><span data-stu-id="49c4a-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="49c4a-112">Det aktuelle opgørelsesdokument opdeles i to forskellige typer: transaktionsopgørelse og regnskabsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="49c4a-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="49c4a-113">Transaktionsopgørelsen samler alle ikke-bogførte og validerede transaktioner og opretter salgsordrer, salgsfakturaer, betalings-og rabatkladder og indtægts-/udgiftstransaktioner med den hyppighed, der har konfigureret.</span><span class="sxs-lookup"><span data-stu-id="49c4a-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="49c4a-114">Du skal konfigurere denne proces til at køre med en høj frekvens, så dokumenter oprettes, når transaktionerne overføres til Headquarters via P-jobbet.</span><span class="sxs-lookup"><span data-stu-id="49c4a-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="49c4a-115">Da transaktionsopgørelsen allerede opretter salgsordrer og salgsfakturaer, er det egentlig ikke nødvendigt at konfigurere batchjobbet **Bogfør lager**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="49c4a-116">Du kan dog stadig bruge det til at imødekomme bestemte virksomhedskrav, som du måtte have.</span><span class="sxs-lookup"><span data-stu-id="49c4a-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="49c4a-117">Regnskabet er beregnet til at blive udarbejdet ved dagens afslutning og understøtter kun afslutningsmetoden **Skift**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="49c4a-118">Denne opgørelse vil være begrænset til økonomisk afstemning og vil kun oprette kladder til differencebeløb mellem optalt beløb og posteringsbeløb for de forskellige betalingsmidler, samt kladder til andre kassestyringstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="49c4a-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="49c4a-119">Hvis du vil beregne transaktionsopgørelsen, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn transaktionsopgørelser i batch**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="49c4a-120">Hvis du vil bogføre transaktionsopgørelserne i batch, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør transaktionsopgørelser i batch**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="49c4a-121">Hvis du vil beregne regnskabet, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn regnskaber i batch**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="49c4a-122">Hvis du vil bogføre regnskabet i batch, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør regnskaber i batch**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="49c4a-123">Menupunkterne **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn opgørelser i batch** og **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør opgørelser i batch** fjernes med den nye funktion.</span><span class="sxs-lookup"><span data-stu-id="49c4a-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="49c4a-124">Du kan også oprette forskellige typer af transaktions- og regnskabsopgørelser manuelt.</span><span class="sxs-lookup"><span data-stu-id="49c4a-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="49c4a-125">Gå til **Retail og Commerce > Kanaler > Butikker**, og klik på **Opgørelser**.</span><span class="sxs-lookup"><span data-stu-id="49c4a-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="49c4a-126">Klik på **Ny**, og vælg derefter den type opgørelse, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="49c4a-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="49c4a-127">Felter på siden **Opgørelser** og handlinger under **Opgørelsesgruppe** på siden, viser relevante data og handlinger, der er baseret på den valgte opgørelsestype.</span><span class="sxs-lookup"><span data-stu-id="49c4a-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
