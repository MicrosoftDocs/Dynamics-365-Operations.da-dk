---
title: (ER) Importere konfigurationer fra RCS
description: Dette emne giver oplysninger om, hvordan en bruger kan importere en ny version af en ER-konfiguration fra RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143217"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="d770e-103">(ER) Importere konfigurationer fra RCS</span><span class="sxs-lookup"><span data-stu-id="d770e-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d770e-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="d770e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="d770e-105">I dette eksempel skal du vælge den version af ER-konfigurationen, der er konfigureret i en RCS-forekomst, og importere den til den aktuelle forekomst for eksempelfirmaet, litware, Inc. Disse trin kan udføres for alle firmaer, fordi ER-konfigurationer deles mellem firmaer.</span><span class="sxs-lookup"><span data-stu-id="d770e-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="d770e-106">For at fuldføre disse trin skal du først fuldføre trinnene i emnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d770e-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="d770e-107">Hvis du vil udføre disse trin, skal du også have adgang til en RCS-forekomst, der indeholder mindst én ER-konfiguration, der enten har statussen **Fuldført** eller **Delt**.</span><span class="sxs-lookup"><span data-stu-id="d770e-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="d770e-108">Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d770e-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="d770e-109">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="d770e-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d770e-110">Hvis denne konfigurationsudbyder ikke vises, skal du fuldføre trinnene i emnet [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d770e-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="d770e-111">Hvis du ikke har klargjort et RCS-miljø til dit firma, skal du klikke på det eksterne link **Regulatory services – konfiguration** og følge instruktionerne for at klargøre et RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="d770e-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="d770e-112">Klik på **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d770e-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="d770e-113">Klik på fanen **RCS**.</span><span class="sxs-lookup"><span data-stu-id="d770e-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="d770e-114">Hvis RCS-miljøet allerede er klargjort til dit firma, skal du anvende indstillingen for præsenteret på sidens URL-adresser for at få adgang til det.</span><span class="sxs-lookup"><span data-stu-id="d770e-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="d770e-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d770e-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="d770e-116">Registrere et nyt ER-lager.</span><span class="sxs-lookup"><span data-stu-id="d770e-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="d770e-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d770e-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="d770e-118">Vælg Litware, Inc.-udbyder</span><span class="sxs-lookup"><span data-stu-id="d770e-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="d770e-119">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d770e-119">Click Repositories.</span></span> 
4. <span data-ttu-id="d770e-120">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d770e-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="d770e-121">Skriv RCS i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="d770e-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="d770e-122">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="d770e-122">Click Create repository.</span></span> 
7. <span data-ttu-id="d770e-123">Angiv eller vælg en værdi i feltet for vist navn for RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="d770e-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="d770e-124">Vælg det ønskede RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="d770e-124">Select the desired RCS instance.</span></span> <span data-ttu-id="d770e-125">Bemærk, at du kan have flere af dem.</span><span class="sxs-lookup"><span data-stu-id="d770e-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="d770e-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d770e-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="d770e-127">Hente ER-konfigurationer fra RCS-baseret lager</span><span class="sxs-lookup"><span data-stu-id="d770e-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="d770e-128">Klik på **Vis filtre**.</span><span class="sxs-lookup"><span data-stu-id="d770e-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="d770e-129">Angiv filterværdien "RCS" i feltet **Navn** ved hjælp af filteroperatoren **begynder med**.</span><span class="sxs-lookup"><span data-stu-id="d770e-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="d770e-130">Når du åbner det valgte lagersted, skal du på siden **Forbind til Regulatory Configuration Services** klikke på linket **Klik her for at oprette forbindelse til Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="d770e-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="d770e-131">Klik på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="d770e-131">Click **Open**.</span></span> 
5. <span data-ttu-id="d770e-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="d770e-132">Click **Close**.</span></span> 
6. <span data-ttu-id="d770e-133">Vælg den ønskede version af ER-konfigurationen, og klik på **Importer** for at bringe den ind i den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="d770e-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

