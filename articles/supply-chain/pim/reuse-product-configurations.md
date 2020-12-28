---
title: Genbrug produktkonfigurationer
description: Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt. Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg. Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd6d730528522f4074b6e2a3ce6059cc12ff5a0f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424397"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="07b36-105">Genbrug produktkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="07b36-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07b36-106">Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt.</span><span class="sxs-lookup"><span data-stu-id="07b36-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="07b36-107">Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="07b36-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="07b36-108">Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute.</span><span class="sxs-lookup"><span data-stu-id="07b36-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="07b36-109">Krav til genbrug af konfigurationer</span><span class="sxs-lookup"><span data-stu-id="07b36-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="07b36-110">Hvis du vil aktivere konfigurationer, der kan genbruges, skal du angive følgende oplysninger for komponenter og attributter på siden **Oplysninger om produktkonfigurationsmodel**:</span><span class="sxs-lookup"><span data-stu-id="07b36-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="07b36-111">**Komponenter og underkomponenter** – I oversigtspanelet **Generelt** skal du vælge **Ja** i feltet **Genbrug konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="07b36-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="07b36-112">**Attributter** – I **Attributter**-oversigtspanelet skal du vælge **Medtag i genbrug**-indstillingen.</span><span class="sxs-lookup"><span data-stu-id="07b36-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="07b36-113">Denne indstilling vises kun, når den relaterede komponent er aktiveret til genbrug.</span><span class="sxs-lookup"><span data-stu-id="07b36-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="07b36-114">Hvis du ikke vælger nogen attributter til genbrug, genbruges konfigurationen altid, uanset brugerens valg under en konfigurationssession.</span><span class="sxs-lookup"><span data-stu-id="07b36-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="07b36-115">Attributværdierne i den eksisterende konfiguration skal svare til brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="07b36-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="07b36-116">Hvis brugeren f.eks. vælger farven **Blå** under en konfigurationssession, kontrollerer systemet, om en eksisterende konfiguration af den pågældende komponent har en attribut for blå farve.</span><span class="sxs-lookup"><span data-stu-id="07b36-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="07b36-117">Nulstilling af konfigurationsgenbrug</span><span class="sxs-lookup"><span data-stu-id="07b36-117">Resetting configuration reuse</span></span>
<span data-ttu-id="07b36-118">Når du nulstiller konfigurationsgenbrug, bruges tidligere oprettede konfigurationer ikke længere.</span><span class="sxs-lookup"><span data-stu-id="07b36-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="07b36-119">Du kan nulstille konfigurationsgenbrug, hvis styklisten eller ruten er ændret, men ingen relaterede attributter blev ændret.</span><span class="sxs-lookup"><span data-stu-id="07b36-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="07b36-120">Du nulstiller konfigurationsgenbrug i **Generelt**-oversigtspanelet for komponenten.</span><span class="sxs-lookup"><span data-stu-id="07b36-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>



