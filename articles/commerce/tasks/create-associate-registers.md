---
title: " Oprette og tilknytte registre"
description: Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ac75d390b8bbb94c6e039b374b51462d348e355
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057144"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="bcfc6-103"> Oprette og tilknytte registre</span><span class="sxs-lookup"><span data-stu-id="bcfc6-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bcfc6-104">Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="bcfc6-105">Denne procedure bruger demodatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="bcfc6-106">Gå til Retail og Commerce> Konfiguration af kanal > POS-opsætning > Kasseapparater.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="bcfc6-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-107">Click New.</span></span>
3. <span data-ttu-id="bcfc6-108">Indtast et id til den nye kasse i feltet Kassenummer.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="bcfc6-109">Kasse-id'et indeholder typisk koder, der kan hjælpe med at knytte kassen til den butik, som den tilhører, og placeringen i butikken.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="bcfc6-110">Skriv et beskrivende navn til kassen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="bcfc6-111">Indtast eller vælg en værdi i feltet Butiksnummer.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="bcfc6-112">Indtast eller vælg en værdi i feltet Hardwareprofil.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfc6-113">Hardwareprofiler bruges til at angive de eksterne enheder, der skal knyttes til kassen, f.eks. pengeskuffen og bonprinteren.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="bcfc6-114">Indtast eller vælg en værdi i feltet Visuel profil.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfc6-115">Visuelle profiler bruges til at angive de billeder, der bruges i POS-baggrunden og på logonside samt temaer for POS.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="bcfc6-116">Skriv en værdi i feltet Autorisationskode - POS-kasseapparatnummer.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="bcfc6-117">Autorisationskode – POS-kasseapparatnummer bruges til at informere betalingsprocessor om, hvilken betalingsterminal der sender anmodninger om godkendelse.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="bcfc6-118">Denne værdi kaldes ofte "Terminal-id" eller "TID".</span><span class="sxs-lookup"><span data-stu-id="bcfc6-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="bcfc6-119">TID findes normalt på en mærkat på betalingsenheden.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="bcfc6-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcfc6-120">Click Save.</span></span>

