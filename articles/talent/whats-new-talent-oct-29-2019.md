---
title: Nyheder eller ændringer i Dynamics 365 Talent (29. oktober 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897436"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="13da0-103">Nyheder eller ændringer i Dynamics 365 Talent (29. oktober 2019)</span><span class="sxs-lookup"><span data-stu-id="13da0-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="13da0-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="13da0-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="13da0-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="13da0-105">Changes in Attract</span></span>

<span data-ttu-id="13da0-106">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="13da0-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="13da0-107">Ændringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="13da0-107">Changes in Onboard</span></span>

<span data-ttu-id="13da0-108">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="13da0-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="13da0-109">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="13da0-109">Changes in Core HR</span></span>

<span data-ttu-id="13da0-110">Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="13da0-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="13da0-111">Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="13da0-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="13da0-112">Slet parter uden roller skal være aktiveret som standard (371233)</span><span class="sxs-lookup"><span data-stu-id="13da0-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="13da0-113">Når du klargør et nyt miljø i Talent, skal du **Slette parter uden roller**, hvis der ikke findes nogen roller, der som standard er slået til.</span><span class="sxs-lookup"><span data-stu-id="13da0-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="13da0-114">Når du sletter en arbejder, fjernes den part, der er knyttet til arbejderen, ikke, medmindre denne indstilling er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="13da0-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="13da0-115">Denne ændring begrænser dublerede poster i det globale adressekartotek, når du har brug for at importere, ændre eller genimportere arbejdere.</span><span class="sxs-lookup"><span data-stu-id="13da0-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="13da0-116">Kladder og annullerede orlovsanmodninger skal have tilladelse til at blive slettet i Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="13da0-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="13da0-117">Med denne ændring kan du nu slette orlovsanmodninger med statussen **Kladde** eller **Annulleret** i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13da0-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="13da0-118">Yderligere listeværdier i brugerdefinerede felter afspejles ikke i Common Data Service, når der klikkes på Anvend på brugerdefinerede formularfelter (379599)</span><span class="sxs-lookup"><span data-stu-id="13da0-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="13da0-119">Når du tilføjer nye listeværdier til et eksisterende brugerdefineret felt, der allerede er synkroniseret med Common Data Service, er de nu tilgængelige i Common data service, når du har anvendt ændringerne i formularen **Brugerdefinerede felter** .</span><span class="sxs-lookup"><span data-stu-id="13da0-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="13da0-120">Anvend onboarding-kontrollister på tværs af juridiske enheder, når der findes mere end én ansættelse (371270)</span><span class="sxs-lookup"><span data-stu-id="13da0-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="13da0-121">I denne uges udgivelse kan du anvende kontrollister på medarbejdere med mere end én ansættelse i **Arbejderformular > Checklister**.</span><span class="sxs-lookup"><span data-stu-id="13da0-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="13da0-122">Forhåndsvisning af Åben tilmelding som frynsegoder er blevet fjernet</span><span class="sxs-lookup"><span data-stu-id="13da0-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="13da0-123">Sammen med vores meddelelse i blogindlægget [Strategiske investeringer i Core HR som drivkraft bag ekspertise](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) har Microsoft fjernet frynsegoder som åben tilmeldingsfunktion fra offentlig prøveversion.</span><span class="sxs-lookup"><span data-stu-id="13da0-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="13da0-124">Nye funktioner bliver udgivet i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="13da0-124">New functionality will be released in the future.</span></span> <span data-ttu-id="13da0-125">Produktionsanvendelsen af funktionen åben tilmelding som frynsegoder understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="13da0-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="13da0-126">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="13da0-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="13da0-127">Udskiv performancegennemgange</span><span class="sxs-lookup"><span data-stu-id="13da0-127">Print performance reviews</span></span>

<span data-ttu-id="13da0-128">Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.</span><span class="sxs-lookup"><span data-stu-id="13da0-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="13da0-129">Arbejdsområdet Administration af funktioner</span><span class="sxs-lookup"><span data-stu-id="13da0-129">Feature management workspace</span></span>

<span data-ttu-id="13da0-130">Funktioner tilføjes og opdateres i alle versioner.</span><span class="sxs-lookup"><span data-stu-id="13da0-130">Features are added and updated in every release.</span></span> <span data-ttu-id="13da0-131">Administrationen af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version.</span><span class="sxs-lookup"><span data-stu-id="13da0-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="13da0-132">Nye funktioner er som standard slået fra.</span><span class="sxs-lookup"><span data-stu-id="13da0-132">By default, new features are turned off.</span></span> <span data-ttu-id="13da0-133">Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.</span><span class="sxs-lookup"><span data-stu-id="13da0-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="13da0-134">Du kan få mere at vide om de ændringer, der kommer til funktionsstyring, under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="13da0-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
