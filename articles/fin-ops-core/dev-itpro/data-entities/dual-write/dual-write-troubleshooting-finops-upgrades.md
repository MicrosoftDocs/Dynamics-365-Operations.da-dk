---
title: Foretage fejlfinding af problemer med opgraderinger af Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131215"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="3f15f-103">Foretage fejlfinding af problemer med opgraderinger af Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3f15f-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3f15f-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3f15f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="3f15f-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="3f15f-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f15f-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="3f15f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3f15f-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="3f15f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="3f15f-108">Fejl ved databasesynkronisering</span><span class="sxs-lookup"><span data-stu-id="3f15f-108">Database synchronization errors</span></span>

<span data-ttu-id="3f15f-109">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="3f15f-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3f15f-110">Du kan få vist en fejlmeddelelse, der ligner følgende eksempel, når du forsøger at bruge tabellen **DualWriteProjectConfiguration** til at opdatere en Finance and Operations-app til Platform Update 30.</span><span class="sxs-lookup"><span data-stu-id="3f15f-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="3f15f-111">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="3f15f-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="3f15f-112">Log på den virtuelle maskine (VM) for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="3f15f-113">Åbn Visual Studio som administrator, og åbn applikationsobjekttræet (AOT).</span><span class="sxs-lookup"><span data-stu-id="3f15f-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="3f15f-114">Søg efter **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="3f15f-115">I applikationsobjekttræet skal du højreklikke på **DualWriteProjectConfiguration** og vælge **Føj til nyt projekt**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="3f15f-116">Vælg **OK** for at oprette det nye projekt, der bruger standardindstillinger.</span><span class="sxs-lookup"><span data-stu-id="3f15f-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="3f15f-117">Højreklik på **Projektegenskaber** i Solution Explorer, og indstil **Synkroniser database i Build** til **True**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="3f15f-118">Byg projektet, og bekræft, at buildet fungerer korrekt.</span><span class="sxs-lookup"><span data-stu-id="3f15f-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="3f15f-119">Vælg **Synkroniser database** i menuen **Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="3f15f-120">Vælg **Synkroniser** for at foretage en komplet databasesynkronisering.</span><span class="sxs-lookup"><span data-stu-id="3f15f-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="3f15f-121">Når hele database synkroniseringen er udført korrekt, skal du køre databasesynkroniseringstrinnet igen i Microsoft Dynamics Lifecycle Services (LCS) og bruge de manuelle opgraderingsscripts, så du kan fortsætte med opdateringen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="3f15f-122">Problem med manglende tabelkolonner i tilknytning</span><span class="sxs-lookup"><span data-stu-id="3f15f-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="3f15f-123">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="3f15f-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3f15f-124">På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="3f15f-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="3f15f-125">*Manglende kildefelt \<field name\> i skemaet.*</span><span class="sxs-lookup"><span data-stu-id="3f15f-125">*Missing source field \<field name\> in the schema.*</span></span>

![Eksempel på fejlmeddelelsen om manglende kildekolonne](media/error_missing_field.png)

<span data-ttu-id="3f15f-127">Hvis du vil løse problemet, skal du først følge disse trin for at sikre, at kolonnerne findes i tabellen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="3f15f-128">Log på den virtuelle maskine for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="3f15f-129">Gå til **Arbejdsområder \> Datastyring**, vælg feltet **Rammeparametre**, og vælg derefter **Opdater tabelliste** under fanen **Tabelindstillinger** for at opdatere tabellerne.</span><span class="sxs-lookup"><span data-stu-id="3f15f-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="3f15f-130">Gå til **Arbejdsområder \> Datastyring**, vælg fanen **Datatabeller**, og kontrollér, at tabellen er vist.</span><span class="sxs-lookup"><span data-stu-id="3f15f-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="3f15f-131">Hvis tabellen ikke vises, skal du logge på den virtuelle maskine for Finance and Operations-appen og kontrollere, at tabellen er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="3f15f-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="3f15f-132">Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="3f15f-133">Vælg **Opdater tabelliste**, så kolonnerne i tabeltilknytninger automatisk udfyldes.</span><span class="sxs-lookup"><span data-stu-id="3f15f-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="3f15f-134">Hvis problemet stadig ikke er løst, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3f15f-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f15f-135">Disse trin fører dig gennem processen til sletning af en tabel og derefter tilføjelse af den igen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="3f15f-136">Hvis du vil undgå problemer, skal du sørge for at følge trinene nøjagtigt.</span><span class="sxs-lookup"><span data-stu-id="3f15f-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="3f15f-137">Gå i Finance and Operations-appen til **Arbejdsområder \> Datastyring**, og markér feltet **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="3f15f-138">Find den tabel, der mangler attributten.</span><span class="sxs-lookup"><span data-stu-id="3f15f-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="3f15f-139">Klik på **Rediger måltilknytning** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="3f15f-140">Klik på **Generér tilknytning** i ruden **Knyt midlertidig placering til mål**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="3f15f-141">Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="3f15f-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="3f15f-142">Hvis attributten ikke udfyldes automatisk på tilknytningen, skal du tilføje den manuelt ved at klikke på knappen **Tilføj attribut** og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="3f15f-143">Vælg tilknytningen, og klik på **Kør**.</span><span class="sxs-lookup"><span data-stu-id="3f15f-143">Select the map and click **Run**.</span></span>
