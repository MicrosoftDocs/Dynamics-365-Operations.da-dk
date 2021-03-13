---
title: Integrere med LinkedIn Talent Hub
description: I dette emne forklares, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 Human Resources og LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fda9d85b459d233e6239f3fcffbb48e596d4085
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111995"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="1861f-103">Integrere med LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1861f-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1861f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er en platform med et ansøgersporingssystem (ATS).</span><span class="sxs-lookup"><span data-stu-id="1861f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="1861f-105">Her kan du rekruttere, administrere og ansætte medarbejdere på ét sted.</span><span class="sxs-lookup"><span data-stu-id="1861f-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="1861f-106">Ved at integrere Microsoft Dynamics 365 Human Resources med LinkedIn Talent Hub kan du nemt oprette medarbejderposter i Human Resources for ansøgere, der er blevet ansat i en stilling.</span><span class="sxs-lookup"><span data-stu-id="1861f-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="1861f-107">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1861f-107">Setup</span></span>

<span data-ttu-id="1861f-108">En systemadministrator skal fuldføre installationsopgaverne, for at integrationen med LinkedIn Talent Hub kan finde sted.</span><span class="sxs-lookup"><span data-stu-id="1861f-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="1861f-109">Først skal du i Power Apps-miljøet oprette en bruger- og sikkerhedsrolle for at tildele LinkedIn Talent Hub de relevante tilladelser til at skrive data i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1861f-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="1861f-110">Knytte miljøet til LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1861f-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="1861f-111">Åbn [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="1861f-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="1861f-112">Vælg **Produktindstillinger** i brugerrullemenuen.</span><span class="sxs-lookup"><span data-stu-id="1861f-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="1861f-113">Vælg **Integrationer** i sektionen **Avanceret** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="1861f-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="1861f-114">Vælg **Autoriser** for Microsoft Dynamics 365 Human Resources-integrationen.</span><span class="sxs-lookup"><span data-stu-id="1861f-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="1861f-115">Vælg det miljø, som du vil knytte LinkedIn Talent Hub til, på siden **Dynamics 365 Human Resources**, og vælg derefter **Link**.</span><span class="sxs-lookup"><span data-stu-id="1861f-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub-onboarding](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="1861f-117">Du kan kun tilknytte miljøer, hvor din brugerkonto har administratoradgang til både Human Resources-miljøet og det tilknyttede Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="1861f-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="1861f-118">Hvis der ikke vises nogen miljøer på siden med Human Resources-link, skal du sikre dig, at du har licens til Human Resources-miljøer i lejeren, og at den bruger, du loggede på linksiden som, har administratorrettigheder til både Human Resources-miljøet og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1861f-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="1861f-119">Oprette en Power Apps-sikkerhedsrolle</span><span class="sxs-lookup"><span data-stu-id="1861f-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="1861f-120">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1861f-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1861f-121">På listen **Miljøer** skal du vælge det miljø, der er knyttet til det Human Resources-miljø, som du vil knytte din forekomst af LinkedIn Talent Hub til.</span><span class="sxs-lookup"><span data-stu-id="1861f-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1861f-122">Vælg **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1861f-122">Select **Settings**.</span></span>

4. <span data-ttu-id="1861f-123">Udvid noden **Brugere + tilladelser**, og vælg **Sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="1861f-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="1861f-124">Vælg **Ny rolle** på værktøjslinjen på siden **Sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="1861f-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="1861f-125">Angiv et navn til rollen under fanen **Detaljer**, f.eks. **LinkedIn Talent Hub HRIS-integration**.</span><span class="sxs-lookup"><span data-stu-id="1861f-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="1861f-126">Vælg tilladelse til at **Læse** på organisationsniveau under fanen **Tilpasning** for følgende enheder:</span><span class="sxs-lookup"><span data-stu-id="1861f-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="1861f-127">Enhed</span><span class="sxs-lookup"><span data-stu-id="1861f-127">Entity</span></span>
    - <span data-ttu-id="1861f-128">Felt</span><span class="sxs-lookup"><span data-stu-id="1861f-128">Field</span></span>
    - <span data-ttu-id="1861f-129">Relation</span><span class="sxs-lookup"><span data-stu-id="1861f-129">Relationship</span></span>

8. <span data-ttu-id="1861f-130">Gem og luk sikkerhedsrollen.</span><span class="sxs-lookup"><span data-stu-id="1861f-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="1861f-131">Oprette en Power Apps-applikationsbruger</span><span class="sxs-lookup"><span data-stu-id="1861f-131">Create a Power Apps application user</span></span>

<span data-ttu-id="1861f-132">Der skal oprettes en applikationsbruger, hvis LinkedIn Talent Hub-adapteren skal give tilladelser til, at kortet skriver kandidatposter ind i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1861f-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="1861f-133">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1861f-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1861f-134">På listen **Miljøer** skal du vælge det miljø, der er knyttet til det Human Resources-miljø, som du vil knytte din forekomst af LinkedIn Talent Hub til.</span><span class="sxs-lookup"><span data-stu-id="1861f-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1861f-135">Vælg **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1861f-135">Select **Settings**.</span></span>

4. <span data-ttu-id="1861f-136">Udvid noden **Brugere + tilladelser**, og vælg **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="1861f-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="1861f-137">Vælg **Administrer brugere i Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1861f-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="1861f-138">Brug rullemenuen over listen til at ændre visningen fra standardvisningen **Aktiverede brugere** til **Applikationsbrugere**.</span><span class="sxs-lookup"><span data-stu-id="1861f-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Visningen Applikationsbrugere](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="1861f-140">Vælg **Ny** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="1861f-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="1861f-141">På siden **Ny bruger** skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="1861f-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="1861f-142">Ret værdien i feltet **Brugertype** til **Applikationsbruger**.</span><span class="sxs-lookup"><span data-stu-id="1861f-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="1861f-143">Indstil feltet **Brugernavn** til **DYNAMICS365 HR LinkedIn HRIS-integration**.</span><span class="sxs-lookup"><span data-stu-id="1861f-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="1861f-144">Indstil feltet **Program-id** til **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1861f-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="1861f-145">Angiv en værdi i felterne **Fornavn**, **Efternavn** og **Primær mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="1861f-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="1861f-146">Vælg **Gem \& Luk** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="1861f-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="1861f-147">Tildele en sikkerhedsrolle til den nye bruger</span><span class="sxs-lookup"><span data-stu-id="1861f-147">Assign a security role to the new user</span></span>

<span data-ttu-id="1861f-148">Når du har gemt og lukket den nye applikationsbruger i forrige afsnit, kommer du tilbage til siden **Brugerliste**.</span><span class="sxs-lookup"><span data-stu-id="1861f-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="1861f-149">På siden **Brugerliste** kan du ændre visningen til **Applikationsbrugere**.</span><span class="sxs-lookup"><span data-stu-id="1861f-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="1861f-150">Vælg den applikationsbruger, du oprettede i foregående afsnit.</span><span class="sxs-lookup"><span data-stu-id="1861f-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="1861f-151">Vælg **Administrer roller** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="1861f-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="1861f-152">Vælg den sikkerhedsrolle, du oprettede tidligere til integrationen.</span><span class="sxs-lookup"><span data-stu-id="1861f-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="1861f-153">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1861f-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="1861f-154">Tilføje en Azure Active Directory-app i Human Resources</span><span class="sxs-lookup"><span data-stu-id="1861f-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="1861f-155">I Dynamics 365 Human Resources skal du åbne siden **Azure Active Directory-applikationer**.</span><span class="sxs-lookup"><span data-stu-id="1861f-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="1861f-156">Føj en ny post til listen, og indstil følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1861f-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="1861f-157">**Klient-id**: Angiv **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1861f-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="1861f-158">**Navn**: Angiv navnet på den Power Apps-sikkerhedsrolle, du oprettede tidligere, f.eks. **LinkedIn Talent Hub HRIS-integration**.</span><span class="sxs-lookup"><span data-stu-id="1861f-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="1861f-159">**Bruger-id**: Vælg en bruger, der har rettigheder til at skrive data i personalestyring.</span><span class="sxs-lookup"><span data-stu-id="1861f-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="1861f-160">Oprette tabellen i Dataverse</span><span class="sxs-lookup"><span data-stu-id="1861f-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1861f-161">Integrationen med LinkedIn Talent Hub afhænger af virtuelle tabeller i Dataverse for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1861f-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="1861f-162">Som en forudsætning for dette trin i konfigurationen, skal du konfigurere virtuelle tabeller.</span><span class="sxs-lookup"><span data-stu-id="1861f-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="1861f-163">Du kan finde oplysninger om, hvordan du konfigurerer virtuelle tabeller i [Konfigurere Dataverse virtuelle tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="1861f-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="1861f-164">I Human Resources skal du åbne siden **Dataverse-integration**.</span><span class="sxs-lookup"><span data-stu-id="1861f-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="1861f-165">Vælg fanen **Virtuelle tabeller**.</span><span class="sxs-lookup"><span data-stu-id="1861f-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="1861f-166">Filtrer enhedslisten efter enhedslabel for at finde **Kandidat eksporteret fra LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="1861f-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="1861f-167">Vælg enheden, og vælg derefter **Generer/Opdater**.</span><span class="sxs-lookup"><span data-stu-id="1861f-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="1861f-168">Eksport af kandidatposter</span><span class="sxs-lookup"><span data-stu-id="1861f-168">Exporting candidate records</span></span>

<span data-ttu-id="1861f-169">Når du har fuldført opsætningen, kan rekrutteringsmedarbejdere og medarbejdere i personaleafdelingen bruge funktionen **Eksportér til HRIS** i LinkedIn Talent Hub til at eksportere posterne for de hyrede kandidat fra LinkedIn Talent Hub til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1861f-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="1861f-170">Eksportere poster fra LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1861f-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="1861f-171">Når en ansøger har gennemgået rekrutteringsprocessen og er blevet ansat, kan du eksportere kandidatposten fra LinkedIn Talent Hub til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1861f-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="1861f-172">Åbn det projekt, som du har ansat den nye medarbejder til, i LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="1861f-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="1861f-173">Vælg en kandidatpost.</span><span class="sxs-lookup"><span data-stu-id="1861f-173">Select a candidate record.</span></span>

3. <span data-ttu-id="1861f-174">Vælg **Skift stadie**, og vælg derefter **Ansat**.</span><span class="sxs-lookup"><span data-stu-id="1861f-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="1861f-175">Vælg **Eksportér til HRIS** i ellipsemenuen (**...**) for kandidaten.</span><span class="sxs-lookup"><span data-stu-id="1861f-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="1861f-176">Angiv de oplysninger, der skal eksporteres, i ruden **Eksportér til HRIS**:</span><span class="sxs-lookup"><span data-stu-id="1861f-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="1861f-177">I feltet **HRIS-udbyder** skal du vælge **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="1861f-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="1861f-178">Vælg en startdato for den nye medarbejder i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="1861f-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="1861f-179">Angiv en stillingsbetegnelse for den nye medarbejders job i feltet **Stillingsbetegnelse**.</span><span class="sxs-lookup"><span data-stu-id="1861f-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="1861f-180">Angiv den adresse, hvor medarbejderen bliver baseret, i feltet **Adresse**.</span><span class="sxs-lookup"><span data-stu-id="1861f-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="1861f-181">Angiv eller kontroller medarbejderens mailadresse.</span><span class="sxs-lookup"><span data-stu-id="1861f-181">Enter or verify the employee's email address.</span></span>

![Ruden Eksportér til HRIS i LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="1861f-183">Færdiggøre onboardingen i Human Resources</span><span class="sxs-lookup"><span data-stu-id="1861f-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="1861f-184">Kandidatposter, der eksporteres fra LinkedIn Talent Hub til Human Resources, vises i sektionen **Kandidater, der skal ansættes** på siden **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="1861f-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="1861f-185">Åbn siden **Personalestyring** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1861f-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="1861f-186">Vælg **Ansættelse** for den valgte kandidat i sektionen **Kandidater, der skal ansættes**.</span><span class="sxs-lookup"><span data-stu-id="1861f-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="1861f-187">Gennemse posten i dialogboksen **Ansæt ny arbejder**, og tilføj evt. påkrævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1861f-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="1861f-188">Du kan også vælge det stillingsnummer, som kandidaten er ansat til.</span><span class="sxs-lookup"><span data-stu-id="1861f-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="1861f-189">Når de nødvendige oplysninger er angivet, kan du fortsætte med dine standardprocesser til oprettelse af medarbejderposter og onboarding af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="1861f-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="1861f-190">Følgende oplysninger importeres og medtages i den nye medarbejderpost:</span><span class="sxs-lookup"><span data-stu-id="1861f-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="1861f-191">Fornavn</span><span class="sxs-lookup"><span data-stu-id="1861f-191">First name</span></span>
- <span data-ttu-id="1861f-192">Efternavn</span><span class="sxs-lookup"><span data-stu-id="1861f-192">Last name</span></span>
- <span data-ttu-id="1861f-193">Startdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="1861f-193">Employment start date</span></span>
- <span data-ttu-id="1861f-194">E-mailadresse</span><span class="sxs-lookup"><span data-stu-id="1861f-194">Email address</span></span>
- <span data-ttu-id="1861f-195">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="1861f-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="1861f-196">Se også</span><span class="sxs-lookup"><span data-stu-id="1861f-196">See also</span></span>

[<span data-ttu-id="1861f-197">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="1861f-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="1861f-198">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="1861f-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
