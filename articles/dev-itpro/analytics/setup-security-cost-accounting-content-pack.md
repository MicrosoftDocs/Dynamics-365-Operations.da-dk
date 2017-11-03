---
title: Konfigurer sikkerhed for omkostningsregnskabsanalyse af Power BI-indhold
description: "I dette emne forklares, hvordan du kan overføre sikkerheden på adgangsniveau i omkostningsregnskabet til sikkerhed på rækkeniveau i Microsoft Power BI. Denne funktionalitet hjælper med til at sikre, at brugerne kun får vist de Power BI-data, de er tildelt adgang til."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="1e7af-104">Konfigurer sikkerhed for omkostningsregnskabsanalyse af Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="1e7af-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1e7af-105">I dette emne forklares, hvordan du kan overføre sikkerheden på adgangsniveau i omkostningsregnskabet til sikkerhed på rækkeniveau i Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="1e7af-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="1e7af-106">Denne funktionalitet hjælper med til at sikre, at brugerne kun får vist de Power BI-data, de er tildelt adgang til.</span><span class="sxs-lookup"><span data-stu-id="1e7af-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="1e7af-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="1e7af-107">Overview</span></span>
--------

<span data-ttu-id="1e7af-108">Til **omkostningsregnskabsanalysen** af Microsoft Power BI-indhold bruges sikkerhed på Power BI-rækkeniveau til at begrænse en brugers adgang.</span><span class="sxs-lookup"><span data-stu-id="1e7af-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="1e7af-109">Sikkerheden er baseret på det organisationshierarki for adgangsniveau, der er angivet i parametrene for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="1e7af-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="1e7af-110">Du kan finde yderligere oplysninger om **omkostningsregnskabsanalysen** af Power BI-indhold i [Omkostningsregnskabsanalyse af Power BI-indhold](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="1e7af-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="1e7af-111">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1e7af-111">Setup</span></span>
<span data-ttu-id="1e7af-112">Hvis du vil overføre sikkerhed på adgangsniveau til Power BI, skal ejeren af Power BI-indholdet følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1e7af-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="1e7af-113">**Bemærk!** Den bruger, der udgiver **omkostningsregnskabsanalysen** af Power BI-indhold, bliver automatisk ejer.</span><span class="sxs-lookup"><span data-stu-id="1e7af-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="1e7af-114">Kun en ejer kan konfigurere sikkerhed i Power BI.</span><span class="sxs-lookup"><span data-stu-id="1e7af-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="1e7af-115">Indtil en ejer tilføjer andre brugere på PowerBI.com, kan ingen undtagen ejeren desuden se nogen data i **omkostningsregnskabsanalysen** af Power BI-indhold.</span><span class="sxs-lookup"><span data-stu-id="1e7af-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="1e7af-116">Udgiv definitionsfilen til Power BI.</span><span class="sxs-lookup"><span data-stu-id="1e7af-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="1e7af-117">Log på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="1e7af-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="1e7af-118">Find datasættet til **omkostningsregnskabsanalysen** af Power BI-indhold.</span><span class="sxs-lookup"><span data-stu-id="1e7af-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="1e7af-119">Åbn sikkerhedssiden.</span><span class="sxs-lookup"><span data-stu-id="1e7af-119">Open the security page.</span></span> 

    ![Åbning af sikkerhedssiden](./media/CA-picture-1.png)

5.  <span data-ttu-id="1e7af-121">Rollen **Controller til omkostningsobjekt** er allerede oprettet.</span><span class="sxs-lookup"><span data-stu-id="1e7af-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="1e7af-122">Tilføj andre medlemmer, der er en del af organisationshierarkiet for adgangsniveau for omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="1e7af-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Tilføjelse af medlemmer](./media/CA-picture-2.png)

