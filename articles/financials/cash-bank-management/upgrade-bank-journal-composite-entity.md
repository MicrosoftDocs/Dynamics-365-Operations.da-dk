---
title: Opdater den sammensatte enhed Bankkladde
description: Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565909"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="ffa78-103">Opdater den sammensatte enhed Bankkladde</span><span class="sxs-lookup"><span data-stu-id="ffa78-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffa78-104">Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="ffa78-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="ffa78-105">Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="ffa78-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="ffa78-106">Kompilerer og synkroniserer følgende sammensatte bankkladdeobjekter, objekter, og midlertidige tabeller:</span><span class="sxs-lookup"><span data-stu-id="ffa78-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="ffa78-107">Sammensat enhed\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="ffa78-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="ffa78-108">Enhed\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="ffa78-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="ffa78-109">Enhed\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ffa78-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="ffa78-110">Tabel\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="ffa78-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="ffa78-111">Tabel\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="ffa78-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="ffa78-112">Datastyring\\dataprojekter</span><span class="sxs-lookup"><span data-stu-id="ffa78-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="ffa78-113">Vis typen **Banktransaktion** på **Kildedata-** layout.</span><span class="sxs-lookup"><span data-stu-id="ffa78-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="ffa78-114">Kildedataformat = XML-element</span><span class="sxs-lookup"><span data-stu-id="ffa78-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="ffa78-115">Enhedsnavn = Bankkladde</span><span class="sxs-lookup"><span data-stu-id="ffa78-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="ffa78-116">Upload datafilen = ny version af SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="ffa78-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="ffa78-117">Klik på **Ja** for at overskrive den eksisterende fil.</span><span class="sxs-lookup"><span data-stu-id="ffa78-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="ffa78-118">Klik på **Ja** for at oprette en tilknytning fra grunden.</span><span class="sxs-lookup"><span data-stu-id="ffa78-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="ffa78-119">Kontrollér, at bankposteringstypen er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="ffa78-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="ffa78-120">Klik på **Vis tilknytning** på linjeenhed.</span><span class="sxs-lookup"><span data-stu-id="ffa78-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="ffa78-121">Kontrollér, at bankposteringstypen er knyttet fra Kilde til Midlertidig.</span><span class="sxs-lookup"><span data-stu-id="ffa78-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="ffa78-122">Importér det nye udtog.</span><span class="sxs-lookup"><span data-stu-id="ffa78-122">Import the new statement.</span></span>




