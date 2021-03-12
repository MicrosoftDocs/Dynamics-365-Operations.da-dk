---
title: Importere ISO20022 Direct Debit-konfiguration
description: Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kunde.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68e5a63ea3b037cc111d6732857f0aae1ce7e5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989943"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="24b53-103">Importere ISO20022 Direct Debit-konfiguration</span><span class="sxs-lookup"><span data-stu-id="24b53-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24b53-104">Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kunde.</span><span class="sxs-lookup"><span data-stu-id="24b53-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="24b53-105">Denne procedure bruger formatet ISO 20022 for Direct Debit som eksempel.</span><span class="sxs-lookup"><span data-stu-id="24b53-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="24b53-106">Denne procedure er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til dette formål.</span><span class="sxs-lookup"><span data-stu-id="24b53-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="24b53-107">Det er den første procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="24b53-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="24b53-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="24b53-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="24b53-109">På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24b53-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="24b53-110">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="24b53-110">Click Set active.</span></span>
4. <span data-ttu-id="24b53-111">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="24b53-111">Click Repositories.</span></span>
5. <span data-ttu-id="24b53-112">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="24b53-112">Click Open.</span></span>
6. <span data-ttu-id="24b53-113">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="24b53-113">Click Show filters.</span></span>
7. <span data-ttu-id="24b53-114">Anvend følgende filtre: Angiv filterværdien "ISO20022 Direct debit (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="24b53-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="24b53-115">Du kan også finde konfigurationen på listen, vælge den og springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="24b53-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="24b53-116">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="24b53-116">Click Import.</span></span>
    * <span data-ttu-id="24b53-117">Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="24b53-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="24b53-118">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="24b53-118">Click Yes.</span></span>

