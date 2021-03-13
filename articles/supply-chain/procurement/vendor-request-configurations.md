---
title: Konfigurationer for kreditoranmodning
description: I dette emne beskrives de felter, der skal udfyldes i en ny kreditoranmodning.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 987b9cefef395b3bf3e915f41232fe0daba213b9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021158"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="6c4aa-103">Konfigurationer for kreditoranmodning</span><span class="sxs-lookup"><span data-stu-id="6c4aa-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c4aa-104">For at fuldføre en kreditoranmodning skal en kontaktperson for kreditoren fuldføre registreringsguiden for den mulige kreditor.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="6c4aa-105">I formularen **Konfigurationer for kreditoranmodning** kan du oprette profiler, der angiver nødvendige og synlige felter i registreringsguiden for den mulige kreditor.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="6c4aa-106">Registreringsguiden begynder med at bede den mulige kreditorbruger, hvilket land/område kreditoren gør forretninger i.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="6c4aa-107">Disse oplysninger bestemmer, hvilken konfiguration der er gældende.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="6c4aa-108">Hvis der ikke er defineret nogen bestemt konfiguration for et land/område, bruges en standardkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="6c4aa-109">Konfigurere en kreditoranmodning</span><span class="sxs-lookup"><span data-stu-id="6c4aa-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="6c4aa-110">Som standard findes der en kreditorkonfiguration i formularen Konfigurationer for kreditoranmodning.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="6c4aa-111">Det er ikke muligt at vælge lande/områder til standardkonfigurationen, så afsnittet **Lande/områder** kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="6c4aa-112">Klik på **Indkøb og forsyning** > **Konfiguration** > **Kreditorer**, og klik derefter på **Konfigurationer for kreditoranmodning**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="6c4aa-113">Klik på fanen **Felter** for at angive status for de angivne felter.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="6c4aa-114">Skjult (ikke-synlig)</span><span class="sxs-lookup"><span data-stu-id="6c4aa-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="6c4aa-115">Vist (synlig, men ikke obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="6c4aa-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="6c4aa-116">Påkrævet (synlig og obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="6c4aa-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="6c4aa-117">Klik på fanen **Indhold** for at angive, om tekst skal vises i guiden, og om der skal være en bekræftelse af, at den mulige kreditorbruger skal acceptere dette, før han eller hun går videre til næste trin i guiden.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="6c4aa-118">Der anmodes om bekræftelsen for de vilkår og betingelser, som brugeren skal acceptere for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="6c4aa-119">Du kan også angive en bekræftelsesmeddelelse, der bliver vist, når guiden er færdig, og du kan føje et eller flere spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="6c4aa-120">Oprette en kreditorkonfiguration for et bestemt land/område</span><span class="sxs-lookup"><span data-stu-id="6c4aa-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="6c4aa-121">Klik på **Indkøb og forsyning** > **Konfiguration** > **Kreditorer**, og klik derefter på **Konfigurationer for kreditoranmodning**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="6c4aa-122">Klik på **Ny** for at oprette en ny konfiguration, og angiv et navn til konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="6c4aa-123">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-123">Click **Save**.</span></span>
4.  <span data-ttu-id="6c4aa-124">Åbn fanen **Lande/områder** for at vælge det land/område, som konfigurationen skal bruges til.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="6c4aa-125">Fuldfør konfigurationen ved at følge retningslinjerne for standardkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-125">Complete the configuration by following the guidelines for the default configuration.</span></span>

