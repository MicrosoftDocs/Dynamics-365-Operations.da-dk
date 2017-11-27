---
title: Importere og vedligeholde kreditkorttransaktioner
description: "Dette emne forklarer, hvordan du importerer og vedligeholder udgiftsrelaterede kreditkorttransaktioner. Disse transaktioner kan konfigureres, så de automatisk importeres efter en gentaget plan, eller du kan importere transaktionerne manuelt efter behov."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="b37ec-104">Importere og vedligeholde kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="b37ec-104">Import and maintain credit card transactions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b37ec-105">Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres efter en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="b37ec-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="b37ec-106">Du kan også importere posteringerne manuelt, når det er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="b37ec-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="b37ec-107">Kreditkorttransaktionerne importeres via dataenheden Kreditkorttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b37ec-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="b37ec-108">Du kan finde flere oplysninger om dataenheder under [Dataenheder](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="b37ec-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="b37ec-109">Importér kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="b37ec-109">Import credit card transactions</span></span>

1. <span data-ttu-id="b37ec-110">På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="b37ec-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="b37ec-111">Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataenheder, før du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="b37ec-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="b37ec-112">Indtast en entydig beskrivelse af importjobbet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b37ec-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="b37ec-113">I feltet **Kildedataformat** skal du vælge formatet på den fil, der indeholder kreditkorttransaktionerne, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="b37ec-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="b37ec-114">Vælg **Overfør**, og søg derefter og vælg den fil, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="b37ec-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="b37ec-115">Når filen er blevet overført, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataenheden Kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet.</span><span class="sxs-lookup"><span data-stu-id="b37ec-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="b37ec-116">Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, kan du foretage ændringerne af tilknytningen enten under fanen **Visualisering af tilknytning** eller fanen **Oplysninger om tilknytning** under fanen.</span><span class="sxs-lookup"><span data-stu-id="b37ec-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="b37ec-117">Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret tilbagevendende datajob**.</span><span class="sxs-lookup"><span data-stu-id="b37ec-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="b37ec-118">Du kan derefter angive gentagelsen, der definerer, hvor ofte kreditkorttransaktioner skal importeres.</span><span class="sxs-lookup"><span data-stu-id="b37ec-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="b37ec-119">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="b37ec-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="b37ec-120">Vælg **Importer** for at importere den valgte fil.</span><span class="sxs-lookup"><span data-stu-id="b37ec-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="b37ec-121">Hvis der opstår fejl under importen, kan du se logfilen for udførelsen eller midlertidige data for at få vist de fejl, der skal rettes for at sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="b37ec-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="b37ec-122">Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for hver formattype.</span><span class="sxs-lookup"><span data-stu-id="b37ec-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="b37ec-123">Omfordele fratrådte medarbejderes kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="b37ec-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="b37ec-124">Når en medarbejderpost er afsluttet, deaktiveres medarbejderens Active Directory-domænetjenester (AD DS)-konto.</span><span class="sxs-lookup"><span data-stu-id="b37ec-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="b37ec-125">Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og godtgøres.</span><span class="sxs-lookup"><span data-stu-id="b37ec-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="b37ec-126">Fra siden **Kreditkorttransaktioner** kan du igen tildele medarbejderen enhver kreditkorttransaktion, hvor den tilknyttede medarbejder er fratrådt.</span><span class="sxs-lookup"><span data-stu-id="b37ec-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="b37ec-127">Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Omfordel transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="b37ec-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="b37ec-128">Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="b37ec-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="b37ec-129">Når kreditkorttransaktionerne er blevet tildelt igen, kan de vælges til en udgiftsrapport og betales gennem den normale proces for refusion af udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="b37ec-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

