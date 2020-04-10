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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140012"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="88b42-103">Importere ISO20022 Direct Debit-konfiguration</span><span class="sxs-lookup"><span data-stu-id="88b42-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88b42-104">Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kunde.</span><span class="sxs-lookup"><span data-stu-id="88b42-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="88b42-105">Denne procedure bruger formatet ISO 20022 for Direct Debit som eksempel.</span><span class="sxs-lookup"><span data-stu-id="88b42-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="88b42-106">Denne procedure er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til dette formål.</span><span class="sxs-lookup"><span data-stu-id="88b42-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="88b42-107">Det er den første procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="88b42-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="88b42-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="88b42-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="88b42-109">På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88b42-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="88b42-110">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="88b42-110">Click Set active.</span></span>
4. <span data-ttu-id="88b42-111">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88b42-111">Click Repositories.</span></span>
5. <span data-ttu-id="88b42-112">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="88b42-112">Click Open.</span></span>
6. <span data-ttu-id="88b42-113">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="88b42-113">Click Show filters.</span></span>
7. <span data-ttu-id="88b42-114">Anvend følgende filtre: Angiv filterværdien "ISO20022 Direct debit (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="88b42-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="88b42-115">Du kan også finde konfigurationen på listen, vælge den og springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="88b42-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="88b42-116">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="88b42-116">Click Import.</span></span>
    * <span data-ttu-id="88b42-117">Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="88b42-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="88b42-118">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="88b42-118">Click Yes.</span></span>

