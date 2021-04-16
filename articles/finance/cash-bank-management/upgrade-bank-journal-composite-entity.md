---
title: Opdater den sammensatte enhed Bankkladde
description: Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819596"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="ec1f9-103">Opdater den sammensatte enhed Bankkladde</span><span class="sxs-lookup"><span data-stu-id="ec1f9-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec1f9-104">Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="ec1f9-105">Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="ec1f9-106">Kompilerer og synkroniserer følgende sammensatte bankkladdeobjekter, objekter, og midlertidige tabeller:</span><span class="sxs-lookup"><span data-stu-id="ec1f9-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="ec1f9-107">Sammensat enhed\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="ec1f9-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="ec1f9-108">Enhed\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="ec1f9-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="ec1f9-109">Enhed\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ec1f9-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="ec1f9-110">Tabel\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="ec1f9-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="ec1f9-111">Tabel\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="ec1f9-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="ec1f9-112">Datastyring\\dataprojekter</span><span class="sxs-lookup"><span data-stu-id="ec1f9-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="ec1f9-113">Vis typen **Banktransaktion** på **Kildedata-** layout.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="ec1f9-114">Kildedataformat = XML-element</span><span class="sxs-lookup"><span data-stu-id="ec1f9-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="ec1f9-115">Enhedsnavn = Bankkladde</span><span class="sxs-lookup"><span data-stu-id="ec1f9-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="ec1f9-116">Upload datafilen = ny version af SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="ec1f9-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="ec1f9-117">Klik på **Ja** for at overskrive den eksisterende fil.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="ec1f9-118">Klik på **Ja** for at oprette en tilknytning fra grunden.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="ec1f9-119">Kontrollér, at bankposteringstypen er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="ec1f9-120">Klik på **Vis tilknytning** på linjeenhed.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="ec1f9-121">Kontrollér, at bankposteringstypen er knyttet fra Kilde til Midlertidig.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="ec1f9-122">Importér det nye udtog.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]