---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.6. november 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909323"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="517a0-103">Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.6. november 2019)</span><span class="sxs-lookup"><span data-stu-id="517a0-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="517a0-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="517a0-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="517a0-105">Denne version har et build-nummer på 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="517a0-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="517a0-106">Når den generelle tilgængelighedsdato er november, er de nye funktioner tilgængelige til tidlig frigivelse i oktober.</span><span class="sxs-lookup"><span data-stu-id="517a0-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="517a0-107">Du kan få flere oplysninger om version 10.0.6 i [Yderligere ressourcer](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="517a0-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="517a0-108">V2-dataenhed i produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="517a0-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="517a0-109">Der udgives en anden version til dataenheden "produktkonfigurationsmodeller" (kaldet "Produktkonfigurationsmodeller V2 ").</span><span class="sxs-lookup"><span data-stu-id="517a0-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="517a0-110">Standardskabelonen "418-produktkonfigurationsmodeller" er også nødvendig, så den bruger den nye enhed "produktkonfigurationsmodeller v2"-dataenhed i import/eksport af Framework-skabelonerne.</span><span class="sxs-lookup"><span data-stu-id="517a0-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="517a0-111">Skabelonen opdateres ikke automatisk, så du skal indlæse skabelonen fra standarden manuelt.</span><span class="sxs-lookup"><span data-stu-id="517a0-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="517a0-112">V2-enheden eksporterer en række som en separat fil i en vedhæftet fil i stedet for indlejret og løser derfor størrelsesbegrænsningerne for V1-enheden.</span><span class="sxs-lookup"><span data-stu-id="517a0-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="517a0-113">Hvad skal du gøre for at foretage denne ændring?</span><span class="sxs-lookup"><span data-stu-id="517a0-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="517a0-114">Når v1-enheden er blevet udfaset, skal du starte med at overflytte fra V1 til V2.</span><span class="sxs-lookup"><span data-stu-id="517a0-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="517a0-115">Hvis du bruger skabelonen "418-produktkonfigurationsmodeller", kan du klikke på knappen "Indlæs standardskabeloner" og derefter genindlæse skabelonen "418 – produktkonfigurationsmodeller"</span><span class="sxs-lookup"><span data-stu-id="517a0-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="517a0-116">Hvis du har brug for at bevare kompatibiliteten med eksisterende systemer, kan du nu fortsætte med at bruge den eksisterende skabelon og den (udfasede) V1-enhed, indtil du flytter integrationerne til den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="517a0-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="517a0-117">Forbedringer af funktionsstyringen</span><span class="sxs-lookup"><span data-stu-id="517a0-117">Feature management enhancements</span></span>
<span data-ttu-id="517a0-118">Med funktionsstyring kan du nu aktivere alle nye funktioner, kræve en bekræftelse for at aktivere en funktion og aktivere alle funktioner, der ikke allerede er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="517a0-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="517a0-119">Ansvarlig part for købsaftale</span><span class="sxs-lookup"><span data-stu-id="517a0-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="517a0-120">Nu har du mulighed for at definere primære og sekundære ansvarlige parter i formularen Købsaftaleklassifikation og de resulterede købsaftaler.</span><span class="sxs-lookup"><span data-stu-id="517a0-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="517a0-121">Det giver brugeren adgang til, hvem der har ansvaret for aftalerne.</span><span class="sxs-lookup"><span data-stu-id="517a0-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="517a0-122">RFO-link på linjen Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="517a0-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="517a0-123">Du kan føje et referencelink fra indkøbsordrelinjerne tilbage til de tilsvarende RFO-linjer, som de stammer fra, så brugeren nemt kan få adgang til det understøttende dokument til anmodning om tilbud.</span><span class="sxs-lookup"><span data-stu-id="517a0-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="517a0-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="517a0-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="517a0-125">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="517a0-125">Bug fixes</span></span>
<span data-ttu-id="517a0-126">Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.6, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="517a0-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="517a0-127">Platform update 30</span><span class="sxs-lookup"><span data-stu-id="517a0-127">Platform update 30</span></span>
<span data-ttu-id="517a0-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 indeholder platformsopdatering 30.</span><span class="sxs-lookup"><span data-stu-id="517a0-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="517a0-129">Hvis du vil vide mere om platformsopdatering 30, kan du se [Nyheder eller ændringer i platformsopdatering 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="517a0-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="517a0-130">Dynamics 365: 2019-frigivelsesplan bølge 2</span><span class="sxs-lookup"><span data-stu-id="517a0-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="517a0-131">Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?</span><span class="sxs-lookup"><span data-stu-id="517a0-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="517a0-132">Se [Dynamics 365: 2019-frigivelsesplan bølge 2](/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="517a0-132">Check out the [Dynamics 365: 2019 release wave 2 plan](/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="517a0-133">Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.</span><span class="sxs-lookup"><span data-stu-id="517a0-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="517a0-134">Fjernede og udfasede Supply Chain Management-funktioner</span><span class="sxs-lookup"><span data-stu-id="517a0-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="517a0-135">Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="517a0-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="517a0-136">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="517a0-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="517a0-137">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="517a0-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="517a0-138">Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.</span><span class="sxs-lookup"><span data-stu-id="517a0-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="517a0-139">For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="517a0-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="517a0-140">Det er typisk funktionelle opdateringer, der skal foretages i compileren.</span><span class="sxs-lookup"><span data-stu-id="517a0-140">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]