---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b994473b4535c255f87551a6d97e197516fc2a9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745831"
---
# <a name="create-new-users"></a><span data-ttu-id="61820-103">Oprette nye brugere</span><span class="sxs-lookup"><span data-stu-id="61820-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61820-104">Før du kan få adgang til Finance and Operations-apps, skal du først føjes til siden **Brugere** (**Systemadministration \> Brugere \> Brugere**).</span><span class="sxs-lookup"><span data-stu-id="61820-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="61820-105">Brugere omfatter interne medarbejdere i din organisation eller eksterne kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="61820-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="61820-106">Brugere kan importeres eller tilføjes manuelt.</span><span class="sxs-lookup"><span data-stu-id="61820-106">Users can be imported or added manually.</span></span> <span data-ttu-id="61820-107">Alle brugere skal have korrekt licens for at få kompatibel brug.</span><span class="sxs-lookup"><span data-stu-id="61820-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="61820-108">Du kan finde flere oplysninger om, hvordan du køber og får licens til Finance and Operations-apps, i [licensvejledningen til Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="61820-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="61820-109">Tildele en bruger licens</span><span class="sxs-lookup"><span data-stu-id="61820-109">Assign a license to a user</span></span>
<span data-ttu-id="61820-110">Systemadministratorer kan [tildele licenser til brugere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [Microsoft 365 Administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="61820-110">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="61820-111">Tilføje en ekstern bruger i Azure AD og tildele en licens</span><span class="sxs-lookup"><span data-stu-id="61820-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="61820-112">Eksterne brugere skal være repræsenteret i dit lejerbibliotek (Azure Active Directory (Azure AD)), så de kan tildeles licenser.</span><span class="sxs-lookup"><span data-stu-id="61820-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="61820-113">Disse eksterne brugere skal føjes til lejeren i Azure AD som gæstebrugere og derefter tildeles de relevante licenser.</span><span class="sxs-lookup"><span data-stu-id="61820-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="61820-114">Et krav til Finance and Operations-apps er, at gæstebrugerens firma skal bruge Azure AD.</span><span class="sxs-lookup"><span data-stu-id="61820-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="61820-115">Du kan finde flere oplysninger under [Tilføje Azure Active Directory B2B-samarbejdsbrugere i Azure-portalen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="61820-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="61820-116">Importere nye brugere fra Azure AD</span><span class="sxs-lookup"><span data-stu-id="61820-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="61820-117">Gå til **Systemadministration** \> **Bruger** \> **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="61820-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="61820-118">Vælg **Importer brugere** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="61820-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="61820-119">Vælg de brugere, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="61820-119">Select the users to be imported.</span></span> <span data-ttu-id="61820-120">Listen indeholder Azure AD-brugere, der aktuelt ikke er brugere i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="61820-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="61820-121">Vælg **Importer brugere**.</span><span class="sxs-lookup"><span data-stu-id="61820-121">Select **Import users**.</span></span>
5. <span data-ttu-id="61820-122">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="61820-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="61820-123">Værdien af feltet **Firma** angives på basis af det aktuelle sessionsfirma for administratoren. Efter importen skal du tildele roller og organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="61820-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="61820-124">Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="61820-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="61820-125">Det kan også være nødvendigt at knytte brugeren til en **Person** og opdatere brugerindstillinger som f.eks. sprog.</span><span class="sxs-lookup"><span data-stu-id="61820-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="61820-126">Tilføje en ny bruger manuelt</span><span class="sxs-lookup"><span data-stu-id="61820-126">Manually add a new user</span></span>
1. <span data-ttu-id="61820-127">Gå til **Systemadministration** \> **Brugere** \> **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="61820-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="61820-128">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="61820-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="61820-129">Angiv et entydigt id for brugeren i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="61820-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="61820-130">Angiv brugerens navn i feltet **Brugernavn**.</span><span class="sxs-lookup"><span data-stu-id="61820-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="61820-131">I feltet **Udbyder**:</span><span class="sxs-lookup"><span data-stu-id="61820-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="61820-132">Brug standardværdien til interne brugere.</span><span class="sxs-lookup"><span data-stu-id="61820-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="61820-133">Din Azure AD-lejer har f.eks. præfikset https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="61820-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="61820-134">For ikke-Azure AD-brugere, f.eks. Service-2-Service-konti, skal du angive en grundlæggende tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="61820-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="61820-135">For eksempel Ikke relevant.</span><span class="sxs-lookup"><span data-stu-id="61820-135">For example, NA.</span></span> <span data-ttu-id="61820-136">Denne værdi hjælper med at undgå forkerte godkendelseskald, der kan resultere i fejl, hvis der bruges en gyldig værdi for identitetsudbyderen.</span><span class="sxs-lookup"><span data-stu-id="61820-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="61820-137">For eksterne brugere eller gæstebrugere skal du tilføje deres Azure AD-lejernavn efter https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="61820-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="61820-138">I feltet **Mail** skal du angive brugerens fulde mail/hovednavn.</span><span class="sxs-lookup"><span data-stu-id="61820-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="61820-139">Vælg standardstartfirmaet for brugeren i feltet **Firma**.</span><span class="sxs-lookup"><span data-stu-id="61820-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="61820-140">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="61820-140">Select **Save**.</span></span>

<span data-ttu-id="61820-141">Værdierne for Identitetsudbyder og Telemetri-id opdateres baseret på et [Microsoft-grafkald](https://docs.microsoft.com/graph/overview), når brugerposten gemmes.</span><span class="sxs-lookup"><span data-stu-id="61820-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](https://docs.microsoft.com/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="61820-142">Telemetri-id'et er baseret på brugerens objekt-id/sikkerheds-id (SID) i Azure AD.</span><span class="sxs-lookup"><span data-stu-id="61820-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="61820-143">Når du har tilføjet en bruger, skal du tildele roller og organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="61820-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="61820-144">Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="61820-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="61820-145">Det kan også være nødvendigt at knytte brugeren til en **Person** og opdatere **Brugerindstillinger** som f.eks. sprog.</span><span class="sxs-lookup"><span data-stu-id="61820-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="61820-146">Ændre et bruger-id</span><span class="sxs-lookup"><span data-stu-id="61820-146">Change a user ID</span></span>
<span data-ttu-id="61820-147">Hvis du vil ændre et bruger-id, skal du omdøbe nøglen i databasen.</span><span class="sxs-lookup"><span data-stu-id="61820-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="61820-148">Når du ændrer et bruger-id ved hjælp af denne procedure, ændres alle relaterede brugerindstillinger, så de bruger det nye bruger-id.</span><span class="sxs-lookup"><span data-stu-id="61820-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="61820-149">Brugsoplysningerne i tabellen **SysLastValue** opdateres f.eks. til at referere til det nye bruger-id.</span><span class="sxs-lookup"><span data-stu-id="61820-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="61820-150">Bruger-id'et er primærnøglen i tabellen med brugeroplysninger.</span><span class="sxs-lookup"><span data-stu-id="61820-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="61820-151">Det kan tage et stykke tid at omdøbe primærnøglen for eksisterende brugere, da alle referencer til nøglen også opdateres i databasen.</span><span class="sxs-lookup"><span data-stu-id="61820-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="61820-152">Gå til **Systemadministration \> Brugere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="61820-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="61820-153">Vælg en bruger på listen, og vælg **Indstillinger\> Postoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="61820-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="61820-154">Vælg **Omdøb**.</span><span class="sxs-lookup"><span data-stu-id="61820-154">Select **Rename**.</span></span>
4. <span data-ttu-id="61820-155">Angiv en ny og entydig værdi af bruger-id, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="61820-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="61820-156">Vælg **Ja** for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="61820-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61820-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="61820-157">Additional resources</span></span>

<span data-ttu-id="61820-158">Du kan finde flere indstillinger til implementering af B2B-brugere i [Eksportere B2B-brugere til Azure AD](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="61820-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="61820-159">Du kan finde oplysninger om forudkonfigurerede systemkonti i [Forudkonfigurerede systemkonti](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="61820-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]