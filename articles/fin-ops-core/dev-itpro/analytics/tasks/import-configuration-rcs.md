---
title: (ER) Importere konfigurationer fra RCS
description: Dette emne giver oplysninger om, hvordan en bruger kan importere en ny version af en ER-konfiguration fra RCS.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77d637b2ec1deeabc04a6796644363b330f5756e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744885"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="ee602-103">(ER) Importere konfigurationer fra RCS</span><span class="sxs-lookup"><span data-stu-id="ee602-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee602-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="ee602-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="ee602-105">I dette eksempel skal du vælge den version af ER-konfigurationen, der er konfigureret i en RCS-forekomst, og importere den til den aktuelle forekomst for eksempelfirmaet, litware, Inc. Disse trin kan udføres for alle firmaer, fordi ER-konfigurationer deles mellem firmaer.</span><span class="sxs-lookup"><span data-stu-id="ee602-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="ee602-106">For at fuldføre disse trin skal du først fuldføre trinnene i emnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ee602-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ee602-107">Hvis du vil udføre disse trin, skal du også have adgang til en RCS-forekomst, der indeholder mindst én ER-konfiguration, der enten har statussen **Fuldført** eller **Delt**.</span><span class="sxs-lookup"><span data-stu-id="ee602-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="ee602-108">Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ee602-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ee602-109">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="ee602-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ee602-110">Hvis denne konfigurationsudbyder ikke vises, skal du fuldføre trinnene i emnet [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ee602-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="ee602-111">Hvis du ikke har klargjort et RCS-miljø til dit firma, skal du vælge det eksterne link **Regulatory services – konfiguration** og følge instruktionerne for at klargøre et RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="ee602-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="ee602-112">Vælg **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ee602-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="ee602-113">Vælg fanen **RCS**.</span><span class="sxs-lookup"><span data-stu-id="ee602-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="ee602-114">Hvis RCS-miljøet allerede er klargjort til dit firma, skal du anvende indstillingen for præsenteret på sidens URL-adresser for at få adgang til det.</span><span class="sxs-lookup"><span data-stu-id="ee602-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="ee602-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ee602-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="ee602-116">Registrere et nyt ER-lager.</span><span class="sxs-lookup"><span data-stu-id="ee602-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="ee602-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ee602-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="ee602-118">Vælg Litware, Inc.-udbyder</span><span class="sxs-lookup"><span data-stu-id="ee602-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="ee602-119">Vælg Lagre.</span><span class="sxs-lookup"><span data-stu-id="ee602-119">Select Repositories.</span></span> 
4. <span data-ttu-id="ee602-120">Vælg Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ee602-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="ee602-121">Skriv RCS i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="ee602-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="ee602-122">Vælg Opret lager.</span><span class="sxs-lookup"><span data-stu-id="ee602-122">Select Create repository.</span></span> 
7. <span data-ttu-id="ee602-123">Angiv eller vælg en værdi i feltet for vist navn for RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="ee602-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="ee602-124">Vælg det ønskede RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="ee602-124">Select the desired RCS instance.</span></span> <span data-ttu-id="ee602-125">Du kan have flere af dem.</span><span class="sxs-lookup"><span data-stu-id="ee602-125">You can have several of them.</span></span> 
9. <span data-ttu-id="ee602-126">Vælg OK.</span><span class="sxs-lookup"><span data-stu-id="ee602-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="ee602-127">Importere ER-konfigurationer fra RCS-baseret lager</span><span class="sxs-lookup"><span data-stu-id="ee602-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="ee602-128">Vælg **Vis filtre**.</span><span class="sxs-lookup"><span data-stu-id="ee602-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="ee602-129">Angiv filterværdien "RCS" i feltet **Navn** ved hjælp af filteroperatoren **begynder med**.</span><span class="sxs-lookup"><span data-stu-id="ee602-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="ee602-130">Når du åbner det valgte lagersted, skal du på siden **Forbind til Regulatory Configuration Services** vælge linket **Klik her for at oprette forbindelse til Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="ee602-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="ee602-131">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="ee602-131">Select **Open**.</span></span> 
5. <span data-ttu-id="ee602-132">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ee602-132">Select **Close**.</span></span> 
6. <span data-ttu-id="ee602-133">Vælg den ønskede version af ER-konfigurationen, og vælg **Importér** for at overføre den til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="ee602-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]