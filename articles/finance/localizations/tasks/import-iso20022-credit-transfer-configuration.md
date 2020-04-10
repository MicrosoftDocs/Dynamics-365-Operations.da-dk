---
title: Importere konfiguration for ISO20022-kreditoverførsel
description: Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.
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
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140035"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="d7083-103">Importere konfiguration for ISO20022-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="d7083-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7083-104">Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.</span><span class="sxs-lookup"><span data-stu-id="d7083-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="d7083-105">Det tyske ISO 20022-format for kreditoverførsel bruges som eksempel.</span><span class="sxs-lookup"><span data-stu-id="d7083-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="d7083-106">Denne procedure kan bruges til andre tilgængelige elektroniske rapporteringsformater.</span><span class="sxs-lookup"><span data-stu-id="d7083-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="d7083-107">Denne opgave er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til at udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="d7083-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="d7083-108">Det er den første af fem opgaver, der tilsammen illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d7083-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d7083-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="d7083-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d7083-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d7083-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d7083-111">På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d7083-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="d7083-112">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d7083-112">Click Set active.</span></span>
4. <span data-ttu-id="d7083-113">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d7083-113">Click Repositories.</span></span>
5. <span data-ttu-id="d7083-114">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="d7083-114">Click Open.</span></span>
6. <span data-ttu-id="d7083-115">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="d7083-115">Click Show filters.</span></span>
7. <span data-ttu-id="d7083-116">Anvend følgende filtre: Angiv filterværdien "ISO20022-overførsel (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="d7083-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="d7083-117">Du kan også finde konfigurationen på listen, markere den og derefter flytte den til importopgaven.</span><span class="sxs-lookup"><span data-stu-id="d7083-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="d7083-118">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="d7083-118">Click Import.</span></span>
    * <span data-ttu-id="d7083-119">Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="d7083-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="d7083-120">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="d7083-120">Click Yes.</span></span>

