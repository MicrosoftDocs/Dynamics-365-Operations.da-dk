---
title: Afbryde konfigurationer i RCS Global-lageret
description: Dette emne beskriver, hvordan konfigurationer i RCS Global-lageret skal afbrydes.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018727"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="6dda4-103">Afbryde konfigurationer i RCS Global-lageret</span><span class="sxs-lookup"><span data-stu-id="6dda4-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dda4-104">Dette emne beskriver, hvordan konfigurering i RCS Global-lageret skal afbrydes.</span><span class="sxs-lookup"><span data-stu-id="6dda4-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="6dda4-105">Tidligere var det kun muligt at slette konfigurationer, der ikke længere var nødvendige.</span><span class="sxs-lookup"><span data-stu-id="6dda4-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="6dda4-106">Men nu kan du markere en frigivet konfiguration som **Annulleret** i RCS Global-lageret.</span><span class="sxs-lookup"><span data-stu-id="6dda4-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="6dda4-107">Med denne funktionalitet kan du også gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6dda4-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="6dda4-108">Angiv beskeder på forhånd, når en konfiguration er planlagt til ikke længere at være tilladt.</span><span class="sxs-lookup"><span data-stu-id="6dda4-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="6dda4-109">Medtag relevante oplysninger om erstatningskonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6dda4-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="6dda4-110">Angiv en **Understøttet indtil**-dato for den specifikke konfiguration for at informere brugeren om, hvornår den ikke længere vil blive afbrudt.</span><span class="sxs-lookup"><span data-stu-id="6dda4-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="6dda4-111">Når du ikke længere vil bruge en konfigurationsversion, kan du angive følgende valgfrie oplysninger:</span><span class="sxs-lookup"><span data-stu-id="6dda4-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="6dda4-112">**Erstatningskonfiguration**</span><span class="sxs-lookup"><span data-stu-id="6dda4-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="6dda4-113">**Erstatningskonfigurationsversion**</span><span class="sxs-lookup"><span data-stu-id="6dda4-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="6dda4-114">**Fritekstnote**: Brug dette felt til at angive dokumentationslinks eller referencer</span><span class="sxs-lookup"><span data-stu-id="6dda4-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="6dda4-115">**Understøttes indtil**: Dette felt indeholder den foreslåede dato, indtil hvilken den aktuelle konfiguration/version vil blive understøttet.</span><span class="sxs-lookup"><span data-stu-id="6dda4-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="6dda4-116">Denne dato skal opdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="6dda4-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="6dda4-117">Hvis konfigurationen ikke længere skal afbrydes, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="6dda4-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="6dda4-118">Vælg, om du ikke længere vil afbryde en enkelt version eller alle versioner med samme indstillinger i én handling ved at indstille **Alle versioner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6dda4-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="6dda4-119">Angiv parameteren til **Annuller** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6dda4-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="6dda4-120">Vælg **OK**, hvis konfigurationerne ikke længere skal afbrydes.</span><span class="sxs-lookup"><span data-stu-id="6dda4-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="6dda4-121">Feltet **Understøttet indtil** udfyldes, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="6dda4-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Annullere konfigurationsoplysninger](media/Discontinue-details-2.png)
  
<span data-ttu-id="6dda4-123">Du kan altid gendanne konfiguration til **Delt** eller regulere oplysninger, der ikke længere er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="6dda4-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="6dda4-124">Hvis du deler en konfiguration, skal du angive datoen for **Understøttet indtil** og alle andre oplysninger, der vedrører den afbrydelse, der angiver dine planer for fremtidig afbrydelse.</span><span class="sxs-lookup"><span data-stu-id="6dda4-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="6dda4-125">Hvis du vil dele oplysninger om en planlagt afbrydelse, inden konfigurationen faktisk afbrydes, kan brugeren udfylde alle felter, der er relateret til erstatning, men lade parameteren **Annuller** være angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="6dda4-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="6dda4-126">Afbrydelse begrænser ikke handlinger med konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6dda4-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="6dda4-127">Du kan fortsætte med at importere, køre eller afsende konfigurationerne. Disse felter er oplysninger.</span><span class="sxs-lookup"><span data-stu-id="6dda4-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="6dda4-128">Finans understøtter visning af disse oplysninger med start i version 10.0.14</span><span class="sxs-lookup"><span data-stu-id="6dda4-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="6dda4-129">Med start i version 10.0.14 understøtter Dynamics 365 Finance visning af annullerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="6dda4-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="6dda4-130">På siden **Globalt lager** kan du få vist opdaterede oplysninger, der vedrører afbrydelse.</span><span class="sxs-lookup"><span data-stu-id="6dda4-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="6dda4-131">De konfigurationer, der ikke længere afbrydes, filtreres som standard ud.</span><span class="sxs-lookup"><span data-stu-id="6dda4-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="6dda4-132">På siden **Importerede konfigurationer** (ERSolutionTable) vises de konfigurationer, som allerede var afbrudt, da de blev importeret.</span><span class="sxs-lookup"><span data-stu-id="6dda4-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="6dda4-133">For de konfigurationer, der blev afbrudt efter importen, kan de oplysninger, der ikke længere er tilgængelige, synkroniseres ved at køre jobbet **Importer konfigurationsopdateringer**.</span><span class="sxs-lookup"><span data-stu-id="6dda4-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


