--- 
title: "Importere konfiguration for ISO20022-kreditoverførsel"
description: Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="27966-103">Importere konfiguration for ISO20022-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="27966-103">Import ISO20022 credit transfer configuration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27966-104">Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.</span><span class="sxs-lookup"><span data-stu-id="27966-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="27966-105">Det tyske ISO 20022-format for kreditoverførsel bruges som eksempel.</span><span class="sxs-lookup"><span data-stu-id="27966-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="27966-106">Denne procedure kan bruges til andre tilgængelige elektroniske rapporteringsformater.</span><span class="sxs-lookup"><span data-stu-id="27966-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="27966-107">Denne opgave er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til at udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="27966-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="27966-108">Det er den første af fem opgaver, der tilsammen illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="27966-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="27966-109">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="27966-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="27966-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="27966-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="27966-111">På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27966-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="27966-112">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="27966-112">Click Set active.</span></span>
4. <span data-ttu-id="27966-113">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="27966-113">Click Repositories.</span></span>
5. <span data-ttu-id="27966-114">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="27966-114">Click Open.</span></span>
6. <span data-ttu-id="27966-115">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="27966-115">Click Show filters.</span></span>
7. <span data-ttu-id="27966-116">Anvend følgende filtre: Angiv filterværdien "ISO20022-overførsel (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="27966-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="27966-117">Du kan også finde konfigurationen på listen, markere den og derefter flytte den til importopgaven.</span><span class="sxs-lookup"><span data-stu-id="27966-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="27966-118">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="27966-118">Click Import.</span></span>
    * <span data-ttu-id="27966-119">Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="27966-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="27966-120">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="27966-120">Click Yes.</span></span>