<span data-ttu-id="1e7af-124">Brugere, der føjes til rollen **Controller til omkostningsobjekt** ser kun de data, de har tilladelse til at se ifølge definitionen i organisationshierarkiet for adgangsniveau for omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="1e7af-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="1e7af-125">**Bemærk:** Sikkerhed på rækkeniveau gælder for felter og rapporter i Microsoft Dynamics 365 for Finance and Operations, der er integreret fra Power BI.</span><span class="sxs-lookup"><span data-stu-id="1e7af-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="1e7af-126">Opdatering af sikkerhed</span><span class="sxs-lookup"><span data-stu-id="1e7af-126">Updating security</span></span>
<span data-ttu-id="1e7af-127">Hvis der foretages opdateringer af sikkerheden på adgangsniveau i omkostningsregnskab, og du ønsker, at Power BI skal afspejle disse opdateringer, skal du opdatere enhedslageret for **omkostningsregnskabsanalysen** af Power BI-indhold.</span><span class="sxs-lookup"><span data-stu-id="1e7af-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="1e7af-128">Når du har fuldført opdateringen af enhedslageret fra Finance and Operations, skal du opdatere artefakterne på PowerBI.com. Du kan finde flere oplysninger om, hvordan du foretager en opdatering af enhedslageret , i [Opdatering af enhedslager](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="1e7af-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="1e7af-129">Ejeren af **omkostningsregnskabsanalysen** af Power BI-indhold skal også foretage en opdatering af enhedslager, hvis nye brugere får adgang til det organisatoriske hierarki.</span><span class="sxs-lookup"><span data-stu-id="1e7af-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="1e7af-130">Ejeren skal desuden føje nye brugere til rollen **Controller til omkostningsobjekt** på PowerBI.com, så sikkerhed på rækkeniveau gælder for dem.</span><span class="sxs-lookup"><span data-stu-id="1e7af-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="1e7af-131">Deaktivering af sikkerhed</span><span class="sxs-lookup"><span data-stu-id="1e7af-131">Disabling security</span></span>
<span data-ttu-id="1e7af-132">Vi antager, at din organisation ønsker at begrænse adgang til data.</span><span class="sxs-lookup"><span data-stu-id="1e7af-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="1e7af-133">Hvis sikkerhedsparametrene af en eller anden grund er deaktiveret, når du kører omkostningsregnskab, skal ejeren i stedet føje brugere til rollen **Bogholder** i Power BI.</span><span class="sxs-lookup"><span data-stu-id="1e7af-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="1e7af-134">Hvis du ændrer sikkerhed fra en aktiveret tilstand til en deaktiveret tilstand, er det en god ide at fjerne brugere fra rollen **Controller til omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="1e7af-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="1e7af-135">Og omvendt, hvis du genaktiverer sikkerhed.</span><span class="sxs-lookup"><span data-stu-id="1e7af-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="1e7af-136">Brugere kan tilhøre begge roller.</span><span class="sxs-lookup"><span data-stu-id="1e7af-136">Users can belong to both roles.</span></span> <span data-ttu-id="1e7af-137">Fælles adgang er foreningsmængden af begge roller.</span><span class="sxs-lookup"><span data-stu-id="1e7af-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="1e7af-138">Når det gælder **omkostningsregnskabsanalysen** af Power BI- indhold, har brugerne med fælles adgang ubegrænset adgang til data.</span><span class="sxs-lookup"><span data-stu-id="1e7af-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="1e7af-139">Hvis dit mål er at anvende begrænset adgang, skal brugerne kun tildeles rollen **Controller til omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="1e7af-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="1e7af-140">Disse opdateringer af sikkerhed på rækkeniveau træder straks i kraft.</span><span class="sxs-lookup"><span data-stu-id="1e7af-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="1e7af-141">Berørte brugere skal opdatere deres browsere.</span><span class="sxs-lookup"><span data-stu-id="1e7af-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e7af-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1e7af-142">Additional resources</span></span>
<span data-ttu-id="1e7af-143">Du kan få mere at vide om sikkerhed på rækkeniveau i Power BI i [Administrer sikkerhed på din model i Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="1e7af-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




