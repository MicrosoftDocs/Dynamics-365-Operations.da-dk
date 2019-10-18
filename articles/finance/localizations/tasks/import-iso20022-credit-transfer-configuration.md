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
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174806"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="add08-103">Importere konfiguration for ISO20022-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="add08-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="add08-104">Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.</span><span class="sxs-lookup"><span data-stu-id="add08-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="add08-105">Det tyske ISO 20022-format for kreditoverførsel bruges som eksempel.</span><span class="sxs-lookup"><span data-stu-id="add08-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="add08-106">Denne procedure kan bruges til andre tilgængelige elektroniske rapporteringsformater.</span><span class="sxs-lookup"><span data-stu-id="add08-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="add08-107">Denne opgave er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til at udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="add08-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="add08-108">Det er den første af fem opgaver, der tilsammen illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="add08-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="add08-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="add08-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="add08-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="add08-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="add08-111">På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.</span><span class="sxs-lookup"><span data-stu-id="add08-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="add08-112">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="add08-112">Click Set active.</span></span>
4. <span data-ttu-id="add08-113">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="add08-113">Click Repositories.</span></span>
5. <span data-ttu-id="add08-114">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="add08-114">Click Open.</span></span>
6. <span data-ttu-id="add08-115">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="add08-115">Click Show filters.</span></span>
7. <span data-ttu-id="add08-116">Anvend følgende filtre: Angiv filterværdien "ISO20022-overførsel (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="add08-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="add08-117">Du kan også finde konfigurationen på listen, markere den og derefter flytte den til importopgaven.</span><span class="sxs-lookup"><span data-stu-id="add08-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="add08-118">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="add08-118">Click Import.</span></span>
    * <span data-ttu-id="add08-119">Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="add08-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="add08-120">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="add08-120">Click Yes.</span></span>

