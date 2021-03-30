---
title: Aktivér Azure Active Directory-godkendelse til POS-login
description: I dette emne beskrives, hvordan du kan konfigurere logonprocessen for Microsoft Dynamics 365 Commerce POS, så den bruger Azure Active Directory-godkendelse.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 234d19bb6659af07c65763e05671742b9581e244
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206673"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="72154-103">Aktivere Azure Active Directory-godkendelse for POS-login</span><span class="sxs-lookup"><span data-stu-id="72154-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="72154-104">Mange af de kunder, der bruger Microsoft Dynamics 365 Commerce, bruger også andre Microsoft skytjenester, og de bruger muligvis Azure Active Directory (Azure AD) til at administrere brugerlegitimationsoplysninger til disse tjenester.</span><span class="sxs-lookup"><span data-stu-id="72154-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="72154-105">I disse tilfælde kan kunderne vælge at bruge den samme Azure AD-konto på tværs af programmer.</span><span class="sxs-lookup"><span data-stu-id="72154-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="72154-106">I dette emne beskrives, hvordan du kan konfigurere POS-logonoplevelsen til at bruge Azure AD-godkendelse.</span><span class="sxs-lookup"><span data-stu-id="72154-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="72154-107">Konfigurere Azure AD-godkendelse</span><span class="sxs-lookup"><span data-stu-id="72154-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="72154-108">Hvis du vil gøre Azure AD tilgængelig som godkendelsesmetode for POS-login i en butik, skal du konfigurere indstillingerne for butikkens funktionalitetsprofil og derefter anvende denne indstilling på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="72154-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="72154-109">Gør følgende for at konfigurere en ny funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="72154-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="72154-110">Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **POS-opsætning** \> **POS-profiler** \> **Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="72154-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="72154-111">Vælg den funktionalitetsprofil, du vil ændre.</span><span class="sxs-lookup"><span data-stu-id="72154-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="72154-112">I oversigtspanelet **Funktioner** i sektionen **POS-medarbejderlogon** skal du ændre værdien i feltet **Logongodkendelse** fra **Personale-id og adgangskode** til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="72154-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="72154-113">Som standard bruger alle funktionalitetsprofiler **Personale-id og adgangskode** som POS-godkendelsesmetode.</span><span class="sxs-lookup"><span data-stu-id="72154-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="72154-114">Du skal derfor ændre værdien i feltet **Logongodkendelsesmetode**, hvis du vil bruge Azure AD.</span><span class="sxs-lookup"><span data-stu-id="72154-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="72154-115">Alle de detailbutikker, der er kædet sammen med den valgte funktionalitetsprofil, påvirkes af ændringen.</span><span class="sxs-lookup"><span data-stu-id="72154-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="72154-116">Udfør følgende trin for at anvende indstillingerne til POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="72154-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="72154-117">Gå til **Retail og Commerce** \> **Retail og Commerce IT** \> **Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="72154-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="72154-118">Kør distributionstidsplanen **1070** (**Kannalkonfiguration**).</span><span class="sxs-lookup"><span data-stu-id="72154-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="72154-119">Azure AD-godkendelse kræver en internetforbindelse.</span><span class="sxs-lookup"><span data-stu-id="72154-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="72154-120">Det fungerer ikke, når POS er i offline-tilstand.</span><span class="sxs-lookup"><span data-stu-id="72154-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="72154-121">I øjeblikket understøtter funktionen **Ledertilsidesættelse** ikke Azure AD som godkendelsesmetode.</span><span class="sxs-lookup"><span data-stu-id="72154-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="72154-122">Der kræves et operatør-id og en adgangskode, også selvom Azure AD er konfigureret som godkendelsesmetode for POS-logon.</span><span class="sxs-lookup"><span data-stu-id="72154-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="72154-123">Knytte en Azure AD-konto til en arbejder</span><span class="sxs-lookup"><span data-stu-id="72154-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="72154-124">Før en butiksmedarbejder kan bruge en Azure AD-konto til at logge på POS-programmet, skal Azure AD-kontoen knyttes til den pågældende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="72154-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="72154-125">Hvis du vil knytte en Azure AD-konto til en arbejder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="72154-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="72154-126">Gå til **Retail og Commerce** \> **Medarbejdere** \> **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="72154-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="72154-127">Åbn siden med detaljer til en arbejder.</span><span class="sxs-lookup"><span data-stu-id="72154-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="72154-128">Vælg **Tilknyt eksisterende identitet** i handlingsruden på fanen **Commerce** i gruppen **Eksternt identitet**.</span><span class="sxs-lookup"><span data-stu-id="72154-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="72154-129">Vælg **Søg ved hjælp af mail** i dialogboksen **Brug eksisterende ekstern identitet**, indtast en Azure AD-mailadresse, og vælg derefter **Søg**.</span><span class="sxs-lookup"><span data-stu-id="72154-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="72154-130">Vælg den Azure AD-konto, der returneres, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="72154-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="72154-131">Felterne **Alias**, **UPN** og **Eksternt under-id** under fanen **Commerce** på siden med detaljer om arbejderen udfyldes.</span><span class="sxs-lookup"><span data-stu-id="72154-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="72154-132">Når en arbejderpost er opdateret, f.eks. hvis der er tilknyttet en ny Azure AD-konto, ændres en adgangskode, eller et medarbejderadressekartotek opdateres, men det anbefales, at du kører distributionsplanen **1060** (**Personale**) for at synkronisere de seneste medarbejderoplysninger med kanalen.</span><span class="sxs-lookup"><span data-stu-id="72154-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="72154-133">På denne måde kan POS-programmet hente de korrekte data til brugergodkendelse og godkendelseskontrol.</span><span class="sxs-lookup"><span data-stu-id="72154-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72154-134">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="72154-134">Additional resources</span></span>

[<span data-ttu-id="72154-135">Konfigurere udvidet logonfunktionalitet for MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="72154-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="72154-136">Oprette en detailfunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="72154-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="72154-137"> Konfigurere en arbejder</span><span class="sxs-lookup"><span data-stu-id="72154-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]