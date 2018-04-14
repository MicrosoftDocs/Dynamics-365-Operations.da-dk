---
title: Genbrug produktkonfigurationer
description: "Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt. Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg. Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b9e73f1dec1bc36431227e165d86b7ce052af3be
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="ede04-105">Genbrug produktkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="ede04-105">Reuse product configurations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ede04-106">Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt.</span><span class="sxs-lookup"><span data-stu-id="ede04-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="ede04-107">Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="ede04-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="ede04-108">Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute.</span><span class="sxs-lookup"><span data-stu-id="ede04-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="ede04-109">Krav til genbrug af konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ede04-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="ede04-110">Hvis du vil aktivere konfigurationer, der kan genbruges, skal du angive følgende oplysninger for komponenter og attributter på siden **Oplysninger om produktkonfigurationsmodel**:</span><span class="sxs-lookup"><span data-stu-id="ede04-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="ede04-111">**Komponenter og underkomponenter** – I oversigtspanelet **Generelt** skal du vælge **Ja** i feltet **Genbrug konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ede04-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="ede04-112">**Attributter** – I **Attributter**-oversigtspanelet skal du vælge **Medtag i genbrug**-indstillingen.</span><span class="sxs-lookup"><span data-stu-id="ede04-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="ede04-113">Denne indstilling vises kun, når den relaterede komponent er aktiveret til genbrug.</span><span class="sxs-lookup"><span data-stu-id="ede04-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="ede04-114">Hvis du ikke vælger nogen attributter til genbrug, genbruges konfigurationen altid, uanset brugerens valg under en konfigurationssession.</span><span class="sxs-lookup"><span data-stu-id="ede04-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="ede04-115">Attributværdierne i den eksisterende konfiguration skal svare til brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="ede04-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="ede04-116">Hvis brugeren f.eks. vælger farven **Blå** under en konfigurationssession, kontrollerer systemet, om en eksisterende konfiguration af den pågældende komponent har en attribut for blå farve.</span><span class="sxs-lookup"><span data-stu-id="ede04-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="ede04-117">Nulstilling af konfigurationsgenbrug</span><span class="sxs-lookup"><span data-stu-id="ede04-117">Resetting configuration reuse</span></span>
<span data-ttu-id="ede04-118">Når du nulstiller konfigurationsgenbrug, bruges tidligere oprettede konfigurationer ikke længere.</span><span class="sxs-lookup"><span data-stu-id="ede04-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="ede04-119">Du kan nulstille konfigurationsgenbrug, hvis styklisten eller ruten er ændret, men ingen relaterede attributter blev ændret.</span><span class="sxs-lookup"><span data-stu-id="ede04-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="ede04-120">Du nulstiller konfigurationsgenbrug i **Generelt**-oversigtspanelet for komponenten.</span><span class="sxs-lookup"><span data-stu-id="ede04-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




